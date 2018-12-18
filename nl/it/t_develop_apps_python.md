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

# Sviluppo delle applicazioni Python in Streaming Analytics
{: #t_develop_apps_python}

Puoi ora sviluppare applicazioni Python in {{site.data.keyword.DSX_full}} oppure nel tuo ambiente di sviluppo Python locale e distribuire queste applicazioni in {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

Sviluppa e distribuisci le tue applicazioni Python in {{site.data.keyword.Bluemix_short}} con il servizio {{site.data.keyword.streaminganalyticsshort}} con uno di questi metodi:


## Sviluppo di applicazioni Streams Python in Watson Studio
{: #t_develop_python_dsx}

Se non hai un ambiente di sviluppo Python, il modo più semplice per iniziare è utilizzare i notebook {{site.data.keyword.streamsshort}} in {{site.data.keyword.DSX_short}} e creare delle applicazioni Python di esempio. Questi notebook forniscono la procedura e gli esempi di codice per creare e distribuire delle semplici applicazioni Python per il servizio {{site.data.keyword.streaminganalyticsshort}} nell'ambiente Python {{site.data.keyword.DSX_short}}:

* [Hello World! ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039ca9c6e8): crea una semplice applicazione Hello World! per iniziare e poi distribuisci l'applicazione a un'istanza del servizio {{site.data.keyword.streaminganalyticsshort}}.

* [Healthcare Demo ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039cad29a6): crea un'applicazione che integra e analizza i dati di gestione flussi da un feed e visualizza quindi i dati nel notebook. Invii infine questa applicazione all'istanza del servizio {{site.data.keyword.streaminganalyticsshort}}.

* [Neural Net Demo ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039ca60bb7): Crea un dataset di esempio, crea un modello di dati, utilizza tale modello in un'applicazione di gestione flussi, visualizza i dati di gestione flussi e invia l'applicazione di gestione flussi al servizio.

## Sviluppo di applicazioni nel tuo ambiente Python locale
 {: #t_develop_python_api}

Con la [API dell'applicazione Phyton {{site.data.keyword.streamsshort}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features), che è inclusa nel pacchetto streamsx, puoi creare delle applicazioni di elaborazione della gestione flussi con le funzioni e le classi richiamabili Python. Puoi utilizzare l'API dell'applicazione Python per definire, e quindi inviare, l'applicazione al servizio.

Inizia attenendoti alla procedura nell'esercitazione [Developing for the {{site.data.keyword.streaminganalyticsshort}} service ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html). In questa esercitazione, crei un'applicazione di esempio nel tuo ambiente Python locale e la distribuisci al servizio {{site.data.keyword.streaminganalyticsshort}}.

Per maggiori informazioni sull'{{site.data.keyword.streamsshort}}API dell'applicazione Python, completa [questo corso online ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/courses/all/streaming-analytics-basics-python-developers/){:new_window} e impara le basi {{site.data.keyword.streaminganalyticsshort}} per gli sviluppatori Python.
