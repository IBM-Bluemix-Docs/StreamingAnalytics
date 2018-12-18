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

# Distribuzione delle applicazioni Streams al cloud
{: #t_deploytocloud}

Puoi distribuire le tue applicazioni {{site.data.keyword.streamsshort}} all'istanza {{site.data.keyword.streaminganalyticsshort}} in esecuzione in {{site.data.keyword.Bluemix_short}}.
{:shortdesc}

Le applicazioni {{site.data.keyword.streamsshort}} sono scritte in SPL ({{site.data.keyword.streamsshort}} Processing Language), SPL, Java, Scala o Python in un ambiente {{site.data.keyword.streamsshort}}. Puoi ora sviluppare applicazioni Streams Python senza un ambiente {{site.data.keyword.streamsshort}}. Vedi [Distribuzione di applicazioni {{site.data.keyword.streamsshort}} nel cloud](/docs/services/StreamingAnalytics/t_deploytocloud.html#t_deploypython)


{{site.data.keyword.streaminganalyticsshort}} non include un ambiente di sviluppo
{{site.data.keyword.streamsshort}} nel
cloud, ma puoi distribuire le applicazioni che sviluppi localmente al cloud.

Prima di iniziare, disabilita il Blocco popup del tuo browser per visualizzare la console {{site.data.keyword.streaminganalyticsshort}}.

Per distribuire le tue applicazioni {{site.data.keyword.streamsshort}}
al cloud:

1. Configura il tuo ambiente per lo sviluppo e la verifica della tua applicazione.

	Se vuoi utilizzare un ambiente {{site.data.keyword.streamsshort}}, puoi scaricare [{{site.data.keyword.streamsshort}} Quick Start Edition ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window} per i [piani di servizio v1](/docs/services/StreamingAnalytics/service_plans.html). Utilizza [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi){:new_window} per i [piani di servizio v2](/docs/services/StreamingAnalytics/service_plans.html).

2. Sviluppa la tua applicazione di gestione flussi nel tuo ambiente di sviluppo. Nell'ambiente di sviluppo {{site.data.keyword.streamsshort}}, puoi utilizzare Streams Studio o gli strumenti di riga di comando per sviluppare la tua applicazione.

3. Verifica che la tua applicazione di gestione flussi venga eseguita correttamente nel tuo ambiente di sviluppo.
**Nota:** devi compilare le tue applicazioni in RHEL (Red Hat Enterprise Linux) 7.x se stai utilizzando i piani di servizio v2 o con RHEL 6.5 se stai utilizzando i piani di servizio v1.

4. Invia il bundle dell'applicazione (file .sab) associato alla tua applicazione SPL, Java, Scala o Python alla tua istanza del servizio nel cloud utilizzando uno dei seguenti metodi:
	* Utilizza la console {{site.data.keyword.streaminganalyticsshort}}
per inviare il bundle dell'applicazione.

  * Crea un'applicazione in {{site.data.keyword.Bluemix_notm}} e aggiungi l'applicazione {{site.data.keyword.streamsshort}} ad essa. Eseguine il controllo utilizzando l'[API REST {{site.data.keyword.streaminganalyticsshort}} v1 ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} per i [piani di servizio v1](/docs/services/StreamingAnalytics/service_plans.html) oppure la [API REST {{site.data.keyword.streaminganalyticsshort}} v2![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window} per i piani di servizio v2.

La tua applicazione è ora distribuita nel cloud. Puoi monitorarla nel servizio {{site.data.keyword.streaminganalyticsshort}}. Puoi inoltre inviare più di un'applicazione (file .sab) alla tua istanza del servizio. Puoi inviarne quante desideri.

{{site.data.keyword.streamsshort}} supporta inoltre diversi kit di sviluppo Java™ che puoi utilizzare per sviluppare le tue applicazioni. Per ulteriori informazioni sul supporto Java in  {{site.data.keyword.streamsshort}}, consulta [Supported Java development kits for application development ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.install.doc/doc/ibminfospherestreams-install-prerequisites-java-supported-sdks.html){:new_window}.

## Distribuzione delle applicazioni Streams Python al cloud
{: #t_deploypython}

Distribuisci le tue applicazioni {{site.data.keyword.streamsshort}} Python a un servizio {{site.data.keyword.streaminganalyticsshort}} in esecuzione in {{site.data.keyword.Bluemix_short}}. Non hai bisogno di avere un'installazione di {{site.data.keyword.streamsshort}}.
{:shortdesc}

Con la [API dell'applicazione Python {{site.data.keyword.streamsshort}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features){:new_window}, che è inclusa nel pacchetto streamsx, puoi distribuire le applicazioni Python al servizio {{site.data.keyword.streaminganalyticsshort}}. Consulta l'esercitazione [Developing for the {{site.data.keyword.streaminganalyticsshort}} service ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html){:new_window} per ottenere un esempio di come creare e distribuire una semplice applicazione Python per il servizio {{site.data.keyword.streaminganalyticsshort}}.

{{site.data.keyword.DSX_full}} supporta anche l'invio di applicazioni Python nei notebook interattivi Jupyter. Per ulteriori informazioni, consulta [Sviluppo di applicazioni Python per {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/t_develop_apps_python.html).
