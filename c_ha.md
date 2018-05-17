---

copyright:
  years: 2015, 2018
lastupdated: "2018-04-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics high availability
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} enables high availability for your applications. If an issue is detected on one of your application nodes ({{site.data.keyword.streamsshort}} resources), the node is automatically replaced and any jobs running on that node are migrated. Jobs are only migrated and restarted if the instance contains multiple application nodes. You can resize the instance by using the [service dashboard](/docs/services/StreamingAnalytics/r_service_dashboard.html) or the [{{site.data.keyword.streaminganalyticsshort}} v1 REST API ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/apidocs/220){:new_window} for [v1 service plans](/docs/services/StreamingAnalytics/service_plans.html). For v2 service plans, use the [v2 REST API ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/apidocs/1939){:new_window}
{:shortdesc}

This video shows how to resize your instance using the service dashboard:

<iframe width="560" height="315" title="Resize instance" src="https://www.youtube.com/embed/zbZ9am9UhPw?rel=0" frameborder="0" allowfullscreen>Resize instance</iframe>

## Consistent regions
Because of business requirements, some applications require that all tuples are processed at least once. {{site.data.keyword.streamsshort}} is enhanced with operators and annotations that allow the definition of a region that does not lose tuples during streams processing. Tuples in a consistent region are processed at least once.

You can run and monitor Streams applications with defined consistent regions in {{site.data.keyword.streaminganalyticsshort}}. When you create a {{site.data.keyword.streaminganalyticsshort}} service, the instance is already configured to use consistent regions.

A consistent region is a subgraph where the states of the operators become consistent by processing all the tuples and punctuation marks within defined points on a stream. This enables tuples within the subgraph to be processed at least once. The consistent region is periodically drained of its current tuples. All tuples in the consistent region are processed through to the end of the subgraph. In-memory state of operators are automatically serialized and stored on checkpoint for each of the operators in the region.

You can now write both Java and SPL applications that have guaranteed tuple processing and deploy these applications in {{site.data.keyword.streaminganalyticsshort}}.

You can define the start of a consistent region with the `@consistent` annotation on a capable operator. {{site.data.keyword.streamsshort}} determines the scope of the consistent region automatically, but you can change the end operator of the region with the `@autonomous` annotation. The defined consistent region periodically establishes a consistent state.

Check out the [{{site.data.keyword.streamsshort}} documentation ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.1/com.ibm.streams.dev.doc/doc/consistentregions.html) for more details about using consistent regions in Streams applications.
