---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-16"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# IBM Streams Runner for Apache Beam
{: #gs_beamrunner}

If you have an {{site.data.keyword.streamsshort}} development environment, you can now develop Beam applications locally in your environment and then submit these apps to the {{site.data.keyword.streaminganalyticsshort}} service in {{site.data.keyword.cloud_notm}}. {{site.data.keyword.streamsshort}} Runner for Apache Beam executes Beam pipelines in an {{site.data.keyword.streamsshort}} environment. A Beam application that is launched with Streams Runner is translated into a Streams Application Bundle (SAB) file that you can then deploy and monitor in {{site.data.keyword.streaminganalyticsshort}}.


Get started by using the [sample applications](/docs/StreamingAnalytics?topic=StreamingAnalytics-starterapps) to learn how to submit and monitor a Beam application in the {{site.data.keyword.streaminganalyticsshort}} service. You can download the sample applications from the {{site.data.keyword.streaminganalyticsshort}} console.

Check out the [{{site.data.keyword.streamsshort}} Runner for Apache Beam documentation ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/){:new_window} to see tables that show how Streams Runner fits into the [Beam capability matrix](https://beam.apache.org/documentation/runners/capability-matrix/). See [Installing IBM Streams Runner for Apache Beam ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://bit.ly/2zFDpPr){:new_window} to get instructions on how to install the `com.ibm.streams.beam` toolkit in your Streams environment to create Beam applications that you can submit and monitor in {{site.data.keyword.streaminganalyticsshort}}.

Some familiarity with Beam programming is helpful, though not required; the  [Apache Beam website ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://beam.apache.org/documentation/){:new_window} has a useful [Apache Beam Java SDK Quickstart ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://beam.apache.org/get-started/quickstart-java/){:new_window} page and other documentation.
