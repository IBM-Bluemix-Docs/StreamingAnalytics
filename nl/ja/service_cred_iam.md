---

copyright:
  years:  2017
lastupdated: "2018-12-06"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# ID およびアクセス管理の認証

お客様のアカウント内のユーザーによる {{site.data.keyword.streaminganalyticsshort}} サービス・インスタンスへのアクセスは、{{site.data.keyword.Bluemix_notm}} の ID およびアクセス管理 (IAM) によって制御されます。 お客様の {{site.data.keyword.streaminganalyticsshort}} サービスを管理するには、認証トークンを使用する必要があります。

## IAM アクセス・トークンの取得

### 前提条件

a. 有効な IBM ID を持っている必要があります。

b. [{{site.data.keyword.Bluemix_notm}} CLI](https://{DomainName}/docs/cli/reference/bluemix_cli/get_started.html#getting-started) をダウンロードして、インストールします。

### ステップ 1. {{site.data.keyword.Bluemix_notm}} CLI にログインします。

```
bx api https://api.ng.bluemix.net
bx login
<お客様の資格情報を入力します。>

<お客様が複数の {{site.data.keyword.Bluemix_notm}} アカウントに属している場合は、現行セッション用のアカウントを選択するよう求められます。 また、{{site.data.keyword.Bluemix_notm}} 内の組織とスペースを選択する必要があります。>
```

### ステップ 2. IAM アクセス・トークンを取り出します。

```
bx iam oauth-tokens
```

2 つのトークンが生成されます。1 つは `IAM token` という名前で、もう 1 つは `UAA token` という名前です。 REST API 呼び出しを行うには、`IAM token`を使用します。
