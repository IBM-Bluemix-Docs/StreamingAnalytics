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

# About Streaming Analytics
{: #about}

You can perform real-time analysis on data in motion as part of your {{site.data.keyword.Bluemix_short}} applications by with {{site.data.keyword.streaminganalyticsfull}}.
{:shortdesc}

New to {{site.data.keyword.streaminganalyticsshort}}? Get a [quick introduction to the service ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/streamsdev/docs/streaming-analytics-now-available-bluemix-2/){:new_window}.

The {{site.data.keyword.streaminganalyticsshort}} service provides the following capabilities to deploy, analyze, and monitor your data in the cloud:

**Interactive and programmatic use of the service:**

You can use the service interactively through the [{{site.data.keyword.streaminganalyticsshort}} console](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-console#console), or programmatically through the [{{site.data.keyword.streaminganalyticsshort}} REST API ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/apidocs/streaming-analytics-v2).

**Deployment and monitoring of SPL, Java, Scala, and Python applications:**

You can write {{site.data.keyword.streamsshort}} applications in SPL, Java, Scala, and Python. [Deploy and monitor these applications](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_deploytocloud) with the {{site.data.keyword.streaminganalyticsshort}} console.

If you want to write your applications in SPL, {{site.data.keyword.streamsfull}} Processing Language (SPL) is a programming language that is used to create streams processing applications. If you want to go further with your own SPL applications, you can get an {{site.data.keyword.streamsshort}} development environment and you must get your SPL apps cloud-ready.

To create and deploy Python applications without a {{site.data.keyword.streamsshort}} development environment, use the service notebooks in {{site.data.keyword.DSX_short}} or the {{site.data.keyword.streamsshort}} Python API. For more information, see [Developing Python applications for {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_develop_apps_python).

You can develop Beam applications with Streams runner in your local development environment, which you can then deploy and monitor in the {{site.data.keyword.streaminganalyticsshort}} service. For more information about Beam applications with Streams runner, see the [IBM Streams Runner for Apache Beam in {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-gs_beamrunner).


**Compatibility with {{site.data.keyword.streamsshort}} operators:**

The {{site.data.keyword.streamsshort}} operators in the [{{site.data.keyword.streamsshort}} Processing Language (SPL) standard toolkit are compatible](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-compatible_toolkits) with {{site.data.keyword.streaminganalyticsshort}}.

## Streaming Analytics responsibilities
{: #responsibilities notoc}

### Client responsibilities
{: #clientresponsibilities notoc}

Client is responsible for:

* Following IBM’s initial configuring of the {{site.data.keyword.streamsshort}}, monitoring, configuring, and managing the {{site.data.keyword.streamsshort}} jobs that are running in their instance. Client has flexibility to start and stop the instance and start and stop jobs that are running on the instance.
* Developing, as needed, programs and applications on the service to analyze data and obtain insights from it. Client is also responsible for the quality and performance of such programs or applications developed. Programs can be developed in SPL, Java, or other supported languages by using the {{site.data.keyword.streamsshort}} Topology feature. They must be compiled either with {{site.data.keyword.streamsshort}} Developer Edition or {{site.data.keyword.streamsshort}} Quick Start Edition with the same operating system as used for {{site.data.keyword.streaminganalyticsshort}}.
* Establishing the security of data in transit on interfaces in and out of client applications. This is typically done using secure sockets on connections with Source and Sink operators in the client applications.
* Checking the following link periodically to be informed about a scheduled non-disruptive or disruptive downtime - [https://cloud.ibm.com/status?selected=status ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/status?selected=status){:new_window}  
* Backing up all data, metadata, configuration files, and environment parameters as per business requirements to ensure continuity.
* Restoring data, metadata, configuration files, and environment parameters from any backup to ensure continuity, in an eventuality of failure of any type. This includes but is not limited to data center or pod failure, server failure or hard disk failure, or software failures.

### IBM Responsibilities
{: #ibmresponsibilities notoc}

As part of {{site.data.keyword.streaminganalyticsfull}}, IBM will:

* Provide and manage servers, storage, and networking infrastructure for the Customer instance.
* Provide an initial configuration of the {{site.data.keyword.streamsshort}} on the number of resources selected.
* Provide and manage infrastructure for Internet facing and internal firewall for protection and isolation.
* Monitor and manage the following components on {{site.data.keyword.streaminganalyticsshort}}:
	* Network components
	* Servers and their local storage
	* Infrastructure Operating Systems
	* {{site.data.keyword.streamsshort}} management services
	* {{site.data.keyword.streamsshort}} instances
* Provide maintenance patches, including appropriate security patches for the infrastructure operating systems and {{site.data.keyword.streamsshort}}.
* Perform regular maintenance that should not require any system downtime (“non-disruptive” maintenance) and maintenance that can require some system downtime and restarting (“disruptive” maintenance”), are performed at the scheduled times published at [https://cloud.ibm.com/status?selected=status ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/status?selected=status){:new_window}
* Any changes to the scheduled maintenance times are posted with appropriate notice.
