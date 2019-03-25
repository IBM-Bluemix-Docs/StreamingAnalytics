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

# Streaming Analytics ad alta disponibilità
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} abilita
l'alta disponibilità per le tue applicazioni. Se viene rilevato un problema su uno dei nodi della tua applicazione,
(risorse {{site.data.keyword.streamsshort}}), il nodo viene
automaticamente sostituito e ogni lavoro in esecuzione su tale nodo viene migrato. I lavori vengono migrati e riavviati
solo se l'istanza contiene più nodi di applicazione. Puoi ridimensionare l'istanza utilizzando la [pagina dei dettagli del servizio](/docs/services/StreamingAnalytics?topic=dashboard) oppure l'[API REST {{site.data.keyword.streaminganalyticsshort}} v1 ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} per i [piani di servizio v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans). Per i piani di servizio v2, utilizza l'[API REST v2 ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window}
{:shortdesc}

Questo video mostra come ridimensionare la tua istanza utilizzando la pagina dei dettagli del servizio:

<iframe width="560" height="315" title="Ridimensiona istanza" src="https://www.youtube.com/embed/zbZ9am9UhPw?rel=0" frameborder="0" allowfullscreen>Ridimensiona istanza</iframe>

## Regioni congruenti
Per i requisiti di business, alcune applicazioni richiedono che tutte le tuple vengano elaborate almeno una volta. {{site.data.keyword.streamsshort}} è stato migliorato con operatori e annotazioni che consentono la definizione di una regione che non perde tuple durante l'elaborazione dei flussi. Le tuple in una regione congruente vengono elaborate almeno una volta.

Puoi eseguire e monitorare le applicazioni Streams con le regioni congruenti definite in {{site.data.keyword.streaminganalyticsshort}}. Quando crei un servizio{{site.data.keyword.streaminganalyticsshort}}, l'istanza è già configurata per utilizzare le regioni congruenti.

Una regione congruente è un sottografico in cui gli stati degli operatori diventano congruenti elaborando tutte le tuple e i segni di punteggiatura nei punti definiti di un flusso. Questo abilita le tuple all'interno del sottografico ad essere elaborate almeno una volta. La regione congruente viene periodicamente svuotata delle proprie tuple correnti. Tutte le tuple nella regione congruente vengono elaborate fino alla fine del sottografico. Lo stato in memoria degli operatori viene automaticamente serializzato e archiviato nel punto di controllo di ognuno degli operatori nella regione.

Puoi ora scrivere sia le applicazioni Java che SPL che hanno l'elaborazione tuple garantita e distribuire queste applicazioni in {{site.data.keyword.streaminganalyticsshort}}.

Puoi definire l'inizio di una regione congruente con l'annotazione `@consistent` su un operatore idoneo. {{site.data.keyword.streamsshort}} determina l'ambito della regione congruente automaticamente, ma puoi modificare l'operatore finale della regione con l'annotazione `@autonomous`. La regione congruente definita stabilisce periodicamente uno stato congruente.

Controlla la [documentazione {{site.data.keyword.streamsshort}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html) per ulteriori dettagli sull'utilizzo delle regioni congruenti nelle applicazioni Streams.
