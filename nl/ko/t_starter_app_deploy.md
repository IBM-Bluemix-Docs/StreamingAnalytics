---

copyright:
  years: 2015, 2018
lastupdated: "2018-07-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# 시작하기 튜토리얼
{: #starterapps_deploy}

Streaming Analytics는 시간이 많이 걸리는 설치 및 관리 태스크에 시간을 쓸 필요가 없는 완전히 관리되는 서비스로 사용자는 스트리밍 애플리케이션을 개발하는 데 더욱 집중할 수 있습니다. 이 시작하기 튜토리얼에서는 {{site.data.keyword.streaminganalyticsshort}} 스타터 애플리케이션 중의 하나를 {{site.data.keyword.Bluemix_notm}}에 푸시하고 배치합니다.
{:shortdesc}


## 시작하기 전에
{: #prereqs}

스타터 앱을 배치하려면 다음 단계를 따라야 합니다. 

* [{{site.data.keyword.Bluemix_notm}} 계정 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.{DomainName}/registration){:new_window}을 등록하십시오.
* {{site.data.keyword.Bluemix_notm}} 조직에 {{site.data.keyword.streaminganalyticsshort}} 서비스의 인스턴스를 작성하십시오. [{{site.data.keyword.Bluemix_notm}} 서비스 카탈로그의 **{{site.data.keyword.streaminganalyticsshort}}** 페이지 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.{DomainName}/catalog/services/streaming-analytics/){:new_window}에서 직접 인스턴스를 작성할 수 있습니다.   
* [{{site.data.keyword.Bluemix_notm}} CLI를 설치![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.{DomainName}/docs/cli/reference/bluemix_cli/get_started.html#getting-started)하십시오.



## 1단계. 앱을 작성하고 이를 서비스에 연결
{: #create_connect}

1. {{site.data.keyword.Bluemix_notm}}에서 애플리케이션을 작성하십시오.

    a. **{{site.data.keyword.Bluemix_notm}}** 메뉴에서 **Cloud Foundry 앱**을 선택하고 **리소스 작성**을 클릭하십시오.

    b. Event Detection 또는 Event Detection v2 스타터 앱의 {{site.data.keyword.sdk4node}} 런타임을 선택하십시오.

애플리케이션에 제공한 이름을 기억해 두십시오. 나중에 필요합니다.
1. {{site.data.keyword.streaminganalyticsshort}} 서비스 인스턴스를 애플리케이션에 연결하고 애플리케이션을 다시 스테이징하십시오.

## 2단계. 스타터 애플리케이션 설정
{: #setup_app}

1. [v1 서비스 플랜](/docs/services/StreamingAnalytics/service_plans.html)을 사용하는 경우 [Event Detection ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection) 스타터 앱을 다운로드하십시오. [v2 서비스 플랜](/docs/services/StreamingAnalytics/service_plans.html)의 경우 [Event Detection v2 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://streams-github-samples.mybluemix.net/?get=QuickStart%2FBeta201801%2FEventDetectionV2) 스타터 앱을 다운로드하십시오.

1. {{site.data.keyword.Bluemix_notm}}에서 애플리케이션에 지정한 이름과 일치하도록 디렉토리의 이름을 바꾸십시오.

## 3단계. 스타터 애플리케이션 배치
{: #deploy_app}

1. 스타터 애플리케이션 디렉토리로 이동하십시오.
  <pre><code>cd myapp</code></pre>
  {:pre}

1. {{site.data.keyword.Bluemix_notm}}에 로그인하고 프롬프트가 표시되면 대상 조직을 설정하십시오.
  <pre><code>bx login</code></pre>
  {:pre}

1. 애플리케이션을 {{site.data.keyword.Bluemix_notm}}에 푸시하십시오.
  <pre><code>bx app push myapp</code></pre>
  {:pre}

1. {{site.data.keyword.Bluemix_notm}} 대시보드에서 액세스할 수 있는 애플리케이션 개요 페이지로 이동하여 애플리케이션이 제대로 시작되었는지 확인하십시오.
1. 애플리케이션을 시작하여 브라우저에서 보십시오. 애플리케이션 개요 페이지에서 애플리케이션의 URL(또는 "라우트")을 찾을 수 있습니다.

## 다음 단계
{: #next_steps}

이제 애플리케이션이 실행되고 {{site.data.keyword.streaminganalyticsshort}} 콘솔에서 애플리케이션을 모니터할 수 있습니다. 서비스 대시보드로 이동하여 {{site.data.keyword.streaminganalyticsshort}} 서비스를 선택하고 **실행**을 클릭하십시오.
