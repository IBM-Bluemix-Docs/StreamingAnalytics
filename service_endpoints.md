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

# Managing service endpoints
{: #manage_endpoints}

By using an internal endpoint, {{site.data.keyword.Bluemix_short}} Service Endpoint enables the connection to the {{site.data.keyword.streaminganalyticsshort}} service through the internal IBM Cloud network.
{:shortdesc}

You can now add an internal endpoint to access and manage your service instance.

## Prerequisites
{: #prereqs notoc}

Ensure that you meet the following requirements:
- Create your service instance by using the non-Lite [v2 container plans](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans).
- Create your service instance in the {{site.data.keyword.Bluemix_short}} United Kingdom (London) or Germany (Frankfurt) regions.
- Enable [Virtual Route Forwarding (VRF)](/docs/infrastructure/direct-link?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud) for your {{site.data.keyword.Bluemix_short}} account.


To add an internal endpoint:

1. On the service details page, click **Manage endpoints**. You can see the external endpoint assigned to your service instance.
2. Click  **Add internal endpoint**. An internal endpoint is assigned to your service instance.
3. **Optional.** Use the endpoint toggle to enable or disable endpoints as needed.


For more information about service endpoints, check out the [{{site.data.keyword.Bluemix_short}} Service Endpoint documentation](/docs/services/service-endpoint?topic=about){:new_window}.
