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

# Plans de service versions 1 et 2
{: #service_plans}

{{site.data.keyword.streaminganalyticsshort}} s'exécute désormais sur une infrastructure basée sur un conteneur Kubernetes, qui fournit des avantages au service en matière de sécurité et de disponibilité.
{:shortdesc}

Vous pouvez accéder à cette nouvelle infrastructure basée sur un conteneur à l'aide des plans de service version 2. Vous pouvez choisir le plan {{site.data.keyword.streaminganalyticsshort}} le mieux adapté au travail à effectuer : 


<table summary="Ce tableau fournit une liste des plans de service que vous pouvez utiliser pour créer votre service {{site.data.keyword.streaminganalyticsshort}}. Il répertorie tous les plans de service pour les ensembles de plans versions 1 et 2, et fournit une liste de fonctions pour chaque ensemble.">
  <tr>
    <th>Ensemble de plans de service<br></th>
    <th>Noms de plan<br></th>
    <th>Fonctions disponibles<br></th>
  </tr>
  <tr>
    <td width="15%">
    Plans de service version 1    
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
        <li>Requiert la compilation de votre application Streams sur un système d'exploitation Red Hat Enterprise Linux (RHEL) 6.5 ou une version CentOS équivalente. </li>
        <li>S'exécute sur une infrastructure basée sur une machine virtuelle. </li>
        <li>Prend en charge les API REST versions 1 et 2. <br></li>
        <li>Prend en charge à la fois l'authentification IAM et l'authentification des données d'identification de l'utilisateur. </li>
        <li>Prend en charge l'[image de machine virtuelle {{site.data.keyword.streamsshort}} Quick Start Edition ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-install-vm/)
      </ul>    
    </td>
  </tr>
  <tr>
    <td>
    Plans de service version 2
    </td>
    <td>
      <ul>
        <li>Lite</li>
        <li>Entry Container Hourly</li>
        <li>Entry Container Monthly</li>
        <li>Enhanced Container Hourly</li>
        <li>Enhanced Container Monthly</li>
        <li>Premium Container Hourly</li>
        <li>Premium Container Monthly</li>
      </ul>
    </td>
    <td>
    <ul>
      <li>Requiert la compilation de votre application Streams sur un système d'exploitation RHEL 7.x ou une version CentOS équivalente. </li>
      <li>S'exécute sur une infrastructure basée sur un conteneur. </li>
      <li>Prend en charge les API REST version 2. <br></li>
      <li>Prend en charge l'authentification IAM. </li>
      <li>Prend en charge [{{site.data.keyword.streamsshort}} Quick Start Edition avec Docker ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-install-docker/)</li>
      <li>Disponible uniquement dans la région Sud des Etats-Unis</li>
    </ul>
    </td>
  </tr>
</table>

*Tableau 1. Plans de service {{site.data.keyword.streaminganalyticsshort}} versions 1 et 2*

## Différences entre les plans de service versions 1 et 2

Les fonctions suivantes sont uniquement prises en charge dans les plans de service version 1 : 

* [API REST v1](https://console.bluemix.net/apidocs/220). Dans l'infrastructure v2, vous devez utiliser l'[API REST {{site.data.keyword.streaminganalyticsshort}} v2](https://console.bluemix.net/apidocs/1939).
* Modèles d'application NYC Traffic et Event Detection v1. Voir [Modèles d'application](/docs/services/StreamingAnalytics/c_starterapps.html) pour obtenir la liste des applications que vous pouvez utiliser pour démarrer {{site.data.keyword.streaminganalyticsshort}} dans l'infrastructure basée sur un conteneur version 2. 
* Compatibilité de certains kits d'outils. Voir [Kit d'outils compatibles](/docs/services/StreamingAnalytics/compatible_toolkits.html) pour obtenir la liste des kits d'outils qui sont compatibles avec la nouvelle infrastructure basée sur un conteneur. 

## Variable d'environnement VCAP_SERVICES pour les plans de service version 1
{: #vcap_services}

Les données d'identification de service {{site.data.keyword.streaminganalyticsshort}} et la variable d'environnement VCAP_SERVICES pour les plans de service version 1 incluent les informations VCAP qui sont requises pour utiliser l'API REST {{site.data.keyword.streaminganalyticsshort}} v1. Les informations VCAP fournissent l'URL REST, l'ID instance de service, l'ID liaison et les données d'identification pour chaque API REST {{site.data.keyword.streaminganalyticsshort}} v1.   
{:shortdesc}

 Quand une instance de service {{site.data.keyword.streaminganalyticsshort}} est provisionnée et liée à une application dans {{site.data.keyword.Bluemix_notm}}, les informations VCAP d'instance de service sont disponibles dans l'environnement d'application {{site.data.keyword.Bluemix_notm}} via la variable d'environnement VCAP_SERVICES. Quand une instance de service {{site.data.keyword.streaminganalyticsshort}} est provisionnée sans spécification d'une application dans {{site.data.keyword.Bluemix_notm}} à laquelle se lier, les données d'authentification de service sont automatiquement créées. Les données d'authentification de service {{site.data.keyword.streaminganalyticsshort}} sont accessibles depuis le tableau de bord de service.


Les données d'identification de service {{site.data.keyword.streaminganalyticsshort}} et la variable d'environnement VCAP_SERVICES incluent des informations, comme celles présentées dans l'exemple suivant :

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

Pour plus d'informations sur l'API REST v1, voir la [documentation sur l'API REST v1 ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://console.ng.bluemix.net/apidocs/220){:new_window}.

## Variable d'environnement VCAP_SERVICES pour les plans de service version 2
{: #v2_vcap_services}

Les données d'identification de service {{site.data.keyword.streaminganalyticsshort}} et la variable d'environnement VCAP_SERVICES pour les plans de service version 2 incluent les informations VCAP qui sont requises pour utiliser l'API REST {{site.data.keyword.streaminganalyticsshort}} v2. Les informations VCAP fournissent l'URL REST v2, l'ID de service et les  données d'identification pour accéder à l'API REST {{site.data.keyword.streaminganalyticsshort}} v2.   
{:shortdesc}

Les données d'identification de service {{site.data.keyword.streaminganalyticsshort}} et la variable d'environnement VCAP_SERVICES pour les plans de service version 2 incluent des informations, comme celles présentées dans l'exemple suivant :

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

Pour plus d'informations sur l'API REST v2, voir la [documentation sur l'API REST v2 ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://console.ng.bluemix.net/apidocs/1939){:new_window}.
