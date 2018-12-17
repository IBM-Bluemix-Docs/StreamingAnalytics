---

copyright:
  years: 2015, 2018
lastupdated: "2018-09-04"

---

<!-- Attribute definitions -->
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics 疑難排解
{: #ts_StreamingAnalytics}

您可以找到如何在 {{site.data.keyword.Bluemix_short}} 上使用 {{site.data.keyword.streaminganalyticsshort}} 之常見問題的答案。
{:shortdesc}

## 啟動這項服務時，系統提示我輸入認證以登入主控台
{: #log_in_console}

啟動 {{site.data.keyword.streaminganalyticsshort}} 時，系統會提示您輸入認證以登入服務主控台。
{:shortdesc}

您可以啟動已建立的 {{site.data.keyword.streaminganalyticsshort}} 服務，而且會看到提示您輸入認證的登入頁面，而不是直接存取服務主控台。
{: tsSymptoms}

服務基礎架構中已有更新，但瀏覽器快取導致服務無法取得更新。
{: tsCauses}

請清除瀏覽器快取，以確定取得服務主控台的最新版本。
{: tsResolve}

## 我的應用程式不健全
{: #app_unhealthy}

您無法正確地執行應用程式，且性能狀態為 `unhealthy`。
{:shortdesc}

您將應用程式提交至服務實例，應用程式啟動但立即失敗了，性能狀態為 `unhealthy`。下列錯誤出現在日誌檔中：`/lib64/libc.so.6: version GLIBC_2.14 not found`。
{: tsSymptoms}

您未使用 RHEL 7.x 作業系統或相等的 CentOS 版本編譯應用程式。
{: tsCauses}

如果您是使用 [v2 服務方案](/docs/services/StreamingAnalytics/service_plans.html)，則必須在 Red Hat Enterprise Linux (RHEL) 7.x 中編譯您的應用程式。如果您是使用 [v1 服務方案](/docs/services/StreamingAnalytics/service_plans.html)，則必須使用搭配 Intel 處理器的 RHEL 6.5 編譯您的應用程式。將應用程式重新提交至服務實例。
如果您沒有相容的開發環境，且是使用 v2 服務方案，則可以下載 [{{site.data.keyword.streamsshort}} Quick Start Edition 與 Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi)。如果您使用 v1 服務方案，請下載 [{{site.data.keyword.streamsshort}} QSE ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}。
{: tsResolve}

## 我的應用程式在重新啟動之後不健全
{: #app_restart}

由於系統維護或失敗回復情境，我的應用程式在重新啟動之後不健全。
{:shortdesc}

您在服務實例中有多個應用程式，而且其中一個應用程式使用一個標籤來放置運算子。在應用程式重新啟動之後，會先獲得未標記之運算子的資源，並且在可以放置已標記的運算子之前，便先耗用掉您的所有資源配額。
{: tsSymptoms}

大規模 Pod 重新啟動（最常由服務更新觸發），可能會導致應用程式無法重新啟動，如果它們需要特殊標記，而且已達到資源配額的話。在某些情況下，大規模 Pod 重新啟動可能由失敗回復情境所引起。
{: tsCauses}

您需要增加資源配額或釋放一些資源，讓應用程式可以獲得具有必要標籤的資源。若要增加您的配額，請移至服務詳細資料頁面，並增大您的實例大小。若要釋放資源，請取消現有工作，直到釋放足夠的資源來適當地放置應用程式為止。
{: tsResolve}
