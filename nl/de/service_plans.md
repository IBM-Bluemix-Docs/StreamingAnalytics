---

copyright:
  years: 2015, 2018
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# v1- und v2-Servicepläne
{: #service_plans}

{{site.data.keyword.streaminganalyticsshort}} wird nun in einer containerbasierten Kubernetes-Infrastruktur ausgeführt, die für den Service Vorteile im Bereich der Sicherheit und Verfügbarkeit bietet.
{:shortdesc}

Zugriff auf diese neue containerbasierte Infrastruktur besteht über die v2-Servicepläne. Sie können den {{site.data.keyword.streaminganalyticsshort}}-Plan auswählen, der für Ihre Zwecke am besten geeignet ist:


<table summary="Diese Tabelle enthält eine Liste mit Serviceplänen, die Sie zur Erstellung Ihres {{site.data.keyword.streaminganalyticsshort}}-Service verwenden können. In der Tabelle sind alle Servicepläne sowohl für die v1- als auch für die v2-Plangruppe sowie eine Liste der Features für die jeweilige Plangruppe aufgeführt.">
  <tr>
    <th>Serviceplangruppe<br></th>
    <th>Plannamen<br></th>
    <th>Verfügbare Features<br></th>
  </tr>
  <tr>
    <td width="15%">
    v1-Servicepläne (nicht mehr verwendet)    
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
        <li>Erfordert das Kompilieren der Streams-Anwendung unter dem Betriebssystem Red Hat Enterprise Linux (RHEL) 6.5 oder einer entsprechenden CentOS-Version.</li>
        <li>Wird in einer VM-basierten Infrastruktur ausgeführt.</li>
        <li>Unterstützt v1- und v2-REST-APIs.<br></li>
        <li>Unterstützt sowohl die IAM-Authentifizierung als auch die Authentifizierung mit Benutzerberechtigungsnachweisen.</li>
        <li>Unterstützt das [{{site.data.keyword.streamsshort}} Quick Start Edition-VM-Image ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-linux/)
      </ul>    
    </td>
  </tr>
  <tr>
    <td>
    v2-Servicepläne
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
      <li>Erfordert das Kompilieren der Streams-Anwendung unter einem RHEL 7.x-Betriebssystem oder einer entsprechenden CentOS-Version.</li>
      <li>Wird in einer containerbasierten Infrastruktur ausgeführt.</li>
      <li>Unterstützt v2-REST-APIs.<br></li>
      <li>Unterstützt die IAM-Authentifizierung.</li>
      <li>Unterstützt Serviceendpunkte für Servicepläne, bei denen es sich nicht um Lite-Pläne handelt</li>
      <li>Unterstützt die [{{site.data.keyword.streamsshort}} Quick Start Edition mit Docker ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-docker/)</li>
    </ul>
    </td>
  </tr>
</table>

*Tabelle 1. {{site.data.keyword.streaminganalyticsshort}} v1- und v2-Servicepläne*

## Unterschiede zwischen den v1- und v2-Serviceplänen

Die folgenden Features werden nur in den v1-Serviceplänen unterstützt:

* [v1-REST-API](https://{DomainName}/apidocs/streaming-analytics-v1). In der v2-Infrastruktur müssen Sie die [{{site.data.keyword.streaminganalyticsshort}}-v2-REST-API](https://{DomainName}/apidocs/streaming-analytics-v2) verwenden.
* Beispiel-Apps 'NYC Traffic' und 'Event Detection v1'. In [Beispielanwendungen](/docs/services/StreamingAnalytics/c_starterapps.html) finden Sie eine Liste der Apps, die Sie zum Einstieg in {{site.data.keyword.streaminganalyticsshort}} in der containerbasierten v2-Infrastruktur verwenden können.
* Kompatibilität einiger Toolkits. In [Kompatible Toolkits](/docs/services/StreamingAnalytics/compatible_toolkits.html) finden Sie eine Liste der Toolkits, die mit der neuen containerbasierten Infrastruktur kompatibel sind.

## Umgebungsvariable VCAP_SERVICES für v1-Servicepläne
{: #vcap_services}

Die {{site.data.keyword.streaminganalyticsshort}}-Serviceberechtigungsnachweise und die Umgebungsvariable VCAP_SERVICES für v1-Servicepläne enthalten die VCAP-Informationen, die für die Verwendung der {{site.data.keyword.streaminganalyticsshort}}-v1-REST-API erforderlich sind. Die VCAP-Informationen umfassen die REST-URL, die Serviceinstanz-ID, die Bindungs-ID und die Berechtigungsnachweise für jede {{site.data.keyword.streaminganalyticsshort}}-v1-REST-API.  
{:shortdesc}

 Wenn eine {{site.data.keyword.streaminganalyticsshort}}-Serviceinstanz eingerichtet und an eine Anwendung in {{site.data.keyword.Bluemix_notm}} gebunden wird, stehen die Serviceinstanz-VCAP-Informationen der {{site.data.keyword.Bluemix_notm}}-Anwendungsumgebung zur Verfügung. Diese Informationen sind in der Umgebungsvariablen VCAP_SERVICES enthalten. Wenn eine {{site.data.keyword.streaminganalyticsshort}}-Serviceinstanz ohne Angabe einer Anwendung in {{site.data.keyword.Bluemix_notm}} eingerichtet wird, an die die Instanz gebunden werden kann, werden die Serviceberechtigungsnachweise automatisch erstellt. Der Zugriff auf die {{site.data.keyword.streaminganalyticsshort}}-Serviceberechtigungsnachweise ist über die Servicedetailseite möglich.


Das folgende Beispiel zeigt die Informationen, die in den {{site.data.keyword.streaminganalyticsshort}}-Serviceberechtigungsnachweisen und in der Umgebungsvariablen VCAP_SERVICES enthalten sind:

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

Weitere Informationen zur v1-REST-API finden Sie in der [v1-REST-API-Dokumentation![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window}.

## Umgebungsvariable VCAP_SERVICES für v2-Servicepläne
{: #v2_vcap_services}

Die {{site.data.keyword.streaminganalyticsshort}}-Serviceberechtigungsnachweise und die Umgebungsvariable VCAP_SERVICES für v2-Servicepläne enthalten die VCAP-Informationen, die für die Verwendung der {{site.data.keyword.streaminganalyticsshort}}-v2-REST-API erforderlich sind. Die VCAP-Informationen umfassen die v2-REST-URL, die Service-ID und die Berechtigungsnachweise für den Zugriff auf die {{site.data.keyword.streaminganalyticsshort}}-v2-REST-API.  
{:shortdesc}

Die {{site.data.keyword.streaminganalyticsshort}}-Serviceberechtigungsnachweise und die Umgebungsvariable VCAP_SERVICES für v2-Servicepläne enthalten Informationen, die im folgenden Beisiel dargestellt sind:

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

Weitere Informationen zur v2-REST-API finden Sie in der [v2-REST-API-Dokumentation![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window}.
