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

# 將 Streams 應用程式部署至雲端
{: #t_deploytocloud}

您可以將 {{site.data.keyword.streamsshort}} 應用程式部署至在 {{site.data.keyword.Bluemix_short}} 中執行的 {{site.data.keyword.streaminganalyticsshort}} 實例。
{:shortdesc}

{{site.data.keyword.streamsshort}} 應用程式是以 {{site.data.keyword.streamsshort}} 環境中的 {{site.data.keyword.streamsshort}} Processing Language (SPL)、SPL、Java、Scala 或 Python 所撰寫。您現在可以開發 Streams Python 應用程式而不使用 {{site.data.keyword.streamsshort}} 環境。請參閱[將 {{site.data.keyword.streamsshort}} Python 應用程式部署至雲端](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_deploytocloud#t_deploypython)


{{site.data.keyword.streaminganalyticsshort}} 未包括雲端中的 {{site.data.keyword.streamsshort}} 開發環境，但可以將在本端開發的應用程式部署至雲端。

開始之前，請先停用瀏覽器的蹦現畫面封鎖程式，以便顯示 {{site.data.keyword.streaminganalyticsshort}} 主控台。

若要將 {{site.data.keyword.streamsshort}} 應用程式部署至雲端，請執行下列動作：

1. 設定開發環境來開發及測試應用程式。

	若為 [v1 服務方案](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，如果您要使用 {{site.data.keyword.streamsshort}} 環境，則可以下載 [{{site.data.keyword.streamsshort}} Quick Start Edition ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}。若為 [v2 服務方案](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，請使用 [{{site.data.keyword.streamsshort}} Quick Start Edition 與 Docker ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi){:new_window} 搭配。

2. 在您的開發環境中開發串流應用程式。在 {{site.data.keyword.streamsshort}} 開發環境中，您可以使用 Streams Studio 或指令行工具來開發應用程式。

3. 驗證串流應用程式在開發環境中適當地執行。
**附註：**若您使用 v2 服務方案，您必須在 Red Hat Enterprise Linux (RHEL) 7.x 中編譯應用程式，若您使用 v1 服務方案則使用 RHEL 6.5。

4. 使用下列其中一種方法，將與 SPL、Java、Scala 或 Python 應用程式相關聯的應用程式軟體組（.sab 檔案）提交至雲端中的服務實例：
	* 使用 {{site.data.keyword.streaminganalyticsshort}} 主控台來提交應用程式軟體組。

  * 在 {{site.data.keyword.Bluemix_notm}} 中建立應用程式，並在其中新增 {{site.data.keyword.streamsshort}} 應用程式。若為 [v1 服務方案](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，請使用 [{{site.data.keyword.streaminganalyticsshort}} v1 REST API ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} 控制它，若為 v2 服務方案則使用 [{{site.data.keyword.streaminganalyticsshort}} v2 REST API ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window}。

您的應用程式現在已部署在雲端中。您可以在 {{site.data.keyword.streaminganalyticsshort}} 服務中監視應用程式。您也可以將多個應用程式（.sab 檔案）提交至服務實例。數目由您決定。

{{site.data.keyword.streamsshort}} 也支援數個可用來開發應用程式的 Java™ 開發套件。如需 {{site.data.keyword.streamsshort}} 中 Java 支援的相關資訊，請參閱[支援進行應用程式開發的 Java 開發套件 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.install.doc/doc/ibminfospherestreams-install-prerequisites-java-supported-sdks.html){:new_window}。

## 將 Streams Python 應用程式部署至雲端
{: #t_deploypython}

將 {{site.data.keyword.streamsshort}} Python 應用程式部署至在 {{site.data.keyword.Bluemix_short}} 中執行的 {{site.data.keyword.streaminganalyticsshort}} 服務。您不需要有 {{site.data.keyword.streamsshort}} 安裝。
{:shortdesc}

使用 streamsx 套件中包含的 [{{site.data.keyword.streamsshort}} Python Application API ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features){:new_window}，您可將 Python 應用程式部署至 {{site.data.keyword.streaminganalyticsshort}} 服務。請參閱[開發 {{site.data.keyword.streaminganalyticsshort}} 服務 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html){:new_window} 指導教學，以取得如何針對 {{site.data.keyword.streaminganalyticsshort}} 服務建立和部署簡單 Python 應用程式的範例。

{{site.data.keyword.DSX_full}} 也支援在 Jupyter 互動式記事本中提交 Python 應用程式。如需相關資訊，請參閱[針對 {{site.data.keyword.streaminganalyticsshort}} 開發 Python 應用程式](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_develop_apps_python)。
