---

copyright:
  years:  2017
lastupdated: "2018-07-24"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Identity and Access Management 认证

您帐户中用户对 {{site.data.keyword.streaminganalyticsshort}} 服务实例的访问权由 {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) 控制。要管理 {{site.data.keyword.streaminganalyticsshort}} 服务，必须使用认证令牌。

## 检索 IAM 访问令牌

### 先决条件

a. 您必须具有有效的 IBM 标识。

b. 下载和安装 [{{site.data.keyword.Bluemix_notm}} CLI](https://console.bluemix.net/docs/cli/reference/bluemix_cli/get_started.html#getting-started)。

### 步骤 1. 登录 {{site.data.keyword.Bluemix_notm}} CLI。

```
bx api https://api.ng.bluemix.net
bx login
<输入凭证>

<如果您属于多个 {{site.data.keyword.Bluemix_notm}} 帐户，那么会要求您为当前会话选择一个帐户。此外，您还需要选择一个 {{site.data.keyword.Bluemix_notm}} 组织和空间。>
```

### 步骤 2. 访存 IAM 访问令牌。

```
bx iam oauth-tokens
```

生成两个令牌：一个名为 `IAM token`，另一个名为 `UAA token`。使用 `IAM token` 进行 REST API 调用。
