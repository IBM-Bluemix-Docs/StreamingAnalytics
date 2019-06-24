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

# Streams 애플리케이션을 클라우드에 배치
{: #t_deploytocloud}

{{site.data.keyword.Bluemix_short}}에서 실행 중인 {{site.data.keyword.streaminganalyticsshort}} 인스턴스에 {{site.data.keyword.streamsshort}} 애플리케이션을 배치할 수 있습니다.
{:shortdesc}

{{site.data.keyword.streamsshort}} 애플리케이션은 {{site.data.keyword.streamsshort}} 환경에서 {{site.data.keyword.streamsshort}} Processing Language(SPL), SPL, Java, Scala 또는 Python으로 작성됩니다. 이제 {{site.data.keyword.streamsshort}} 환경 없이 Streams Python 애플리케이션을 개발할 수 있습니다. [클라우드에 {{site.data.keyword.streamsshort}} Python 애플리케이션 배치](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_deploytocloud#t_deploypython)를 참조하십시오.


{{site.data.keyword.streaminganalyticsshort}}는 클라우드에 {{site.data.keyword.streamsshort}} 개발 환경을 포함하지 않지만 로컬로 개발한 애플리케이션을 클라우드에 배치할 수 있습니다.

시작하기 전에 브라우저의 팝업 차단기를 사용 안함으로 설정하여 {{site.data.keyword.streaminganalyticsshort}} 콘솔을 표시하십시오.

{{site.data.keyword.streamsshort}} 애플리케이션을 클라우드에 배치하려면 다음을 수행하십시오.

1. 애플리케이션을 개발하고 테스트하기 위한 개발 환경을 설정하십시오.

	{{site.data.keyword.streamsshort}} 환경을 사용하려는 경우, [v1 서비스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)용 [{{site.data.keyword.streamsshort}} Quick Start Edition ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}을 다운로드할 수 있습니다. [v2 서비스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)용으로는 [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi){:new_window}를 사용하십시오.

2. 개발 환경에서 스트리밍 애플리케이션을 개발하십시오. {{site.data.keyword.streamsshort}} 개발 환경에서 사용자는 Streams Studio 또는 명령행 도구를 사용하여 애플리케이션을 개발할 수 있습니다.

3. 개발 환경에서 스트리밍 애플리케이션이 올바르게 실행되는지 확인하십시오.
**참고:** v2 서비스 플랜을 사용하거나 RHEL 6.5와 함께 v1 서비스 플랜을 사용하는 경우 Red Hat Enterprise Linux(RHEL) 7.x에서 애플리케이션을 컴파일해야 합니다.

4. 다음 방법 중 하나를 사용하여 SPL, Java, Scala 또는 Python 애플리케이션과 연관된 애플리케이션 번들(.sab 파일)을 클라우드의 서비스 인스턴스에 제출하십시오.
	* {{site.data.keyword.streaminganalyticsshort}} 콘솔을 사용하여 애플리케이션 번들을 제출하십시오.

  * {{site.data.keyword.Bluemix_notm}}에서 애플리케이션을 작성하고 여기에 {{site.data.keyword.streamsshort}} 애플리케이션을 추가하십시오. [v1 서비스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)용 [{{site.data.keyword.streaminganalyticsshort}} v1 REST API ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} 또는 v2 서비스 플랜용 [{{site.data.keyword.streaminganalyticsshort}} v2 REST API ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window}를 사용하여 이를 제어하십시오.

애플리케이션이 이제 클라우드에 배치됩니다. {{site.data.keyword.streaminganalyticsshort}} 서비스에서 애플리케이션을 모니터할 수 있습니다. 서비스 인스턴스에 둘 이상의 애플리케이션(.sab 파일)을 제출할 수도 있습니다. 원하는 수만큼 제출할 수 있습니다.

{{site.data.keyword.streamsshort}}는 또한 사용자의 애플리케이션을 개발하기 위해 사용할 수 있는 여러 가지 Java™ 개발 킷을 지원합니다. {{site.data.keyword.streamsshort}}에서 Java 지원에 대한 자세한 정보는 [애플리케이션 개발을 위해 지원되는 Java 개발 킷 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.install.doc/doc/ibminfospherestreams-install-prerequisites-java-supported-sdks.html){:new_window}을 참조하십시오.

## Streams Python 애플리케이션을 클라우드에 배치
{: #t_deploypython}

{{site.data.keyword.Bluemix_short}}에서 실행 중인 {{site.data.keyword.streaminganalyticsshort}} 서비스에 {{site.data.keyword.streamsshort}} Python 애플리케이션을 배치하십시오. {{site.data.keyword.streamsshort}} 설치는 필요하지 않습니다.
{:shortdesc}

streamsx 패키지에 포함되어 있는 [{{site.data.keyword.streamsshort}}Python 애플리케이션 API ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features){:new_window}를 사용하면 Python 애플리케이션을 {{site.data.keyword.streaminganalyticsshort}} 서비스에 배치할 수 있습니다. {{site.data.keyword.streaminganalyticsshort}} 서비스에 대한 간단한 Python 애플리케이션을 작성하고 배치하는 방법에 대한 예제를 가져오려면 [{{site.data.keyword.streaminganalyticsshort}} 서비스를 위한 개발 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html){:new_window} 튜토리얼을 확인하십시오.

{{site.data.keyword.DSX_full}}는 Jupyter 대화식 노트북에서 Python 애플리케이션의 제출도 지원합니다. 자세한 정보는 [{{site.data.keyword.streaminganalyticsshort}}용 Python 애플리케이션 개발](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_develop_apps_python)을 참조하십시오.
