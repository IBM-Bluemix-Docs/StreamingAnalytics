---

copyright:
  years: 2015, 2018
lastupdated: "2018-04-24"

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

## 서비스를 실행할 때 콘솔에 로그인하려면 신임 정보에 대한 프롬프트가 표시됨
{: #log_in_console}

{{site.data.keyword.streaminganalyticsshort}}를 실행할 때 서비스 콘솔에 로그인하려면 신임 정보에 대한 프롬프트가 표시됩니다.
{:shortdesc}

서비스 콘솔에 직접 액세스하는 대신 이전에 작성된 {{site.data.keyword.streaminganalyticsshort}} 서비스를 실행하면 신임 정보에 대한 프롬프트가 표시되는 로그인 페이지가 나타납니다.
{: tsSymptoms}

서비스 인프라가 업데이트되었으며 브라우저 캐시로 인해 서비스가 업데이트를 가져오지 못합니다.
{: tsCauses}

브라우저 캐시를 지우고 서비스 콘솔의 최신 버전을 보유하고 있는지 확인하십시오.
{: tsResolve}

## 내 애플리케이션의 상태가 비정상(unhealthy)임
{: #app_unhealthy}

애플리케이션을 제대로 실행할 수 없으며 상태가 `unhealthy`입니다.
{:shortdesc}

애플리케이션을 서비스 인스턴스에 제출한 이후, 애플리케이션이 시작되기는 하지만 바로 실패하며 상태가 `unhealthy`입니다. 로그 파일에 `/lib64/libc.so.6: version GLIBC_2.14 not found` 오류가 나타납니다.
{: tsSymptoms}

애플리케이션이 RHEL 7.x 운영 체제 또는 이와 동등한 CentOS 버전을 사용하여 컴파일되지 않았습니다.
{: tsCauses}

[v2 서비스 플랜](/docs/services/StreamingAnalytics/service_plans.html)을 사용하거나 RHEL 6.5와 함께 [v1 서비스 플랜](/docs/services/StreamingAnalytics/service_plans.html)을 사용하는 경우 Intel 프로세서를 사용하여 Red Hat Enterprise Linux(RHEL) 7.x에서 애플리케이션을 다시 컴파일해야 합니다. 애플리케이션을 서비스 인스턴스에 다시 제출하십시오. 호환 가능한 개발 환경이 없고 v2 서비스 플랜을 사용하는 경우 [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi)를 다운로드할 수 있습니다. v1 서비스 플랜을 사용하는 경우 [{{site.data.keyword.streamsshort}} QSE ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window}를 다운로드하십시오.
{: tsResolve}
