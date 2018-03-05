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


# 高可用性增强功能
{: #consistentregions}

由于业务需求，某些应用程序要求至少处理所有元组一次。{{site.data.keyword.streamsshort}} 通过操作程序和注释得到增强，这些操作程序和注释允许定义在流处理期间不会丢失元组的区域。至少处理一致区域中的元组一次。


如果使用 Beta-Entry 或 Beta-Enhanced 价格套餐，您现在可以使用 {{site.data.keyword.streaminganalyticsshort}}中定义的一致区域来运行和监视 Streams 应用程序。使用 Beta-Entry 或 Beta-Enhanced 套餐创建 {{site.data.keyword.streaminganalyticsshort}} 服务时，实例已配置为使用一致区域。

一致区域是一个子图，其中通过处理流上定义的点中的所有元组和标点符号来使操作程序的状态一致。这样可使子图中的元组至少处理一次。一致区域会定期排放其当前元组。一致区域中的所有元组都会进行处理，直至子图末尾。操作程序的内存中状态会自动序列化，并存储于区域中每个操作程序的检查点上。

您现在可以写入已保证元组处理的 Java 和 SPL 应用程序，并将这些应用程序部署到 {{site.data.keyword.streaminganalyticsshort}} 中。

可在有能力的操作程序上使用 `@consistent` 注释定义一致区域的开头。{{site.data.keyword.streamsshort}} 自动确定一致区域的作用域，但是您可使用 `@autonomous` 注释更改该区域的结束操作程序。所定义的一致区域将定期建立一致状态。

请查看 [{{site.data.keyword.streamsshort}} 文档 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.1/com.ibm.streams.dev.doc/doc/consistentregions.html) 以获取在 Streams 应用程序中使用一致区域的更多详细信息。
