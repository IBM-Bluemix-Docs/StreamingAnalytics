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

# v1 및 v2 서비스 플랜
{: #service_plans}

{{site.data.keyword.streaminganalyticsshort}}는 이제 서비스에 보안 및 가용성 이점을 제공하는 Kubernetes 컨테이너 기반 인프라에서 실행됩니다.
{:shortdesc}

v2 서비스 플랜으로 이 새로운 컨테이너 기반 인프라에 액세스할 수 있습니다. 수행해야 하는 작업에 가장 적합한 {{site.data.keyword.streaminganalyticsshort}} 플랜을 선택할 수 있습니다.


<table summary="이 표는 {{site.data.keyword.streaminganalyticsshort}} 서비스를 작성하는 데 사용할 수 있는 서비스 플랜의 목록을 제공합니다. 표에는 v1 및 v2 플랜 세트 모두에 대한 모든 서비스 플랜이 나열되어 있으며 각 세트에 대한 기능의 목록을 제공합니다.">
  <tr>
    <th>서비스 플랜 세트<br></th>
    <th>플랜 이름<br></th>
    <th>사용 가능한 기능<br></th>
  </tr>
  <tr>
    <td width="15%">
    v1 서비스 플랜(더 이상 사용되지 않음)    
    </td>
    <td width="35%">
    <ul>
      <li>Lite VM</li>
      <li>엔트리 VM 시간별</li>
      <li>엔트리 VM 월별</li>
      <li>고급 VM 시간별</li>
      <li>고급 VM 월별</li>
      <li>고급 VM 구독</li>
      <li>프리미엄 VM 월별</li>
      <li>프리미엄 VM 구독</li>
    </ul>
    </td>
    <td>
      <ul>
        <li>Red Hat Enterprise Linux(RHEL) 6.5 운영 체제 또는 이와 동등한 CentOS 버전에서 Streams 애플리케이션을 컴파일해야 합니다.</li>
        <li>VM 기반 인프라에서 실행됩니다.</li>
        <li>v1 및 v2 REST API를 지원합니다.<br></li>
        <li>IAM 인증 및 사용자 인증 정보 인증을 모두 지원합니다.</li>
        <li>[{{site.data.keyword.streamsshort}} Quick Start Edition VM 이미지 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-linux/)를 지원합니다.
      </ul>    
    </td>
  </tr>
  <tr>
    <td>
    v2 서비스 플랜
    </td>
    <td>
      <ul>
        <li>Lite</li>
        <li>엔트리 컨테이너 시간별</li>
        <li>엔트리 컨테이너 월별</li>
        <li>엔트리 컨테이너 구독</li>
        <li>고급 컨테이너 시간별</li>
        <li>고급 컨테이너 월별</li>
        <li>고급 컨테이너 구독</li>
        <li>프리미엄 컨테이너 시간별</li>
        <li>프리미엄 컨테이너 월별</li>
        <li>프리미엄 컨테이너 구독</li>
      </ul>
    </td>
    <td>
    <ul>
      <li>RHEL 7.x 운영 체제 또는 이와 동등한 CentOS 버전에서 Streams 애플리케이션을 컴파일해야 합니다.</li>
      <li>컨테이너 기반 인프라에서 실행됩니다.</li>
      <li>v2 REST API를 지원합니다.<br></li>
      <li>IAM 인증을 지원합니다.</li>
      <li>Lite 이외의 서비스 플랜에 대한 서비스 엔드포인트를 지원합니다.</li>
      <li>[{{site.data.keyword.streamsshort}} Quick Start Edition with Docker ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-docker/)를 지원합니다.</li>
    </ul>
    </td>
  </tr>
</table>

*표 1. {{site.data.keyword.streaminganalyticsshort}} v1 및 v2 서비스 플랜*

## v1 및 v2 서비스 플랜 간의 차이점

다음 기능은 v1 서비스 플랜에서만 지원됩니다.

* [v1 REST API](https://{DomainName}/apidocs/streaming-analytics-v1). v2 인프라에서는 [{{site.data.keyword.streaminganalyticsshort}} v2 REST API](https://{DomainName}/apidocs/streaming-analytics-v2)를 사용해야 합니다.
* NYC Traffic 및 Event Detection v1 샘플 앱. v2 컨테이너 기반 인프라에서 {{site.data.keyword.streaminganalyticsshort}}를 시작하는 데 사용할 수 있는 앱의 목록을 가져오려면 [샘플 애플리케이션](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps)을 참조하십시오.
* 일부 툴킷의 호환성. 새 컨테이터 기반 인프라와 호환되는 툴킷의 목록을 가져오려면 [호환 가능 툴킷](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-compatible_toolkits)을 참조하십시오.

## v1 서비스 플랜용 VCAP_SERVICES 환경 변수
{: #vcap_services}

v1 서비스 플랜용 {{site.data.keyword.streaminganalyticsshort}} 서비스 인증 정보 및 VCAP_SERVICES 환경 변수는 {{site.data.keyword.streaminganalyticsshort}} v1 REST API를 사용하기 위해 필요한 VCAP 정보를 포함합니다. VCAP 정보는 각 {{site.data.keyword.streaminganalyticsshort}} v1 REST API에 대한 REST URL, 서비스 인스턴스 ID, 바인딩 ID 및 인증 정보를 제공합니다.  
{:shortdesc}

 {{site.data.keyword.streaminganalyticsshort}} 서비스 인스턴스가 프로비저닝되어 {{site.data.keyword.Bluemix_notm}}의 애플리케이션에 바인드되면 서비스 인스턴스 VCAP 정보를 {{site.data.keyword.Bluemix_notm}} 애플리케이션 환경에서 사용할 수 있습니다. VCAP_SERVICES 환경 변수에서 이 정보를 찾을 수 있습니다. {{site.data.keyword.streaminganalyticsshort}} 서비스 인스턴스가 바인드할 대상인 {{site.data.keyword.Bluemix_notm}}의 애플리케이션을 지정하지 않고 프로비저닝되면 서비스 인증 정보가 자동으로 작성됩니다. {{site.data.keyword.streaminganalyticsshort}} 서비스 인증 정보는 서비스 세부사항 페이지에서 액세스할 수 있습니다.


{{site.data.keyword.streaminganalyticsshort}} 서비스 인증 정보와 VCAP_SERVICES 환경 변수에는 다음 예제에서 제시하는 정보가 포함됩니다.

<pre><code>
{
  "streaming-analytics": [
    {
      "name": "NYCTrafficStreaming Analytics-t6",
      "label": "streaming-analytics",
      "plan": "Standard",
      "credentials": {
        "status_path": "/jax-rs/streams/status/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "size_path": "/jax-rs/streams/size/service_instances/0fb17393-90eb-4066-96b6-df1ac9860743/service_bindings/b37b89df-b0d7-464e-b7d9-3db607a26550",
        "start_path": "/jax-rs/streams/start/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "stop_path": "/jax-rs/streams/stop/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "resources_path": "/jax-rs/resources/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "jobs_path": "/jax-rs/jobs/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "rest_host": "{rest_url}",
        "rest_port": "443",
        "rest_url": "{rest_url}",
        "userid": "xxx",
        "password": "yyy"
      }
    }
  ]
}	  
</code></pre>

v1 REST API에 대한 자세한 정보는 [v1 REST API 문서 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window}를 참조하십시오.

## v2 서비스 플랜용 VCAP_SERVICES 환경 변수
{: #v2_vcap_services}

v2 서비스 플랜용 {{site.data.keyword.streaminganalyticsshort}} 서비스 인증 정보 및 VCAP_SERVICES 환경 변수는 사용자가 {{site.data.keyword.streaminganalyticsshort}} v2 REST API를 사용해야 하는 VCAP 정보를 포함합니다. VCAP 정보는 {{site.data.keyword.streaminganalyticsshort}} v2 REST API에 액세스하기 위한 v2 REST URL, 서비스 ID 및 인증 정보를 제공합니다.  
{:shortdesc}

v2 서비스 플랜용 {{site.data.keyword.streaminganalyticsshort}} 서비스 인증 정보 및 VCAP_SERVICES 환경 변수는 다음 예제에서 제공되는 정보를 포함합니다.

<pre><code>
    {
      "apikey": "aaaabbbbb1111222ABCDEFgh567appjurHKyY",
      "iam_apikey_description": "Auto generated apikey during resource-key operation for Instance - crn:v1:bluemix:public:streaming-analytics:us-south:a/aaabbbb120110ab123d456e78a0b78910:12e3456e-102f-47e0-9600-4313d496e07a::",
      "iam_apikey_name": "auto-generated-apikey-ab12c34d-e5d6-7890-123f-45dcece304df",
      "iam_role_crn": "crn:v1:bluemix:public:iam::::serviceRole:Manager",
      "iam_serviceid_crn": "crn:v1:bluemix:public:iam-identity::a/b123bb45670ab123d123e12d0a12345::serviceid:ServiceId-a1234b5c-678d-9f6f-bdb4-16c23935efb5",
      "v2_rest_url": "{rest_url}/v2/streaming_analytics/a1234b5c-678d-9f6f-bdb4-16c23935efb5"
    }
</code></pre>

v2 REST API에 대한 자세한 정보는 [v2 REST API 문서 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window}를 참조하십시오.
