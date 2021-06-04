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

# Deploying Beam applications in {{site.data.keyword.streaminganalyticsshort}}
{: #develop_beam_apps}

{{site.data.keyword.streaminganalyticsfull}} is deprecated. As of July 30, 2021, 
you can't create new instances, and access to free Lite instances will be removed. 
Existing paid plan instances are supported until May 1, 2022. Any instance that still exist on that date will be stopped and deleted. 
For more information, see [End of Market](/docs/StreamingAnalytics?topic=StreamingAnalytics-end_of_market).
{: deprecated}

You can now develop Beam applications in your local {{site.data.keyword.streamsshort}} development environment and deploy these applications in {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

{{site.data.keyword.streamsshort}} Runner for Apache Beam executes Beam pipelines in an {{site.data.keyword.streamsshort}} environment. A Beam application that is launched with Streams Runner is translated into a Streams Application Bundle (SAB) file that you can then deploy and monitor in {{site.data.keyword.streaminganalyticsshort}}.

To submit a Beam application to your {{site.data.keyword.streaminganalyticsshort}} service on {{site.data.keyword.cloud_notm}}, you must create a JSON-formatted VCAP file that holds credentials and other information for the service.

1. In your Streams local environment, navigate to the samples subfolder where you installed the toolkit (`$STREAMS_BEAM_RUNNER/samples`) and copy the template.vcap file to a new file. Give the file a meaningful name and a file extension of `.vcap.`
1. [Copy the credentials of your {{site.data.keyword.streaminganalyticsshort}} service](/docs/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans#vcap_services) and paste the credentials in the VCAP file you created, replacing the following line:
```
 <REMOVE THIS LINE AND INSERT CREDENTIALS HERE>
 ```
1. Verify that your Beam application runs properly in your  development environment. When you launch your Beam application with Streams Runner, the application is translated into a Streams Application Bundle (SAB) file.
1. Submit the SAB file that is associated with your Beam application to {{site.data.keyword.streaminganalyticsshort}}

Your application is now deployed in the cloud. You can monitor your application with the {{site.data.keyword.streaminganalyticsshort}} service.

For more information about deploying and monitoring your Beam applications in {{site.data.keyword.streaminganalyticsshort}}, see [Streams Runner for Apache Beam ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/).
