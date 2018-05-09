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

# Piani di servizio v1 e v2
{: #service_plans}

{{site.data.keyword.streaminganalyticsshort}} è ora in esecuzione su un'infrastruttura basata sui contenitori Kubernetes che fornisce vantaggi di sicurezza e disponibilità al servizio.
{:shortdesc}

Puoi accedere a questa nuova struttura basata sui contenitori utilizzando i piani di servizio v2. Puoi scegliere il piano {{site.data.keyword.streaminganalyticsshort}} che è più adatto per il lavoro che devi eseguire:


<table summary="Questa tabella fornisce un elenco di piani di servizio che puoi utilizzare per creare il tuo servizio {{site.data.keyword.streaminganalyticsshort}}. La tabella elenca tutti i piani di servizio sia per gli insiemi di piani v1 che per quelli v2 e fornisce un elenco di funzioni per ciascun insieme.">
  <tr>
    <th>Insieme di piani di servizio<br></th>
    <th>Nomi del piano<br></th>
    <th>Funzioni disponibili<br></th>
  </tr>
  <tr>
    <td width="15%">
    Piani del servizio v1    
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
        <li>Richiede che tu compili la tua applicazione Streams in un sistema operativo RHEL (Red Hat Enterprise Linux) 6.5 o una versione CentOS equivalente.</li>
        <li>Viene eseguito su un'infrastruttura basata sulle VM.</li>
        <li>Supporta API REST v1 e v2.<br></li>
        <li>Supporta sia l'autenticazione IAM sia l'autenticazione di credenziali utente.</li>
        <li>Supporta l'[immagine della VM {{site.data.keyword.streamsshort}} Quick Start Edition ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-install-vm/)
      </ul>    
    </td>
  </tr>
  <tr>
    <td>
    Piani di servizio v2
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
      <li>Richiede che tu compili la tua applicazione Streams in un sistema operativo RHEL 7.x o una versione CentOS equivalente.</li>
      <li>Viene eseguito su un'infrastruttura basata sui contenitori.</li>
      <li>Supporta le API REST v2.<br></li>
      <li>Supporta l'autenticazione IAM.</li>
      <li>Supporta [{{site.data.keyword.streamsshort}} Quick Start Edition con Docker ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-install-docker/)</li>
      <li>Disponibile solo nella regione Stati Uniti Sud</li>
    </ul>
    </td>
  </tr>
</table>

*Tabella 1. Piani di servizio {{site.data.keyword.streaminganalyticsshort}} v1 e v2*

## Differenze tra i piani di servizio v1 e v2

Le seguenti funzioni sono supportate solo nei piani di servizio v1:

* [API REST v1](https://console.bluemix.net/apidocs/220). Nell'infrastruttura v2, devi utilizzare la [{{site.data.keyword.streaminganalyticsshort}}API REST v2](https://console.bluemix.net/apidocs/1939)
* Applicazioni di esempio v1 NYC Traffic e Event Detection. Consulta [Applicazioni di esempio](/docs/services/StreamingAnalytics/c_starterapps.html) per ottenere un elenco di applicazioni che puoi utilizzare come introduzione a {{site.data.keyword.streaminganalyticsshort}} nell'infrastruttura basata sui contenitori v2.
* Compatibilità di alcuni toolkit. Consulta [Toolkit compatibili](/docs/services/StreamingAnalytics/compatible_toolkits.html) per ottenere un elenco di toolkit compatibili con la nuova infrastruttura basata sui contenitori.

## Variabili di ambiente VCAP_SERVICES per i piani di servizio v1
{: #vcap_services}

Le credenziali di servizio {{site.data.keyword.streaminganalyticsshort}} e la variabile di ambiente VCAP_SERVICES per i piani di servizio v1 includono le informazioni VCAP necessarie per utilizzare la API REST {{site.data.keyword.streaminganalyticsshort}} v1. Le informazioni VCAP forniscono l'URL REST,
l'ID dell'istanza del servizio, l'ID di bind e le credenziali per ogni API REST {{site.data.keyword.streaminganalyticsshort}} v1.  
{:shortdesc}

 Quando un'istanza del servizio {{site.data.keyword.streaminganalyticsshort}} viene fornita e associata a un'applicazione in {{site.data.keyword.Bluemix_notm}}, le informazioni VCAP dell'istanza del servizio sono disponibili nell'ambiente dell'applicazione {{site.data.keyword.Bluemix_notm}} tramite la variabile di ambiente VCAP_SERVICES. Quando un'istanza del servizio {{site.data.keyword.streaminganalyticsshort}}
viene fornita senza specificare un'applicazione in {{site.data.keyword.Bluemix_notm}} a cui eseguire il binding, le credenziali del servizio vengono create automaticamente. È possibile accedere alle credenziali del servizio {{site.data.keyword.streaminganalyticsshort}}
dal dashboard del servizio.


Le credenziali del servizio {{site.data.keyword.streaminganalyticsshort}}
e la variabile di ambiente VCAP_SERVICES includono informazioni come sono presentate nel seguente esempio:

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

Per ulteriori informazioni sulla API REST v1, consulta la [documentazione della API REST v1 ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://console.ng.bluemix.net/apidocs/220){:new_window}.

## Variabili di ambiente VCAP_SERVICES per i piani di servizio v2
{: #v2_vcap_services}

Le credenziali di servizio {{site.data.keyword.streaminganalyticsshort}} e la variabile di ambiente VCAP_SERVICES per i piani di servizio v2 includono le informazioni VCAP necessarie per utilizzare la API REST {{site.data.keyword.streaminganalyticsshort}} v2. Le informazioni VCAP forniscono l'URL REST v2, l'ID servizio e le credenziali per accedere alla API REST {{site.data.keyword.streaminganalyticsshort}} v2.  
{:shortdesc}

Le credenziali di servizio {{site.data.keyword.streaminganalyticsshort}} e la variabile di ambiente VCAP_SERVICES per i piani di servizio v2 includono informazioni come sono presentate nel seguente esempio:

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

Per ulteriori informazioni sulla API REST v2, consulta la [documentazione della API REST v2 ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://console.ng.bluemix.net/apidocs/1939){:new_window}.
