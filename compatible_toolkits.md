---

copyright:
  years: 2015, 2018
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Supported toolkits and adapters
{: #compatible_toolkits}

These analytics toolkits and adapters are supported by {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

| Toolkits                        | Description							                  |
| --------------------------------| --------------------------|
| [Complex Event Processing (CEP) ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://ibm.co/2zOwODa)    |	Provides the MatchRegex operator to perform complex event processing.  		 |
| [Datetime ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://ibmstreams.github.io/streamsx.datetime/)	|	Set of utilities to handle dates, times, and timestamps.	 |
| [HBase![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.hbase/)        | Enables Streams applications to connect to Apache HBase.	 	   |
| [HDFS ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.hdfs/)          | Provides operators and functions that interact with Hadoop Distributed File System.	|
| [Internet (Inet) ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.inet)|  Focuses on interacting with network hosted data.				       |
| [IoT ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.iot/)            | Provides Internet of Things (IoT) integration with IBM Watson IoT Platform, either in {{site.data.keyword.Bluemix_notm}} or on-premise ({{site.data.keyword.streamsshort}}). |
| [JDBC ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.jdbc/)          | Enables Streams applications to work with databases via JDBC.		   |
| [JSON ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.json/)          | Learn how to convert data from JSON to Streams tuples format, and conversely.   		|
| [Kafka ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://ibmstreams.github.io/streamsx.kafka/)       | Enables Streams applications to easily integrate with Apache Kafka. 	 |
| [MessageHub ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://ibmstreams.github.io/streamsx.messagehub/) | Enables Streams applications to work with MessageHub.			     |
| [Messaging ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://ibmstreams.github.io/streamsx.messaging/)   |  	Focuses on interacting with popular messaging systems such as Kafka, MQTT, JMS, and XMS	<br>**Note**: To use JMSSource, JMSSink, XMSSource, XMSSink with WebSphere MQ, complete these steps in your development environment: <br>1. Go to [IBMStreams on GitHub ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://github.com/IBMStreams){:new_window} and download the Messaging Toolkit (com.ibm.streamsx.messaging) version 3.0.0 or later on your development environment.<br>2. Use version 5.1.0 or later version of the toolkit to build your application.<br>3. Put the required `.bindings` file in the `/etc` directory of your application to include it in the {{site.data.keyword.streamsshort}} application bundle.	    |
| [Mining ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://ibm.co/2rj2lKw)              	   	            |  Includes operators that you can use to mine data streams by applying models. <br> **Restriction:** This toolkit is not supported if you are using the [v2 service plans](/docs/services/StreamingAnalytics/service_plans.html), since you must compile your application bundle in a RHEL 7 environment or an equivalent CentOS version. 	     |
| [RabbitMQ ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://ibmstreams.github.io/streamsx.rabbitmq/)     |  Provides operators that allow your Streams application to read and send messages from Rabbit MQ.  |
| [R-project ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://ibm.co/2rj2lKw)          	   	              |   Includes the RScript operator, which you can use to run R commands and apply complex data mining algorithms to detect patterns of interest in data streams.			     |
| [Topology ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.topology/)      |  Learn how to build Python streaming applications for {{site.data.keyword.streaminganalyticsshort}} service on the {{site.data.keyword.Bluemix_notm}} platform and {{site.data.keyword.streamsshort}}.		     |
| [DPS ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.dps/) |	 Enables multiple applications that are running processing elements (PEs) on one or more machines to share application-specific state information.<br>**Restriction:** Only REDIS is supported as database backend.	| 	 	 	
| [Geospatial ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://ibm.co/2KWf6nd) 	     |	Includes operators and functions that facilitate efficient processing and indexing of location data.<br>**Restriction:** Operators that use shared map mode are not supported (`MapStore`, `PointMapMatcher` in shared map mode).		 |
| [TEDA ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://ibm.co/2FYeTRL)	   | 	Provides a set of generic operators that is used in telecommunications applications, and it also provides an application framework to set up new file-to-file applications. Get started by following the [TEDA tutorials ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.tutorial.teda/). All operators and functions of the toolkit are supported. <br>**Restriction:** The application framework is not supported.	 	 |
| [TimeSeries ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://ibm.co/2FXzsgX)	 	  | The operators and functions in the TimeSeries Toolkit condition, analyze, and model time series data. <br>**Restriction:** Deprecated operators are not supported.	   |
| [{{site.data.keyword.cos_short}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://bit.ly/2Ggp03T)	 	  | Provides primitive operators and native functions for reading and writing data from and to {{site.data.keyword.cos_short}} respectively. The toolkit supports S3 compatible {{site.data.keyword.cos_short}}.	   |

*Table 1. Supported toolkits*

## Other toolkits and operators
{: #other_operators}

Other operators, including those toolkit operators that you developed for your own needs, can be supported by {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

Toolkits must meet the following criteria to be compatible with {{site.data.keyword.streaminganalyticsshort}}:

1. No additional software needs to be pre-installed on the application nodes of your service instance.
2. Any configuration information that the toolkit requires can be included in the application bundle by using the toolkit.
