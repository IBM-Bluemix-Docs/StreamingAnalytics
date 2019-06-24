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

# 高可用性與災難回復
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} 在 {{site.data.keyword.Bluemix_notm}} 位置（例如，達拉斯、華盛頓特區、倫敦、法蘭克福）內具有高可用性。不過，從影響整個 {{site.data.keyword.Bluemix_notm}} 地區的可能災難回復需要規劃與準備。
{:shortdesc}


您要負責瞭解服務的配置、自訂作業和使用。您也要負責準備好，在新的 {{site.data.keyword.Bluemix_notm}} 位置重建服務實例，以及重新部署應用程式到該位置。請參閱[如何確保運作零中斷？](/docs/services/overview?topic=overview-zero-downtime#zero-downtime)以進一步瞭解 {{site.data.keyword.Bluemix_notm}} 中的高可用性和災難回復標準。您也可以找到[服務水準合約](/docs/services/overview?topic=overview-zero-downtime#zero-downtime#SLAs)的相關資訊。

## 高可用性

{{site.data.keyword.streaminganalyticsshort}} 可啟用您應用程式的高可用性。您的應用程式會部署到在 Kubernetes 叢集執行的 Docker 容器中。若要撰寫高可用性的應用程式，您必須瞭解這些容器如何運作以確保高可用性：

* 應用程式資源是具有根據服務方案配置之 CPU 和記憶體的容器。
* 在硬體故障或軟體失敗期間，容器可能會移動。當容器移動時，處理元素便重新啟動。
* 在計劃性維護期間，容器可能會移動（處理元素會重新啟動）。

因此，在撰寫應用程式時，您必須考量容器可能偶爾會移動。此外，請考量下列項目：
* 確定 PE 可重新啟動且可重新定位。
* 確定您的應用程式可以容忍重新啟動部分或所有處理元素 (PE)，且按照任何順序。
* 確定 Streams 應用程式中的來源和接收槽運算子已配置為當它們的 PE 重新啟動時，重新建立連線。

請參閱 [{{site.data.keyword.streaminganalyticsshort}} development guide](https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/#troubleshooting)，以取得如何進行應用程式疑難排解的範例。

為了實作高可用性，已啟用 Streams 應用程式，保證處理所有值組。為了達到保證的值組處理，會針對「一致地區」中的所有運算子定期建立檢查點。在應用程式失敗時水，所有運算子會回復到前次成功的檢查點狀態。{{site.data.keyword.streaminganalyticsshort}} 容許使用「一致地區」。

### 保證的值組處理
由於業務需求，部分應用程式需要所有值組都至少處理一次。{{site.data.keyword.streamsshort}} 可透過運算子及註釋予以加強，這些運算子及註釋容許使用在串流處理期間不會遺失值組的地區定義。一致地區中的值組會至少處理一次。

如果在「一致地區」內偵測到應用程式失敗，{{site.data.keyword.streaminganalyticsshort}} 可以將應用程式設回前次一致狀態（也稱為檢查點），並指示應用程式資料來源重播從該點起的值組。

您可以使用 {{site.data.keyword.streaminganalyticsshort}} 中定義的「一致地區」來執行及監視 Streams 應用程式。當您建立 {{site.data.keyword.streaminganalyticsshort}} 服務時，實例便已配置為容許使用「一致地區」。

「一致地區」是一個子圖，在其中，運作子的狀態會透過處理串流定義點內的所有值組和標點符號變得一致。這可讓子圖內的值組至少被處理一次。一致地區會定期排除其現行值組。將處理一致地區中的所有值組直到子圖的結尾。運算子的記憶體內狀態會自動序列化，並儲存在該地區中每個運算子的檢查點上。

您可以撰寫具有保證值組處理的 Java、SPL 及 Python 應用程式，並在 {{site.data.keyword.streaminganalyticsshort}} 中部署這些應用程式。

在有效運算子上使用 `@consistent` 註釋，即可定義一致地區的開頭。{{site.data.keyword.streamsshort}} 會自動判斷一致地區的範圍，但您可以使用 `@autonomous` 註釋來變更地區的結束運算子。定義的一致地區會定期建立一致狀態。

如需在 Streams 應用程式中使用一致地區的詳細資料，請參閱 [{{site.data.keyword.streamsshort}} 文件 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html)。

## 災難回復
{{site.data.keyword.streaminganalyticsshort}} 是 GA 服務，提供於多個 {{site.data.keyword.Bluemix_notm}} 地區。{{site.data.keyword.streaminganalyticsshort}} 不會在 {{site.data.keyword.Bluemix_notm}} 上儲存使用者資料。

根據您的業務需求，選取下列其中一項災難回復策略：
* 如果您要求不會岔斷應用程式：
  1. 在多個 {{site.data.keyword.Bluemix_notm}} 地區建立 {{site.data.keyword.streaminganalyticsshort}} 的實例。
  2. 將應用程式提交至多個地區。


* 如果您要求儘量少岔斷應用程式：
  1. 在多個 {{site.data.keyword.Bluemix_notm}} 地區建立 {{site.data.keyword.streaminganalyticsshort}} 的實例。
  2. 使用[服務 REST API](https://ibm.co/2Gt9mB6) 監視您的應用程式，並視需要動態地將工作負載移到新地區。

**附註：**每個一致地區都關聯於 {{site.data.keyword.Bluemix_notm}} 地區。在災難回復的情境中，應用程式裡的「一致地區」沒有任何角色。
