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

# Applicazioni di esempio
{: #starterapps}

Distribuisci e modifica le applicazioni starter e impara velocemente come utilizzare il servizio {{site.data.keyword.streaminganalyticsshort}}. Nota: i piani di servizio v2 richiedono l'esecuzione di Streams su RHEL 7. {{site.data.keyword.streaminganalyticsshort}} fornisce un [insieme di applicazioni starter e di esempio](https://developer.ibm.com/streamsdev/docs/starter-sample-apps-v2-plans/) per offrirti una rapida introduzione ai piani di servizio v2. Le applicazioni di esempio EventDetection e NYCTraffic non funzionano con i piani di servizio v2.
{:shortdesc}


<table summary="Questa tabella descrive, nella prima riga, l'applicazione starter Stock Trades. La tabella include nella seconda riga:
1. Nella prima colonna, un link a un video su come distribuire l'applicazione starter Stock Trades. 2. Nella seconda colonna, un link per scaricare direttamente l'applicazione starter Stock Trades.
 ">
  <tr>
    <th id="stocktrades" colspan="3">Applicazione di esempio Stock Trades<br></th>
  </tr>
  <tr>
    <td headers="stocktrades" colspan="3">Questa applicazione analizza un flusso di quotazioni titolo e produce una media mobile dei prezzi utilizzando l'operatore <a href="https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$spl/op$spl.relational$Aggregate.html">Aggregate ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a>.
Puoi eseguire l'applicazione starter senza alcuna modifica. Se vuoi provare con un altro servizio, puoi anche modificare
il codice e rimandare le tue modifiche all'ambiente {{site.data.keyword.Bluemix_short}} . L'origine completa dell'applicazione starter è <a href="https://github.com/IBMStreams/samples/tree/master/QuickStart/TradesApp">disponibile in GitHub ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a>.</p>
</td>
  </tr>
  <tr>
    <td headers="stocktrades"><a href="https://developer.ibm.com/streamsdev/videos/getting-started-streaming-analytics-service-using-trades-starter-application/" target="_blank">DISTRIBUISCI L'APPLICAZIONE ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a><br></td>
    <td headers="stocktrades"><a href="https://github.com/IBMStreams/samples/raw/master/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab" target="_blank">SCARICA ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a></td>
  </tr>
</table>

*Tabella 1. Applicazione di esempio Stock Trades*


<table summary="Questa tabella descrive, nella prima riga, l'applicazione di esempio Event Detection v2. La tabella include nella seconda riga:
1. Nella prima colonna, un link alle istruzioni relative alla modalità di distribuzione dell'applicazione starter Event Detection v2. 2. Nella seconda colonna, un link alle esercitazioni relative alla modalità di utilizzo dell'applicazione starter Event Detection. 3. Nella terza colonna, un link per scaricare direttamente l'applicazione starter Event Detection.
 ">
  <tr>
    <th id="EventDetection2" colspan="3">Applicazione di esempio Event Detection v2<br></th>
  </tr>
  <tr>
    <td colspan="3" headers="EventDetection2">L'applicazione Event Detection v2 è implementata con il runtime <a href="https://{DomainName}/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">SDK for Node.js ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a>. Questa applicazione starter è compatibile solo con i [piani di servizio v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans).
L'applicazione
fornisce una IU web di esempio per visualizzare lo stato e i risultati delle analisi.
L'applicazione Node.js è associata a un'istanza del servizio {{site.data.keyword.streaminganalyticsshort}}. L'applicazione controlla il servizio tramite l'API REST {{site.data.keyword.streaminganalyticsshort}} v2.
<p>Puoi eseguire l'applicazione starter senza alcuna modifica.
Se vuoi provare con un altro servizio, puoi anche modificare il codice e rimandare le tue modifiche all'ambiente {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td headers="EventDetection2"><a href="/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps_deploy#starterapps_deploy" target="_blank">DISTRIBUISCI L'APPLICAZIONE</a><br></td>
    <td headers="EventDetection2"><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">ESERCITAZIONE ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a></td>
    <td headers="EventDetection2"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetectionV2" target="_blank">SCARICA ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a></td>
  </tr>
</table>

*Tabella 2. Applicazione di esempio Event Detection v2*
<table summary="Questa tabella descrive, nella prima riga, l'applicazione di esempio Event Detection. Nella seconda riga, la tabella include:
1. Nella prima colonna, un link alle istruzioni su come distribuire l'applicazione starter Event Detection. 2. Nella seconda colonna, un link alle esercitazioni su come utilizzare l'applicazione starter Event Detection. 3. Nella terza colonna, un link per scaricare direttamente l'applicazione starter Event Detection.
 ">
  <tr>
    <th id="EventDetection1" colspan="3">Applicazione di esempio Event Detection<br></th>
  </tr>
  <tr>
    <td headers="EventDetection1" colspan="3">L'applicazione Event Detection è implementata con il runtime <a href="https://{DomainName}/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">SDK for Node.js ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a>.
Questa applicazione starter è compatibile solo con i [piani di servizio v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans). L'applicazione
fornisce una IU web di esempio per visualizzare lo stato e i risultati delle analisi.
L'applicazione Node.js è associata a un'istanza del servizio {{site.data.keyword.streaminganalyticsshort}}. L'applicazione controlla il servizio tramite l'API REST {{site.data.keyword.streaminganalyticsshort}}.
<p>Puoi eseguire l'applicazione starter senza alcuna modifica.
Se vuoi provare con un altro servizio, puoi anche modificare il codice e rimandare le tue modifiche all'ambiente {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td headers="EventDetection1"><a href="/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps_deploy" target="_blank">DISTRIBUISCI L'APPLICAZIONE</a><br></td>
    <td headers="EventDetection1"><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">ESERCITAZIONE ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a></td>
    <td headers="EventDetection1"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection" target="_blank">SCARICA ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a></td>
  </tr>
</table>

*Tabella 2. Applicazione di esempio Event Detection*

<table summary="Questa tabella descrive, nella prima riga, l'applicazione di esempio New York Traffic. Nella seconda riga, la tabella include:
1. Nella prima colonna, un link alle istruzioni su come distribuire l'applicazione di esempio New York Traffic. 2. Nella seconda colonna, un link alle esercitazioni su come utilizzare l'applicazione di esempio New York Traffic. 3. Nella terza colonna, un link per scaricare direttamente l'applicazione di esempio New York Traffic.">
  <tr>
    <th id="NYCTraffic" colspan="3">Applicazione di esempio NYC Traffic<br></th>
  </tr>
  <tr>
    <td headers="NYCTraffic" colspan="3">L'applicazione starter NYC Traffic è un'applicazione per {{site.data.keyword.Bluemix_short}} scritta in Liberty for Java. Contiene un'applicazione {{site.data.keyword.streamsshort}} che richiama i dati pubblici dai sensori del traffico
di New York City, calcola le statistiche aggregate e restituisce i risultati all'applicazione Liberty. Questa applicazione starter è compatibile solo con i [piani di servizio v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans).
<p>Puoi eseguire l'applicazione starter senza alcuna modifica. Se vuoi provare con un altro servizio, puoi anche modificare il codice e rimandare le tue modifiche all'ambiente {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td headers="NYCTraffic" deploylink><a href="/docs/services/StreamingAnalytics/?topic=StreamingAnalytics-starterapps_deploy" target="_blank">DISTRIBUISCI L'APPLICAZIONE</a><br></td>
    <td headers="NYCTraffic"><a href="https://developer.ibm.com/streamsdev/docs/bluemix-streaming-analytics-starter-application/" target="_blank">ESERCITAZIONE ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a></td>
    <td headers="NYCTraffic"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic" target="_blank">SCARICA ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a></td>
  </tr>
</table>

*Tabella 3. Applicazione di esempio NYC Traffic*

## IBM Streams Runner per le applicazioni di esempio Apache Beam

<table summary="Questa tabella descrive, nella prima riga, l'applicazione TemperatureSample Beam. La tabella include nella seconda riga, un link a un'esercitazione su come distribuire l'applicazione TemperatureSample Beam.
 ">
  <tr>
    <th id="TemperatureSample" colspan="3">Applicazione TemperatureSample Beam<br></th>
  </tr>
  <tr>
    <td headers="TemperatureSample" colspan="3">Questa applicazione prende le letture della temperatura da più dispositivi. Questa applicazione starter è disponibile solo con i [piani di servizio v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans). L'applicazione divide le letture in “good” (valida) e “bad” (non valida) in base a una soglia specifica. Conta le letture non buone e genera alcune statistiche di base per le letture buone e infine registra i risultati. Puoi scaricare l'applicazione TemperatureSample dalla console Streaming Analytics.
</td>
  </tr>
  <tr>
    <td headers="TemperatureSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/sample/#running-the-temperaturesample-application" target="_blank">DISTRIBUISCI L'APPLICAZIONE ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a><br></td>
    <td headers="TemperatureSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/sample/#viewing-the-running-application" target="_blank">VISUALIZZA L'APPLICAZIONE ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a></td>
  </tr>
</table>

*Tabella 4. Applicazione TemperatureSample*

<table summary="Questa tabella descrive, nella prima riga, l'applicazione di esempio WordCount Beam. La tabella include nella seconda riga, un link a un'esercitazione su come distribuire l'applicazione di esempio WordCount.
 ">
  <tr>
    <th id="WordCountSample" colspan="3">Applicazione di esempio WordCount<br></th>
  </tr>
  <tr>
    <td headers="WordCountSample" colspan="3">L'applicazione di esempio Apache Beam 2.0 Java SDK Quickstart WordCount crea pipeline riutilizzabili e che è possibile conservare e leggere da un file di testo, applica le trasformazioni per suddividere in token e conta le parole e scrive i dati in un file di testo di output.
</td>
  </tr>
  <tr>
    <td headers="WordCountSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/wordcount/" target="_blank">DISTRIBUISCI L'APPLICAZIONE ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a><br></td>
  </tr>
</table>

*Tabella 5. Applicazione di esempio WordCount*

<table summary="Questa tabella illustra, nella prima riga, l'applicazione di esempio FileStreamSample. La tabella include nella seconda riga un link a un'esercitazione su come distribuire l'applicazione FileStreamSample.
 ">
  <tr>
    <th id="FilterStreamSample" colspan="3">Applicazione FileStreamSample<br></th>
  </tr>
  <tr>
    <td headers="FilterStreamSample" colspan="3">Puoi utilizzare l'applicazione di esempio IBM® Streams Runner for Apache Beam FileStreamSample per imparare come utilizzare l'archivio dell'oggetto {{site.data.keyword.Bluemix_notm}} per l'input e l'output del file.
</td>
  </tr>
  <tr>
    <td headers="FilterStreamSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/objstor/" target="_blank">DISTRIBUISCI L'APPLICAZIONE ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")</a><br></td>
  </tr>
</table>

*Tabella 6. Applicazione FileStreamSample*
