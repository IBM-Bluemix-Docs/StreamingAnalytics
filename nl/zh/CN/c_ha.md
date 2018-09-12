---

copyright:
  years: 2015, 2018
lastupdated: "2018-07-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics 高可用性
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} 使得您的应用程序具有高可用性。
如果在其中一个应用程序节点（{{site.data.keyword.streamsshort}} 资源）上检测到问题，那么会自动替换该节点，且会迁移在该节点上运行的任何作业。
仅当实例包含多个应用程序节点时，才会迁移和重新启动作业。
使用 [V1 服务套餐](/docs/services/StreamingAnalytics/service_plans.html)时，您可以使用[服务仪表板](/docs/services/StreamingAnalytics/r_service_dashboard.html)或 [{{site.data.keyword.streaminganalyticsshort}} V1 REST API ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://console.bluemix.net/apidocs/streaming-analytics-v1){:new_window} 来调整实例的大小。对于 V2 服务套餐，使用 [v2 REST API ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")https://console.bluemix.net/apidocs/streaming-analytics-v2){:new_window}
{:shortdesc}

此视频说明如何使用服务仪表板来调整实例大小：

<iframe width="560" height="315" title="调整实例大小" src="https://www.youtube.com/embed/zbZ9am9UhPw?rel=0" frameborder="0" allowfullscreen>调整实例大小</iframe>

## 一致区域
由于业务需求，某些应用程序要求至少处理所有元组一次。{{site.data.keyword.streamsshort}} 通过操作程序和注释得到增强，这些操作程序和注释允许定义在流处理期间不会丢失元组的区域。至少处理一致区域中的元组一次。

使用 {{site.data.keyword.streaminganalyticsshort}} 中定义的一致区域来运行和监视 Streams 应用程序。创建 {{site.data.keyword.streaminganalyticsshort}} 服务时，实例已配置为使用一致区域。

一致区域是一个子图，其中通过处理流上定义的点中的所有元组和标点符号来使操作程序的状态一致。这样可使子图中的元组至少处理一次。一致区域会定期排放其当前元组。一致区域中的所有元组都会进行处理，直至子图末尾。操作程序的内存中状态会自动序列化，并存储于区域中每个操作程序的检查点上。

您现在可以写入已保证元组处理的 Java 和 SPL 应用程序，并将这些应用程序部署到 {{site.data.keyword.streaminganalyticsshort}} 中。

可在有能力的操作程序上使用 `@consistent` 注释定义一致区域的开头。{{site.data.keyword.streamsshort}} 自动确定一致区域的作用域，但是您可使用 `@autonomous` 注释更改该区域的结束操作程序。所定义的一致区域将定期建立一致状态。

请查看 [{{site.data.keyword.streamsshort}} 文档 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.1/com.ibm.streams.dev.doc/doc/consistentregions.html) 以获取在 Streams 应用程序中使用一致区域的更多详细信息。
