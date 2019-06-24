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

# 在 Streaming Analytics 中部署 Beam 应用程序
{: #develop_beam_apps}

现在可以在本地 {{site.data.keyword.streamsshort}} 开发环境中开发 Beam 应用程序，并在 {{site.data.keyword.streaminganalyticsshort}} 中部署这些应用程序。
{:shortdesc}

{{site.data.keyword.streamsshort}} Runner for Apache Beam 在 {{site.data.keyword.streamsshort}} 环境中执行 Beam 管道。使用 Streams Runner 启动的 Beam 应用程序将转换为 Streams 应用程序捆绑软件 (SAB) 文件，然后可以在 {{site.data.keyword.streaminganalyticsshort}} 中进行部署和监视。

要向 {{site.data.keyword.Bluemix_notm}} 上的 {{site.data.keyword.streaminganalyticsshort}} 服务提交 Beam 应用程序，必须创建 JSON 格式的 VCAP 文件，用于保存服务的凭证和其他信息。

1. 在 Streams 本地环境中，浏览到安装工具箱的样本子文件夹 (`$STREAMS_BEAM_RUNNER/samples`)，然后将 template.vcap 文件复制到新文件。为该文件提供一个有意义的名称及文件扩展名 `.vcap`。
1. [复制 {{site.data.keyword.streaminganalyticsshort}} 服务的凭证](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans#vcap_services)，并将凭证粘贴到所创建的 VCAP 文件中，然后替换以下行：
```
 <REMOVE THIS LINE AND INSERT CREDENTIALS HERE>
 ```
1. 验证 Beam 应用程序在开发环境中是否正常运行。使用 Streams Runner 启动 Beam 应用程序时，该应用程序将转换为 Streams 应用程序捆绑软件 (SAB) 文件。
1. 向 {{site.data.keyword.streaminganalyticsshort}} 提交与 Beam 应用程序关联的 SAB 文件

现在，您的应用程序已在云中部署。您可以使用 {{site.data.keyword.streaminganalyticsshort}} 服务来监视应用程序。

有关在 {{site.data.keyword.streaminganalyticsshort}} 中部署和监视 Beam 应用程序的更多信息，请参阅 [Streams Runner for Apache Beam ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/)。
