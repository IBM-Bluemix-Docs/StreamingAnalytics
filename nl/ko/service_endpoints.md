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

# 서비스 엔드포인트 관리
{: #manage_endpoints}

{{site.data.keyword.Bluemix_short}} 서비스 엔드포인트는 사설 엔드포인트를 사용하여 {{site.data.keyword.Bluemix_notm}} 네트워크를 통해 {{site.data.keyword.streaminganalyticsshort}} 서비스에 연결할 수 있도록 합니다.
{:shortdesc}

이제 서비스 인스턴스에 액세스하고 관리하기 위한 사설 엔드포인트를 추가할 수 있습니다.

## 전제조건
{: #prereqs notoc}

다음 요구사항을 충족하는지 확인하십시오.
- Lite 이외의 [v2 인스턴스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)을 사용하여 서비스 인스턴스를 작성합니다.
- {{site.data.keyword.Bluemix_notm}} 계정에 대해 [VRF(Virtual Route Forwarding)](/docs/infrastructure/direct-link?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud)를 사용합니다.


사설 엔드포인트를 추가하려면 다음을 수행하십시오.

1. 서비스 세부사항 페이지에서 **엔드포인트 관리**를 클릭하십시오. 서비스 인스턴스에 지정된 공용 엔드포인트를 볼 수 있습니다.
2. **사설 엔드포인트 추가**를 클릭하십시오. 사설 엔드포인트가 서비스 인스턴스에 지정됩니다.
3. **선택사항:** 필요에 따라 엔드포인트 전환을 사용하여 엔드포인트를 사용 또는 사용 안함으로 설정하십시오.


서비스 엔드포인트에 대한 자세한 정보는 [{{site.data.keyword.Bluemix_notm}} 서비스 엔드포인트 문서](/docs/services/service-endpoint?topic=service-endpoint-about#about){:new_window}를 확인하십시오.
