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

# 常見問題
{: #faq}

## 如何註冊 Streaming Analytics 服務？
{: #signup notoc}
{: faq}  

如需 {{site.data.keyword.streaminganalyticsshort}} 服務方案的相關資訊，請參閱 [{{site.data.keyword.Bluemix_short}} 型錄](https://{DomainName}/catalog/services/streaming-analytics)。

## 我正在使用的 Streaming Analytics 服務版本為何？
{: #version notoc}
{: faq}   

增進功能會定期推送至所有 {{site.data.keyword.streaminganalyticsshort}} 服務。您一律會使用最新版的受管理服務，而且不得追蹤任何產品版本或層次。

## IBM 為我管理的項目為何？
{: #ibm_manage notoc}
{: faq}   

我們處理安裝、軟體升級、建立和管理網域，以及硬體維護。此服務包括全年無休的性能監視。


## 我負責的作業為何？  
{: #responsible notoc}
{: faq}

您可以撰寫在 {{site.data.keyword.streaminganalyticsshort}} 服務及 Streams 實例內部部署中執行的應用程式，並確定它們的運作正確且符合效能需求。您也負責任何應用程式特定監視。

## 是否支援高可用性 (HA)？
{: #ha notoc}
{: faq}

高可用性是由 IBM 所管理。{{site.data.keyword.streaminganalyticsshort}} 配置成支援 HA。執行失效接手時，還有其他伺服器資源可用。

## 如何管理 Streaming Analytics 服務的安全？
{: #security notoc}
{: faq}   

安全是由 IBM 完全管理。會針對每一個服務產生認證，並將它提供給您。安全更新是由 IBM 所管理，並在其可用時立即套用。

## 需要配置 Streaming Analytics 服務嗎？  
{: #configure notoc}
{: faq}

此服務是由 IBM 所建立及完全管理。每一個服務都會包含一組專用應用程式資源。

## 如何開發 Streams 應用程式？
{: #streamsapp notoc}
{: faq}

您必須使用免費 Streams [{{site.data.keyword.streamsshort}} Quick Start Edition 與 Docker ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-docker/) 配合 [v2 服務方案](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，以在本端開發 Streams 應用程式，或是如果您使用 [v1 服務方案](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，則可以下載 [{{site.data.keyword.streamsshort}} Quick Start Edition VM 映像檔 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}。

您也可以使用現有的內部部署 {{site.data.keyword.streamsshort}} 安裝。在本端開發及編譯的應用程式接著可以當成軟體組，緊密部署至雲端中的 Streams 服務。

但是，如果您要執行雲端中的 Python 應用程式，則不需要安裝 {{site.data.keyword.streamsshort}} 內部部署。只需要使用 `STREAMING\_ANALYTICS\_SERVICE` 環境定義，即可將 Python 應用程式提交至 {{site.data.keyword.streaminganalyticsshort}} 服務。您可以在標準 Python 開發環境或 Jupyter 互動式記事本中開發應用程式，但必須使用 Python 3.5。

如需開發應用程式的相關資訊，請參閱 [{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.streaminganalyticsshort}} Development Guide ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/streamsdev/?p=16589&post_type=doc&preview=1&_ppp=7ad76a418b)。

## 我可以直接登入 Streaming Analytics 服務主機嗎？
{: #host notoc}  
{: faq}

否。不支援使用 Telnet 或「安全 Shell (ssh)」直接登入伺服器。您無法安裝其他軟體，或在 Streams 主機上執行非 Streams 軟體。

## 我可以在 Streaming Analytics 服務上存取檔案系統嗎？
{: #filesystem notoc}
{: faq}   

只有 Streams 應用程式才能直接存取 Streams 主機上的檔案系統。

需要讓 Streams 與其他解決方案元件互動之機制的解決方案，存在具有雲端功能的替代方案。您可以使用其他來源及接收槽通訊協定，而不是檔案。例如，雲端型資料儲存庫。

## Streaming Analytics 服務應用程式如何存取我組織的企業資料？
{: #access notoc}  

您可以使用 [{{site.data.keyword.Bluemix_notm}} Secure Gateway 服務](https://{DomainName}/catalog/services/secure-gateway)，安全地將 Streams 應用程式連接至您的企業。

## 雲端中的 Streaming Analytics 服務支援 IBM Streams 內部部署的所有特性？
{: #features notoc}

{{site.data.keyword.streaminganalyticsshort}} 服務不支援的一些特性包含：

  - 需要網域權限之實例的管理作業。例如，新增自訂主機標籤，或建立工作群組。
  - 一致的地區檢查點。
  - 不支援一些工具箱運算子。如需相關資訊，請參閱[支援的工具箱及配接器](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-compatible_toolkits)。
  - Streams JMX API。

## 我可以在哪裏進一步瞭解 Streaming Analytics 服務？
{: #roadmap notoc}

IBM developerWorks® 文章 [{{site.data.keyword.Bluemix_notm}} 上 {{site.data.keyword.streaminganalyticsshort}} 服務的導覽圖 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/streamsdev/docs/roadmap-for-streaming-analytics-service-on-bluemix/) 包含用於瞭解服務的指引，以及資訊性部落格、展示及文章的鏈結。
