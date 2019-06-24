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

# 关于 Streaming Analytics
{: #about}

作为您 {{site.data.keyword.Bluemix_short}} 应用程序的一部分，您可以使用 {{site.data.keyword.streaminganalyticsfull}}，对动态数据执行实时分析。
{:shortdesc}

第一次使用 {{site.data.keyword.streaminganalyticsshort}}？获取[服务的快速简介 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/streamsdev/docs/streaming-analytics-now-available-bluemix-2/){:new_window}。

{{site.data.keyword.streaminganalyticsshort}} 服务提供下列功能，可在云中部署、分析和监视数据：


**服务的交互和编程使用：**

您可以通过 [{{site.data.keyword.streaminganalyticsshort}} 控制台](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-console#console)以交互方式使用该服务；如果您使用的是 [V1 服务套餐](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，那么也可以通过 [{{site.data.keyword.streaminganalyticsshort}} V1 REST API ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} 以编程方式使用该服务。对于 [V2 服务套餐](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，可以使用 [{{site.data.keyword.streaminganalyticsshort}} V2 REST API ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/apidocs/streaming-analytics-v2)。

**部署和监视 SPL、Java、Scala 和 Python 应用程序：**

您可以用 SPL、Java、Scala 和 Python 编写 {{site.data.keyword.streamsshort}} 应用程序。使用 {{site.data.keyword.streaminganalyticsshort}} 控制台[部署和监视这些应用程序](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_deploytocloud)。

如果要使用 SPL 编写应用程序，{{site.data.keyword.streamsfull}} Processing Language (SPL) 是用于创建流处理应用程序的编程语言。如果您想要进一步使用自己的 SPL 应用程序，可以获取 {{site.data.keyword.streamsshort}} 开发环境，而且必须使 SPL 应用程序处于云就绪状态。

要在没有 {{site.data.keyword.streamsshort}} 开发环境的情况下创建和部署 Python 应用程序，请使用 {{site.data.keyword.DSX_short}} 中的服务配置页或 {{site.data.keyword.streamsshort}} Python API。有关更多信息，请参阅[开发针对 {{site.data.keyword.streaminganalyticsshort}} 的 Python 应用程序](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_develop_apps_python)。

您可以在本地开发环境中使用 Streams Runner 来开发 Beam 应用程序，然后在 {{site.data.keyword.streaminganalyticsshort}} 服务中进行部署和监视。有关使用 Streams Runner 的 Beam 应用程序的更多信息，请参阅 [{{site.data.keyword.streaminganalyticsshort}} 中的 IBM Streams Runner for Apache Beam](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-gs_beamrunner)。


**与 {{site.data.keyword.streamsshort}} 操作程序的兼容性：**

[{{site.data.keyword.streamsshort}} Processing Language (SPL) 标准工具箱](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-compatible_toolkits)中的 {{site.data.keyword.streamsshort}} 操作程序与 {{site.data.keyword.streaminganalyticsshort}} 兼容。

## Streaming Analytics 职责
{: #responsibilities notoc}

### 客户职责
{: #clientresponsibilities notoc}

客户负责：

* 遵循 IBM 最初的 {{site.data.keyword.streamsshort}} 配置，监视、配置和管理在其实例中运行的 {{site.data.keyword.streamsshort}} 作业。
客户可灵活地启动和停止实例，以及启动和停止在实例上运行的作业。
* 根据需要，在服务上开发程序和应用程序，以分析数据并从中获得洞察。
客户还负责所开发此类程序或应用程序的质量和性能。
程序可能通过 {{site.data.keyword.streamsshort}} Topology 功能，使用 SPL、Java 或其他受支持的语言开发。
它们必须通过用于 {{site.data.keyword.streaminganalyticsshort}} 的相同操作系统，使用 {{site.data.keyword.streamsshort}} Developer Edition 或 {{site.data.keyword.streamsshort}} Quick Start Edition 进行编译。
* 定期检查以下链接，以随时了解已安排的非中断性或中断性停机 - [https://developer.ibm.com/bluemix/support/#status ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/bluemix/support/#status){:new_window}  
* 根据业务需求，备份所有数据、元数据、配置文件和环境参数，以确保连续性。

* 在可能发生的任何类型的故障中，从任何备份复原数据、元数据、配置文件和环境参数，以确保连续性。
这包括但不限于数据中心或 pod 故障、服务器故障、硬盘故障或软件故障。

### IBM 职责
{: #ibmresponsibilities notoc}

作为 {{site.data.keyword.streaminganalyticsfull}} 的一部分，IBM 将：

* 为客户实例提供和管理服务器、存储器和网络基础架构。
* 根据所选的资源数，提供 {{site.data.keyword.streamsshort}} 的初始配置。
* 为面向因特网的内部防火墙提供和管理基础架构，用于保护和隔离。

* 在 {{site.data.keyword.streaminganalyticsshort}} 上监视和管理以下组件：
	* 网络组件
	* 服务器及其本地存储器
	* 基础架构操作系统
	* {{site.data.keyword.streamsshort}} 管理服务
	* {{site.data.keyword.streamsshort}} 实例
* 为基础架构操作系统和 {{site.data.keyword.streamsshort}} 提供维护补丁，包括适当的安全补丁。
* 执行应该不需要任何系统停机的定期维护（“非中断性”维护），以及可能需要一些系统停机和重新启动的维护（“中断性”维护），这些维护将在 [https://developer.ibm.com/bluemix/support/#status ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/bluemix/support/#status){:new_window} 中发布的所安排时间执行
* 对所安排维护时间的任何更改都以适当的通知形式发布。
