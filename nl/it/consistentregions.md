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


# Miglioramenti per l'alta disponibilità 
{: #consistentregions}

Per i requisiti di business, alcune applicazioni richiedono che tutte le tuple vengano elaborate almeno una volta. {{site.data.keyword.streamsshort}} è stato migliorato con operatori e annotazioni che consentono la definizione di una regione che non perde tuple durante l'elaborazione dei flussi. Le tuple in una regione coerente vengono elaborate almeno una volta. 


Se utilizzi i piani dei prezzi Beta-Entry o Beta-Enhanced, puoi ora eseguire e monitorare le applicazioni Streams con le regioni coerenti definite in  {{site.data.keyword.streaminganalyticsshort}}. Quando crei un servizio {{site.data.keyword.streaminganalyticsshort}} con i piani Beta-Entry o Beta-Enhanced, l'istanza è già configurata per utilizzare le regioni coerenti.

Una regione coerente è un sottografico in cui gli stati degli operatori diventano coerenti elaborando tutte le tuple e i segni di punteggiatura nei punti definiti di un flusso. Questo abilita le tuple all'interno del sottografico ad essere elaborate almeno una volta. La regione coerente viene periodicamente svuotata delle proprie tuple correnti. Tutte le tuple nella regione coerente vengono elaborate fino alla fine del sottografico. Lo stato in memoria degli operatori viene automaticamente serializzato e archiviato nel punto di controllo di ognuno degli operatori nella regione.

Puoi ora scrivere sia le applicazioni Java che SPL che hanno l'elaborazione tuple garantita e distribuire queste applicazioni in {{site.data.keyword.streaminganalyticsshort}}.

Puoi definire l'inizio di una regione coerente con l'annotazione `@consistent` su un operatore idoneo. {{site.data.keyword.streamsshort}} determina l'ambito della regione coerente automaticamente, ma puoi modificare l'operatore finale della regione con l'annotazione `@autonomous`. La regione coerente definita stabilisce periodicamente uno stato coerente.

Controlla la [documentazione {{site.data.keyword.streamsshort}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.1/com.ibm.streams.dev.doc/doc/consistentregions.html) per ulteriori dettagli sull'utilizzo delle regioni coerenti nelle applicazioni Streams.
