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

# 고가용성 및 재해 복구
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}}는 {{site.data.keyword.Bluemix_notm}} 위치(예: 댈러스, 워싱턴 DC, 런던, 프랑크프루트) 내에서 고가용성을 지원합니다. 그러나 전체 {{site.data.keyword.Bluemix_notm}}에 영향을 주는 잠재적인 재해로부터 복구하려면 계획 및 준비가 필요합니다.
{:shortdesc}


사용자는 서비스의 구성, 사용자 정의 및 사용에 대해 이해하고 있어야 합니다. 또한 새 {{site.data.keyword.Bluemix_notm}} 위치에서 서비스 인스턴스를 다시 작성하고 애플리케이션을 해당 위치에 다시 배치할 준비도 되어 있어야 합니다. {{site.data.keyword.Bluemix_notm}}의 고가용성 및 재해 복구 표준에 대해 알아보려면 [작동 중단이 발생하지 않도록 하는 방법](/docs/services/overview?topic=overview-zero-downtime#zero-downtime)을 참조하십시오. [서비스 레벨 계약](/docs/services/overview?topic=overview-zero-downtime#zero-downtime#SLAs)에 대한 정보도 찾을 수 있습니다.

## 고가용성

{{site.data.keyword.streaminganalyticsshort}}는 애플리케이션의 고가용성을 사용 가능하게 합니다. 애플리케이션이 Kubernetes 클러스터에서 실행되는 Docker 컨테이너에 배치됩니다. 고가용성 애플리케이션을 작성하려면 고가용성을 보장하기 위해 이러한 컨테이너가 작동하는 방식을 이해해야 합니다. 

* 애플리케이션 리소스는 서비스 플랜에 따라 할당된 CPU 및 메모리가 포함되어 있는 컨테이너입니다. 
* 하드웨어 또는 소프트웨어 장애 발생 중에 컨테이너가 이동될 수 있습니다. 컨테이너가 이동되면 처리 요소가 다시 시작됩니다. 
* 계획된 유지보수 중에 컨테이너가 이동될 수 있습니다(처리 요소가 다시 시작됨).

그러므로 애플리케이션을 작성할 때 컨테이너가 때때로 이동될 수 있음을 고려해야 합니다. 또한 다음 항목도 고려하십시오.
* PE가 다시 시작될 수 있고 다시 배치될 수 있는지 확인하십시오.
* 애플리케이션이 원하는 순서로 일부 또는 모든 처리 요소(PE)의 다시 시작을 허용할 수 있는지 확인하십시오.
* Streams 애플리케이션의 소스 및 싱크(sink) 연산자가 PE 다시 시작 시 연결을 다시 설정하도록 구성되어 있는지 확인하십시오. 

애플리케이션의 문제점 해결 방법에 대한 예는 [{{site.data.keyword.streaminganalyticsshort}} 배치 안내서](https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/#troubleshooting)를 참조하십시오.

고가용성을 구현하기 위해 Streams 애플리케이션은 모든 튜플의 처리를 보장하도록 사용 설정됩니다. 보장된 튜플 처리를 이행하기 위해 체크포인트가 일관성 있는 지역의 모든 연산자에 대해 정기적으로 설정됩니다. 애플리케이션에 장애가 발생하면 모든 연산자가 마지막으로 성공한 체크포인트 상태로 롤백됩니다.
{{site.data.keyword.streaminganalyticsshort}}는 일관성 있는 지역의 사용을 허용합니다.

### 보장된 튜플 처리
비즈니스 요구사항으로 인해 일부 애플리케이션의 경우 모든 튜플이 한 번 이상은 처리되어야 합니다. {{site.data.keyword.streamsshort}}는 스트림 처리 동안 튜플이 손실되지 않는 지역 정의를 허용하는 연산자 및 어노테이션으로 개선되었습니다. 일관성 있는 지역의 튜플은 한 번 이상 처리됩니다.

애플리케이션 장애가 일관성 있는 지역 내에서 발견된 경우 {{site.data.keyword.streaminganalyticsshort}}는 애플리케이션을 다시 마지막 일관성 있는 상태(즉, 체크포인트)로 설정하고, 해당 지점의 튜플을 재생하도록 애플리케이션 데이터 소스를 지정할 수 있습니다. 

{{site.data.keyword.streaminganalyticsshort}}에서 정의된 일관성 있는 지역을 사용하여 Streams 애플리케이션을 실행하고 모니터할 수 있습니다. {{site.data.keyword.streaminganalyticsshort}} 서비스를 작성하는 경우, 인스턴스가 이미 일관성 있는 지역의 사용을 허용하도록 구성되어 있습니다.

일관성 있는 지역은 스트림에서 정의된 지점 내의 모든 튜플 및 구두점 표시를 처리하여 연산자의 상태가 일관성 있게 되는 서브그래프입니다. 이로 인해 서브그래프 내의 튜플이 한 번 이상 처리될 수 있습니다. 일관성 있는 지역에서는 정기적으로 현재 튜플이 소모됩니다. 일관성 있는 지역의 모든 튜플은 서브그래프의 끝까지 처리됩니다. 연산자의 인메모리 상태는 자동으로 직렬화되어 지역의 각 연산자에 대한 체크포인트에 저장됩니다.

튜플 처리를 보장하는 Java, SPL 및 Python 애플리케이션을 작성할 수 있으며 이러한 애플리케이션을 {{site.data.keyword.streaminganalyticsshort}}에서 배치할 수 있습니다.

가능한 연산자에 `@consistent` 어노테이션을 사용하여 일관성 있는 지역의 시작을 정의할 수 있습니다. {{site.data.keyword.streamsshort}}가 일관성 있는 지역의 범위를 자동으로 판별하지만 `@autonomous` 어노테이션을 사용하여 지역의 종료 연산자를 변경할 수 있습니다. 정의된 일관성 있는 지역은 정기적으로 일관성 있는 상태를 설정합니다.

Streams 애플리케이션에서 일관성 있는 지역을 사용하는 방법에 대한 세부사항은 [{{site.data.keyword.streamsshort}} 문서 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html)를 확인하십시오.

## 재해 복구
{{site.data.keyword.streaminganalyticsshort}}는 여러 {{site.data.keyword.Bluemix_notm}} 지역에서 제공되는 GA 서비스입니다. {{site.data.keyword.streaminganalyticsshort}}는 {{site.data.keyword.Bluemix_notm}}에 사용자 데이터를 저장하지 않습니다.

비즈니스 요구사항에 따라 다음 재해 복구 전략 중 하나를 선택하십시오.
* 애플리케이션에 대한 중단이 필요하지 않은 경우 다음을 수행하십시오.
  1. 여러 {{site.data.keyword.Bluemix_notm}} 지역에서 {{site.data.keyword.streaminganalyticsshort}}의 인스턴스를 작성하십시오. 
  2. 애플리케이션을 여러 지역에 제출하십시오.


* 애플리케이션에 대한 최소한의 중단이 필요한 경우 다음을 수행하십시오.
  1. 여러 {{site.data.keyword.Bluemix_notm}} 지역에서 {{site.data.keyword.streaminganalyticsshort}}의 인스턴스를 작성하십시오. 
  2. [서비스 REST API](https://ibm.co/2Gt9mB6)를 사용하여 애플리케이션을 모니터하고 필요에 따라 새 지역으로 워크로드를 동적으로 이동하십시오.

**참고**: 각 일관성 있는 지역은 {{site.data.keyword.Bluemix_notm}} 지역으로 연결됩니다. 재해 복구 시나리오에서 애플리케이션의 일관성 있는 지역에는 역할이 부여되지 않습니다. 
