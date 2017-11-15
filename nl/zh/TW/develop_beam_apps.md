---

copyright:
  years: 2015, 2017
lastupdated: "2017-10-27"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# 在 Streaming Analytics 中部署 Beam 應用程式
{: #develop_beam_apps}

您現在可以在本端 {{site.data.keyword.streamsshort}} 開發環境中開發 Beam 應用程式，並在 {{site.data.keyword.streaminganalyticsshort}} 部署這些應用程式。
{:shortdesc}

{{site.data.keyword.streamsshort}} Runner for Apache Beam 會在 {{site.data.keyword.streamsshort}} 環境執行 Beam 管線。使用 Streams Runner 啟動的 Beam 應用程式會轉換成 Streams Application Bundle (SAB) 檔案，然後您可以在 {{site.data.keyword.streaminganalyticsshort}} 部署及監視它。

若要將 Beam 應用程式提交至 {{site.data.keyword.Bluemix_notm}} 上的 {{site.data.keyword.streaminganalyticsshort}} 服務，您必須建立 JSON 格式的 VCAP 檔案，其中存放認證和服務的其他資訊。

1. 在 Streams 本端環境中，導覽至安裝工具箱之處的 samples 子資料夾 ($STREAMS_BEAM_RUNNER/samples)，並將 template.vcap 檔複製為新的檔案。請給予檔案有意義的檔案，及副檔名 .vcap。
1. [複製 {{site.data.keyword.streaminganalyticsshort}} 服務的認證](/docs/services/StreamingAnalytics/r_vcap_services.md)，並將認證貼在您建立的 VCAP 檔案，取代下行：
```
 <REMOVE THIS LINE AND INSERT CREDENTIALS HERE>
 ```
1. 驗證 Beam 應用程式在開發環境中適當地執行。當您使用 Streams Runner 啟動 Beam 應用程式時，應用程式會轉換成 Streams Application Bundle (SAB) 檔案。
1. 將與您的 Beam 應用程式相關聯的 SAB 檔案提交到 {{site.data.keyword.streaminganalyticsshort}}

您的應用程式現在已部署在雲端中。您可以使用 {{site.data.keyword.streaminganalyticsshort}} 服務來監視應用程式。

如需在 {{site.data.keyword.streaminganalyticsshort}} 中部署及監視 Beam 應用程式的詳細資料，請參閱 [Streams Runner for Apache Beam ](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/)。
