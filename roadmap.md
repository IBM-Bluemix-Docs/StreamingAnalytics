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
{:video .video}


# Roadmap for {{site.data.keyword.streaminganalyticsshort}} on IBM Cloud
{: #roadmap}

{{site.data.keyword.streaminganalyticsshort}} is built upon the IBM Streams technology. Streams is an advanced analytic platform allowing user-developed applications to quickly ingest, analyze, and correlate information as it arrives from a wide variety of real-time sources. The {{site.data.keyword.streaminganalyticsshort}} service gives you the ability to deploy Streams applications to run in the IBM Cloud. This roadmap helps you get started and learn about the IBM {{site.data.keyword.streaminganalyticsshort}} Service.


## Step 1 – Learn about Streams

If you are new to Streams, please take some time to learn about the Streams technology. If you already have experience with Streams, please move to the next step.

**Video: Introduction to {{site.data.keyword.streaminganalyticsshort}} with IBM Streams**

![Introduction to streaming analytics with IBM Streams](https://www.youtube.com/embed/oQKeejV74lg){: video output="iframe" data-script="none" id="youtubeplayer" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen}

## Developing Streams applications with Python

You can create Streams applications using Streams Processing Language (SPL) or Python and the Streams Python API. These applications can also be deployed in the {{site.data.keyword.streaminganalyticsshort}} service.  _The remainder of this tutorial focuses on developing applications with Streams Processing Language (SPL)._  
If you would like to develop applications using Python, [please follow the Python development guide](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide/) to learn more about developing Python applications for the {{site.data.keyword.streaminganalyticsshort}} service.

## Learn more

- [IBM Streams Quick Start for SPL](https://ibmstreams.github.io/streamsx.documentation/docs/spl/quick-start/qs-0/)

## Step 2 – Learn about the {{site.data.keyword.streaminganalyticsshort}} service

Please read this quick introduction to the [{{site.data.keyword.streaminganalyticsshort}} Service](https://developer.ibm.com/streamsdev/docs/streaming-analytics-now-available-bluemix-2/).

## Step 3 – Run a Sample

There are a number of sample applications you can use to learn about the {{site.data.keyword.streaminganalyticsshort}} service. Please run one or more of the samples below that most closely match your intended use of the {{site.data.keyword.streaminganalyticsshort}} service.

### Deploy the stock trades starter application

This is a simple application that is ready to be deployed to the {{site.data.keyword.streaminganalyticsshort}} service. You do not have to write any code or install any software.

To try it, [download the application file from GitHub](https://github.com/IBMStreams/samples/releases/download/20170322_release/StockTradesStarterApp.sab), and then watch this video to see how to:

- Create an instance of the {{site.data.keyword.streaminganalyticsshort}} Service (00:22)
- Run the [starter application](https://github.com/IBMStreams/samples/releases/download/20170322_release/StockTradesStarterApp.sab) in the service (00:56)
- See the actual data being processed by an application (02:13)
- Look at the applications logs and any data printed to stdout/stderr (03:17)

<iframe src="https://www.youtube.com/embed/aXAqAaijzWc" width="600" height="450" allowfullscreen="allowfullscreen"></iframe>


### End-to-End Starter Application

Deploy the end-to-end starter application to the cloud if you want to explore how to use {{site.data.keyword.streaminganalyticsshort}} in the context of a larger IBM Cloud application.

#### <span style="text-decoration: underline;">EventDetection Starter  
</span>

The EventDetection starter application uses the SDK for Node.js runtime in the IBM Cloud. EventDetection uses the {{site.data.keyword.streaminganalyticsshort}} service to detect simple and complex events in a Stream of real-time weather data.

[Article: {{site.data.keyword.streaminganalyticsshort}} Event Detection Starter Application](https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/)

* * *

### Other Streams Application Samples

Run additional Streams application samples to further explore Streams apps in the cloud. Use the link below to access a wide variety of sample applications. Click on the link and search for “Cloud” to find the samples that are can be deployed in the cloud.

[IBMStreams/samples Github project](http://ibmstreams.github.io/samples/)

* * *

## Step 4 – Learn More about Developing Streams Applications for the Cloud

See the [{{site.data.keyword.streaminganalyticsshort}} Development Guide](https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/) for a comprehensive description of how to develop and deploy applications to the {{site.data.keyword.streaminganalyticsshort}} service. The development guide features a sample Streams application that analyzes Twitter data and step-by-step instructions for completing tasks that are part of the application development life cycle.

If you have an existing Streams application that you would like to deploy to the cloud, see [Getting your SPL application ready for the cloud.](https://developer.ibm.com/streamsdev/docs/getting-spl-application-ready-cloud/)

## Step 5 – Learn about Integrating with other IBM Cloud Services

A variety of tutorials and resources are available to help you use the {{site.data.keyword.streaminganalyticsshort}} service with other IBM Cloud services.

### General

[Integrating with Cloudant and many other RESTful Services](https://developer.ibm.com/streamsdev/docs/integrating-with-cloudant-and-many-other-restful-services/)

[Connect {{site.data.keyword.streaminganalyticsshort}} to your Enterprise Data using Secure Gateway](https://developer.ibm.com/streamsdev/docs/connect-streaming-analytics-to-your-enterprise/)

### Messaging

[Getting Started with {{site.data.keyword.streaminganalyticsshort}} and Message Hub](https://www.ibm.com/blogs/bluemix/2018/04/get-started-streaming-analytics-message-hub/)

### Watson IoT / Internet of Things Platform

Demo: [IoT Device Events to {{site.data.keyword.streaminganalyticsshort}} in 15 Minutes](https://www.ibm.com/blogs/bluemix/2016/10/iot-device-events-to-streaming-analytics-in-15-minutes/)

Demo: [Using Apache Edgent, Watson IoT, and {{site.data.keyword.streaminganalyticsshort}} to Create a Smart Sprinkler](https://developer.ibm.com/bluemix/2016/06/01/better-analytics-with-apache-quarks/)

Tutorial: [Watson IoT Recipe: Integrate IBM {{site.data.keyword.streaminganalyticsshort}} Service with Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/integrate-ibm-streaming-analytics-service-with-watson-iot-platform/)

Tutorial: [Connect Apache Edgent running on Raspberry Pi to the {{site.data.keyword.streaminganalyticsshort}} service](https://developer.ibm.com/recipes/tutorials/connect-apache-edgent-to-the-streaming-analytics-service-using-the-watson-iot-platform/)

### Hadoop

[Integrating {{site.data.keyword.streaminganalyticsshort}} with HDFS on IBM Cloud](https://developer.ibm.com/bluemix/2016/02/26/streaming-analytics-and-biginsights-using-hdfs/)

[Integrating {{site.data.keyword.streaminganalyticsshort}} Service with HBase on IBM Cloud](https://developer.ibm.com/streamsdev/docs/integrating-streams-biginsights-hbase-service-bluemix/)

### Database

[Using {{site.data.keyword.streaminganalyticsshort}} with JDBC-enabled Databases in IBM Cloud](https://developer.ibm.com/bluemix/2016/01/26/streaming-analytics-with-jdbc-enabled-databases/)

[Integrating with Cloudant and many other RESTful Services](https://developer.ibm.com/streamsdev/docs/integrating-with-cloudant-and-many-other-restful-services/)

### Predictive Analytics

[Support for SPSS Analytics Toolkit in the {{site.data.keyword.streaminganalyticsshort}} Service](https://developer.ibm.com/streamsdev/docs/spss-in-bluemix-streaming-analytics-service/)

### File-based Data Sources

The [Streams ObjectStorage Toolkit](https://ibmstreams.github.io/streamsx.objectstorage/) can be used to integrate your {{site.data.keyword.streaminganalyticsshort}} application with the Object Storage service in IBM Cloud.

## Step 6 – Taking Care of your Streams Application in the Cloud

If you have a Streams application running in the {{site.data.keyword.streaminganalyticsshort}} service, it is most likely one that runs continuously – 24 hours a day and 7 days a week. But how can you make sure that your application is running normally? See [Monitoring Your Streams App in the IBM Cloud using the Streams REST API](https://developer.ibm.com/streamsdev/2018/12/07/dig-deeper-into-streaming-analytics-by-using-the-streams-rest-api/) to learn how you can programmatically assess whether your app is operating normally and extract valuable metrics about its execution.



