---

copyright:
  years: 2015, 2018
lastupdated: "2017-12-15"

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


* {{site.data.keyword.streaminganalyticsshort}} 未包括雲端中的 {{site.data.keyword.streamsshort}} 開發環境，或雲端中的 Streams Studio。請在本端安裝的 {{site.data.keyword.streamsshort}} 環境中開發應用程式，並將它們提交為應用程式軟體組。如果您沒有開發環境，則可以免費下載 [{{site.data.keyword.streamsshort}} Quick Start Edition ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/)。
* 在 Red Hat Enterprise Linux 6.5 環境（或對等的 CentOS 版本）中編譯應用程式軟體組，以確保相容性。

  **附註：**如果您要使用「測試版入門」及「測試版加強」方案，則必須在 RHEL 7 環境或相等的 CentOS 版本中編譯您的應用程式軟體組。如果沒有相容的開發環境，您可以使用 [{{site.data.keyword.streamsshort}} QSE for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi)。如需詳細資料，請參閱[測試版方案文件](/docs/services/StreamingAnalytics/beta_plans.html)。
* 在 {{site.data.keyword.streamsshort}} 開發環境中，將環境變數 `JAVA_HOME` 設為 $STREAMS_INSTALL/java。
