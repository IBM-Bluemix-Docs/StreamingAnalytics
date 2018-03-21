---

copyright:
  years: 2015, 2018
lastupdated: "2018-02-14"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Piani Beta-Entry e Beta-Enhanced
{: #beta_plans}

I nuovi piani Beta-Entry e Beta-Enhanced del servizio {{site.data.keyword.streaminganalyticsshort}} includono diversi miglioramenti e differenze rispetto ai piani di servizio esistenti:
{:shortdesc}

**Nuova [{{site.data.keyword.streamsshort}} QSE per Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi):** la Quick Start Edition {{site.data.keyword.streamsshort}} è una versione gratuita, non per la produzione di {{site.data.keyword.streamsshort}}. Per utilizzare i piani Beta-Entry e Beta-Enhanced per distribuire le applicazioni a {{site.data.keyword.streaminganalyticsshort}}, devi compilare le tue applicazioni utilizzando la versione RHEL (Red Hat Enterprise Linux) 7 della QSE {{site.data.keyword.streamsshort}}.
Controlla la [Beta Development Guide ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/streamsdev/docs/cloud-beta-devguide/) per informazioni su come utilizzare la nuova Streams QSE con RHEL 7 in esecuzione su un ambiente Docker per compilare e distribuire le tue applicazioni con i nuovi piani beta {{site.data.keyword.streaminganalyticsshort}}.   

**API REST v2 {{site.data.keyword.streaminganalyticsshort}}:** puoi utilizzare l'[API REST v2 {{site.data.keyword.streaminganalyticsshort}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#introduction) per gestire le tue istanze del servizio e i lavori {{site.data.keyword.streamsshort}}. L'API v2 {{site.data.keyword.streaminganalyticsshort}} è supportata solo per le istanze del servizio create con uno dei nuovi piani beta. L'[API REST v1 ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/apidocs/220-streaming-analytics?&language=node#introduction) è supportata solo per le istanze {{site.data.keyword.streaminganalyticsshort}} esistenti e per tutte le nuove istanze che crei con i piani del servizio esistenti.

**Nuove applicazioni starter e di esempio:** poiché i nuovi piani beta richiedono l'esecuzione di Streams su RHEL 7, molte delle applicazioni di esempio esistenti non funzionano con i nuovi piani beta. {{site.data.keyword.streaminganalyticsshort}} fornisce una [nuova serie di applicazioni starter e di esempio]( https://developer.ibm.com/streamsdev/docs/cloud-beta-samples/) per farti iniziare ad utilizzare velocemente i nuovi piani beta.

**Miglioramenti per l'alta disponibilità:** evita la perdita di dati nelle applicazioni di elaborazione dei flussi definendo regioni coerenti. {{site.data.keyword.streamsshort}} è stato migliorato con operatori e annotazioni che consentono la definizione di una regione che non perde tuple durante l'elaborazione dei flussi. Le tuple in una regione coerente vengono elaborate almeno una volta.
Se utilizzi i piani dei prezzi Beta-Entry o Beta-Enhanced, puoi ora eseguire e monitorare le applicazioni Streams con [regioni coerenti definite in {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/consistentregions.html).

**Nuove funzioni di determinazione del problema:** i piani Beta-Entry e Beta-Enhanced includono diversi miglioramenti per aiutarti a trovare e correggere velocemente gli errori nelle tue applicazioni. Per ulteriori informazioni, consulta [La console {{site.data.keyword.streaminganalyticsshort}} ti fornisce ulteriori modi di trovare e correggere gli errori (piani beta) ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno").](https://wp.me/p4IICn-4cx)

**Monitoraggio di come gli operatori si comportano e dell'elaborazione tuple garantita nel cloud:** {{site.data.keyword.streamsshort}} fornisce metriche per aiutarti a valutare l'integrità dei servizi {{site.data.keyword.streamsshort}}, come ausilio nella diagnosi dei problemi delle prestazioni e per analizzare la velocità effettiva delle richieste. Puoi utilizzare la console di Streams in {{site.data.keyword.streaminganalyticsshort}} per [monitorare come gli operatori si comportano e garantire l'ottimizzazione della risorsa ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno").](https://wp.me/p4IICn-4bH)
