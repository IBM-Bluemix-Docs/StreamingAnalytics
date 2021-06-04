---

copyright:
  years: 2015, 2021
lastupdated: "2021-06-07"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:deprecated: .deprecated}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:video: .video}

# Using the {{site.data.keyword.streaminganalyticsshort}} service
{: #using_streaming_analytics}

{{site.data.keyword.streaminganalyticsfull}} is deprecated. As of July 30, 2021, 
you can't create new instances, and access to free Lite instances will be removed. 
Existing paid plan instances are supported until May 1, 2022. Any instance that still exist on that date will be stopped and deleted. 
For more information, see [End of Market](/docs/StreamingAnalytics?topic=StreamingAnalytics-end_of_market).
{: deprecated}

There are two ways that you can use your {{site.data.keyword.streaminganalyticsshort}} instance:

- Interactively – through the {{site.data.keyword.streaminganalyticsshort}} console
- Programmatically – through the {{site.data.keyword.streaminganalyticsshort}} REST API

You can also combine the two usage methods.  For example, you could submit Streams applications through the REST API and explore the running applications using the Streams console.

### Interactive approach: using the Streams Console
{: #interactive}

You can launch the Streams console from the {{site.data.keyword.streaminganalyticsshort}} instance, and submit applications to your instance from the console.  You may also explore, monitor, and control your running applications from the console.  To access the Streams Console, perform the following steps:

1.  Bring up the {{site.data.keyword.streaminganalyticsshort}} service dashboard by clicking on the tile in the IBM Cloud web portal associated with your instance.
2.  Click on the LAUNCH button to launch the Streams console.

![{{site.data.keyword.streaminganalyticsshort}} dashboard](images/using/Dashboard.png "{{site.data.keyword.streaminganalyticsshort}} dashboard")

This version of the Streams Console is specifically tailored for the Cloud environment.  The Application Dashboard view gives you an overview of your Streams instance.  It shows a summary of all of the jobs and PEs that are running on the instance.  From the dashboard, you can see status and performance information, live application graphs, tuples rates, and a wide variety of other information about your instance and applications.

![Streams Console](images/using/Console.png "Streams Console")

Below is the initial view of the Streams Console, just as it would appear after you launch it from the service dashboard for your new instance.

![Streams Console with no running jobs](images/using/ConsoleNoJobs.png "Streams Console with no running jobs")

The Streams Console can be used to submit a Streams application to your instance in the cloud.  Select the “play” icon from the top menu bar to submit a job.

![Job submit icon](images/using/ConsoleSubmitJobIcon.png "Job submit icon")

When submitting a job, you are prompted to identify a Streams Application Bundle (.sab file) to upload and submit to your Streams instance.  Below, a .sab file is chosen for an application that was developed locally on a laptop using the Streams Quick Start Edition.  (The {{site.data.keyword.streaminganalyticsshort}} service requires you to develop your Streams application in a Streams environment.  If you don’t already have a Streams environment where you can develop and test applications, the Streams Quick Start Edition provides a full Streams environment, free-of-charge.  See the [{{site.data.keyword.streaminganalyticsshort}} Development Guide](/docs/StreamingAnalytics?topic=StreamingAnalytics-development_guide) for instructions on downloading and setting up the Streams Quick Start Edition.)

![Submit twitter stream job](images/using/SubmitJobTwitterStream.png "Submit twitter stream job")

After identifying the Streams Application Bundle, click Configure.

On the next page, specify any submission time parameters required by your application or any other submission configuration information. Click Submit to deploy the application to your Streams instance.

![Job submission parameters](images/using/SubmitParams.png "Job submission parameters")

In addition to submitting applications, the console can be used to explore and manage your applications.  For example, the Streams graph for the instance in the cloud is shown below, displaying the live status of the application in the form of a flow graph.

![Application flow graph and tuple rates](images/using/Graph.png "Application flow graph and tuple rates")

### Putting it all together:  Deploy a starter application
{: #putting_it_all_together}

  This short video demonstrates the features and concepts just discussed.  You can follow along simply by downloading the sample application and submitting it to the service, no coding required!

[Download the application](https://github.com/IBMStreams/samples/raw/main/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab), and then watch the video. It shows how to:

- Create an instance of the {{site.data.keyword.streaminganalyticsshort}} Service (00:22)
- Run the [starter application](https://github.com/IBMStreams/samples/raw/main/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab) in the service (00:56)
- See the actual data being processed by an application  (02:13)
- Look at the applications logs and any data printed to stdout/stderr  (03:17)

![Getting Started with {{site.data.keyword.streaminganalyticsshort}}](https://www.youtube.com/embed/aXAqAaijzWc){: video output="iframe" data-script="none" id="getstartedplayer" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen}

### Programmatic approach: Using the {{site.data.keyword.streaminganalyticsshort}} REST API
{: #programmatic}

The {{site.data.keyword.streaminganalyticsshort}} service provides a REST API to allow IBM Cloud applications to interact with a Streams instance programmatically.  The API provides several operations allowing an application to submit Streams application bundles, control the instance, query statuses, etc.  See the [{{site.data.keyword.streaminganalyticsshort}} v2 - IBM Cloud API Docs](https://ibm.co/2Gt9mB6) to view detailed information about its REST API.

Starter applications have been provided as working examples of how to use the {{site.data.keyword.streaminganalyticsshort}} REST API.  See the [Event Detection starter application tutorial](/docs/StreamingAnalytics?topic=StreamingAnalytics-detect_events) for an exmaple of how to use the {{site.data.keyword.streaminganalyticsshort}} service programatically through its REST API.

## Related information
{: #related}

- [Roadmap for {{site.data.keyword.streaminganalyticsshort}}](/docs/StreamingAnalytics?topic=StreamingAnalytics-roadmap)

