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

# V1 和 V2 服务套餐
{: #service_plans}

{{site.data.keyword.streaminganalyticsshort}} 现在在基于 Kubernetes 容器的基础架构上运行，对服务而言，该基础架构具有安全性好、可用性佳的优点。
{:shortdesc}

使用 V2 服务套餐时，您可以访问这个基于容器的新基础架构。您可以选择最适合所需工作的 {{site.data.keyword.streaminganalyticsshort}} 套餐：


<table summary="此表列出创建 {{site.data.keyword.streaminganalyticsshort}} 服务时可以使用的服务套餐的列表。表中列出了 V1 和 V2 套餐集的所有服务套餐，并提供每一个套餐集的功能列表。">
  <tr>
    <th>服务套餐集<br></th>
    <th>套餐名称<br></th>
    <th>可用功能<br></th>
  </tr>
  <tr>
    <td width="15%">
   V1 服务套餐    
    </td>
    <td width="35%">
    <ul>
      <li>精简 VM</li>
      <li>入门级 VM 按小时</li>
      <li>入门级 VM 按月</li>
      <li>增强型 VM 按小时</li>
      <li>增强型 VM 按月</li>
      <li>增强型 VM 预订</li>
      <li>高级 VM 按月</li>
      <li>高级 VM 预订</li>
    </ul>
    </td>
    <td>
      <ul>
        <li>要求使用 Red Hat Enterprise Linux (RHEL) 6.5 操作系统或等同的 CentOS 版本，编译 Streams 应用程序。</li>
        <li>在基于 VM 的基础架构上运行。</li>
        <li>支持 V1 和 V2 REST API。<br></li>
        <li>支持 IAM 认证和用户凭证认证。</li>
        <li>支持 [{{site.data.keyword.streamsshort}} Quick Start Edition VM 映像 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-install-vm/)
      </ul>    
    </td>
  </tr>
  <tr>
    <td>
    V2 服务套餐</td>
    <td>
      <ul>
        <li>精简</li>
        <li>入门级容器按小时</li>
        <li>入门级容器按月</li>
        <li>增强型容器按小时</li>
        <li>增强型容器按月</li>
        <li>高级容器按小时</li>
        <li>高级容器按月</li>
      </ul>
    </td>
    <td>
    <ul>
      <li>要求您在 RHEL 7.x 操作系统或等同的 CentOS 版本上编译 Streams 应用程序。</li>
      <li>在基于容器的基础架构上运行。</li>
      <li>支持 V2 REST API。<br></li>
      <li>支持 IAM 认证。</li>
      <li>支持 [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-install-docker/)</li>
      <li>仅在美国南部区域提供</li>
    </ul>
    </td>
  </tr>
</table>

*表 1. {{site.data.keyword.streaminganalyticsshort}} V1 和 V2 服务套餐*

## V1 与 V2 服务套餐的不同之处

只有 V1 服务套餐支持以下功能：

* [V1 REST API](https://console.bluemix.net/apidocs/220)。在 V2 基础架构中，必须使用 [{{site.data.keyword.streaminganalyticsshort}} V2 REST API](https://console.bluemix.net/apidocs/1939)
* “NYC 交通”和“事件检测”V1 样本应用程序。请参阅[样本应用程序](/docs/services/StreamingAnalytics/c_starterapps.html)列表，以了解在基于 V2 容器的基础架构中开始使用 {{site.data.keyword.streaminganalyticsshort}} 时可以使用哪些应用程序。
* 部分工具箱的兼容性。请参阅[兼容的工具箱](/docs/services/StreamingAnalytics/compatible_toolkits.html)列表，以了解哪些工具箱与基于容器的新基础架构兼容。

## V1 服务套餐的 VCAP_SERVICES 环境变量
{: #vcap_services}

V1 套餐的 {{site.data.keyword.streaminganalyticsshort}} 服务凭证和 VCAP_SERVICES 环境变量中包含要使用 {{site.data.keyword.streaminganalyticsshort}} V1 REST API 所需的 VCAP 信息。VCAP 信息为每个 {{site.data.keyword.streaminganalyticsshort}} V1 REST API 提供 REST URL、服务实例标识、绑定标识和凭证。  
{:shortdesc}

 当 {{site.data.keyword.streaminganalyticsshort}} 服务实例得到供应并绑定到 {{site.data.keyword.Bluemix_notm}} 中的应用程序时，就会通过 VCAP_SERVICES 环境变量向 {{site.data.keyword.Bluemix_notm}} 应用程序环境提供该服务实例的 VCAP 信息。未指定 {{site.data.keyword.Bluemix_notm}} 中要绑定到的应用程序即供应 {{site.data.keyword.streaminganalyticsshort}} 服务实例时，会自动创建服务凭证。从服务仪表板可访问 {{site.data.keyword.streaminganalyticsshort}} 服务凭证。



{{site.data.keyword.streaminganalyticsshort}} 服务凭证和 VCAP_SERVICES 环境变量包括以下示例中所呈现的信息：

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

有关 V1 REST API 的更多信息，请参阅 [V1 REST API 文档 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://console.ng.bluemix.net/apidocs/220){:new_window}。

## V2 服务套餐的 VCAP_SERVICES 环境变量
{: #v2_vcap_services}

V2 服务套餐的 {{site.data.keyword.streaminganalyticsshort}} 服务凭证和 VCAP_SERVICES 环境变量中包含要使用 {{site.data.keyword.streaminganalyticsshort}} V2 REST API 所需的 VCAP 信息。VCAP 信息提供用于访问 {{site.data.keyword.streaminganalyticsshort}} V2 REST API 的 V2 REST URL、服务标识和凭证。  
{:shortdesc}

V2 服务套餐的 {{site.data.keyword.streaminganalyticsshort}} 服务凭证和 VCAP_SERVICES 环境变量包括以下示例中所呈现的信息：

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

有关 V2 REST API 的更多信息，请参阅 [V2 REST API 文档 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://console.ng.bluemix.net/apidocs/1939){:new_window}。
