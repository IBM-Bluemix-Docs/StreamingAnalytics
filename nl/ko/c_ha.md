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

# Streaming Analytics 고가용성
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}}는 애플리케이션의 고가용성을 사용 가능하게 합니다. 애플리케이션 노드({{site.data.keyword.streamsshort}} 리소스) 중 하나에서 문제가 발견되면 노드가 자동으로 대체되고 해당 노드에서 실행 중인 작업은 마이그레이션됩니다. 인스턴스에 여러 애플리케이션 노드가 있는 경우에만 작업이 마이그레이션 및 재시작됩니다. [서비스 세부사항 페이지](/docs/services/StreamingAnalytics?topic=dashboard) 또는 [v1 서비스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)용 [{{site.data.keyword.streaminganalyticsshort}} v1 REST API ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window}를 사용하여 인스턴스의 크기를 조정할 수 있습니다. v2 서비스 플랜의 경우 [v2 REST API ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window}를 사용하십시오.
{:shortdesc}

다음 동영상은 서비스 세부사항 페이지를 사용하여 인스턴스의 크기를 조정하는 방법을 보여줍니다.

<iframe width="560" height="315" title="인스턴스 크기 조정" src="https://www.youtube.com/embed/zbZ9am9UhPw?rel=0" frameborder="0" allowfullscreen>인스턴스 크기 조정</iframe>

## 일관성 있는 지역
비즈니스 요구사항으로 인해 일부 애플리케이션의 경우 모든 튜플이 한 번 이상은 처리되어야 합니다. {{site.data.keyword.streamsshort}}는 스트림 처리 동안 튜플이 손실되지 않는 지역 정의를 허용하는 연산자 및 어노테이션으로 개선되었습니다. 일관성 있는 지역의 튜플은 한 번 이상 처리됩니다.

{{site.data.keyword.streaminganalyticsshort}}에서 정의된 일관성 있는 지역을 사용하여 Streams 애플리케이션을 실행하고 모니터할 수 있습니다. {{site.data.keyword.streaminganalyticsshort}} 서비스를 작성하는 경우, 인스턴스가 이미 일관성 있는 지역을 사용하도록 구성되어 있습니다.

일관성 있는 지역은 스트림에서 정의된 지점 내의 모든 튜플 및 구두점 표시를 처리하여 연산자의 상태가 일관성 있게 되는 서브그래프입니다. 이로 인해 서브그래프 내의 튜플이 한 번 이상 처리될 수 있습니다. 일관성 있는 지역에서는 정기적으로 현재 튜플이 소모됩니다. 일관성 있는 지역의 모든 튜플은 서브그래프의 끝까지 처리됩니다. 연산자의 인메모리 상태는 자동으로 직렬화되어 지역의 각 연산자에 대한 체크포인트에 저장됩니다.

이제 튜플 처리를 보장하는 Java 및 SPL 애플리케이션을 둘 다 작성할 수 있으며 이러한 애플리케이션을 {{site.data.keyword.streaminganalyticsshort}}에서 배치할 수 있습니다.

가능한 연산자에 `@consistent` 어노테이션을 사용하여 일관성 있는 지역의 시작을 정의할 수 있습니다. {{site.data.keyword.streamsshort}}이 일관성 있는 지역의 범위를 자동으로 판별하지만 `@autonomous` 어노테이션을 사용하여 지역의 종료 연산자를 변경할 수 있습니다. 정의된 일관성 있는 지역은 정기적으로 일관성 있는 상태를 설정합니다.

Streams 애플리케이션에서 일관성 있는 지역을 사용하는 방법에 대한 세부사항은 [{{site.data.keyword.streamsshort}} 문서 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html)를 확인하십시오.
