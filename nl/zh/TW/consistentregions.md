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


# 高可用性加強功能
{: #consistentregions}

由於業務需求，部分應用程式需要所有值組都至少處理一次。{{site.data.keyword.streamsshort}} 可透過運算子及註釋予以加強，這些運算子及註釋容許使用在串流處理期間不會遺失值組的地區定義。一致地區中的值組會至少處理一次。


如果使用「測試版入門」或「測試版加強」定價方案，您現在可以使用 {{site.data.keyword.streaminganalyticsshort}} 中定義的一致地區來執行及監視 Streams 應用程式。當您使用「測試版入門」或「測試版加強」方案建立 {{site.data.keyword.streaminganalyticsshort}} 服務時，實例便已配置為使用一致地區。

一致地區是一個子圖，在其中，運作子的狀態會透過處理串流定義點內的所有值組和標點符號變得一致。這可讓子圖內的值組至少被處理一次。一致地區會定期排除其現行值組。將處理一致地區中的所有值組直到子圖的結尾。運算子的記憶體內狀態會自動序列化，並儲存在該地區中每個運算子的檢查點上。

您現在可以同時撰寫具有保證值組處理的 Java 及 SPL 應用程式，並在 {{site.data.keyword.streaminganalyticsshort}} 中部署這些應用程式。

在有效運算子上使用 `@consistent` 註釋，即可定義一致地區的開頭。{{site.data.keyword.streamsshort}} 會自動判斷一致地區的範圍，但您可以使用 `@autonomous` 註釋來變更地區的結束運算子。定義的一致地區會定期建立一致狀態。

如需在 Streams 應用程式中使用一致地區的詳細資料，請參閱 [{{site.data.keyword.streamsshort}} 文件 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.1/com.ibm.streams.dev.doc/doc/consistentregions.html)。
