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


# Utilizzo delle risorse
{: #resourceusage}

{{site.data.keyword.streaminganalyticsshort}} ha diverse modalità di funzionamento e politiche per garantire l'utilizzo e l'assegnazione appropriati delle risorse. 

## Visualizzazione e modifica delle risorse dell'istanza
Puoi visualizzare e modificare il numero di risorse dell'istanza nel dashboard del servizio o utilizzare l'[API REST v2 {{site.data.keyword.streaminganalyticsshort}}](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#get-a-streaming-analytics-instance).

## Assegnazione delle risorse 
- Le risorse sono automaticamente assegnate all'istanza quando invii un lavoro che viene eseguito correttamente.
- Le risorse vengono rimosse dall'istanza se nessun lavoro è in esecuzione nella risorsa. Ad esempio, hai due lavori dove il lavoro 1 è in esecuzione nella risorsa 1 e il lavoro 2 è in esecuzione sia sulla risorsa 1 che sulla 2. Se il lavoro 2 viene annullato, la risorsa 1 rimane nell'istanza mentre la risorsa 2 viene rimossa.
- Quando invii un lavoro, tale lavoro viene posizionato in una nuova risorsa se l'istanza non ha raggiunto il proprio limite di assegnazione.
- Quando un'istanza sta utilizzando tutte le proprie risorse, vengono pianificati dei nuovi lavori nelle risorse esistenti.

## Vincoli della risorsa 

I vincoli della risorsa possono essere utilizzati per controllare l'utilizzo e l'assegnazione delle risorse. Ad esempio, utilizzando i vincoli della risorsa puoi specificare che due lavori utilizzino una sola risorsa invece di essere separati su due risorse.
