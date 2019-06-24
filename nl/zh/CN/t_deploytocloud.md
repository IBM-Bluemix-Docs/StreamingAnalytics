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

# 将 Streams 应用程序部署到云
{: #t_deploytocloud}

您可以将 {{site.data.keyword.streamsshort}} 应用程序部署到在 {{site.data.keyword.Bluemix_short}} 中运行的 {{site.data.keyword.streaminganalyticsshort}} 实例。
{:shortdesc}

在 {{site.data.keyword.streamsshort}} 环境中，{{site.data.keyword.streamsshort}} 应用程序是使用 {{site.data.keyword.streamsshort}} Processing Language (SPL)、SPL、Java、Scala 或 Python 编写的。现在您可以在没有 {{site.data.keyword.streamsshort}} 环境的情况下开发 Streams Python 应用程序。请参阅[将 {{site.data.keyword.streamsshort}} Python 应用程序部署到云](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_deploytocloud#t_deploypython)


{{site.data.keyword.streaminganalyticsshort}} 未在云中包括 {{site.data.keyword.streamsshort}} 开发环境，但是您可以将本地开发的应用程序部署到云。

开始之前，先禁用浏览器的弹出窗口阻止程序，以显示 {{site.data.keyword.streaminganalyticsshort}} 控制台。

要将 {{site.data.keyword.streamsshort}} 应用程序部署到云：

1. 设置用于开发和测试应用程序的开发环境。

	如果要使用 {{site.data.keyword.streamsshort}} 环境，那么您可以免费下载 [V1 服务套餐](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)的 [{{site.data.keyword.streamsshort}} Quick Start Edition ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}。
使用 [V2 服务套餐](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)的 [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi){:new_window}。

2. 在开发环境中开发流式应用程序。在 {{site.data.keyword.streamsshort}} 开发环境中，可以使用 Streams Studio 或命令行工具来开发应用程序。

3. 验证流式应用程序在开发环境中是否正常运行。
**注意：**如果您要使用 V2 服务套餐，那么必须以 Red Hat Enterprise Linux (RHEL) 7.x 编译应用程序，如果您要使用 V1 服务套餐，那么必须使用 RHEL 6.5 编译应用程序。

4. 使用以下某种方法，将与您 SPL、Java、Scala 或 Python 应用程序相关联的应用程序捆绑软件（.sab 文件）提交到云中的服务实例：
	* 使用 {{site.data.keyword.streaminganalyticsshort}} 控制台，来提交应用程序捆绑软件。

  * 在 {{site.data.keyword.Bluemix_notm}} 中创建应用程序并向其添加 {{site.data.keyword.streamsshort}} 应用程序。使用 [{{site.data.keyword.streaminganalyticsshort}} V1 REST API ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window}（适用于 [V1 服务套餐](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)）或 [{{site.data.keyword.streaminganalyticsshort}} V2 REST API ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window}（适用于 V2 服务套餐）进行控制。

现在，您的应用程序已在云中部署。您可以在 {{site.data.keyword.streaminganalyticsshort}} 服务中监视应用程序。您还可以将多个应用程序（.sab 文件）提交到服务实例。多少个都可以。

{{site.data.keyword.streamsshort}} 还支持若干 Java™ Development Kit，您可用于开发应用程序。有关 {{site.data.keyword.streamsshort}} 中 Java 支持的更多信息，请参阅[应用程序开发支持的 Java Development Kit ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.install.doc/doc/ibminfospherestreams-install-prerequisites-java-supported-sdks.html){:new_window}。

## 将 Streams Python 应用程序部署到云
{: #t_deploypython}

将 {{site.data.keyword.streamsshort}} Python 应用程序部署到在 {{site.data.keyword.Bluemix_short}} 中运行的 {{site.data.keyword.streaminganalyticsshort}} 服务。无需安装 {{site.data.keyword.streamsshort}}。
{:shortdesc}

利用 streamsx 程序包中包含的 [{{site.data.keyword.streamsshort}} Python 应用程序 API ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features){:new_window}，您可以将 Python 应用程序部署到 {{site.data.keyword.streaminganalyticsshort}} 服务。查看[针对 {{site.data.keyword.streaminganalyticsshort}} 服务进行开发 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html){:new_window} 教程以获取有关如何针对 {{site.data.keyword.streaminganalyticsshort}} 服务创建和部署简单 Python 应用程序的示例。

{{site.data.keyword.DSX_full}} 还支持在 Jupyter 交互式配置页中提交 Python 应用程序。有关更多信息，请参阅[开发针对 {{site.data.keyword.streaminganalyticsshort}} 的 Python 应用程序](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_develop_apps_python)。
