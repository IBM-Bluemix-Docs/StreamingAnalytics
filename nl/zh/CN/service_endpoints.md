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

# 管理服务端点
{: #manage_endpoints}

使用专用端点时，{{site.data.keyword.Bluemix_short}} 服务端点支持通过内部 {{site.data.keyword.Bluemix_notm}} 网络连接到 {{site.data.keyword.streaminganalyticsshort}} 服务。
{:shortdesc}

现在，您可以添加专用端点以访问并管理服务实例。

## 先决条件
{: #prereqs notoc}

请确保满足以下需求：
- 通过使用非轻量 [V2 容器套餐](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)创建服务实例。
- 为 {{site.data.keyword.Bluemix_notm}} 帐户启用 [Virtual Route Forwarding (VRF)](/docs/infrastructure/direct-link?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud)。


要添加专用端点：

1. 在服务详细信息页面上，单击**管理端点**。您可以查看分配到服务实例的公共端点。
2. 单击**添加专用端点**。专用端点会分配到服务实例。
3. **可选。** 根据需要使用端点切换按钮来启用或禁用端点。


有关服务端点的更多信息，请查看 [{{site.data.keyword.Bluemix_notm}} 服务端点文档](/docs/services/service-endpoint?topic=service-endpoint-about#about){:new_window}。
