---

copyright:
  years: 2015, 2017
lastupdated: "2017-12-15"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# 개발 도구 및 환경
{: #c_beta_tooling}


이 고려사항은 {{site.data.keyword.streaminganalyticsshort}}에 대한 애플리케이션을 개발하기 위해 사용하는 도구와 환경에 적용됩니다.
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}}에는 클라우드의 {{site.data.keyword.streamsshort}} 개발 환경 또는 클라우드의 Streams Studio가 포함되어 있지 않습니다. 로컬로 설치된 {{site.data.keyword.streamsshort}} 환경에서 애플리케이션을 개발하고 애플리케이션 번들로 제출하십시오. 개발 환경이 없는 경우에는 [{{site.data.keyword.streamsshort}} Quick Start Edition ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/)을 무료로 다운로드할 수 있습니다. 
* 호환성을 확인하려면 Red Hat Enterprise Linux 6.5 환경 또는 해당 CentOS 버전에서 애플리케이션 번들을 컴파일하십시오.
* {{site.data.keyword.streamsshort}} 개발 환경에서 환경 변수 `JAVA_HOME`을 $STREAMS_INSTALL/java로 설정하십시오.
