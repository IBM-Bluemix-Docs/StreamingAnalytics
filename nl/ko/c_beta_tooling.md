---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-16"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# 개발 도구 및 환경
{: #c_beta_tooling}


이 고려사항은 {{site.data.keyword.streaminganalyticsshort}}용 애플리케이션을 개발하기 위해 사용하는 도구와 환경에 적용됩니다.
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}}에는 클라우드의 {{site.data.keyword.streamsshort}} 개발 환경 또는 클라우드의 Streams Studio가 포함되어 있지 않습니다. 로컬로 설치된 {{site.data.keyword.streamsshort}} 환경에서 애플리케이션을 개발하고 애플리케이션 번들로 제출하십시오. 개발 환경이 없는 경우 [v2 서비스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)용 [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi)를 다운로드할 수 있으며, [v1 서비스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)을 사용하는 경우에는 [{{site.data.keyword.streamsshort}} Quick Start Edition VM 이미지 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}를 무료로 다운로드할 수 있습니다.
* v2 서비스 플랜을 사용하거나 RHEL 6.5와 함께 v1 서비스 플랜을 사용하는 경우 Intel 프로세서를 사용하여 Red Hat Enterprise Linux(RHEL) 7.x에서 애플리케이션을 컴파일해야 합니다.
* {{site.data.keyword.streamsshort}} 개발 환경에서 환경 변수 `JAVA_HOME`을 $STREAMS_INSTALL/java로 설정하십시오.
