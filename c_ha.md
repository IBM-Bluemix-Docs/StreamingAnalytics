---

copyright:
  years: 2015, 2021
lastupdated: "2021-02-09"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}
{:note: .note}

# Understanding high availability and disaster recovery for {{site.data.keyword.streaminganalyticsshort}}
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} is highly available within an {{site.data.keyword.cloud_notm}} location (for example, Dallas, London, Frankfurt). However, recovering from potential disasters that affect an entire {{site.data.keyword.cloud_notm}} region requires planning and preparation.
{:shortdesc}


You are responsible for understanding your configuration, customization, and usage of the service. You are also responsible for being ready to re-create an instance of the service in a new {{site.data.keyword.cloud_notm}} location and to re-deploy your applications to that location. See [How do I ensure zero downtime?](/docs/overview?topic=overview-zero-downtime#zero-downtime) to learn more about the high availability and disaster recovery standards in {{site.data.keyword.cloud_notm}}. You can also find information about [Service Level Agreements](/docs/overview?topic=overview-zero-downtime#zero-downtime#SLAs).

## High availability

{{site.data.keyword.streaminganalyticsshort}} enables high availability for your applications. Your applications are deployed in Docker containers that run in Kubernetes clusters. To write highly available applications, you must understand how these containers work to ensure high availability:

* Application resources are containers with CPU and memory that are allocated according to your service plan.
* During a hardware or software failure, containers may move. When containers are moved processing elements are restarted.
* During planned maintenance, containers may move (processing elements are restarted).

Therefore, when writing your applications, you must consider that containers can move occasionally. Additionally, consider the following items:
* Ensure that PEs are restartable and relocatable.
* Ensure that your application can tolerate the restarting of some or all of its processing elements (PEs), in any order.
* Ensure that the source and sink operators in your Streams application are configured to reestablish connections when their PE restarts.

Check out the [{{site.data.keyword.streaminganalyticsshort}} development guide](/docs/StreamingAnalytics?topic=StreamingAnalytics-development_guide#troubleshooting) for examples on how to troubleshoot your application.

To implement high availability, Streams applications are enabled to guarantee processing of all tuples. To achieve guaranteed tuple processing, a checkpoint is periodically established for all the operators in a Consistent Region. Upon an application failure, all operators will be rolled back to the last successful checkpoint states.
{{site.data.keyword.streaminganalyticsshort}} allows the use of Consistent Regions.

### Guaranteed tuple processing

Because of business requirements, some applications require that all tuples are processed at least once. {{site.data.keyword.streamsshort}} is enhanced with operators and annotations that allow the definition of a Region that does not lose tuples during streams processing. Tuples in a Consistent Region are processed at least once.

If any application failure is detected within a Consistent Region, {{site.data.keyword.streaminganalyticsshort}} can set the application back to the last consistent state (a.k.a. checkpoint), and direct the application data sources to replay tuples from that point on.

You can run and monitor Streams applications with defined Consistent Regions in {{site.data.keyword.streaminganalyticsshort}}. When you create a {{site.data.keyword.streaminganalyticsshort}} service, the instance is already configured to allow the use of Consistent Regions.

A Consistent Region is a subgraph where the states of the operators become consistent by processing all the tuples and punctuation marks within defined points on a stream. This enables tuples within the subgraph to be processed at least once. The Consistent Region is periodically drained of its current tuples. All tuples in the Consistent Region are processed through to the end of the subgraph. In-memory state of operators are automatically serialized and stored on checkpoint for each of the operators in the Region.

You can write Java, SPL, and Python applications that have guaranteed tuple processing and deploy these applications in {{site.data.keyword.streaminganalyticsshort}}.

You can define the start of a Consistent Region with the `@consistent` annotation on a capable operator. {{site.data.keyword.streamsshort}} determines the scope of the Consistent Region automatically, but you can change the end operator of the Region with the `@autonomous` annotation. The defined Consistent Region periodically establishes a consistent state.

Check out the [{{site.data.keyword.streamsshort}} documentation ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html) for more details about using Consistent Regions in Streams applications.

## Disaster recovery

{{site.data.keyword.streaminganalyticsshort}} is a GA service that is offered in multiple {{site.data.keyword.cloud_notm}} regions. {{site.data.keyword.streaminganalyticsshort}} stores no user data on {{site.data.keyword.cloud_notm}}.

Based on your business requirements, select one of the following disaster recovery strategies:

* If you require no interruption to your application:
    1. Create instances of {{site.data.keyword.streaminganalyticsshort}} in multiple {{site.data.keyword.cloud_notm}} regions.
    2. Submit your application to multiple regions.


* If you require minimal interruption to your application:
    1. Create instances of {{site.data.keyword.streaminganalyticsshort}} in multiple {{site.data.keyword.cloud_notm}} regions.
    2. Monitor your application by using the [service REST API](https://ibm.co/2Gt9mB6) and dynamically shift your workload to a new region as needed.

Each consistent region is tied to {{site.data.keyword.cloud_notm}} region. In a disaster recovery scenario, Consistent Regions in an application do not have any role.
{:note .note}

