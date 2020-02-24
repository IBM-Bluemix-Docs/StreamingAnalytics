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
{:faq: data-hd-content-type='faq'}

# FAQs
{: #faq}

## How do I sign up for Streaming Analytics service?
{: #signup notoc}
{: faq}  

For more information about the {{site.data.keyword.streaminganalyticsshort}} service plans, see the [{{site.data.keyword.Bluemix_short}} catalog](https://{DomainName}/catalog/services/streaming-analytics).

## What version of Streaming Analytics service am I using?
{: #version notoc}
{: faq}   

Improvements are pushed regularly to all {{site.data.keyword.streaminganalyticsshort}} services. You always use the latest version of the managed service, and you must not keep track of any no product version or level.

## What does IBM manage for me?
{: #ibm_manage notoc}
{: faq}   

We handle installation, software upgrades, creating and managing domains, and hardware maintenance. The service includes 24 x 7 health monitoring.


## What tasks am I responsible for?  
{: #responsible notoc}
{: faq}

You write the applications that run in a {{site.data.keyword.streaminganalyticsshort}} service and Streams instance on-prem and ensure that they are functioning correctly and meeting performance requirements. You are also responsible for any application-specific monitoring.

## Is high availability (HA) supported?
{: #ha notoc}
{: faq}

High availability is managed by IBM. {{site.data.keyword.streaminganalyticsshort}} is configured to support HA. More server resources are in place in the event of a failover.

## How is security managed for the Streaming Analytics service?
{: #security notoc}
{: faq}   

Security is fully managed by IBM. Credentials are generated for each service and are provided to you. Security updates are managed and applied by IBM promptly after they become available.

## Do I need to configure a Streaming Analytics service?  
{: #configure notoc}
{: faq}

The service is created and fully managed by IBM. Each service consists of a dedicated set of application resources.

## How do I develop Streams applications?
{: #streamsapp notoc}
{: faq}

You must develop Streams applications locally by using the free Streams [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-docker/).

You can also use the on-premises {{site.data.keyword.streamsshort}} installation if you have one. Applications that you develop and compile locally can then be seamlessly deployed as a bundle to a Streams service in the cloud.

But if you want to run your Python applications in the cloud, you don’t need to install {{site.data.keyword.streamsshort}} on-premises. Simply use the `STREAMING\_ANALYTICS\_SERVICE` context to submit your Python applications to the {{site.data.keyword.streaminganalyticsshort}} service. You can develop the applications in a standard Python development environment or in a Jupyter interactive notebook, but you must use Python 3.5.

For more information on developing applications, see the [{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.streaminganalyticsshort}} Development Guide ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/).

## Can I sign in to a Streaming Analytics service host directly?
{: #host notoc}  
{: faq}

No. A direct login to the server with Telnet or a Secure Shell (ssh) is not supported. You cannot install additional software or run non-Streams software on a Streams host.

## Can I access the file system on the Streaming Analytics service?
{: #filesystem notoc}
{: faq}   

Only your Streams applications can directly access the file system on a Streams host.

Cloud-ready alternatives exist for solutions that need a mechanism for Streams to interact with other solution components. You can use other source and sink protocols instead of files. For example, cloud-based data stores.

## How can the Streaming Analytics service applications access my organization's enterprise data?
{: #access notoc}  

You can use the [{{site.data.keyword.Bluemix_notm}} Secure Gateway Service](https://{DomainName}/catalog/services/secure-gateway) to securely connect streams applications to your enterprise.

## Are all the features for IBM Streams for on premises supported by the Streaming Analytics service in the cloud?
{: #features notoc}

Some of the features that are not supported for {{site.data.keyword.streaminganalyticsshort}} service include:

  - Administrative tasks for an instance that require domain authority. For example, adding custom host tags or creating a job group.
  - Consistent region checkpoints.
  - Some of the toolkit operators are not supported. For more information, see [Supported toolkits and adapters](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-compatible_toolkits).
  - The Streams JMX API.

## Where can I learn more about the Streaming Analytics service?
{: #roadmap notoc}

The IBM developerWorks® article, [Roadmap for {{site.data.keyword.streaminganalyticsshort}} Service on {{site.data.keyword.Bluemix_notm}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/streamsdev/docs/roadmap-for-streaming-analytics-service-on-bluemix/), has guidance for learning about the service, plus links to informative blogs, demos, and articles.
