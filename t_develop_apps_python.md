---

copyright:
  years: 2015, 2018
lastupdated: "2017-12-15"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Developing Python applications in Streaming Analytics
{: #t_develop_apps_python}

You can now develop Python applications in IBM Data Science Experience (DSX) or in your local Python development environment and deploy these applications in {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

Develop and deploy your Python applications to {{site.data.keyword.Bluemix_short}} using the {{site.data.keyword.streaminganalyticsshort}} service using one of these methods:


## Developing Streams Python applications in DSX
{: #t_develop_python_dsx}

If you do not have a Python development environment, the easiest way to get started is to use our  notebooks in DSX and create sample Python applications for the {{site.data.keyword.streaminganalyticsshort}} service. These notebooks provide the steps and code samples to create and deploy simple Python applications for the {{site.data.keyword.streaminganalyticsshort}} service within the DSX Python environment:

* [Hello World! ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039ca9c6e8): Create a simple Hello World! application to get started and then deploy the application to an instance of the {{site.data.keyword.streaminganalyticsshort}} service.

* [Healthcare Demo ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039cad29a6): Create an application that ingests and analyzes streaming data from a feed, and then visualizes the data in the notebook. You finally submit this application to the {{site.data.keyword.streaminganalyticsshort}} service instance.

* [Neural Net Demo ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039ca60bb7): Create a sample data set, create a model for the sample data, use that model in a streaming application, visualize the streaming data, and finally submit the streaming application to the {{site.data.keyword.streaminganalyticsshort}} service.

## Developing applications in your local Python environment
 {: #t_develop_python_api}

 The [{{site.data.keyword.streamsshort}} Python Application API ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features), which is included in the streamsx package, enables you to create stream processing applications using Python callable classes or functions. You use the Python Application API to then define and submit the application to the service.

Get started by following the steps in the [Developing for the {{site.data.keyword.streaminganalyticsshort}} service ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html) tutorial to create a sample application in your local Python environment and deploy it to the {{site.data.keyword.streaminganalyticsshort}} service.

To dig deeper on the {{site.data.keyword.streamsshort}} Python Application API, complete [this online course ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/courses/all/streaming-analytics-basics-python-developers/){:new_window} and learn {{site.data.keyword.streaminganalyticsshort}} basics for Python developers.
