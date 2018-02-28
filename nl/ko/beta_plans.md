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

# Beta-Entry 및 Beta-Enhanced 플랜
{: #beta_plans}

{{site.data.keyword.streaminganalyticsshort}} 서비스에 대한 새 Beta-Entry 및 Beta-Enhanced 플랜에는 기존 서비스 플랜에 비해 몇 가지 개선사항 및 차이가 있습니다.
{:shortdesc}

**새 [{{site.data.keyword.streamsshort}} QSE for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi):** {{site.data.keyword.streamsshort}} Quick Start Edition은 {{site.data.keyword.streamsshort}}의 무료, 비프로덕션 버전입니다. Beta-Entry 및 Beta-Enhanced 플랜을 사용하여 {{site.data.keyword.streaminganalyticsshort}}에 애플리케이션을 배치하려면 {{site.data.keyword.streamsshort}} QSE의 Red Hat Enterprise Linux(RHEL) 7 버전을 사용하여 애플리케이션을 컴파일해야 합니다.
Docker 환경에서 실행 중인 RHEL 7과 함께 새 Streams QSE를 사용하여 새 {{site.data.keyword.streaminganalyticsshort}} 베타 플랜으로 애플리케이션을 컴파일하고 배치하는 방법을 배우려면 [베타 개발 안내서 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/streamsdev/docs/cloud-beta-devguide/)를 확인하십시오.   

**{{site.data.keyword.streaminganalyticsshort}} v2 REST API:** [{{site.data.keyword.streaminganalyticsshort}} v2 REST API ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#introduction)를 사용하여 서비스 인스턴스 및 {{site.data.keyword.streamsshort}} 작업을 관리할 수 있습니다. {{site.data.keyword.streaminganalyticsshort}} v2 API는 새 베타 플랜 중 하나로 작성된 서비스 인스턴스에서만 지원됩니다. [v1 REST API ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.bluemix.net/apidocs/220-streaming-analytics?&language=node#introduction)는 기존 {{site.data.keyword.streaminganalyticsshort}} 인스턴스 및 기존 서비스 플랜을 사용하여 작성한 임의의 새 인스턴스에서만 지원됩니다.

**새 스타터 및 샘플 애플리케이션:** 새 베타 플랜의 경우, RHEL 7에서 Streams를 실행해야 하므로 많은 기존 샘플 애플리케이션이 새 베타 플랜에서는 작동하지 않습니다. {{site.data.keyword.streaminganalyticsshort}}에서는 신속하게 새 베타 플랜을 시작할 수 있도록 [새 스타터 및 샘플 애플리케이션 세트]( https://developer.ibm.com/streamsdev/docs/cloud-beta-samples/)를 제공합니다.

**고가용성(HA) 개선사항:** 일관성 있는 지역을 정의하여 스트림 처리 애플리케이션에서 데이터 손실을 방지할 수 있습니다. {{site.data.keyword.streamsshort}}는 스트림 처리 동안 튜플이 손실되지 않는 지역 정의를 허용하는 연산자 및 어노테이션으로 개선되었습니다. 일관성 있는 지역의 튜플은 한 번 이상 처리됩니다.
Beta-Entry 또는 Beta-Enhanced 가격 책정 플랜을 사용하는 경우, [{{site.data.keyword.streaminganalyticsshort}}에서 정의된 일관성 있는 지역](/docs/services/StreamingAnalytics/consistentregions.html)을 사용하여 Streams 애플리케이션을 실행하고 모니터링할 수 있습니다.

**새 문제점 판별 기능:** Beta-Entry 및 Beta-Enhanced 플랜에는 애플리케이션에서 신속하게 오류를 발견하고 수정할 수 있도록 돕는 몇 가지 개선사항이 포함되어 있습니다. 세부사항은 [{{site.data.keyword.streaminganalyticsshort}} 콘솔에서 오류를 발견하고 수정할 수 있도록 더 많은 방법 제공(베타 플랜) ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://wp.me/p4IICn-4cx)을 참조하십시오.

**클라우드에서 연산자가 작동하는 방법 모니터링 및 튜플 처리 보장:** {{site.data.keyword.streamsshort}}에서는 {{site.data.keyword.streamsshort}} 서비스의 상태를 평가하는 데 도움이 되고 성능 문제 진단을 지원하며 요청 처리량을 분석할 수 있는 메트릭을 제공합니다. {{site.data.keyword.streaminganalyticsshort}}에서 Streams 콘솔을 사용하여 [연산자가 작동하는 방법을 모니터링하고 리소스 최적화를 보장![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://wp.me/p4IICn-4bH)할 수 있습니다.
