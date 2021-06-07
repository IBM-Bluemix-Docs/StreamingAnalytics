---

copyright:
  years: 2015, 2021
lastupdated: "2021-06-07"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:deprecated: .deprecated}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Service plans
{: #service_plans}

{{site.data.keyword.streaminganalyticsfull}} is deprecated. As of July 30, 2021, 
you can't create new instances, and access to free Lite instances will be removed. 
Existing paid plan instances are supported until May 1, 2022. Any instance that still exist on that date will be stopped and deleted. 
For more information, see [End of Market](/docs/StreamingAnalytics?topic=StreamingAnalytics-end_of_market).
{: deprecated}

{{site.data.keyword.streaminganalyticsshort}} is runs on a Kubernetes container-based infrastructure that provides security and availability advantages to the service.
{:shortdesc}

You can choose the {{site.data.keyword.streaminganalyticsshort}} plan that is best suited for the work that you need to do:


<table summary="This table provides a list of service plans that you can use to create your {{site.data.keyword.streaminganalyticsshort}} service. The table lists all service plans and provides a list of features.">
  <tr>
    <th>Plan names<br></th>
    <th>Available features<br></th>
  </tr>
  <tr>
    <td width="40%">
      <ul>
        <li>Lite
        <br>Dedicated application resources with 1 core and 4GB RAM
        </li>
        <li>Entry Container Hourly
        <br>Dedicated application resources with 1 core and 4GB RAM
        </li>
        <li>Entry Container Monthly
        <br>Dedicated application resources with 1 core and 4GB RAM
        </li>
        <li>Enhanced Container Hourly
        <br>Dedicated application resources with 4 cores and 12GB RAM
        </li>
        <li>Enhanced Container Monthly
        <br>Dedicated application resources with 4 cores and 12GB RAM
        </li>
        <li>Premium Container Hourly
        <br>Dedicated application resources with 16 cores and 128GB RAM
        </li>
        <li>Premium Container Monthly
        <br>Dedicated application resources with 16 cores and 128GB RAM
        </li>
      </ul>
    </td>
    <td>
    <ul>
      <li>Requires that your Streams applications can run on a RHEL 7.4 or CentOS 7.4 x86_64 system.</li>
      <li>Runs on a container-based infrastructure.</li>
      <li>Supports REST APIs.<br></li>
      <li>Supports IAM authentication.</li>
      <li>Supports service endpoints for non-Lite service plans</li>
      <li>Supports [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-docker/)</li>
    </ul>
    </td>
  </tr>
</table>

**Subscription Plan**: Subscription plan is available with [IBM Cloud Pak for Data as a Service ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/products/cloud-pak-for-data/as-a-service){:new_window}.

## VCAP_SERVICES environment variable
{: #v2_vcap_services}

The {{site.data.keyword.streaminganalyticsshort}} service credentials and VCAP_SERVICES environment variable include the VCAP information that you must use with the {{site.data.keyword.streaminganalyticsshort}} REST API. The VCAP information provides the REST URL, service ID, and credentials to access the  {{site.data.keyword.streaminganalyticsshort}} REST API.  
{:shortdesc}

The {{site.data.keyword.streaminganalyticsshort}} service credentials and VCAP_SERVICES environment variable include information as presented in the following example:

```
    {
      "apikey": "aaaabbbbb1111222ABCDEFgh567appjurHKyY",
      "iam_apikey_description": "Auto generated apikey during resource-key operation for Instance - crn:v1:bluemix:public:streaming-analytics:us-south:a/aaabbbb120110ab123d456e78a0b78910:12e3456e-102f-47e0-9600-4313d496e07a::",
      "iam_apikey_name": "auto-generated-apikey-ab12c34d-e5d6-7890-123f-45dcece304df",
      "iam_role_crn": "crn:v1:bluemix:public:iam::::serviceRole:Manager",
      "iam_serviceid_crn": "crn:v1:bluemix:public:iam-identity::a/b123bb45670ab123d123e12d0a12345::serviceid:ServiceId-a1234b5c-678d-9f6f-bdb4-16c23935efb5",
      "v2_rest_url": "{rest_url}/v2/streaming_analytics/a1234b5c-678d-9f6f-bdb4-16c23935efb5"
    }
```
{:pre}

For more information about the REST API, see the  [REST API documentation ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window}.
