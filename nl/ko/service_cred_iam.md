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


# Identity and Access Management(IAM) 인증

{{site.data.keyword.Bluemix_notm}} Identity and Access Management(IAM)로 제어되는 계정에서 사용자용 {{site.data.keyword.streaminganalyticsshort}} 서비스 인스턴스에 액세스하십시오. {{site.data.keyword.streaminganalyticsshort}} 서비스를 관리하려면 인증 토큰을 사용해야 합니다.

## IAM 액세스 토큰 검색

### 전제조건

a. 유효한 IBM ID가 있어야 합니다.

b. [{{site.data.keyword.Bluemix_notm}} CLI](https://console.bluemix.net/docs/cli/reference/bluemix_cli/get_started.html#getting-started)를 다운로드하여 설치하십시오.

### 1단계. {{site.data.keyword.Bluemix_notm}} CLI에 로그인하십시오.

```
bx api https://api.ng.bluemix.net
bx login
<신임 정보를 입력하십시오.>

<여러 {{site.data.keyword.Bluemix_notm}} 계정 중 하나인 경우 현재 세션에 대한 계정을 선택하라는 요청을 받게 됩니다. 또한, {{site.data.keyword.Bluemix_notm}}의 조직 및 영역을 선택해야 합니다.>
```

### 2단계. IAM 액세스 토큰을 페치하십시오.

```
bx iam oauth-tokens
```

두 개의 토큰이 생성됩니다. 하나는 이름이 `IAM token`이고 다른 하나는 이름이 `UAA token`입니다. REST API 호출 시 `IAM token`을 사용하십시오.
