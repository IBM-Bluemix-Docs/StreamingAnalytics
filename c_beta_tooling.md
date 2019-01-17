---

copyright:
  years: 2015, 2019
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Development tools and environment
{: #c_beta_tooling}


These considerations apply to the tools and environment that you use to develop your applications for {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}} doesn't include an {{site.data.keyword.streamsshort}} development environment in the cloud or Streams Studio in the cloud. Develop your applications in a locally installed {{site.data.keyword.streamsshort}} environment and submit them as application bundles. If you don’t have the development environment, you can download the [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) for [v2 service plans](/docs/services/StreamingAnalytics/service_plans.html) or if you are using the [v1 service plans](/docs/services/StreamingAnalytics/service_plans.html), you can download the [{{site.data.keyword.streamsshort}} Quick Start Edition VM image ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}, free-of-charge.
* Compile your applications in Red Hat Enterprise Linux (RHEL) 7.x if you are using the v2 service plans or with RHEL 6.5 if you're using v1 service plans, using Intel processors.
* In your {{site.data.keyword.streamsshort}} development environment, set the environment variable `JAVA_HOME` to $STREAMS_INSTALL/java.
