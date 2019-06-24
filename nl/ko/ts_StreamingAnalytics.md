---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-16"

subcollection: StreamingAnalytics

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

# Streaming Analytics 문제점 해결
{: #ts_StreamingAnalytics}

{{site.data.keyword.Bluemix_short}}에서 {{site.data.keyword.streaminganalyticsshort}} 사용 방법에 대한 일반적 질문에 대해 답변을 찾을 수 있습니다.
{:shortdesc}

## 서비스를 실행할 때 콘솔에 로그인하려면 인증 정보에 대한 프롬프트가 표시됨
{: #log_in_console}

{{site.data.keyword.streaminganalyticsshort}}를 실행할 때 서비스 콘솔에 로그인하려면 인증 정보에 대한 프롬프트가 표시됩니다.
{:shortdesc}

이전에 작성된 {{site.data.keyword.streaminganalyticsshort}} 서비스를 실행하고, 서비스 콘솔에 직접 액세스하는 대신에 인증 정보에 대한 프롬프트가 표시되는 로그인 페이지를 봅니다.
{: tsSymptoms}

서비스 인프라에 업데이트가 있었으며 브라우저 캐시 때문에 서비스가 업데이트를 가져올 수 없습니다.
{: tsCauses}

브라우저 캐시를 지우고 서비스 콘솔의 최신 버전을 보유하고 있는지 확인하십시오.
{: tsResolve}

## 내 애플리케이션의 상태가 비정상(unhealthy)임
{: #app_unhealthy}

애플리케이션을 제대로 실행할 수 없으며 상태가 `unhealthy`입니다.
{:shortdesc}

애플리케이션을 서비스 인스턴스에 제출한 이후, 애플리케이션이 시작되기는 하지만 바로 실패하며 상태가 `unhealthy`입니다. 로그 파일에 `/lib64/libc.so.6: version GLIBC_2.14 not found` 오류가 나타납니다.
{: tsSymptoms}

RHEL 7.x 운영 체제 또는 이와 동등한 CentOS 버전을 사용하여 애플리케이션을 컴파일하지 않았습니다.
{: tsCauses}

[v2 서비스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)을 사용 중이면 Red Hat Enterprise Linux(RHEL) 7.x에서 애플리케이션을 컴파일해야 합니다. [v1 서비스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)을 사용 중이면 Intel 프로세서의 RHEL 6.5에서 애플리케이션을 컴파일해야 합니다. 애플리케이션을 서비스 인스턴스에 다시 제출하십시오. 호환 가능한 개발 환경이 없으며 v2 서비스 플랜을 사용 중이면 [{{site.data.keyword.streamsshort}}Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi)를 다운로드할 수 있습니다. v1 서비스 플랜을 사용하는 경우 [{{site.data.keyword.streamsshort}} QSE ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}를 다운로드하십시오.
{: tsResolve}

## 다시 시작한 후에 내 애플리케이션이 비정상 상태임
{: #app_restart}

시스템 유지보수 또는 장애 복구 시나리오 때문에 다시 시작한 후에 내 애플리케이션 비정상 상태입니다.
{:shortdesc}

서비스 인스턴스에 다수의 애플리케이션이 있으며 애플리케이션 중 하나가 연산자 배치에 태그를 활용합니다. 애플리케이션이 다시 시작한 후에 태그가 지정되지 않은 연산자에 대한 리소스가 우선 확보되며 태그 지정된 연산자를 배치하기 전에 모든 리소스 할당량을 소진합니다.
{: tsSymptoms}

특수 태그 지정을 요구하며 리소스 할당량에 이미 도달한 경우에는 서비스 업데이트에 의해 가장 자주 트리거되는 대규모 팟(Pod) 재시작으로 인해 애플리케이션이 다시 시작하지 못할 수 있습니다. 
일부 경우에는 대규모 팟(Pod) 재시작이 장애 복구 시나리오에 의해 발생될 수 있습니다.
{: tsCauses}

애플리케이션이 필요한 태그를 사용하여 리소스를 확보할 수 있도록 리소스 할당량을 늘리거나 일부 리소스를 해제해야 합니다. 할당량을 늘리려면 서비스 세부사항 페이지로 이동하고 인스턴스 크기를 늘리십시오. 리소스를 해제하려면, 애플리케이션을 적절히 배치하기에 충분한 리소스가 해제될 때까지 기존 작업을 취소하십시오.
{: tsResolve}
