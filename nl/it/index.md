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


# Panoramica su Streaming Analytics
{: #gettingstarted}

{{site.data.keyword.streaminganalyticsfull}} è fornito da
{{site.data.keyword.streamsshort}}, una piattaforma di analisi avanzata
che puoi utilizzare per inserire, analizzare e correlare le informazioni come arrivano da diversi tipi
di origini dati in tempo reale. Quando crei un'istanza del servizio {{site.data.keyword.streaminganalyticsshort}}, ottieni la tua propria istanza {{site.data.keyword.streamsshort}} in esecuzione in {{site.data.keyword.Bluemix_short}}, pronta per eseguire le tue applicazioni {{site.data.keyword.streamsshort}}.
{:shortdesc}

Inizia a utilizzare subito {{site.data.keyword.streaminganalyticsshort}} eseguendo le [applicazioni starter](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps_deploy){:new_window}.

Per iniziare a utilizzare {{site.data.keyword.streaminganalyticsshort}}, usa uno dei seguenti metodi per inviare il bundle dell'applicazione (file .sab) associato alla tua applicazione SPL, Java™, Python o Scala Streams:
* Usa il pulsante **Invia lavoro** nella console {{site.data.keyword.streaminganalyticsshort}}.
* Sviluppa un'applicazione in {{site.data.keyword.Bluemix_notm}} e aggiungi l'applicazione {{site.data.keyword.streamsshort}} ad essa. Eseguine il controllo utilizzando l'[API REST {{site.data.keyword.streaminganalyticsshort}} v1 ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} per i [piani di servizio v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) oppure la [API REST {{site.data.keyword.streaminganalyticsshort}} v2![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window} per i piani di servizio v2.

Utilizza {{site.data.keyword.streaminganalyticsshort}} con altri servizi, incluso {{site.data.keyword.cloudant}}. Consulta le [Esercitazioni per l'integrazione con altri servizi {{site.data.keyword.Bluemix_short}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-tutorials){:new_window} per gli esempi che ti renderanno subito operativo.

Se vuoi fare ancora di più con le tue applicazioni, puoi ottenere un ambiente di sviluppo {{site.data.keyword.streamsshort}} e devi preparare la tua applicazione per il cloud. Se non hai un ambiente {{site.data.keyword.streamsshort}}, puoi scaricare [{{site.data.keyword.streamsshort}} Quick Start Edition con Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) per i [piani di servizio v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) o, se stai utilizzando i [piani di servizio v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans), puoi scaricare l'[immagine della VM {{site.data.keyword.streamsshort}} Quick Start Edition ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}.

Se non hai familiarità con la distribuzione dell'applicazione {{site.data.keyword.streamsshort}}, sono presenti delle risorse per aiutarti nell'apprendimento. Per ulteriori informazioni, consulta [{{site.data.keyword.streamsshort}} Knowledge Center ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.welcome.doc/doc/kc-homepage.html){:new_window}

Se già disponi di un'applicazione SPL che esegui in loco, devi [preparare la tua applicazione per il cloud.![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/streamsdev/docs/getting-spl-application-ready-cloud/){:new_window}

**Nota:** devi compilare le tue applicazioni in RHEL (Red Hat Enterprise Linux) 7.x se stai utilizzando i piani di servizio v2 o con RHEL 6.5 se stai utilizzando i piani di servizio v1.
