---

copyright:
  years: 2015, 2018
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics 高可用性
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} 可啟用您應用程式的高可用性。如果在其中一個應用程式節點（{{site.data.keyword.streamsshort}} 資源）上偵測到問題，則會自動更換該節點，並移轉在該節點上執行的任何工作。如果實例包含多個應用程式節點，則只會移轉及重新啟動工作。您可以使用[服務詳細資料頁面](/docs/services/StreamingAnalytics/r_service_dashboard.html)或 [{{site.data.keyword.streaminganalyticsshort}} v1 REST API ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} 來配合 [v1 服務方案](/docs/services/StreamingAnalytics/service_plans.html)。若為 v2 服務方案，請使用 [v2 REST API ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window}。
{:shortdesc}

此視訊顯示如何使用服務詳細資料頁面來調整實例大小：

<iframe width="560" height="315" title="調整實例大小" src="https://www.youtube.com/embed/zbZ9am9UhPw?rel=0" frameborder="0" allowfullscreen>調整實例大小</iframe>

## 一致地區
由於業務需求，部分應用程式需要所有值組都至少處理一次。{{site.data.keyword.streamsshort}} 可透過運算子及註釋予以加強，這些運算子及註釋容許使用在串流處理期間不會遺失值組的地區定義。一致地區中的值組會至少處理一次。

您可以使用 {{site.data.keyword.streaminganalyticsshort}} 中定義的一致地區來執行及監視 Streams 應用程式。當您建立 {{site.data.keyword.streaminganalyticsshort}} 服務時，實例便已配置為使用一致地區。

一致地區是一個子圖，在其中，運作子的狀態會透過處理串流定義點內的所有值組和標點符號變得一致。這可讓子圖內的值組至少被處理一次。一致地區會定期排除其現行值組。將處理一致地區中的所有值組直到子圖的結尾。運算子的記憶體內狀態會自動序列化，並儲存在該地區中每個運算子的檢查點上。

您現在可以同時撰寫具有保證值組處理的 Java 及 SPL 應用程式，並在 {{site.data.keyword.streaminganalyticsshort}} 中部署這些應用程式。

在有效運算子上使用 `@consistent` 註釋，即可定義一致地區的開頭。{{site.data.keyword.streamsshort}} 會自動判斷一致地區的範圍，但您可以使用 `@autonomous` 註釋來變更地區的結束運算子。定義的一致地區會定期建立一致狀態。

如需在 Streams 應用程式中使用一致地區的詳細資料，請參閱 [{{site.data.keyword.streamsshort}} 文件 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html)。
