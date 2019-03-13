---

copyright:
  years: 2015, 2019
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics 정보
{: #about}

{{site.data.keyword.streaminganalyticsfull}}를 사용하여 {{site.data.keyword.Bluemix_short}} 애플리케이션의 일부로 작동 중인 데이터 관련 실시간 분석을 수행할 수 있습니다.
{:shortdesc}

{{site.data.keyword.streaminganalyticsshort}}의 새로운 기능은 [서비스에 대한 간단한 소개 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/streamsdev/docs/streaming-analytics-now-available-bluemix-2/){:new_window}를 확인하십시오.

{{site.data.keyword.streaminganalyticsshort}} 서비스는 클라우드에서 데이터를 배치, 분석, 모니터하기 위한 다음 기능을 제공합니다.

**대화식 및 프로그램 방식 서비스의 사용:**

[v1 서비스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)을 사용하는 경우에는 [{{site.data.keyword.streaminganalyticsshort}} 콘솔](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-console#console)을 통해 대화식으로 또는 [{{site.data.keyword.streaminganalyticsshort}} v1 REST API ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window}를 통해 프로그래밍 방식으로 서비스를 사용할 수 있습니다. [v2 서비스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)의 경우 [{{site.data.keyword.streaminganalyticsshort}}v2 REST API ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/apidocs/streaming-analytics-v2)를 사용하십시오.

**SPL, Java, Scala 및 Python 애플리케이션의 배치 및 모니터링:**

SPL, Java, Scala 및 Python으로 {{site.data.keyword.streamsshort}} 애플리케이션을 작성할 수 있습니다. {{site.data.keyword.streaminganalyticsshort}} 콘솔을 사용하여 [이러한 애플리케이션을 배치하고 모니터](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_deploytocloud)하십시오.

SPL에서 애플리케이션을 작성하려는 경우, {{site.data.keyword.streamsfull}} Processing Language(SPL)가 스트림 처리 애플리케이션의 작성에 사용되는 프로그래밍 언어입니다. 자체 SPL 애플리케이션으로 추가 작업을 진행하려는 경우, {{site.data.keyword.streamsshort}} 개발 환경을 가져올 수 있으며 SPL 앱을 클라우드에 맞게 준비해야 합니다.

{{site.data.keyword.streamsshort}} 개발 환경 없이 Python 애플리케이션을 작성하고 배치하려면 {{site.data.keyword.DSX_short}} 또는 {{site.data.keyword.streamsshort}} Python API에서 서비스 노트북을 사용하십시오. 자세한 정보는 [{{site.data.keyword.streaminganalyticsshort}}용 Python 애플리케이션 개발](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_develop_apps_python)을 참조하십시오.

로컬 개발 환경에서 Streams Runner를 사용하여 Beam 애플리케이션을 개발할 수 있으며, {{site.data.keyword.streaminganalyticsshort}} 서비스에서 이를 배치하고 모니터할 수 있습니다. Streams Runner를 사용하는 Beam 애플리케이션에 대한 자세한 정보는 [{{site.data.keyword.streaminganalyticsshort}}의 IBM Streams Runner for Apache Beam](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-gs_beamrunner)을 참조하십시오.


**{{site.data.keyword.streamsshort}} 연산자와의 호환성:**

[{{site.data.keyword.streamsshort}} Processing Language(SPL) 표준 툴킷](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-compatible_toolkits)의 {{site.data.keyword.streamsshort}} 연산자는 {{site.data.keyword.streaminganalyticsshort}}와 호환 가능합니다.

## Streaming Analytics 책임
{: #responsibilities notoc}

### 고객의 책임
{: #clientresponsibilities notoc}

고객은 다음과 같은 부분을 담당합니다.

* {{site.data.keyword.streamsshort}}에 대한 IBM의 초기 구성에 이어, 해당 인스턴스에서 실행하는 {{site.data.keyword.streamsshort}} 작업의 모니터링, 구성 및 관리. 고객에게는 인스턴스를 시작 및 중지하고 인스턴스에서 실행 중인 작업을 시작 및 중지할 수 있는 유연성이 있습니다.
* 필요에 따라 서비스에서 프로그램 및 애플리케이션을 개발하여 데이터를 분석하고 여기에서 인사이트 확보. 고객은 또한 그러한 개발된 프로그램이나 애플리케이션의 품질과 성능에 대해 책임을 집니다. 프로그램은 {{site.data.keyword.streamsshort}} 토폴로지 기능을 사용하여 SPL, Java 또는 기타 지원되는 언어로 개발될 수 있습니다. 이는 {{site.data.keyword.streaminganalyticsshort}}에 사용된 것과 동일한 운영 체제에서 {{site.data.keyword.streamsshort}} Developer Edition 또는 {{site.data.keyword.streamsshort}} Quick Start Edition 중 하나를 사용하여 컴파일되어야 합니다.
* 링크([https://developer.ibm.com/bluemix/support/#status ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/bluemix/support/#status){:new_window})를 정기적으로 확인하여 스케줄된 "비중단" 또는 "중단" 작동 중단 시간이 있는지 파악.  
* 연속성 보장을 위해 비즈니스 요구사항에 따라 모든 데이터, 메타데이터, 구성 파일 및 환경 매개변수 백업.
* 모든 유형의 장애 발생에 대비하여 연속성을 보장하기 위해 백업에서 데이터, 메타데이터, 구성 파일 및 환경 매개변수 복원. 여기에는 데이터 센터 또는 팟(Pod) 장애, 서버 장애 또는 하드 디스크 장애 또는 소프트웨어 장애가 포함되지만 이로 제한되지는 않습니다.

### IBM의 책임
{: #ibmresponsibilities notoc}

{{site.data.keyword.streaminganalyticsfull}}의 일부로 IBM은 다음을 수행합니다.

* 고객 인스턴스에 대한 서버, 스토리지 및 네트워킹 인프라의 제공 및 관리.
* 노드의 수를 선택하고 해당 노드에서 {{site.data.keyword.streamsshort}}의 초기 구성 제공.
* 보호 및 고립을 위해 인터넷 페이싱과 내부 방화벽을 위한 인프라 제공 및 관리.
* {{site.data.keyword.streaminganalyticsshort}}에서 다음 컴포넌트의 모니터링 및 관리.
	* 네트워크 컴포넌트
	* 서버 및 관련 로컬 스토리지
	* 인프라 운영 체제
	* {{site.data.keyword.streamsshort}} 관리 서비스
	* {{site.data.keyword.streamsshort}} 인스턴스
* 인프라 운영 체제 및 {{site.data.keyword.streamsshort}}에 대한 보안 패치를 비롯하여 유지보수 패치 제공.
* 시스템 중단이 필요하지 않은 정기 유지보수(“비중단” 유지보수) 및 일부 시스템 중단과 재시작이 필요할 수 있는 유지보수(“중단” 유지보수) 수행. 이는 [https://developer.ibm.com/bluemix/support/#status ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/bluemix/support/#status){:new_window}에 게시된 예정된 시간에 수행됩니다.
* 스케줄된 유지보수 시간의 변경은 적절한 공지사항으로 게시됩니다.
