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

# Development tools and environment
{: #c_beta_tooling}

{{site.data.keyword.streaminganalyticsfull}} is deprecated. As of July 30, 2021, 
you can't create new instances, and access to free Lite instances will be removed. 
Existing paid plan instances are supported until May 1, 2022. Any instance that still exist on that date will be stopped and deleted. 
For more information, see [End of Market](/docs/StreamingAnalytics?topic=StreamingAnalytics-end_of_market).
{: deprecated}

These considerations apply to the tools and environment that you use to develop your applications for {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}} doesn't include an {{site.data.keyword.streamsshort}} development environment in the cloud or Streams Studio in the cloud. Develop your applications in a locally installed {{site.data.keyword.streamsshort}} environment and submit them as application bundles. If you don’t have the development environment, you can download the [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi).
* Compile your applications on a RHEL 7.4 or CentOS 7.4 x86_64 system.
* In your {{site.data.keyword.streamsshort}} development environment, set the environment variable `JAVA_HOME` to $STREAMS_INSTALL/java.
