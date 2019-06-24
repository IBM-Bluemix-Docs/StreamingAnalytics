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

# 常见问题
{: #faq}

## 如何注册 Streaming Analytics 服务？
{: #signup notoc}
{: faq}  

有关 {{site.data.keyword.streaminganalyticsshort}} 服务套餐的更多信息，请参阅 [{{site.data.keyword.Bluemix_short}} 目录](https://{DomainName}/catalog/services/streaming-analytics)。

## 我使用的是哪个版本的 Streaming Analytics 服务？
{: #version notoc}
{: faq}   

所有 {{site.data.keyword.streaminganalyticsshort}} 服务都会定期改进。您始终会使用最新版本的受管服务，而无需跟踪任何产品版本或级别。

## IBM 会为我做什么？
{: #ibm_manage notoc}
{: faq}   

我们处理安装、软件升级、创建和管理域，以及硬件维护。服务包括 24 x 7 运行状况监视器。


## 我负责做什么工作？  
{: #responsible notoc}
{: faq}

您编写要在 {{site.data.keyword.streaminganalyticsshort}} 服务和 Streams 实例内部部署中运行的应用程序，并确保它们运作正常且满足性能需求。您还负责任何特定于应用程序的监视。

## 支持高可用性 (HA) 吗？
{: #ha notoc}
{: faq}

高可用性由 IBM 进行管理。{{site.data.keyword.streaminganalyticsshort}} 配置为支持 HA。在发生故障转移时，可以使用更多服务器资源。

## Streaming Analytics 服务的安全性是如何管理的？
{: #security notoc}
{: faq}   

安全性由 IBM 完全管理。针对每个服务，都会生成凭证并提供给您。安全性更新可用时立即由 IBM 管理和应用。

## 我需要配置 Streaming Analytics 服务吗？  
{: #configure notoc}
{: faq}

该服务由 IBM 创建并完全管理。每个服务都包含一组专用应用程序资源。

## 如何开发 Streams 应用程序？
{: #streamsapp notoc}
{: faq}

对于 [V2 服务套餐](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，必须使用免费的 Streams [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-docker/) 在本地开发 Streams 应用程序，如果要使用 [V1 服务套餐](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，那么可以下载 [{{site.data.keyword.streamsshort}} Quick Start Edition VM 映像 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}。

您还可以使用内部部署 {{site.data.keyword.streamsshort}} 安装（如果有的话）。然后，您在本地开发并编译的应用程序可以作为捆绑软件无缝地部署到云中的 Streams 服务。

但是，如果您想要运行云中的 Python 应用程序，您无需安装 {{site.data.keyword.streamsshort}} 内部部署。只要使用 `STREAMING\_ANALYTICS\_SERVICE` 上下文，将 Python 应用程序提交到 {{site.data.keyword.streaminganalyticsshort}} 服务即可。您可以在标准 Python 开发环境或 Jupyter 交互配置页中开发应用程序，但是必须使用 Python 3.5。

有关开发应用程序的更多信息，请参阅 [{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.streaminganalyticsshort}} 开发指南 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/streamsdev/?p=16589&post_type=doc&preview=1&_ppp=7ad76a418b)。

## 我可以直接登录到 Streaming Analytics 服务主机吗？
{: #host notoc}  
{: faq}

不可以。不支持使用 Telnet 或 Secure Shell (ssh) 直接登录到服务器。您无法在 Streams 主机上安装其他软件或运行非 Streams 软件。

## 我可以访问 Streaming Analytics 服务上的文件系统吗？
{: #filesystem notoc}
{: faq}   

只有 Streams 应用程序才可以直接访问 Streams 主机上的文件系统。

对于某些解决方案，它们需要一种让 Streams 与其他解决方案组件进行交互的机制，此时可以使用云就绪替代方法。您可以使用其他源和接收器协议来替代文件。例如，基于云的数据存储。

## Streaming Analytics 服务应用程序如何访问组织的企业数据？
{: #access notoc}  

您可以使用 [{{site.data.keyword.Bluemix_notm}} Secure Gateway 服务](https://{DomainName}/catalog/services/secure-gateway)，将 Streams 应用程序安全地连接到企业。

## 云中的 Streaming Analytics 服务支持内部部署的 IBM Streams 的所有功能吗？
{: #features notoc}

有一些功能不支持用于 {{site.data.keyword.streaminganalyticsshort}} 服务，包括以下功能：

  - 需要域授权的实例的管理任务。例如，添加定制主机标记或创建作业组。
  - 一致区域检查点。
  - 不支持一些工具箱操作程序。有关更多信息，请参阅[支持的工具箱和适配器](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-compatible_toolkits)。
  - Streams JMX API。

## 在哪里可以了解到有关 Streaming Analytics 服务的更多信息？
{: #roadmap notoc}

IBM developerWorks® 文章 [Roadmap for {{site.data.keyword.streaminganalyticsshort}} Service on {{site.data.keyword.Bluemix_notm}} ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/streamsdev/docs/roadmap-for-streaming-analytics-service-on-bluemix/) 提供了解服务的指南，以及指向具有详细信息的博客、演示和文章的链接。
