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


# 資源用量
{: #resourceusage}

{{site.data.keyword.streaminganalyticsshort}} 具有一系列的行為和原則，可確保適當的資源配置及用量。

## 檢視及編輯實例資源
您可以在服務儀表板上檢視及編輯授與給實例的資源數目，或使用 [{{site.data.keyword.streaminganalyticsshort}} 第 2 版 REST API](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#get-a-streaming-analytics-instance) 來執行相同作業。

## 資源配置
- 當您提交順利執行的工作時，資源會自動配置給實例。
- 如果沒有工作在資源上執行，就會從實例中移除這些資源。例如，您有兩個工作，其中工作 1 在資源 1 上執行，而工作 2 在資源 1 及資源 2 上執行。如果取消了工作 2，資源 1 會保留在實例中，而資源 2 則予以移除。
- 當您提交工作時，如果實例尚未達到其配置限制，則此工作將置於新資源上。
- 在實例用完其所有授與的資源之後，新的工作就會排定在現有資源上執行。

## 資源限制

資源限制可用來控制資源配置及用量。例如，您可以使用資源限制來指定兩個工作使用單一資源，而不是分開在兩個資源上執行。
