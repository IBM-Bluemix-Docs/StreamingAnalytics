---

copyright:
  years: 2015, 2021
lastupdated: "2021-06-07"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Managing service endpoints
{: #manage_endpoints}

By using a private endpoint, {{site.data.keyword.cloud}} Service Endpoint enables the connection to the {{site.data.keyword.streaminganalyticsshort}} service through the internal {{site.data.keyword.cloud_notm}} network.
{:shortdesc}

You can now add an private endpoint to access and manage your service instance.

## Prerequisites
{: #prereqs notoc}

Ensure that you meet the following requirements:
- Create your service instance by using the non-Lite [plan](/docs/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans).
- Enable [virtual routing and forwarding (VRF)](/docs/direct-link?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud) for your {{site.data.keyword.cloud_notm}} account.

To add an private endpoint:

1. On the service details page, click **Manage endpoints**. You can see the public endpoint assigned to your service instance.
2. Click  **Add private endpoint**. A private endpoint is assigned to your service instance.
3. **Optional.** Use the endpoint toggle to enable or disable endpoints as needed.


For more information about service endpoints, check out the [{{site.data.keyword.cloud_notm}} Service Endpoint documentation](/docs/account?topic=account-service-endpoints-overview){:new_window}.
