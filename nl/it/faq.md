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

# Domande frequenti (FAQ)
{: #faq}

## Come mi registro al servizio Streaming Analytics?
{: #signup notoc}  

Per ulteriori informazioni sui piani del servizio {{site.data.keyword.streaminganalyticsshort}}, consulta la [pagina del catalogo {{site.data.keyword.Bluemix_short}}](https://console.bluemix.net/catalog/services/streaming-analytics).

## Quale versione del servizio Streaming Analytics sto utilizzando?
{: #version notoc}   

I miglioramenti vengono distribuiti regolarmente a tutti i servizi {{site.data.keyword.streaminganalyticsshort}}. Utilizzi sempre la versione più recente del servizio gestito e non devi tenere traccia di eventuali versioni o livelli del prodotto.

## Cosa gestisce IBM al mio posto?
{: #ibm_manage notoc}   

Noi gestiamo l'installazione, gli aggiornamenti software, la creazione e la gestione dei domini e la manutenzione hardware. Il servizio include il monitoraggio dell'integrità 24 ore su 24 e 7 giorni su 7.


## Di quali azioni sono responsabile?  
{: #responsible notoc}

Tu scrivi le applicazioni che vengono eseguite in un servizio {{site.data.keyword.streaminganalyticsshort}} e nell'istanza Streams in loco e ti assicuri che stiano funzionando correttamente e soddisfino i requisiti delle prestazioni. Sei anche responsabile di tutto il monitoraggio specifico dell'applicazione.

## L'elevata disponibilità (HA) è supportata?
{: #ha notoc}

L'elevata disponibilità è gestita da IBM. {{site.data.keyword.streaminganalyticsshort}} è configurato per supportare l'elevata disponibilità (HA). Ulteriori risorse server sono implementate nel caso di un failover.

## Come è gestita la sicurezza per il servizio Streaming Analytics?
{: #security notoc}  

La sicurezza è completamente gestita da IBM. Le credenziali sono generate per ogni servizio e ti vengono fornite. Gli aggiornamenti della sicurezza sono gestiti e applicati tempestivamente da IBM come sono disponibili.

## Ho bisogno di configurare un servizio Streaming Analytics?  
{: #configure notoc}

Il servizio viene creato e completamente gestito da IBM. Ogni servizio è composto da una serie dedicata di nodi dell'applicazione.

## Come sviluppo le applicazioni Streams?
{: #streamsapp notoc}

Devi sviluppare le applicazioni Streams in locale utilizzando la [{{site.data.keyword.streamsshort}} Quick Start Edition con Docker ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-install-docker/) gratuita di Streams per i [piani di servizio v2](/docs/services/StreamingAnalytics/service_plans.html) o, se stai utilizzando i [piani di servizio v1](/docs/services/StreamingAnalytics/service_plans.html), puoi scaricare l'[immagine della VM {{site.data.keyword.streamsshort}} Quick Start Edition ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window}.

Puoi anche utilizzare l'installazione di {{site.data.keyword.streamsshort}} in loco se ne disponi. Le applicazioni che sviluppi e compili localmente possono essere perfettamente distribuite come un bundle a un servizio Streams nel cloud.

Ma se desideri eseguire le tue applicazioni Python nel cloud, non hai bisogno di installare {{site.data.keyword.streamsshort}} in loco. Utilizza semplicemente il contesto `STREAMING\_ANALYTICS\_SERVICE` per inviare le tue applicazioni Python al servizio {{site.data.keyword.streaminganalyticsshort}}. Puoi sviluppare le applicazioni in un ambiente di sviluppo Python standard o in un notebook interattivo Jupyter, ma devi utilizzare Python 3.5.

Per ulteriori informazioni sullo sviluppo delle applicazioni, consulta la [{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.streaminganalyticsshort}} Development Guide ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/streamsdev/?p=16589&post_type=doc&preview=1&_ppp=7ad76a418b).

## Possono registrarmi direttamente a un host del servizio Streaming Analytics?
{: #host notoc}  

No. Un accesso diretto al server con Telnet o SSH (Secure Shell) non è supportato. Non puoi installare software aggiuntivo o eseguire un software non Streams su un host Streams.

## Posso accedere al file system in un servizio Streaming Analytics?
{: #filesystem notoc}  

Solo le tue applicazioni Streams possono accedere direttamente al file system in un host Streams.

Esistono alternative pronte per il cloud per le soluzioni che necessitano di un meccanismo per Streams di interagire con gli altri componenti della soluzione. Puoi utilizzare un'altra origine e il sink dei protocolli invece dei file. Ad esempio, archivi di dati basati sul cloud.

## Come le applicazioni del servizio Streaming Analytics possono accedere ai dati aziendali della mia organizzazione?
{: #access notoc}  

Puoi utilizzare il [Servizio Secure Gateway {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/catalog/services/secure-gateway) per collegare in sicurezza le applicazioni Streams alla tua azienda.

## Sono supportate tutte le funzioni di IBM Streams in loco dal servizio Streaming Analytics nel cloud?
{: #features notoc}

Alcune delle funzioni che non sono supportate per il servizio {{site.data.keyword.streaminganalyticsshort}} includono:

  - Le attività di gestione di un'istanza che richiede l'autorità di dominio. Ad esempio, l'aggiunta di tag host personalizzate o la creazione di un gruppo di lavori.
  - I punti di controllo della regione congruente.
  - Alcuni degli operatori del toolkit non sono supportati. Per ulteriori informazioni, vedi [Adattatori e toolkit supportati](/docs/services/StreamingAnalytics/compatible_toolkits.html).
  - L'API Streams JMX.

## Dove posso trovare ulteriori informazioni sul servizio Streaming Analytics?
{: #roadmap notoc}

L'articolo IBM developerWorks®, [Roadmap for {{site.data.keyword.streaminganalyticsshort}} Service on {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/streamsdev/docs/roadmap-for-streaming-analytics-service-on-bluemix/), ha indicazioni sul servizio, con in più link a demo, articoli e blog informativi.
