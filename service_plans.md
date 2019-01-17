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

# v1 and v2 service plans
{: #service_plans}

{{site.data.keyword.streaminganalyticsshort}} is now running on a Kubernetes container-based infrastructure that provides security and availability advantages to the service.
{:shortdesc}

You can access this new container-based infrastructure with the v2 service plans. You can choose the {{site.data.keyword.streaminganalyticsshort}} plan that is best suited for the work that you need to do:


<table summary="This table provides a list of service plans that you can use to create your {{site.data.keyword.streaminganalyticsshort}} service. The table lists all service plans for both v1 and v2 plan sets and provides a list of features for each set.">
  <tr>
    <th>Service plan set<br></th>
    <th>Plan names<br></th>
    <th>Available features<br></th>
  </tr>
  <tr>
    <td width="15%">
    v1 service plans (deprecated)    
    </td>
    <td width="35%">
    <ul>
      <li>Lite VM</li>
      <li>Entry VM Hourly</li>
      <li>Entry VM Monthly</li>
      <li>Enhanced VM Hourly</li>
      <li>Enhanced VM Monthly</li>
      <li>Enhanced VM Subscription</li>
      <li>Premium VM Monthly</li>
      <li>Premium VM Subscription</li>
    </ul>
    </td>
    <td>
      <ul>
        <li>Requires that you compile your Streams application in a Red Hat Enterprise Linux (RHEL) 6.5 operating system or an equivalent CentOS version.</li>
        <li>Runs on a VM-based infrastructure.</li>
        <li>Supports v1 and v2 REST APIs.<br></li>
        <li>Supports both IAM authentication and user credentials authentication.</li>
        <li>Supports [{{site.data.keyword.streamsshort}} Quick Start Edition VM image ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-linux/)
      </ul>    
    </td>
  </tr>
  <tr>
    <td>
    v2 service plans
    </td>
    <td>
      <ul>
        <li>Lite</li>
        <li>Entry Container Hourly</li>
        <li>Entry Container Monthly</li>
        <li>Entry Container Subscription</li>
        <li>Enhanced Container Hourly</li>
        <li>Enhanced Container Monthly</li>
        <li>Enhanced Container Subscription</li>
        <li>Premium Container Hourly</li>
        <li>Premium Container Monthly</li>
        <li>Premium Container Subscription</li>
      </ul>
    </td>
    <td>
    <ul>
      <li>Requires that you compile your Streams application in an RHEL 7.x operating system or an equivalent CentOS version.</li>
      <li>Runs on a container-based infrastructure.</li>
      <li>Supports v2 REST APIs.<br></li>
      <li>Supports IAM authentication.</li>
      <li>Supports service endpoints for non-Lite service plans</li>
      <li>Supports [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-docker/)</li>
    </ul>
    </td>
  </tr>
</table>

*Table 1. {{site.data.keyword.streaminganalyticsshort}} v1 and v2 service plans*

## Differences between v1 and v2 service plans

The following features are only supported in the v1 service plans:

* [v1 REST API](https://{DomainName}/apidocs/streaming-analytics-v1). In the v2 infrastructure, you must use the [{{site.data.keyword.streaminganalyticsshort}} v2 REST API](https://{DomainName}/apidocs/streaming-analytics-v2)
* NYC Traffic and Event Detection v1 sample apps. See [Sample applications](/docs/services/StreamingAnalytics/c_starterapps.html) to get a list of apps you can use to get you started with {{site.data.keyword.streaminganalyticsshort}} in the v2 container-based infrastructure.
* Compatibility of some toolkits. See [Compatible toolkits](/docs/services/StreamingAnalytics/compatible_toolkits.html) to get a list of toolkits that are compatible with the new container-based infrastructure.

## VCAP_SERVICES environment variable for v1 service plans
{: #vcap_services}

The {{site.data.keyword.streaminganalyticsshort}} service credentials and VCAP_SERVICES environment variable for v1 service plans include the VCAP information that is required to use the {{site.data.keyword.streaminganalyticsshort}} v1 REST API. The VCAP information provides the REST URL, service instance ID, binding ID, and credentials for each {{site.data.keyword.streaminganalyticsshort}} v1 REST API.  
{:shortdesc}

 When a {{site.data.keyword.streaminganalyticsshort}} service instance is provisioned and bound to an application in {{site.data.keyword.Bluemix_notm}}, the service instance VCAP information is available to the {{site.data.keyword.Bluemix_notm}} application environment. You can find this information in the VCAP_SERVICES environment variable. When a {{site.data.keyword.streaminganalyticsshort}} service instance is provisioned without specifying an application in {{site.data.keyword.Bluemix_notm}} to bind to, service credentials are automatically created. {{site.data.keyword.streaminganalyticsshort}} service credentials can be accessed from the service details page.


The {{site.data.keyword.streaminganalyticsshort}} service credentials and VCAP_SERVICES environment variable include information as presented in the following example:

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

For more information about the v1 REST API, see the  [v1 REST API documentation ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window}.

## VCAP_SERVICES environment variable for v2 service plans
{: #v2_vcap_services}

The {{site.data.keyword.streaminganalyticsshort}} service credentials and VCAP_SERVICES environment variable for v2 service plans include the VCAP information that you must use the {{site.data.keyword.streaminganalyticsshort}} v2 REST API. The VCAP information provides the v2 REST URL, service ID, and credentials to access the  {{site.data.keyword.streaminganalyticsshort}} v2 REST API.  
{:shortdesc}

The {{site.data.keyword.streaminganalyticsshort}} service credentials and VCAP_SERVICES environment variable for v2 service plans include information as presented in the following example:

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

For more information about the v2 REST API, see the  [v2 REST API documentation ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window}.
