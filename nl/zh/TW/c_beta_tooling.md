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

# 開發工具和環境
{: #c_beta_tooling}


這些考量適用於用來開發 {{site.data.keyword.streaminganalyticsshort}} 之應用程式的工具和環境。
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}} 未包括雲端中的 {{site.data.keyword.streamsshort}} 開發環境，或雲端中的 Streams Studio。請在本端安裝的 {{site.data.keyword.streamsshort}} 環境中開發應用程式，並將它們提交為應用程式軟體組。如果您沒有開發環境，則可以下載 [v2 服務方案](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)的 [{{site.data.keyword.streamsshort}} Quick Start Edition 與 Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi)，或是如果您使用 [v1 服務方案](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，則可以免費下載 [{{site.data.keyword.streamsshort}} Quick Start Edition VM 映像檔 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}。
* 若您使用 v2 服務方案，請在 Red Hat Enterprise Linux (RHEL) 7.x 中編譯應用程式，若您使用 v1 服務方案則使用 RHEL 6.5，並且使用 Intel 處理器。
* 在 {{site.data.keyword.streamsshort}} 開發環境中，將環境變數 `JAVA_HOME` 設為 $STREAMS_INSTALL/java。
