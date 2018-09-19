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

# Planes de servicio v1 y v2
{: #service_plans}

{{site.data.keyword.streaminganalyticsshort}} ahora está ejecutándose en una infraestructura basada en contenedores de Kubernetes que proporciona ventajas de seguridad y de disponibilidad al servicio.
{:shortdesc}

Puede acceder a esta nueva infraestructura basada en contenedores con los planes de servicio de v2. Puede elegir el plan de {{site.data.keyword.streaminganalyticsshort}} que mejor se ajuste para el trabajo que necesite realizar:


<table summary="Esta tabla proporciona una lista de planes de servicio que puede utilizar para crear el servicio de {{site.data.keyword.streaminganalyticsshort}}. La tabla lista todos los planes de servicio para los conjuntos de planes de v1 y v2 y proporciona una lista de características para cada conjunto.">
  <tr>
    <th>Plan de servicio establecido<br></th>
    <th>Nombres de planes<br></th>
    <th>Características disponibles<br></th>
  </tr>
  <tr>
    <td width="15%">
    Planes de servicio de v1    
    </td>
    <td width="35%">
    <ul>
      <li>Lite VM</li>
      <li>Entry VM - Cada hora</li>
      <li>Entry VM - Cada mes</li>
      <li>Enhanced VM - Cada hora</li>
      <li>Enhanced VM - Cada mes</li>
      <li>Enhanced VM - Suscripción</li>
      <li>Premium VM - Cada mes</li>
      <li>Premium VM - Suscripción</li>
    </ul>
    </td>
    <td>
      <ul>
        <li>Requiere la compilación de su aplicación de Streams en un sistema operativo Red Hat Enterprise Linux (RHEL) 6.5 o una versión de CentOS equivalente.</li>
        <li>Se ejecuta en una infraestructura basada en máquina virtual.</li>
        <li>Admite las API REST v1 y v2.<br></li>
        <li>Admite tanto la autenticación de IAM como la autenticación de credenciales de usuario.</li>
        <li>Admite la [imagen de {{site.data.keyword.streamsshort}} Quick Start Edition VM ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-install-vm/)
      </ul>    
    </td>
  </tr>
  <tr>
    <td>
    Planes de servicio de v2
    </td>
    <td>
      <ul>
        <li>Lite</li>
        <li>Entry Container - Cada hora</li>
        <li>Entry Container - Cada mes</li>
        <li>Suscripción Entry Container</li>
        <li>Enhanced Container - Cada hora</li>
        <li>Enhanced Container - Cada mes</li>
        <li>Suscripción Enhanced Container</li>
        <li>Premium Container - Cada hora</li>
        <li>Premium Container - Cada mes</li>
        <li>Suscripción Premium Container</li>
      </ul>
    </td>
    <td>
    <ul>
      <li>Requiere que compile la aplicación de Streams en un sistema operativo RHEL 7.x o una versión de CentOS equivalente.</li>
      <li>Se ejecuta en una infraestructura basada en contenedores.</li>
      <li>Admite las API REST de v2.<br></li>
      <li>Admite la autenticación de IAM.</li>
      <li>Admite [{{site.data.keyword.streamsshort}} Quick Start Edition con Docker ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-install-docker/)</li>
      <li>Disponible únicamente en la región EE.UU. sur</li>
    </ul>
    </td>
  </tr>
</table>

*Tabla 1. Planes de servicio de v1 y v2 de {{site.data.keyword.streaminganalyticsshort}}*

## Diferencias entre los planes de servicio de v1 y v2

Las siguientes características solo están admitidas en los planes de servicio de v1:

* [API REST de v1](https://console.bluemix.net/apidocs/streaming-analytics-v1). En la infraestructura de v2, debe utilizar la [API REST de {{site.data.keyword.streaminganalyticsshort}} v2](https://console.bluemix.net/apidocs/streaming-analytics-v2)
* Apps de muestra de v1 NYC Traffic y Event Detection. Consulte [Aplicaciones de ejemplo](/docs/services/StreamingAnalytics/c_starterapps.html) para obtener una lista de apps que puede utilizar para empezar a utilizar {{site.data.keyword.streaminganalyticsshort}} en la infraestructura basada en contenedores de v2.
* Compatibilidad de algunos kits de herramientas. Consulte [Kits de herramientas compatibles](/docs/services/StreamingAnalytics/compatible_toolkits.html) para obtener una lista de kits de herramientas compatibles con la nueva infraestructura basada en contenedores.

## Variable de entorno VCAP_SERVICES para planes de servicio de v1
{: #vcap_services}

Las credenciales de servicio de {{site.data.keyword.streaminganalyticsshort}} y la variable de entorno VCAP_SERVICES para los planes de servicio de v1 incluyen la información de VCAP necesaria para utilizar la API REST de {{site.data.keyword.streaminganalyticsshort}} v1. La información de VCAP proporciona el URL REST, el ID de instancias de servicio, el ID de enlace y las credenciales para cada API REST de {{site.data.keyword.streaminganalyticsshort}} v1.  
{:shortdesc}

 Cuando una instancia de servicio de {{site.data.keyword.streaminganalyticsshort}} se suministra y se enlaza con una aplicación de {{site.data.keyword.Bluemix_notm}}, la instancia del servicio de información VCAP está disponible en el entorno de aplicación de {{site.data.keyword.Bluemix_notm}}. Puede encontrar esta información en la variable de entorno VCAP_SERVICES. Cuando una instancia de servicio de {{site.data.keyword.streaminganalyticsshort}} se suministra sin especificar ninguna aplicación de {{site.data.keyword.Bluemix_notm}} con la que vincularse, se crean automáticamente las credenciales de servicio. Se puede acceder a las credenciales de servicio de {{site.data.keyword.streaminganalyticsshort}} desde el panel de control del servicio.


Las credenciales de servicio de {{site.data.keyword.streaminganalyticsshort}} y la variable de entorno VCAP_SERVICES incluyen información tal como se presenta en el siguiente ejemplo:

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

Para obtener más información sobre la API REST de v1, consulte la [documentación de la API REST de v1 ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://console.ng.bluemix.net/apidocs/220){:new_window}.

## Variable de entorno VCAP_SERVICES para planes de servicio de v2
{: #v2_vcap_services}

Las credenciales de servicio de {{site.data.keyword.streaminganalyticsshort}} y la variable de entorno VCAP_SERVICES para los planes de servicio de v2 incluyen la información de VCAP que debe utilizar para la API REST de {{site.data.keyword.streaminganalyticsshort}} v2. La información de VCAP proporciona el URL REST de v2, el ID de servicio y las credenciales para acceder a la API REST de {{site.data.keyword.streaminganalyticsshort}} v2.  
{:shortdesc}

Las credenciales de servicio de {{site.data.keyword.streaminganalyticsshort}} y la variable de entorno VCAP_SERVICES para los planes de servicio de v2 incluyen información tal como se presenta en el siguiente ejemplo:

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

Para obtener más información sobre la API REST de v2, consulte la [documentación de la API REST de v2 ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://console.ng.bluemix.net/apidocs/1939){:new_window}.
