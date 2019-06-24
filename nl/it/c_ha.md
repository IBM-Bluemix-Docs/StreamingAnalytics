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

# Alta disponibilità e ripristino di emergenza 
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} è altamente disponibile all'interno di un'ubicazione {{site.data.keyword.Bluemix_notm}} (ad esempio, Dallas, Washington DC, Londra, Francoforte). Tuttavia, il ripristino da potenziali perdite di dati che interessano un'intera regione {{site.data.keyword.Bluemix_notm}} richiede pianificazione e preparazione.
{:shortdesc}


Sei responsabile della comprensione della configurazione, della personalizzazione e dell'utilizzo del servizio. Sei anche responsabile di essere pronto a ricreare un'istanza del servizio in una nuova ubicazione {{site.data.keyword.Bluemix_notm}} e di ridistribuire le tue applicazioni in tale ubicazione. Vedi [Come garantisco nessun tempo di inattività?](/docs/services/overview?topic=overview-zero-downtime#zero-downtime) per ulteriori informazioni sugli standard di alta disponibilità e ripristino di emergenza in {{site.data.keyword.Bluemix_notm}}. Puoi anche trovare delle informazioni sugli [SLA (Service Level Agreement)](/docs/services/overview?topic=overview-zero-downtime#zero-downtime#SLAs).

## Alta disponibilità (HA) 

{{site.data.keyword.streaminganalyticsshort}} abilita
l'alta disponibilità per le tue applicazioni. Le tue applicazioni vengono distribuite in contenitori Docker eseguiti in cluster Kubernetes. Per scrivere applicazioni altamente disponibili, devi comprendere come questi contenitori possono garantire l'alta disponibilità:

* Le risorse dell'applicazione sono contenitori con CPU e memoria assegnate in base al tuo piano del servizio.
* Durante un malfunzionamento hardware o software, i contenitori possono essere spostati. Quando i contenitori vengono spostati, gli elementi elaborati vengono riavviati. 
* Durante la manutenzione pianificata, i contenitori possono essere spostati (gli elementi elaborati vengono riavviati).

Pertanto, quando scrivi le tue applicazioni, devi tenere presente che occasionalmente i contenitori possono essere spostati. Inoltre, considera i seguenti elementi:
* Assicurati che gli elementi elaborati (PE) siano riavviabili e riassegnabili.
* Assicurati che la tua applicazione possa tollerare il riavvio di alcuni o di tutti i propri elementi elaborati (PE), in qualsiasi ordine.
* Assicurati che gli operatori di origine e sink nella tua applicazione Streams siano configurati per ristabilire le connessioni quando vengono riavviati i loro PE.

Consulta la [{{site.data.keyword.streaminganalyticsshort}} development guide](https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/#troubleshooting) per degli esempi su come risolvere i problemi con la tua applicazione.

Per implementare l'alta disponibilità, le applicazioni Streams sono abilitate a garantire l'elaborazione di tutte le tuple. Per ottenere l'elaborazione tuple garantita, viene periodicamente stabilito un checkpoint per tutti gli operatori in una regione congruente. Quando un'applicazione ha un malfunzionamento, sarà eseguito il rollback di tutti gli operatori agli ultimi stati con un checkpoint valido.
{{site.data.keyword.streaminganalyticsshort}} consente di utilizzare regioni congruenti.

### Elaborazione tuple garantita 
Per i requisiti di business, alcune applicazioni richiedono che tutte le tuple vengano elaborate almeno una volta. {{site.data.keyword.streamsshort}} è stato migliorato con operatori e annotazioni che consentono la definizione di una regione che non perde tuple durante l'elaborazione dei flussi. Le tuple in una regione congruente vengono elaborate almeno una volta.

Se viene rilevato un malfunzionamento all'interno di una regione congruente, {{site.data.keyword.streaminganalyticsshort}} può riportare l'applicazione all'ultimo stato congruente (anche noto come checkpoint) e indirizzare le origini dati dell'applicazione a rispondere alle tuple da quel punto.

Puoi eseguire e monitorare le applicazioni Streams con le regioni congruenti definite in {{site.data.keyword.streaminganalyticsshort}}. Quando crei un servizio{{site.data.keyword.streaminganalyticsshort}}, l'istanza è già configurata per consentire di utilizzare le regioni congruenti.

Una regione congruente è un sottografico in cui gli stati degli operatori diventano congruenti elaborando tutte le tuple e i segni di punteggiatura nei punti definiti di un flusso. Questo abilita le tuple all'interno del sottografico ad essere elaborate almeno una volta. La regione congruente viene periodicamente svuotata delle proprie tuple correnti. Tutte le tuple nella regione congruente vengono elaborate fino alla fine del sottografico. Lo stato in memoria degli operatori viene automaticamente serializzato e archiviato nel checkpoint di ognuno degli operatori nella regione.

Puoi ora scrivere applicazioni Java, SPL e Python che hanno l'elaborazione tuple garantita e distribuire queste applicazioni in {{site.data.keyword.streaminganalyticsshort}}.

Puoi definire l'inizio di una regione congruente con l'annotazione `@consistent` su un operatore idoneo. {{site.data.keyword.streamsshort}} determina l'ambito della regione congruente automaticamente, ma puoi modificare l'operatore finale della regione con l'annotazione `@autonomous`. La regione congruente definita stabilisce periodicamente uno stato congruente.

Controlla la [documentazione {{site.data.keyword.streamsshort}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html) per ulteriori dettagli sull'utilizzo delle regioni congruenti nelle applicazioni Streams.

## Ripristino di emergenza 
{{site.data.keyword.streaminganalyticsshort}} è un servizio GA offerto in più regioni {{site.data.keyword.Bluemix_notm}}. {{site.data.keyword.streaminganalyticsshort}} non archivia i dati dell'utente su {{site.data.keyword.Bluemix_notm}}.

In base ai tuoi requisiti di business, seleziona una delle seguenti strategie di ripristino di emergenza:
* Se richiedi che non ci siano interruzioni con la tua applicazione:
  1. Crea le istanze di {{site.data.keyword.streaminganalyticsshort}} in più regioni {{site.data.keyword.Bluemix_notm}}.
  2. Invia la tua applicazione a più regioni.


* Se richiedi un'interruzione minima della tua applicazione:
  1. Crea le istanze di {{site.data.keyword.streaminganalyticsshort}} in più regioni {{site.data.keyword.Bluemix_notm}}.
  2. Monitora la tua applicazione utilizzando l'[API REST del servizio](https://ibm.co/2Gt9mB6) e sposta in modo dinamico il tuo carico di lavoro in una nuova regione se necessario.

**Nota**: ogni regione congruente è collegata a una regione {{site.data.keyword.Bluemix_notm}}. In uno scenario di ripristino di emergenza, le regioni congruenti in un'applicazione non hanno alcun ruolo.
