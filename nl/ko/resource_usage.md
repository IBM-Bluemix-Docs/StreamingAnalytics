---

copyright:
  years: 2015, 2018
lastupdated: "2018-07-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}


# 리소스 사용량
{: #resourceusage}

{{site.data.keyword.streaminganalyticsshort}}에는 적절한 리소스 할당 및 사용량을 보장하기 위한 일련의 동작 및 정책이 있습니다.

## 인스턴스 리소스 보기 및 편집
[v1 서비스 플랜](/docs/services/StreamingAnalytics/service_plans.html)용 v1 REST API 또는 서비스 대시보드에서 인스턴스에 대해 권한 부여된 다수의 리소스를 보고 편집할 수 있습니다. [v2 서비스 플랜](/docs/services/StreamingAnalytics/service_plans.html)용으로는 [{{site.data.keyword.streaminganalyticsshort}} v2 REST API](https://console.bluemix.net/apidocs/streaming-analytics-v2-streaming-analytics-v2#get-a-streaming-analytics-instance)를 사용해야 합니다. 

## 리소스 할당
- 성공적으로 실행되는 작업을 제출할 때 자동으로 리소스가 인스턴스에 할당됩니다.
- 리소스에서 실행 중인 작업이 없으면 리소스가 인스턴스에서 제거됩니다. 예를 들어, 리소스 1에 대해 작업 1이 실행 중이고 리소스 1 및 리소스 2에 대해 작업 2가 실행 중인 경우, 작업 2가 취소되면 리소스 2는 제거되는 반면 리소스 1은 인스턴스에 남아 있습니다.
- 작업을 제출할 때 인스턴스가 자체 할당 한계에 도달하지 않으면 이 작업이 새 리소스에 배치됩니다. 
- 일단 인스턴스가 권한이 있는 리소스를 모두 사용하면 기존 리소스에서 새 작업이 스케줄링됩니다. 

## 리소스 제한조건

리소스 할당 및 사용량을 제어하기 위해 리소스 제한조건이 사용될 수 있습니다. 예를 들어, 리소스 제한조건을 사용하면 두 작업이 두 리소스에 분할되는 대신 단일 리소스를 사용하도록 지정할 수 있습니다.
