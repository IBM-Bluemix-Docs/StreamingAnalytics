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

# 入門指導教學
{: #starterapps_deploy}

Streaming Analytics 是讓您不需要執行耗時安裝、系統管理及管理作業的完整受管理服務，讓您有更多時間可以開發多媒體串流應用程式。在此入門指導教學中，您可以將其中一個 {{site.data.keyword.streaminganalyticsshort}} 入門範本應用程式推送及部署至 {{site.data.keyword.Bluemix_notm}}。
{:shortdesc}


## 開始之前
{: #prereqs}

部署新手入門應用程式之前，您必須遵循下列步驟：

* 登錄 [{{site.data.keyword.Bluemix_notm}} 帳戶 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://console.{DomainName}/registration){:new_window}
* 在 {{site.data.keyword.Bluemix_notm}} 組織中，建立 {{site.data.keyword.streaminganalyticsshort}} 服務實例。您可以直接從 [{{site.data.keyword.Bluemix_notm}} 服務型錄中的 {{site.data.keyword.streaminganalyticsshort}} 頁面 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://console.{DomainName}/catalog/services/streaming-analytics/){:new_window} 建立實例。  
* [安裝 {{site.data.keyword.Bluemix_notm}} CLI ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://console.stage1.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install)。



## 步驟 1：建立應用程式並將應用程式連接至您的服務
{: #create_connect}

1. 在 {{site.data.keyword.Bluemix_notm}} 中建立應用程式：

    a. 在 {{site.data.keyword.Bluemix_notm}} 功能表中，選取 **Cloud Foundry 應用程式**，然後按一下**建立資源**。

    b. 選取應用程式運行環境：
  	* 若要部署 Event Detection 入門範本應用程式，請使用 {{site.data.keyword.sdk4node}} 運行環境來建立應用程式。
  	* 若要部署 NYC Traffic 入門範本應用程式，請使用 Liberty for Java™ 運行環境來建立應用程式。

  請記住您提供給應用程式的名稱，稍後您會需要用到它。
1. 將 {{site.data.keyword.streaminganalyticsshort}} 服務實例連接至應用程式，並重新編譯打包應用程式。

## 步驟 2：設定入門範本應用程式
{: #setup_app}

1. 下載 [Event Detection ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection) 或 [NYC Traffic ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic) 入門範本應用程式。

1. 在 {{site.data.keyword.Bluemix_notm}} 中，重新命名目錄，使其符合您提供給應用程式的名稱。

## 步驟 3：部署入門範本應用程式
{: #deploy_app}

1. 移至入門範本應用程式目錄：
  <pre><code>cd myapp</code></pre>
  {:pre}

1. 登入 {{site.data.keyword.Bluemix_notm}}，並在系統提示時設定目標組織：
  <pre><code>bx login</code></pre>
  {:pre}

1. 將應用程式推送至 {{site.data.keyword.Bluemix_notm}}：
  <pre><code>bx app push myapp</code></pre>
  {:pre}

1. 移至您的應用程式概觀頁面（可從 {{site.data.keyword.Bluemix_notm}} 儀表板存取），以驗證您的應用程式已順利啟動。
1. 啟動應用程式以在瀏覽器中看到它。您可以在應用程式概觀頁面上找到應用程式的 URL（或「路徑」）。

## 後續步驟
{: #next_steps}

既然您的應用程式正在執行，您可以從 {{site.data.keyword.streaminganalyticsshort}} 主控台監視應用程式。請移至服務儀表板，並選取 {{site.data.keyword.streaminganalyticsshort}} 服務，然後按一下**啟動**。
