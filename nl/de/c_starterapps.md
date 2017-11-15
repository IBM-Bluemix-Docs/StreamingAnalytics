---

copyright:
  years: 2015, 2017
lastupdated: "2017-10-27"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics-Starteranwendung verwenden
{: #starterapps}

Sie können Starteranwendungen bereitstellen und modifizieren und Sie können in kürzester Zeit lernen, wie der {{site.data.keyword.streaminganalyticsshort}}-Service verwendet wird:
{:shortdesc}

<table summary="Die erste Zeile dieser Tabelle enthält eine Beschreibung der Starteranwendung 'Stock Trades'. In der zweiten Zeile der Tabelle ist Folgendes enthalten: 1. In der ersten Spalte ein Link zu einem Video mit einer Beschreibung zur Bereitstellung der Starteranwendung 'Stock Trades'. 2. In der zweiten Spalte ein Link zum direkten Download der Starteranwendung 'Stock Trades'.">
  <tr>
    <th colspan="3">Beispiel-App 'Stock Trades'<br></th>
  </tr>
  <tr>
    <td colspan="3">Diese Anwendung analysiert einen Datenstrom mit Börsennotierungen und generiert einen gleitenden Durchschnittswert der Preise mithilfe des Operators für die <a href="https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$spl/op$spl.relational$Aggregate.html">Aggregierung</a>.
Sie können die Starteranwendung unverändert ausführen. Wenn Sie weiter mit dem Service experimentieren wollen, können Sie den Code modifizieren und Ihre Änderungen in die {{site.data.keyword.Bluemix_short}}-Umgebung zurückübertragen. Die vollständige Quelle für die Starteranwendung ist <a href="https://github.com/IBMStreams/samples/tree/master/QuickStart/TradesApp">auf GitHub verfügbar</a>.</p>
</td>
  </tr>
  <tr>
    <td><a href="https://developer.ibm.com/streamsdev/videos/getting-started-streaming-analytics-service-using-trades-starter-application/" target="_blank">APP BEREITSTELLEN</a><br></td>
    <td><a href="https://github.com/IBMStreams/samples/raw/master/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab" target="_blank">DOWNLOAD</a></td>
  </tr>
</table>

*Tabelle 1. Beispiel-App 'Stock Trades'*


<table summary="In dieser Tabelle wird in der ersten Zeile die Beispielanwendung 'Event Detection' beschrieben. Die zweite Zeile der Tabelle enthält Folgendes: 1. In der ersten Spalte einen Link zu Anweisungen für die Bereitstellung der Starteranwendung 'Event Detection'. 2. In der zweiten Spalte einen Link zu Lernprogrammen für die Verwendung der Starteranwendung 'Event Detection'. 3. In der dritten Spalte einen Link zum direkten Download der Starteranwendung 'Event Detection'.">
  <tr>
    <th colspan="3">Beispiel-App 'Event Detection'<br></th>
  </tr>
  <tr>
    <td colspan="3">Die App 'Event Detection' wird über die Laufzeitumgebung <a href="https://console.ng.bluemix.net/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">{{site.data.keyword.sdk4node}}</a> implementiert.
Die App bietet eine einfache Webbenutzerschnittstelle zum Anzeigen des Status und der Ergebnisse der Analyse. Die Node.js-App ist an eine Instanz des {{site.data.keyword.streaminganalyticsshort}}-Service gebunden. Die App steuert den Service über die {{site.data.keyword.streaminganalyticsshort}}-REST-API.
<p>Sie können die Starteranwendung unverändert ausführen.
Wenn Sie weiter mit dem Service experimentieren wollen, können Sie den Code modifizieren und Ihre Änderungen in die {{site.data.keyword.Bluemix_short}}-Umgebung zurückübertragen.</p>
</td>
  </tr>
  <tr>
    <td><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">APP BEREITSTELLEN</a><br></td>
    <td><a href="http://www.ibm.com/developerworks/library/ba-bluemix-detect-complex-events-from-data-stream-trs/index.html" target="_blank">LERNPROGRAMM</a></td>
    <td><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection" target="_blank">DOWNLOAD</a></td>
  </tr>
</table>

*Tabelle 2. Beispiel-App 'Event Detection'*

<table summary="In dieser Tabelle wird in der ersten Zeile die Beispielanwendung 'New York Traffic' beschrieben. Die zweite Zeile der Tabelle enthält Folgendes: 1. In der ersten Spalte einen Link zu Anweisungen für die Bereitstellung der Beispielanwendung 'New York Traffic'. 2. In der zweiten Spalte einen Link zu Lernprogrammen für die Verwendung der Beispielanwendung 'New York Traffic'. 3. In der dritten Spalte einen Link zum direkten Download der Beispielanwendung 'New York Traffic'.">
  <tr>
    <th colspan="3">Beispiel-App 'NYC Traffic'<br></th>
  </tr>
  <tr>
    <td colspan="3">Die Starter-App 'NYC Traffic' ist eine Anwendung für {{site.data.keyword.Bluemix_short}}, die in Liberty for Java geschrieben ist. Sie enthält eine {{site.data.keyword.streamsshort}}-Anwendung, die öffentliche Daten von Verkehrssensoren in New York City abruft, kumulierte Statistikdaten berechnet und die Ergebnisse an die Liberty-Anwendung zurücksendet.
<p>Sie können die Starteranwendung unverändert ausführen. Wenn Sie weiter mit dem Service experimentieren wollen, können Sie den Code modifizieren und Ihre Änderungen in die {{site.data.keyword.Bluemix_short}}-Umgebung zurückübertragen.</p>
</td>
  </tr>
  <tr>
    <td><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">APP BEREITSTELLEN</a><br></td>
    <td><a href="https://developer.ibm.com/streamsdev/docs/bluemix-streaming-analytics-starter-application/" target="_blank">LERNPROGRAMM</a></td>
    <td><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic" target="_blank">DOWNLOAD</a></td>
  </tr>
</table>

*Tabelle 3. Beispiel-App 'NYC Traffic'*

## IBM Streams Runner for Apache Beam - Beispiel-Apps

<table summary="In der ersten Zeile dieser Tabelle wird die Beam-Anwendung 'TemperatureSample' beschrieben. Die zweite Zeile enthält einen Link zu einem Lernprogramm für die Bereitstellung der Beam-Anwendung 'TemperatureSample'.">
  <tr>
    <th colspan="3">Beam-App `TemperatureSample`<br></th>
  </tr>
  <tr>
    <td colspan="3">Diese Anwendung erfasst Temperaturmesswerte mehrerer Geräte. Die Anwendung unterteilt die Messwerte in 'gut' (gültig) und 'schlecht' (ungültig) auf der Basis eines bestimmten Schwellenwerts. Die ungültigen Werte werden gezählt, für die gültigen Werte wird eine Basisstatistik generiert und die Ergebnisse werden schließlich protokolliert. Die App 'TemperatureSample' kann über die Streaming Analytics-Konsole heruntergeladen werden.
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3-sample/#running-the-temperaturesample-application" target="_blank">APP BEREITSTELLEN</a><br></td>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3-sample/#viewing-the-running-application" target="_blank">APP ANZEIGEN</a></td>
  </tr>
</table>

*Tabelle 4. App 'TemperatureSample'*

<table summary="Die erste Zeile dieser Tabelle enthält eine Beschreibung der Beam-Beispielanwendung 'WordCount'. Die zweite Zeile enthält einen Link zu einem Lernprogramm für die Bereitstellung der Beispielanwendung 'WordCount'.">
  <tr>
    <th colspan="3">Beispiel-App 'WordCount'<br></th>
  </tr>
  <tr>
    <td colspan="3">Die Apache Beam 2.0 Java SDK Quickstart-Beispielanwendung 'WordCount' erstellt Pipelines, die wiederverwendet und verwaltet werden können. Diese Pipelines lesen aus einer Textdatei, wenden Umsetzungen zur Aufbereitung an, zählen die Wörter und schreiben die Daten in eine Ausgabetextdatei.
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3b-wordcount/" target="_blank">APP BEREITSTELLEN</a><br></td>
  </tr>
</table>

*Tabelle 5. Beispiel-App `'WordCount'`*

<table summary="Die erste Zeile dieser Tabelle enthält eine Beschreibung der Beispielanwendung `FileStreamSample`. Die zweite Zeile enthält einen Link zu einem Lernprogramm für die Bereitstellung der Anwendung `FileStreamSample`.">
  <tr>
    <th colspan="3">App 'FileStreamSample'<br></th>
  </tr>
  <tr>
    <td colspan="3">Mit der IBM® Streams Runner for Apache Beam-Beispielanwendung 'FileStreamSample' lernen Sie die Verwendung des {{site.data.keyword.Bluemix_notm}}-Objektspeichers für die Dateiein- und -ausgabe.
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-5b-objstor/" target="_blank">APP BEREITSTELLEN</a><br></td>
  </tr>
</table>

*Tabelle 6. App `FileStreamSample`*
