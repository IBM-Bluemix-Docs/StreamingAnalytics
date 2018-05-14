---

copyright:
  years: 2015, 2018
lastupdated: "2018-04-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}


# Streaming Analytics 개요
{: #gettingstarted}

{{site.data.keyword.streaminganalyticsfull}}는 실시간으로 다양한 유형의 데이터 소스에서 도착하는 정보를 수집, 분석, 상관시키기 위해 사용할 수 있는 고급 분석 플랫폼인 {{site.data.keyword.streamsshort}}에서 제공합니다. {{site.data.keyword.streaminganalyticsshort}} 서비스의 인스턴스를 작성하면 사용자의 {{site.data.keyword.streamsshort}} 애플리케이션을 실행할 준비가 된, {{site.data.keyword.Bluemix_short}}에서 실행되고 있는 사용자 고유의 {{site.data.keyword.streamsshort}} 인스턴스를 얻게 됩니다.
{:shortdesc}

[스타터 애플리케이션](/docs/services/StreamingAnalytics/t_starter_app_deploy.html){:new_window}을 실행하여 바로 {{site.data.keyword.streaminganalyticsshort}}를 시작하십시오.

{{site.data.keyword.streaminganalyticsshort}}를 시작하려면 다음 방법 중 하나를 사용하여 SPL, Java™, Python 또는 Scala Streams 애플리케이션과 연관된 애플리케이션 번들(.sab 파일)을 제출하십시오.
* {{site.data.keyword.streaminganalyticsshort}} 콘솔에서 **작업 제출** 단추를 사용하십시오.
* {{site.data.keyword.Bluemix_notm}}에서 애플리케이션을 개발하고 여기에 {{site.data.keyword.streamsshort}} 애플리케이션을 추가하십시오. [v1 서비스 플랜](/docs/services/StreamingAnalytics/service_plans.html)용 [{{site.data.keyword.streaminganalyticsshort}} v1 REST API ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.bluemix.net/apidocs/220){:new_window} 또는 v2 서비스 플랜용 [{{site.data.keyword.streaminganalyticsshort}} v2 REST API ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.bluemix.net/apidocs/1939){:new_window}를 사용하여 이를 제어하십시오.

{{site.data.keyword.cloudant}}를 포함하여 기타 서비스와 함께 {{site.data.keyword.streaminganalyticsshort}}를 사용하십시오. 시작하고 실행할 수 있게 하는 예제에 대해서는 [기타 {{site.data.keyword.Bluemix_short}} 서비스와의 통합을 위한 튜토리얼](/docs/services/StreamingAnalytics/r_integrating_cloudant_rest.html){:new_window}을 참조하십시오.

자체 애플리케이션으로 추가 작업을 진행하려는 경우, {{site.data.keyword.streamsshort}} 개발 환경을 가져올 수 있으며 애플리케이션을 클라우드에 맞게 준비해야 합니다. {{site.data.keyword.streamsshort}} 환경이 없는 경우 [v2 서비스 플랜](/docs/services/StreamingAnalytics/service_plans.html)용 [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi)를 다운로드할 수 있으며, [v1 서비스 플랜](/docs/services/StreamingAnalytics/service_plans.html)을 사용하는 경우에는 [{{site.data.keyword.streamsshort}} Quick Start Edition VM 이미지 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window}를 다운로드할 수 있습니다.

{{site.data.keyword.streamsshort}} 애플리케이션 개발이 익숙하지 않는 경우 학습을 도와줄 리소스가 있습니다. 자세한 정보는 [{{site.data.keyword.streamsshort}} Knowledge Center ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.2.1/com.ibm.streams.welcome.doc/doc/kc-homepage.html){:new_window}를 참조하십시오.

온프레미스에서 실행하는 SPL 애플리케이션이 이미 있는 경우 [클라우드에 맞게 애플리케이션을 준비![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/streamsdev/docs/getting-spl-application-ready-cloud/){:new_window}해야 합니다.

**참고:** v2 서비스 플랜을 사용하거나 RHEL 6.5와 함께 v1 서비스 플랜을 사용하는 경우 Red Hat Enterprise Linux(RHEL) 7.x에서 애플리케이션을 컴파일해야 합니다. 
