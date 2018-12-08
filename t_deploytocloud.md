---

copyright:
  years: 2015, 2018
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Deploying Streams applications to the cloud
{: #t_deploytocloud}

You can deploy your {{site.data.keyword.streamsshort}} applications to a {{site.data.keyword.streaminganalyticsshort}} instance that is running in {{site.data.keyword.Bluemix_short}}.
{:shortdesc}

{{site.data.keyword.streamsshort}} applications are written in {{site.data.keyword.streamsshort}} Processing Language (SPL), SPL, Java, Scala, or Python in an {{site.data.keyword.streamsshort}} environment. You can now develop Streams Python applications without an {{site.data.keyword.streamsshort}} environment. See [Deploying {{site.data.keyword.streamsshort}} Python applications to the cloud](/docs/services/StreamingAnalytics/t_deploytocloud.html#t_deploypython)


{{site.data.keyword.streaminganalyticsshort}} doesn't include an {{site.data.keyword.streamsshort}} development environment in the cloud, but you can deploy the applications that you develop locally to the cloud.

Before you begin, disable the pop-up blocker of your browser to display the {{site.data.keyword.streaminganalyticsshort}} console.

To deploy your {{site.data.keyword.streamsshort}} applications to the cloud:

1. Set up your development environment to develop and test your application.

	If you want to use an {{site.data.keyword.streamsshort}} environment, you can download the [{{site.data.keyword.streamsshort}} Quick Start Edition ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window} for [v1 service plans](/docs/services/StreamingAnalytics/service_plans.html). Use the [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi){:new_window} for [v2 service plans](/docs/services/StreamingAnalytics/service_plans.html).

2. Develop your streaming application in your development environment. In {{site.data.keyword.streamsshort}} development environment, you can use Streams Studio or the command-line tools to develop your application.

3. Verify that your streaming application runs properly in your development environment.
**Note:** You must compile your applications in Red Hat Enterprise Linux (RHEL) 7.x if you are using the v2 service plans or with RHEL 6.5 if you're using v1 service plans.

4. Submit the application bundle (.sab file) that is associated with your SPL, Java, Scala, or Python application to your service instance in the cloud by using one of these methods:
	* Use the {{site.data.keyword.streaminganalyticsshort}} console to submit the application bundle.

  * Create an application in {{site.data.keyword.Bluemix_notm}} and add the {{site.data.keyword.streamsshort}} application to it. Control it by using the [{{site.data.keyword.streaminganalyticsshort}} v1 REST API ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} for [v1 service plans](/docs/services/StreamingAnalytics/service_plans.html) or the [{{site.data.keyword.streaminganalyticsshort}} v2 REST API ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window} for v2 service plans.

Your application is now deployed in the cloud. You can monitor your application in the {{site.data.keyword.streaminganalyticsshort}} service. You can also submit more than one application (.sab files) to your service instance. As many as you want.

{{site.data.keyword.streamsshort}} also supports several Java™ development kits that you can use to develop your applications. For more information about the Java support in {{site.data.keyword.streamsshort}}, see [Supported Java development kits for application development ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.install.doc/doc/ibminfospherestreams-install-prerequisites-java-supported-sdks.html){:new_window}.

## Deploying Streams Python applications to the cloud
{: #t_deploypython}

Deploy your {{site.data.keyword.streamsshort}} Python applications to a {{site.data.keyword.streaminganalyticsshort}} service that is running in {{site.data.keyword.Bluemix_short}}. You do not need to have an {{site.data.keyword.streamsshort}} installation.
{:shortdesc}

With the [{{site.data.keyword.streamsshort}} Python Application API ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features){:new_window}, which is included in the streamsx package, you can deploy Python applications to the {{site.data.keyword.streaminganalyticsshort}} service. Check out the [Developing for the {{site.data.keyword.streaminganalyticsshort}} service ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html){:new_window} tutorial to get an example of how to create and deploy a simple Python application for the {{site.data.keyword.streaminganalyticsshort}} service.

{{site.data.keyword.DSX_full}} also supports the submission of Python applications in Jupyter interactive notebooks. For more information, see [Developing Python applications for {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/t_develop_apps_python.html).
