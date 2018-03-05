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

# Beta-Entry 和 Beta-Enhanced 套餐
{: #beta_plans}

新的 {{site.data.keyword.streaminganalyticsshort}} 服务 Beta-Entry 和 Beta-Enhanced 套餐包括对现有服务套餐的数个增强功能和差异：
{:shortdesc}

**新的 [{{site.data.keyword.streamsshort}} QSE for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi)：**{{site.data.keyword.streamsshort}} Quick Start Edition 是免费的 {{site.data.keyword.streamsshort}} 非生产版本。要使用 Beta-Entry 和 Beta-Enhanced 套餐来将应用程序部署到 {{site.data.keyword.streaminganalyticsshort}}，您必须使用 Red Hat Enterprise Linux (RHEL) 7 版本的 {{site.data.keyword.streamsshort}} QSE 来编译应用程序。请查看 [Beta 部署指南 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/streamsdev/docs/cloud-beta-devguide/) 以了解如何搭配使用 Docker 环境中运行的新 Streams QSE 与 RHEL 7 来编译和部署新的 {{site.data.keyword.streaminganalyticsshort}} beta 套餐中的应用程序。   

**{{site.data.keyword.streaminganalyticsshort}} V2 REST API：**您可以使用 [{{site.data.keyword.streaminganalyticsshort}} V2 REST API ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#introduction) 来管理服务实例和 {{site.data.keyword.streamsshort}} 作业。{{site.data.keyword.streaminganalyticsshort}} V2 API 仅在使用其中一个新 beta 套餐创建的服务实例上受支持。[V1 REST API ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://console.bluemix.net/apidocs/220-streaming-analytics?&language=node#introduction) 仅在现有 {{site.data.keyword.streaminganalyticsshort}} 实例以及使用现有服务套餐创建的任何新实例上受支持。

**新的入门模板和样本应用程序：**由于新的 beta 套餐需要在 RHEL 7 上运行 Streams，因此很多现有样本应用程序无法用于新的 beta 套餐。{{site.data.keyword.streaminganalyticsshort}} 提供了[一组新的入门模板和样本应用程序]( https://developer.ibm.com/streamsdev/docs/cloud-beta-samples/)，可让您快速开始使用新的 beta 套餐。

**高可用性增强功能：**通过定义一致区域，避免流处理应用程序中发生数据丢失。{{site.data.keyword.streamsshort}} 通过操作程序和注释得到增强，这些操作程序和注释允许定义在流处理期间不会丢失元组的区域。至少处理一致区域中的元组一次。如果使用 Beta-Entry 或 Beta-Enhanced 价格套餐，您现在可以使用 [{{site.data.keyword.streaminganalyticsshort}}中定义的一致区域](/docs/services/StreamingAnalytics/consistentregions.html)来运行和监视 Streams 应用程序。

**新的问题确定功能：**Beta-Entry 和 Beta-Enhanced 套餐包括数个增强功能来帮助您快速查找和解决应用程序中的错误。有关更多详细信息，请参阅 [{{site.data.keyword.streaminganalyticsshort}} 控制台提供了更多查找和解决错误的方法（Beta 套餐）![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")。](https://wp.me/p4IICn-4cx)

**监视云的操作程序行为和保证的元组处理：**{{site.data.keyword.streamsshort}} 提供了度量值来帮助评估 {{site.data.keyword.streamsshort}} 服务的运行状况，协助诊断性能问题以及分析请求的吞吐量。您可以使用 {{site.data.keyword.streaminganalyticsshort}} 中的 Streams 控制台来[监视操作程序行为并确保资源优化 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")。](https://wp.me/p4IICn-4bH)
