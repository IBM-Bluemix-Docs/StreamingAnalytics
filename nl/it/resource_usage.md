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


# Utilizzo delle risorse
{: #resourceusage}

{{site.data.keyword.streaminganalyticsshort}} ha diverse modalità di funzionamento e politiche per garantire l'utilizzo e l'assegnazione appropriati delle risorse.

## Visualizzazione e modifica delle risorse dell'istanza
Puoi visualizzare e modificare il numero di risorse autorizzate all'istanza nella pagina dei dettagli del servizio oppure all'API REST v1 per i [piani di servizio v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans). Devi utilizzare l'[API REST {{site.data.keyword.streaminganalyticsshort}} v2](https://{DomainName}/apidocs/streaming-analytics-v2#get-a-streaming-analytics-instance) per i [piani di servizio v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans).

## Assegnazione delle risorse
- Le risorse sono automaticamente assegnate all'istanza quando invii un lavoro che viene eseguito correttamente.
- Le risorse vengono rimosse dall'istanza se nessun lavoro è in esecuzione sulla risorsa. Ad esempio, hai due lavori dove il lavoro 1 è in esecuzione nella risorsa 1 e il lavoro 2 è in esecuzione sia sulla risorsa 1 che sulla 2. Se il lavoro 2 viene annullato, la risorsa 1 rimane nell'istanza mentre la risorsa 2 viene rimossa.
- Quando invii un lavoro, tale lavoro viene posizionato in una nuova risorsa se l'istanza non raggiunge il proprio limite di assegnazione.
- Quando un'istanza utilizza tutte le risorse a cui è autorizzata, i nuovi lavori vengono pianificati sulle risorse esistenti.

## Vincoli della risorsa

I vincoli della risorsa possono essere utilizzati per controllare l'utilizzo e l'assegnazione delle risorse. Ad esempio, utilizzando i vincoli della risorsa puoi specificare che due lavori utilizzino una sola risorsa invece di essere separati su due risorse.
