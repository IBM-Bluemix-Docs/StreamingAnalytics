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

# Development tools and environment
{: #c_beta_tooling}


These considerations apply to the tools and environment that you use to develop your applications for {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}} doesn't include an {{site.data.keyword.streamsshort}} development environment in the cloud or Streams Studio in the cloud. Develop your applications in a locally installed {{site.data.keyword.streamsshort}} environment and submit them as application bundles. If you don’t have the development environment, you can download the [{{site.data.keyword.streamsshort}} Quick Start Edition ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/), free-of-charge.
* Compile the application bundle in a Red Hat Enterprise Linux 6.5 environment, or an equivalent CentOS version, to ensure compatibility.

  **Note:** If you are using the Beta-Entry and Beta-Enhanced plans, you must compile your application bundle in a RHEL 7 environment or an equivalent CentOS version. You can use the [{{site.data.keyword.streamsshort}} QSE for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) if you don't have a a compatible development environment. Check out the [Beta plans documentation](/docs/services/StreamingAnalytics/beta_plans.html) for details.
* In your {{site.data.keyword.streamsshort}} development environment, set the environment variable `JAVA_HOME` to $STREAMS_INSTALL/java.
