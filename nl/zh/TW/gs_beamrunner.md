---

copyright:
  years: 2015, 2017
lastupdated: "2017-12-15"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics 中的 IBM Streams Runner for Apache Beam
{: #gs_beamrunner}

如果您有 {{site.data.keyword.streamsshort}} 開發環境，您現在可以在環境中本端開發 Beam 應用程式，然後將這些應用程式提交到 {{site.data.keyword.Bluemix_notm}} 中的 {{site.data.keyword.streaminganalyticsshort}} 服務。{{site.data.keyword.streamsshort}} Runner for Apache Beam 會在 {{site.data.keyword.streamsshort}} 環境執行 Beam 管線。使用 Streams Runner 啟動的 Beam 應用程式會轉換成 Streams Application Bundle (SAB) 檔案，然後您可以在 {{site.data.keyword.streaminganalyticsshort}} 部署及監視它。


從使用[範例應用程式](/docs/services/StreamingAnalytics/c_starterapps.html)開始，了解如何在 {{site.data.keyword.streaminganalyticsshort}} 服務提交及監視 Beam 應用程式。您可以從 {{site.data.keyword.streaminganalyticsshort}} 主控台下載範例應用程式。

請參閱 [{{site.data.keyword.streamsshort}} Runner for Apache Beam 文件 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/){:new_window}，以查看顯示 Streams Runner 如何適用於 [Beam 功能矩陣] 的表格。請參閱[安裝 IBM Streams Runner for Apache Beam ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://bit.ly/2zFDpPr){:new_window}，以取得如何在 Streams 環境安裝 `com.ibm.streams.beam` 工具箱的指示，建立您可以在 {{site.data.keyword.streaminganalyticsshort}} 提交及監視的 Beam 應用程式。

熟悉 Beam 程式設計會有幫助，但並非必要；[Apache Beam 網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://beam.apache.org/documentation/){:new_window} 有實用的 [Apache Beam Java SDK 快速入門 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://beam.apache.org/get-started/quickstart-java/){:new_window} 頁面及其他文件。
