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


# High-availability enhancements
{: #consistentregions}

Because of business requirements, some applications require that all tuples are processed at least once. {{site.data.keyword.streamsshort}} is enhanced with operators and annotations that allow the definition of a region that does not lose tuples during streams processing. Tuples in a consistent region are processed at least once.


If you use the Beta-Entry or the Beta-Enhanced pricing plans, you can now run and monitor Streams applications with defined consistent regions in {{site.data.keyword.streaminganalyticsshort}}. When you create a {{site.data.keyword.streaminganalyticsshort}} service with the Beta-Entry or Beta-Enhanced plans, the instance is already configured to use consistent regions.

A consistent region is a subgraph where the states of the operators become consistent by processing all the tuples and punctuation marks within defined points on a stream. This enables tuples within the subgraph to be processed at least once. The consistent region is periodically drained of its current tuples. All tuples in the consistent region are processed through to the end of the subgraph. In-memory state of operators are automatically serialized and stored on checkpoint for each of the operators in the region.

You can now write both Java and SPL applications that have guaranteed tuple processing and deploy these applications in {{site.data.keyword.streaminganalyticsshort}}.

You can define the start of a consistent region with the `@consistent` annotation on a capable operator. {{site.data.keyword.streamsshort}} determines the scope of the consistent region automatically, but you can change the end operator of the region with the `@autonomous` annotation. The defined consistent region periodically establishes a consistent state.

Check out the [{{site.data.keyword.streamsshort}} documentation ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.1/com.ibm.streams.dev.doc/doc/consistentregions.html) for more details about using consistent regions in Streams applications.
