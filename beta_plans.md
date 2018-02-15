---

copyright:
  years: 2015, 2018
lastupdated: "2018-02-14"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Beta-Entry and Beta-Enhanced plans
{: #beta_plans}

The new Beta-Entry and the Beta-Enhanced plans of the {{site.data.keyword.streaminganalyticsshort}} service include several enhancements and differences from the existing the service plans:
{:shortdesc}

**New [{{site.data.keyword.streamsshort}} QSE for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi):** The {{site.data.keyword.streamsshort}} Quick Start Edition is a no-charge, non-production version of {{site.data.keyword.streamsshort}}. To use the Beta-Entry and Beta-Enhanced plans to deploy applications to {{site.data.keyword.streaminganalyticsshort}}, you must compile your applications using the Red Hat Enterprise Linux (RHEL) 7 version of the {{site.data.keyword.streamsshort}} QSE.
Check out the [Beta Development Guide ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/streamsdev/docs/cloud-beta-devguide/) to learn how to use the new Streams QSE with RHEL 7 running in a Docker environment to compile and deploy your applications with the new {{site.data.keyword.streaminganalyticsshort}} beta plans.   

**{{site.data.keyword.streaminganalyticsshort}} v2 REST API:** You can use the [{{site.data.keyword.streaminganalyticsshort}} v2 REST API ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#introduction) to manage your service instances and {{site.data.keyword.streamsshort}} jobs. The {{site.data.keyword.streaminganalyticsshort}} v2 API is only supported on service instances created with one of the new beta plans. The [v1 REST API ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/apidocs/220-streaming-analytics?&language=node#introduction) is only supported on existing {{site.data.keyword.streaminganalyticsshort}} instances and any new instances you create with the existing service plans.

**New starter and sample applications:** Since the new beta plans require to run Streams on RHEL 7, many of the existing sample applications do not work with the new beta plans. {{site.data.keyword.streaminganalyticsshort}} provides a [new set of starter and sample applications]( https://developer.ibm.com/streamsdev/docs/cloud-beta-samples/) to quickly get you started with the new beta plans.

**High-availability enhancements:** Avoid data loss in streams processing applications by defining consistent regions. {{site.data.keyword.streamsshort}} is enhanced with operators and annotations that allow the definition of a region that does not lose tuples during streams processing. Tuples in a consistent region are processed at least once.
If you use the Beta-Entry or the Beta-Enhanced pricing plans, you can now run and monitor Streams applications with [defined consistent regions in {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/consistentregions.html).

**New problem determination features:** The Beta-Entry and the Beta-Enhanced plans include several enhancements to help you quickly find and fix errors in your applications. For more details, see [The {{site.data.keyword.streaminganalyticsshort}} Console gives you more ways to find and fix errors (Beta plans) ![External link icon](../../icons/launch-glyph.svg "External link icon").](https://wp.me/p4IICn-4cx)

**Monitoring how operators behave and guaranteed tuple processing in the cloud:** {{site.data.keyword.streamsshort}} provides metrics to help evaluate the health of {{site.data.keyword.streamsshort}} services, to aid in diagnosing performance issues, and to analyze throughput of requests. You can use the Streams Console in {{site.data.keyword.streaminganalyticsshort}} to [monitor how operators behave and ensure resource optimization ![External link icon](../../icons/launch-glyph.svg "External link icon").](https://wp.me/p4IICn-4bH)
