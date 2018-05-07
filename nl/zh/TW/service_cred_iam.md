---

copyright:
  years:  2017
lastupdated: "2018-04-24"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Identity and Access Management 鑑別

對於您帳戶中的使用者，對 {{site.data.keyword.streaminganalyticsshort}} 服務實例的存取權是由 {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) 所控制。若要管理您的 {{site.data.keyword.streaminganalyticsshort}} 服務，您必須使用鑑別記號。

## 擷取 IAM 存取記號

### 必要條件

a. 您必須具有有效的 IBM ID。

b. 下載並安裝 [{{site.data.keyword.Bluemix_notm}} CLI](https://console.bluemix.net/docs/cli/reference/bluemix_cli/get_started.html#getting-started)。

### 步驟 1：登入 {{site.data.keyword.Bluemix_notm}} CLI。

```
bx api https://api.ng.bluemix.net
bx login
<enter your credentials>

<If you are part of multiple {{site.data.keyword.Bluemix_notm}} accounts, you'll be asked to choose an account for the current session. Also, you'll need to choose an organization and space in {{site.data.keyword.Bluemix_notm}}.>
```

### 步驟 2：提取 IAM 存取記號。

```
bx iam oauth-tokens
```

將會產生兩個記號：一個名為 `IAM token`，另一個名為 `UAA token`。請使用 `IAM token` 來進行 REST API 呼叫。
