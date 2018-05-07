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

# v1 及 v2 服務方案
{: #service_plans}

{{site.data.keyword.streaminganalyticsshort}} 現在是在以 Kubernetes 容器為基礎的基礎架構上執行，這個基礎架構為服務提供了安全及可用性優點。
{:shortdesc}

您可以使用 v2 服務方案來存取這個以容器為基礎的新基礎架構。您可以選擇最適合您需要進行之工作的 {{site.data.keyword.streaminganalyticsshort}} 方案：


<table summary="此表格提供您可以用來建立 {{site.data.keyword.streaminganalyticsshort}} 服務的服務方案清單。表格列出 v1 及 v2 方案集的所有服務方案，並針對每個集合提供特性的清單。">
  <tr>
    <th>服務方案集<br></th>
    <th>方案名稱<br></th>
    <th>可用的特性<br></th>
  </tr>
  <tr>
    <td width="15%">
    v1 服務方案    
    </td>
    <td width="35%">
    <ul>
      <li>精簡 VM</li>
      <li>入門 VM 每小時</li>
      <li>入門 VM 每月</li>
      <li>加強 VM 每小時</li>
      <li>加強 VM 每月</li>
      <li>加強 VM 訂閱</li>
      <li>超值 VM 每月</li>
      <li>超值 VM 訂閱</li>
    </ul>
    </td>
    <td>
      <ul>
        <li>要求您在 Red Hat Enterprise Linux (RHEL) 6.5 作業系統或相等的 CentOS 版本中，編譯您的 Streams 應用程式。</li>
        <li>在以 VM 為基礎的基礎架構上執行。</li>
        <li>支援 v1 及 v2 REST API。<br></li>
        <li>同時支援 IAM 鑑別與使用者認證鑑別。</li>
        <li>支援 [{{site.data.keyword.streamsshort}} Quick Start Edition VM 映像檔 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-install-vm/)
      </ul>    
    </td>
  </tr>
  <tr>
    <td>
    v2 服務方案</td>
    <td>
      <ul>
        <li>精簡</li>
        <li>入門容器每小時</li>
        <li>入門容器每月</li>
        <li>加強容器每小時</li>
        <li>加強容器每月</li>
        <li>超值容器每小時</li>
        <li>超值容器每月</li>
      </ul>
    </td>
    <td>
    <ul>
      <li>要求您在 RHEL 7.x 作業系統或相等的 CentOS 版本中，編譯您的 Streams 應用程式。</li>
      <li>在以容器為基礎的基礎架構上執行。</li>
      <li>支援 v2 REST API。<br></li>
      <li>支援 IAM 鑑別。</li>
      <li>支援 [{{site.data.keyword.streamsshort}} Quick Start Edition 與 Docker ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-install-docker/)</li>
      <li>僅在美國南部地區提供</li>
    </ul>
    </td>
  </tr>
</table>

*表 1. {{site.data.keyword.streaminganalyticsshort}} v1 及 v2 服務方案*

## v1 及 v2 服務方案之間的差異

下列特性只在 v1 服務方案中受到支援：

* [v1 REST API](https://console.bluemix.net/apidocs/220)。在 v2 基礎架構中，您必須使用 [{{site.data.keyword.streaminganalyticsshort}} v2 REST API](https://console.bluemix.net/apidocs/1939)。
* NYC Traffic 及 Event Detection v1 範例應用程式。請參閱[範例應用程式](/docs/services/StreamingAnalytics/c_starterapps.html)，以取得您可以用來在 v2 容器型基礎架構中開始使用 {{site.data.keyword.streaminganalyticsshort}} 的應用程式清單。
* 部分工具箱的相容性。請參閱[相容的工具箱](/docs/services/StreamingAnalytics/compatible_toolkits.html)，以取得與新容器型基礎架構相容的工具箱清單。

## v1 服務方案的 VCAP_SERVICES 環境變數
{: #vcap_services}

v1 服務方案的 {{site.data.keyword.streaminganalyticsshort}} 服務認證和 VCAP_SERVICES 環境變數，包含了使用 {{site.data.keyword.streaminganalyticsshort}} v1 REST API 所需的 VCAP 資訊。VCAP 資訊提供每一個 {{site.data.keyword.streaminganalyticsshort}} v1 REST API 的 REST URL、服務實例 ID、連結 ID 和認證。  
{:shortdesc}

 佈建 {{site.data.keyword.streaminganalyticsshort}} 服務實例並將其連結至 {{site.data.keyword.Bluemix_notm}} 中的應用程式時，可透過 VCAP_SERVICES 環境變數將服務實例 VCAP 資訊提供給 {{site.data.keyword.Bluemix_notm}} 應用程式環境。佈建 {{site.data.keyword.streaminganalyticsshort}} 服務實例但未指定要連結的 {{site.data.keyword.Bluemix_notm}} 應用程式時，會自動建立服務認證。您可以從服務儀表板存取 {{site.data.keyword.streaminganalyticsshort}} 服務認證。


{{site.data.keyword.streaminganalyticsshort}} 服務認證和 VCAP_SERVICES 環境變數，包含了下列範例中所呈現的資訊：

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
        "rest_host": "streams-app-service.ng.bluemix.net",
        "rest_port": "443",
        "rest_url": "https://streams-app-service.ng.bluemix.net",
        "userid": "xxx",
        "password": "yyy"
      }
    }
  ]
}	  
</code></pre>

如需 v1 REST API 的相關資訊，請參閱 [v1 REST API 文件 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://console.ng.bluemix.net/apidocs/220){:new_window}。

## v2 服務方案的 VCAP_SERVICES 環境變數
{: #v2_vcap_services}

v2 服務方案的 {{site.data.keyword.streaminganalyticsshort}} 服務認證和 VCAP_SERVICES 環境變數，包含了使用 {{site.data.keyword.streaminganalyticsshort}} v2 REST API 所需的 VCAP 資訊。VCAP 資訊提供存取 {{site.data.keyword.streaminganalyticsshort}} v2 REST API 用的 v2 REST URL、服務 ID 和認證。  
{:shortdesc}

v2 服務方案的 {{site.data.keyword.streaminganalyticsshort}} 服務認證和 VCAP_SERVICES 環境變數，包含了下列範例中所呈現的資訊：

<pre><code>
    {
      "apikey": "aaaabbbbb1111222ABCDEFgh567appjurHKyY",
      "iam_apikey_description": "Auto generated apikey during resource-key operation for Instance - crn:v1:bluemix:public:streaming-analytics:us-south:a/aaabbbb120110ab123d456e78a0b78910:12e3456e-102f-47e0-9600-4313d496e07a::",
      "iam_apikey_name": "auto-generated-apikey-ab12c34d-e5d6-7890-123f-45dcece304df",
      "iam_role_crn": "crn:v1:bluemix:public:iam::::serviceRole:Manager",
      "iam_serviceid_crn": "crn:v1:bluemix:public:iam-identity::a/b123bb45670ab123d123e12d0a12345::serviceid:ServiceId-a1234b5c-678d-9f6f-bdb4-16c23935efb5",
      "v2_rest_url": "https://streams-app-service.ng.bluemix.net/v2/streaming_analytics/a1234b5c-678d-9f6f-bdb4-16c23935efb5"
    }
</code></pre>

如需 v2 REST API 的相關資訊，請參閱 [v2 REST API 文件 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://console.ng.bluemix.net/apidocs/1939){:new_window}。
