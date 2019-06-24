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

# 高可用性和灾难恢复
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} 在 {{site.data.keyword.Bluemix_notm}} 位置（例如，达拉斯、华盛顿特区、伦敦和法兰克福）中具有高可用性。但是，要从影响整个 {{site.data.keyword.Bluemix_notm}} 区域的潜在灾难中恢复需要进行规划和准备工作。
{:shortdesc}


您负责了解服务的配置、定制和使用情况。还负责准备在新 {{site.data.keyword.Bluemix_notm}} 位置中重新创建服务实例，并将应用程序重新部署到该位置。请参阅[如何确保停机时间为零？](/docs/services/overview?topic=overview-zero-downtime#zero-downtime)以了解有关 {{site.data.keyword.Bluemix_notm}} 中高可用性和灾难恢复标准的更多信息。您还可以查找有关[服务级别协议](/docs/services/overview?topic=overview-zero-downtime#zero-downtime#SLAs)的信息。

## 高可用性

{{site.data.keyword.streaminganalyticsshort}} 使得您的应用程序具有高可用性。
您的应用程序会部署在 Kubernetes 集群中运行的 Docker 容器内。要编写高可用性应用程序，必须了解如何通过这些容器来确保高可用性：

* 应用程序资源是具有根据服务套餐分配的 CPU 和内存的容器。
* 在硬件或软件出现故障期间，容器可能会移动。容器移动时，处理元素会重新启动。
* 在计划维护期间，容器可能会移动（处理元素重新启动）。

因此，编写应用程序时，必须考虑到容器偶尔会移动。此外，还要考虑以下项：
* 确保处理元素可重新启动和重新定位。
* 确保应用程序能够容许以任何顺序重新启动其部分或全部处理元素 (PE)。
* 确保重新启动其处理元素时，Streams 应用程序中的源和 Sink 运算符配置为重新建立连接。

有关如何对应用程序进行故障诊断的示例，请查看 [{{site.data.keyword.streaminganalyticsshort}} 开发指南](https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/#troubleshooting)。

要实现高可用性，请启用 Streams 应用程序以保证处理所有元组。要完成已保证的元组处理，定期为一致区域中的所有操作程序建立一个检查点。一旦应用程序发生故障，所有操作程序都将回滚到上次成功的检查点状态。
{{site.data.keyword.streaminganalyticsshort}} 允许使用一致区域。

### 已保证的元组处理
由于业务需求，某些应用程序要求至少处理所有元组一次。{{site.data.keyword.streamsshort}} 通过操作程序和注释得到增强，这些操作程序和注释允许定义在流处理期间不会丢失元组的区域。至少处理一致区域中的元组一次。

如果在一致区域中检测到任何应用程序故障，那么 {{site.data.keyword.streaminganalyticsshort}} 可以将应用程序设置回上次一致状态（a.k.a. 检查点），并指示应用程序数据源从该点上重放元组。

使用 {{site.data.keyword.streaminganalyticsshort}} 中定义的一致区域来运行和监视 Streams 应用程序。创建 {{site.data.keyword.streaminganalyticsshort}} 服务时，实例已配置为允许使用一致区域。

一致区域是一个子图，其中通过处理流上定义的点中的所有元组和标点符号来使操作程序的状态一致。这样可使子图中的元组至少处理一次。一致区域会定期排空其当前元组。一致区域中的所有元组都会进行处理，直至子图末尾。操作程序的内存中状态会自动序列化，并存储于区域中每个操作程序的检查点上。

您可以编写已保证元组处理的 Java、SPL 和 Python 应用程序，并将这些应用程序部署到 {{site.data.keyword.streaminganalyticsshort}} 中。

可以在有能力的操作程序上使用 `@consistent` 注释定义一致区域的开头。{{site.data.keyword.streamsshort}} 自动确定一致区域的作用域，但是您可使用 `@autonomous` 注释更改该区域的结束操作程序。所定义的一致区域将定期建立一致状态。

请查看 [{{site.data.keyword.streamsshort}} 文档 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html) 以获取有关在 Streams 应用程序中使用一致区域的更多详细信息。

## 灾难恢复
{{site.data.keyword.streaminganalyticsshort}} 是在多个 {{site.data.keyword.Bluemix_notm}} 区域中提供的 GA 服务。{{site.data.keyword.streaminganalyticsshort}} 不会在 {{site.data.keyword.Bluemix_notm}} 上存储用户数据。

基于您的业务需求，请选择以下其中一种灾难恢复策略：
* 如果您希望不中断应用程序，请执行以下操作：
  1. 在多个 {{site.data.keyword.Bluemix_notm}} 区域中创建 {{site.data.keyword.streaminganalyticsshort}} 的实例。
  2. 向多个区域提交应用程序。


* 如果您希望尽量减少应用程序中断次数，请执行以下操作：
  1. 在多个 {{site.data.keyword.Bluemix_notm}} 区域中创建 {{site.data.keyword.streaminganalyticsshort}} 的实例。
  2. 通过使用[服务 REST API](https://ibm.co/2Gt9mB6) 来监视应用程序，并根据需要动态地将工作负载转移到新区域。

**注**：每个一致区域都与 {{site.data.keyword.Bluemix_notm}} 区域绑定。在灾难恢复方案中，应用程序中的一致区域没有任何角色。
