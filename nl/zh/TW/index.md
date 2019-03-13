---

copyright:
  years: 2015, 2019
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}


# Streaming Analytics 概觀
{: #gettingstarted}

{{site.data.keyword.streaminganalyticsfull}} 採用 {{site.data.keyword.streamsshort}} 技術，這是一種進階分析平台，可用來即時吸收及分析來自不同資料來源類型的資訊，並與之產生關聯。當您建立 {{site.data.keyword.streaminganalyticsshort}} 服務的實例時，即可獲得在 {{site.data.keyword.Bluemix_short}} 中執行的專屬 {{site.data.keyword.streamsshort}} 實例，以執行 {{site.data.keyword.streamsshort}} 應用程式。
{:shortdesc}

執行[入門範本應用程式](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps_deploy){:new_window}，立即開始使用 {{site.data.keyword.streaminganalyticsshort}}。

若要開始使用 {{site.data.keyword.streaminganalyticsshort}}，請使用下列其中一種方法來提交與您 SPL、Java™、Python 或 Scala Streams 應用程式相關聯的應用程式軟體組（.sab 檔案）：
* 使用 {{site.data.keyword.streaminganalyticsshort}} 主控台中的**提交工作**按鈕。
* 在 {{site.data.keyword.Bluemix_notm}} 中開發應用程式，並在其中新增 {{site.data.keyword.streamsshort}} 應用程式。若為 [v1 服務方案](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，請使用 [{{site.data.keyword.streaminganalyticsshort}} v1 REST API ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} 控制它，若為 v2 服務方案則使用 [{{site.data.keyword.streaminganalyticsshort}} v2 REST API ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window}。

搭配使用 {{site.data.keyword.streaminganalyticsshort}} 與其他服務，包括 {{site.data.keyword.cloudant}}。請參閱[與其他 {{site.data.keyword.Bluemix_short}} 服務整合的指導教學](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-tutorials){:new_window}，來取得開始進行的範例。

如果要進一步使用您自己的應用程式，可以取得 {{site.data.keyword.streamsshort}} 開發環境，而且應用程式必須準備好使用雲端。如果您沒有 {{site.data.keyword.streamsshort}} 環境，則可以下載 [v2 服務方案](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)的 [{{site.data.keyword.streamsshort}} Quick Start Edition 與 Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi)，或是如果您使用 [v1 服務方案](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，則可以下載 [{{site.data.keyword.streamsshort}} Quick Start Edition VM 映像檔 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}。

如果您不熟悉 {{site.data.keyword.streamsshort}} 應用程式開發，則有資源可協助您瞭解。如需相關資訊，請參閱 [{{site.data.keyword.streamsshort}} Knowledge Center ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.welcome.doc/doc/kc-homepage.html){:new_window}

如果您已有在內部部署執行的 SPL 應用程式，則必須[準備好用於雲端的應用程式 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/streamsdev/docs/getting-spl-application-ready-cloud/){:new_window}。

**附註：**若您使用 v2 服務方案，您必須在 Red Hat Enterprise Linux (RHEL) 7.x 中編譯應用程式，若您使用 v1 服務方案則使用 RHEL 6.5。
