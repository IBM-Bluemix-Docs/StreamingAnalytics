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

# 管理服务端点
{: #manage_endpoints}

使用内部端点时，{{site.data.keyword.Bluemix_short}} Service Endpoint 支持通过内部 IBM Cloud 网络连接到 {{site.data.keyword.streaminganalyticsshort}} 服务。
{:shortdesc}

现在，您可以添加内部端点以访问并管理服务实例。

## 先决条件
{: #prereqs notoc}

请确保满足以下需求：
- 通过使用非轻量 [V2 容器套餐](/docs/services/StreamingAnalytics/service_plans.html)创建服务实例。
- 在 {{site.data.keyword.Bluemix_short}} 英国（伦敦）或德国（法兰克福）区域创建服务实例。
- 为 {{site.data.keyword.Bluemix_short}} 帐户启用 [Virtual Route Forwarding (VRF)](/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud)。


要添加内部端点：

1. 在服务详细信息页面上，单击**管理端点**。您可以查看分配到服务实例的内部端点。
2. 单击**添加内部端点**。将内部端点分配到服务实例。
3. **可选。** 根据需要使用端点切换按钮来启用或禁用端点。


有关服务端点的更多信息，请查看 [{{site.data.keyword.Bluemix_short}} 服务端点文档](/docs/services/service-endpoint/getting-started.html#about){:new_window}。
