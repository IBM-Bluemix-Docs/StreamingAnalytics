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

# 測試版入門方案及測試版加強方案
{: #beta_plans}

{{site.data.keyword.streaminganalyticsshort}} 服務的新「測試版入門」及「測試版加強」方案包含數項加強功能以及與現有服務方案的差異：
{:shortdesc}

**新的 [{{site.data.keyword.streamsshort}} QSE for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi)：**{{site.data.keyword.streamsshort}} Quick Start Edition 是免費的 {{site.data.keyword.streamsshort}} 非正式作業版本。若要使用「測試版入門」及「測試版加強」方案，將應用程式部署至 {{site.data.keyword.streaminganalyticsshort}}，您必須使用 Red Hat Enterprise Linux (RHEL) 7 版本的 {{site.data.keyword.streamsshort}} QSE 來編譯您的應用程式。
請參閱[測試版開發指南 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/streamsdev/docs/cloud-beta-devguide/)，瞭解如何使用新的 Streams QSE 與 Docker 環境中執行的 RHEL 7 搭配，以利用新的 {{site.data.keyword.streaminganalyticsshort}} 測試版方案編譯及部署您的應用程式。   

**{{site.data.keyword.streaminganalyticsshort}} 第 2 版 REST API：**您可以使用 [{{site.data.keyword.streaminganalyticsshort}} 第 2 版 REST API ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#introduction) 來管理服務實例及 {{site.data.keyword.streamsshort}} 工作。{{site.data.keyword.streaminganalyticsshort}} 第 2 版 API 只有在使用其中一個新的測試版方案建立的服務實例上才受到支援。[第 1 版 REST API ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://console.bluemix.net/apidocs/220-streaming-analytics?&language=node#introduction) 則只有在現有 {{site.data.keyword.streaminganalyticsshort}} 實例及任何使用現有服務方案建立的新實例上才受到支援。

**新的入門範本及範例應用程式：**由於新的測試版方案需要在 RHEL 7 上執行 Streams，因此許多現有的範例應用程式不適用於新的測試版方案。{{site.data.keyword.streaminganalyticsshort}} 提供了[一組新的入門範本及範例應用程式]( https://developer.ibm.com/streamsdev/docs/cloud-beta-samples/)，以協助您快速開始使用新的測試版方案。

**高可用性加強功能：**藉由定義一致地區，避免在串流處理應用程式中流失資料。{{site.data.keyword.streamsshort}} 可透過運算子及註釋予以加強，這些運算子及註釋容許使用在串流處理期間不會遺失值組的地區定義。一致地區中的值組會至少處理一次。如果使用「測試版入門」或「測試版加強」定價方案，您現在可以使用 [{{site.data.keyword.streaminganalyticsshort}} 中定義的一致地區](/docs/services/StreamingAnalytics/consistentregions.html)來執行及監視 Streams 應用程式。

**新的問題判斷特性：**「測試版入門」及「測試版加強」方案包含數項加強功能，可協助您快速找出應用程式中的錯誤並加以修正。如需詳細資料，請參閱 [{{site.data.keyword.streaminganalyticsshort}} 主控台為您提供更多尋找及修正錯誤的方法（測試版方案）![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")。](https://wp.me/p4IICn-4cx)

**監視運算子的運作方式及雲端中的保證值組處理：**{{site.data.keyword.streamsshort}} 提供度量值來協助評估 {{site.data.keyword.streamsshort}} 服務的性能，以輔助診斷效能問題及分析要求的傳輸量。您可以使用 {{site.data.keyword.streaminganalyticsshort}} 中的「Streams 主控台」來[監視運算子的運作方式並確保資源最佳化 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")。](https://wp.me/p4IICn-4bH)
