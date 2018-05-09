---

copyright:
  years: 2015, 2018
lastupdated: "2018-04-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics 中的 IBM Streams Runner for Apache Beam
{: #gs_beamrunner}

如果您拥有 {{site.data.keyword.streamsshort}} 开发环境，那么现在可以在环境中本地开发 Beam 应用程序，然后向 {{site.data.keyword.Bluemix_notm}} 中的 {{site.data.keyword.streaminganalyticsshort}} 服务提交这些应用程序。{{site.data.keyword.streamsshort}} Runner for Apache Beam 在 {{site.data.keyword.streamsshort}} 环境中执行 Beam 管道。使用 Streams Runner 启动的 Beam 应用程序将转换为 Streams 应用程序捆绑软件 (SAB) 文件，然后可以在 {{site.data.keyword.streaminganalyticsshort}} 中进行部署和监视。


首先，使用[样本应用程序](/docs/services/StreamingAnalytics/c_starterapps.html)来了解如何在 {{site.data.keyword.streaminganalyticsshort}} 服务中提交和监视 Beam 应用程序。可以从 {{site.data.keyword.streaminganalyticsshort}} 控制台下载样本应用程序。

查看 [{{site.data.keyword.streamsshort}}Runner for Apache Beam 文档 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/){:new_window}，以了解说明 Streams Runner 如何适应 [Beam 功能矩阵] 的表。请参阅[安装 IBM Streams Runner for Apache Beam ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://bit.ly/2zFDpPr){:new_window}，以获取有关如何在 Streams 环境中安装 `com.ibm.streams.beam` 工具箱，以创建可以在 {{site.data.keyword.streaminganalyticsshort}} 中提交和监视的 Beam 应用程序。

对 Beam 编程略有些了解会很有帮助，但这不是必需的；[Apache Beam Web 站点 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://beam.apache.org/documentation/){:new_window} 具有十分有用的 [Apache Beam Java SDK Quickstart ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://beam.apache.org/get-started/quickstart-java/){:new_window} 页面和其他文档。
