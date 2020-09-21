---

copyright:
  years: 2015, 2020
lastupdated: "2020-07-28"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}
{:tip .tip}
{:note .note}

# Getting your SPL application ready for the cloud
{: #spl_cloud_ready}


Use these techniques to make sure your existing SPL applications are ready to run in the cloud.
{:shortdesc}

An SPL application that runs in a non-cloud, on-premises installation of Streams might require modification before it can run in the Streaming Analytics service in IBM Cloud. This article describes SPL application constructs and patterns that may not work or may function differently in the cloud, and provides advice on how to make SPL applications that use these techniques “cloud-ready.”

## Passing configuration information to an SPL operator as a file
{: #passing-config}


### *_Issue_*
{: #passing-config-issue}

Several SPL operators have parameters that expect a file reference. One example is the RScript operator that uses a parameter to identify the file name containing an R script, i.e. `param rScriptFileName : "myScript";`. Users of the Streaming Analytics service in IBM Cloud do not have direct access to the file system of the hosts in the cloud, so a specific technique must be used to supply operator configuration files to the cloud.

### *_Cloud-ready technique_*
{: #passing-config-technique}

If you use SPL operators that require configuration files, there are a couple of alternatives for updating your application to make it cloud-ready:

1. The most straightforward technique is to include the configuration files in the streams application bundle (SAB). The preferred location for most configuration files is the etc directory of the application. The etc directory is automatically included in the application bundle. The file reference in the SPL application should then refer to the files by dynamically obtaining the bundle location, i.e. `rScriptFileName : getThisToolkitDir() +"/etc/process.r" ; `. (Alternatively you may use a different directory in the .sab structure for your operator configuration files by specifying a `<sabFiles>` element in the application’s info.xml file.)
1. If your configuration files are very large, including them in the streams application bundle (SAB) will significantly increase the size of your SAB. Large SABs take longer to upload on job submission, and some SABs could even become too large to submit. Instead of including the large files in your SAB, you can store them using the Object Storage service in IBM Cloud, and then access them from your Streams application. See the [Streams Object Storage Toolkit](https://ibmstreams.github.io/streamsx.objectstorage/) for more information about using Object Storage in a Streams application.


## Use of FileSource and DirectoryScan to stream new data into an SPL Application
{: #use-of-filesource}

### *_Issue_*
{: #use-of-filesource-issue}

A common pattern in SPL applications it to get data into the application via a FileSource. The FileSource operator will function correctly in the cloud, but the ability of the application to get new data into the application via a FileSource is limited as you do not have direct access to the file system on the streams application nodes.

The files accessed by a FileSource are in the local file system of a Streams host in the cloud. An SPL application running in the cloud can access the local file system, but there is no way for an entity outside of Streams to populate a file with new data or put a new file into a directory that is being monitored by a DirectoryScan.

The FileSource model will work correctly to get one-time input, configuration, initialization or other data into an SPL application, if the file is included in the streams application bundle.

### *_Cloud-ready technique_*
{: #use-of-filesource-technique}

If your SPL application uses FileSource as the means for obtaining new data, there are a few alternatives for modifying your application to make it cloudy-ready:

1. Store your data files using the Object Storage service in IBM Cloud and access them from your Streams application. This enables your solution to dynamically create new files or update existing files in Cloud Object Storage that your Streams application can access. See the [Streams Object Storage Toolkit](https://ibmstreams.github.io/streamsx.objectstorage/) for more information about using Object Storage in a Streams application.
1. Serve your files through a web application server, and access them using the InetSource operator instead of FileSource.
1. Use a IBM Cloud application to access the file-based data, and stream the data from your IBM Cloud application into your SPL application via another type of adapter.
1. Move to a non file-based approach for input (e.g. MessageHub, Kafka, MQTT, MQ, HTTP, etc.)
1. Create a new SPL application that includes the new file in the stream application bundle, then use a FileSource to read from the bundle and FileSink to write the file out to /tmp in the file system on the same streams application node. (See the next section about considerations around the use of FileSink)


## Use of FileSink to write output data
{: #use-of-filesink}

### *_Issue_*
{: #use-of-filesink-issue}

A common pattern in SPL applications is to produce data and write it to files using a FileSink for consumption by other <span style="text-decoration: underline;">non-streams applications</span>. The FileSink operator will function correctly in the cloud, but since only the SPL application can access the file system on a Streams host in the cloud, writing data to files is of limited value (unless another Streams operator located on the same cloud host is accessing it.)

_**In addition, using FileSink can have some unpredictable side effects. Your PE using FileSink will crash when the available local disk space runs out, so if your application runs forever and keeps adding to the size of a file, it will eventually run out of space.**_


### *_Cloud-ready technique_*
{: #use-of-filesink-technique}

If your SPL application uses FileSink as the means for producing output data, there are a few alternatives for modifying your application to make it cloudy-ready.

1. Move to a non file-based approach for output. For example use MessageHub, Kafka, HTTPPost, JMSSink, or other adapters to send results out from your SPL application.
1. Store the file written by your FileSink using the Object Storage service in IBM Cloud, so other components in your overall solution can access it. See the [Streams Object Storage Toolkit](https://ibmstreams.github.io/streamsx.objectstorage/) for more information about using Object Storage in a Streams application.
1. If you were merely using the FileSink to write out debugging data, you should instead:

    1. Remove the FileSink and use a view annotation or create a dynamic view in the Streams Console to see the data, or
    1. Replace the FileSink with a Custom operator that prints the data and then use the Streams Console to download the job log to view the data.
    
        ```
        () as trace1 = Custom(strFile) {
            logic
                onTuple strFile: {
                    printLn(strFile);
                } 
        }
        ```
        {: codeblock}

If you still decide to use FileSink instead of the alternatives listed above, please be aware that **you must control the size of your files using the closeMode parameter (and its associated parameters) on FileSink and use a static file name**. This will cause the file to be closed when it reaches its limit, and a new file with the same name will be created. Below are a couple of examples of a FileSink that controls the size of the file it creates.

Limiting file size by number of bytes:
```
    () as MySink1 = FileSink(myTuple) {
        param
            file: "MyFile1.dat";
            closeMode: size;
            bytesPerFile: (uint64)(128 * 1024);
            flush: 1u;
    }
```

Limiting file size by number of tuples:
```
    () as MySink2 = FileSink(myTuple) {
        param 
            file: "MyFile2.dat"; 
            closeMode: count; 
            tuplesPerFile: 500u; 
            flush: 1u; 
    }
```
{: codeblock}


## Logging and Tracing
{: #logging-and-tracing}

### *_Issue_*
{: #logging-and-tracing-issue}

SPL applications can produce log and trace messages that get stored in a variety of locations, depending on the method of logging/tracing used.  Logging to Streams product logs from your application provides no benefit to you in the cloud, since the Streams product logs are not visible to you.  In addition, cloud applications that log to the Streams product logs can fill up and otherwise clutter the logs making them more difficult for IBM Cloud administrators to use.

### *_Cloud-ready technique_*
{: #logging-and-tracing-technique}

If your application uses the **appLog()** function from the SPL standard toolkit or the **SPLAPPLOG** macro, there are alternatives you can use that are more effective in the cloud.


- If your application uses the **appLog()** function, change it to use the **appTrc()** function.  appTrc() messages are sent to PE logs that are visible to you, instead of being sent to the Streams product logs.
- Similarly, if you’ve written your own primitive operators as part of your application and you use the **SPLAPPTRC** macro, use the **SPLAPPTRC** macro instead.



## Accessing on-premise data
{: #accessing-on-premise-data}


### *_Issue_*
{: #accessing-on-premise-data-issue}

SPL applications often access on-premise data; that is, enterprise or other data that is not located in the cloud. When Streams is installed on-premise, accessing on-premise data is straightforward. When Streams in running in the cloud, additional work may be necessary to access on-premise data.

In some rare cases, on-premise data might be publicly available, i.e. the data may be accessible via the public internet (with or without authentication.) But in most cases, on premise data is protected behind a firewall, preventing access from outside environments such as IBM Cloud.

### *_Cloud-ready technique_*
{: #accessing-on-premise-data-technique}

If your SPL application needs to access on-premise data, you have a couple of options for modifying your application to make it cloudy-ready.

- Use the Secure Gateway service in IBM Cloud to build a secure path for accessing your on-premises data. Then, access that on-premises data through a protocol that is compatible with Secure Gateway. See <a href="https://developer.ibm.com/streamsdev/docs/connect-streaming-analytics-to-your-enterprise/" target="_blank" rel="noopener">Connecting Streaming Analytics to Your Enterprise Data</a> for more information on this technique.
- Open up ports on the on-premises firewall to allow a Streams adapter to access the data. This method works, but it is not recommended because it is not as secure as the previous technique.


## Using the com.ibm.streamsx.inet.rest operators (e.g. HTTPTupleView, HTTPTupleInjection, HTTPJSONInjection, etc.)
{: #using-the-com-ibm-streamsx-inet-rest-operators}

Streaming Analytics supports a wide variety of connectors, enabling you to stream data into and out of your Streams applications. These connectors are provided in toolkits as “source” or “sink” operators. Source operators bring data into a Streams application. Sink operators send data out of a Streams application. The set of Streams toolkits that are built into Streams are documented in [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.toolkits.doc/spldoc/dita/toolkits/toolkits.html), and an additional set of toolkits can be downloaded from [The IBM Streams GitHub project](https://github.com/IBMStreams).

There are some special considerations when connecting to Streams applications running in the IBM Cloud. 

The connection rule for IBM Cloud instances is very simple:  _**Connections between Streams apps and data sources/sinks must be initiated by the Streams app.**_  This means that a Streams connector operator, whether it is a source or a sink, is playing the client role in the connection.  Conveniently, many Streams connector operators always run in client mode.  The subset of operators that also support running in the server role cannot be used in server mode in an IBM Cloud Streaming Analytics.  Running a connector operator in server mode is not possible in an IBM Cloud Streaming Analytics instance because instances do not externalize host names or IP addresses associated with the application containers used in the instance.

### Related Information

*   If you need to connect your Streams app to a data source/sink that is protected by an enterprise firewall, see [Connect Streaming Analytics to your Enterprise Data using Secure Gateway](https://developer.ibm.com/streamsdev/docs/connect-streaming-analytics-to-your-enterprise/)



## Use of operators that are not compatible with Streaming Analytics
{: #using-incompatible-operators}

### *_Issue_*
{: #using-incompatible-operators-issue}

Some operators in the specialized toolkits that are provided with IBM Streams or provided by the IBMStreams GitHub project are not compatible by the Streaming Analytics service. Here are some examples:

- None of the adapters in the com.ibm.streams.db toolkit are currently supported by the service.
- The streamsx.opencv toolkit is not supported by the service because it pre-reqs open source packages that IBM cannot install on behalf of the customer.

If the operators that you need for your SPL applications are not supported, we would like to hear from you! Post your operator needs to the [Streams Support Forums](https://www.ibm.com/mysupport/s/forumsproduct?name=Streams&id=0TO50000000IQN0GAO).
{:note .note}

### *_Cloud-ready technique_*
{: #using-incompatible-operators-technique}

If your application uses database adapters from the com.ibm.streams.db toolkit, consider using the [Streams JDBC toolkit](https://ibmstreams.github.io/streamsx.jdbc/) as an alternative.

If your application uses unsupported data source or sink adapters, you can use a {{site.data.keyword.cloud_notm}} application to access the data store, and then stream the data from your {{site.data.keyword.cloud_notm}} application to your SPL application using another type of supported adapter.

If your SPL application uses analytics that are not currently supported, your only option is to replace that part of the processing with another analytic operator that is supported.
