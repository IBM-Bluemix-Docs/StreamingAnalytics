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

# Streams Python applications
{: #gettingstarted_py}

{{site.data.keyword.streaminganalyticsfull}} is deprecated. As of July 30, 2021, 
you can't create new instances, and access to free Lite instances will be removed. 
Existing paid plan instances are supported until May 1, 2022. Any instance that still exist on that date will be stopped and deleted. 
For more information, see [End of Market](/docs/StreamingAnalytics?topic=StreamingAnalytics-end_of_market).
{: deprecated}

You can now create Streams apps in a Python environment such as {{site.data.keyword.DSX_full}}, and submit these apps to the {{site.data.keyword.streaminganalyticsshort}} instance to be deployed in {{site.data.keyword.cloud_notm}}. You no longer need to install {{site.data.keyword.streamsshort}} locally to compile and deploy a Streams Python app.

Get started by creating sample Streams Python apps using Jupyter notebooks in {{site.data.keyword.DSX_short}}, and submit these apps to the service instance directly from {{site.data.keyword.DSX_short}}. For more information, see [Developing Streams Python apps in {{site.data.keyword.DSX_short}}](/docs/StreamingAnalytics?topic=StreamingAnalytics-t_develop_apps_python#t_develop_python_dsx).

{{site.data.keyword.streaminganalyticsshort}} also supports the deployment of Streams apps from your local Python environment. You must use the [{{site.data.keyword.streamsshort}} Python Application API ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features), which is included in the streamsx package, to develop your Streams Python apps locally and submit them to the service instance. To get started, follow the steps in the [Developing for the {{site.data.keyword.streaminganalyticsshort}} service ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html) tutorial.
