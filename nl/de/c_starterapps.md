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

# Beispielanwendungen
{: #starterapps}

Sie können Starteranwendungen bereitstellen und modifizieren und Sie können in kürzester Zeit lernen, wie der {{site.data.keyword.streaminganalyticsshort}}-Service verwendet wird. Beachten Sie, dass für die v2-Servicepläne die Ausführung von Streams unter RHEL 7 erforderlich ist. {{site.data.keyword.streaminganalyticsshort}} stellt eine [Reihe von Starter- und Beispielanwendungen](https://developer.ibm.com/streamsdev/docs/starter-sample-apps-v2-plans/) bereit, die einen schnellen Einstieg in die Verwendung der v2-Servicepläne ermöglichen. Die Beispielanwendungen 'Event Detection' und 'NYC Traffic' können mit den v2-Serviceplänen nicht verwendet werden.
{:shortdesc}


<table summary="Die erste Zeile dieser Tabelle enthält eine Beschreibung der Starteranwendung 'Stock Trades'. In der zweiten Zeile der Tabelle ist Folgendes enthalten: 1. In der ersten Spalte ein Link zu einem Video mit einer Beschreibung zur Bereitstellung der Starteranwendung 'Stock Trades'. 2. In der zweiten Spalte ein Link zum direkten Download der Starteranwendung 'Stock Trades'.">
  <tr>
    <th id="stocktrades" colspan="3">Beispiel-App 'Stock Trades'<br></th>
  </tr>
  <tr>
    <td headers="stocktrades" colspan="3">Diese Anwendung analysiert einen Datenstrom mit Börsennotierungen und generiert einen gleitenden Durchschnittswert der Preise mithilfe des Operators für die <a href="https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$spl/op$spl.relational$Aggregate.html">Aggregierung ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a>.
Sie können die Starteranwendung unverändert ausführen. Wenn Sie weiter mit dem Service experimentieren wollen, können Sie den Code modifizieren und Ihre Änderungen in die {{site.data.keyword.Bluemix_short}}-Umgebung zurückübertragen. Die vollständige Quelle für die Starteranwendung ist <a href="https://github.com/IBMStreams/samples/tree/master/QuickStart/TradesApp">auf GitHub verfügbar ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a>.</p>
</td>
  </tr>
  <tr>
    <td headers="stocktrades"><a href="https://developer.ibm.com/streamsdev/videos/getting-started-streaming-analytics-service-using-trades-starter-application/" target="_blank">App bereitstellen ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a><br></td>
    <td headers="stocktrades"><a href="https://github.com/IBMStreams/samples/raw/master/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab" target="_blank">Download ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a></td>
  </tr>
</table>

*Tabelle 1. Beispiel-App 'Stock Trades'*


<table summary="In der ersten Zeile dieser Tabelle wird die Beispielanwendung 'Event Detection v2' beschrieben. Die zweite Zeile enthält Folgendes: 1. In der ersten Spalte einen Link zu Anweisungen für die Bereitstellung der Starteranwendung 'Event Detection v2'. 2. In der zweiten Spalte einen Link zu Lernprogrammen für die Verwendung der Starteranwendung 'Event Detection'. 3. In der dritten Spalte einen Link zum direkten Download der Starteranwendung 'Event Detection'">
  <tr>
    <th id="EventDetection2" colspan="3">Beispiel-App 'Event Detection v2'<br></th>
  </tr>
  <tr>
    <td colspan="3" headers="EventDetection2">Die App 'Event Detection v2' wird über die Laufzeitumgebung von <a href="https://{DomainName}/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">SDK for Node.js ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a> implementiert. Diese Starter-App ist nur mit [v2-Serviceplänen](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) kompatibel.
Die App bietet eine einfache Webbenutzerschnittstelle zum Anzeigen des Status und der Ergebnisse der Analyse.
Die Node.js-App ist an eine Instanz des {{site.data.keyword.streaminganalyticsshort}}-Service gebunden. Die App steuert den Service über die {{site.data.keyword.streaminganalyticsshort}}-v2-REST-API.
<p>Sie können die Starteranwendung unverändert ausführen.
Wenn Sie weiter mit dem Service experimentieren wollen, können Sie den Code modifizieren und Ihre Änderungen in die {{site.data.keyword.Bluemix_short}}-Umgebung zurückübertragen.</p>
</td>
  </tr>
  <tr>
    <td headers="EventDetection2"><a href="/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps_deploy#starterapps_deploy" target="_blank">APP BEREITSTELLEN</a><br></td>
    <td headers="EventDetection2"><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">Lernprogramm ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a></td>
    <td headers="EventDetection2"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetectionV2" target="_blank">Download ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a></td>
  </tr>
</table>

*Tabelle 2. Beispiel-App 'Event Detection v2'*
<table summary="In dieser Tabelle wird in der ersten Zeile die Beispielanwendung 'Event Detection' beschrieben. Die zweite Zeile der Tabelle enthält Folgendes: 1. In der ersten Spalte einen Link zu Anweisungen für die Bereitstellung der Starteranwendung 'Event Detection'. 2. In der zweiten Spalte einen Link zu Lernprogrammen für die Verwendung der Starteranwendung 'Event Detection'. 3. In der dritten Spalte einen Link zum direkten Download der Starteranwendung 'Event Detection'.">
  <tr>
    <th id="EventDetection1" colspan="3">Beispiel-App 'Event Detection'<br></th>
  </tr>
  <tr>
    <td headers="EventDetection1" colspan="3">Die App 'Event Detection' wird über die Laufzeitumgebung von <a href="https://{DomainName}/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">SDK for Node.js ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a> implementiert.
Diese Starter-App ist nur mit [v1-Serviceplänen](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) kompatibel. Die App bietet eine einfache Webbenutzerschnittstelle zum Anzeigen des Status und der Ergebnisse der Analyse.
Die Node.js-App ist an eine Instanz des {{site.data.keyword.streaminganalyticsshort}}-Service gebunden. Die App steuert den Service über die {{site.data.keyword.streaminganalyticsshort}}-REST-API.
<p>Sie können die Starteranwendung unverändert ausführen.
Wenn Sie weiter mit dem Service experimentieren wollen, können Sie den Code modifizieren und Ihre Änderungen in die {{site.data.keyword.Bluemix_short}}-Umgebung zurückübertragen.</p>
</td>
  </tr>
  <tr>
    <td headers="EventDetection1"><a href="/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps_deploy" target="_blank">APP BEREITSTELLEN</a><br></td>
    <td headers="EventDetection1"><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">Lernprogramm ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a></td>
    <td headers="EventDetection1"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection" target="_blank">Download ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a></td>
  </tr>
</table>

*Tabelle 2. Beispiel-App 'Event Detection'*

<table summary="In dieser Tabelle wird in der ersten Zeile die Beispielanwendung 'New York Traffic' beschrieben. Die zweite Zeile der Tabelle enthält Folgendes: 1. In der ersten Spalte einen Link zu Anweisungen für die Bereitstellung der Beispielanwendung 'New York Traffic'. 2. In der zweiten Spalte einen Link zu Lernprogrammen für die Verwendung der Beispielanwendung 'New York Traffic'. 3. In der dritten Spalte einen Link zum direkten Download der Beispielanwendung 'New York Traffic'.">
  <tr>
    <th id="NYCTraffic" colspan="3">Beispiel-App 'NYC Traffic'<br></th>
  </tr>
  <tr>
    <td headers="NYCTraffic" colspan="3">Die Starter-App 'NYC Traffic' ist eine Anwendung für {{site.data.keyword.Bluemix_short}}, die in Liberty for Java geschrieben ist. Sie enthält eine {{site.data.keyword.streamsshort}}-Anwendung, die öffentliche Daten von Verkehrssensoren in New York City abruft, kumulierte Statistikdaten berechnet und die Ergebnisse an die Liberty-Anwendung zurücksendet. Diese Starter-App ist nur mit [v1-Serviceplänen](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) kompatibel.
<p>Sie können die Starteranwendung unverändert ausführen. Wenn Sie weiter mit dem Service experimentieren wollen, können Sie den Code modifizieren und Ihre Änderungen in die {{site.data.keyword.Bluemix_short}}-Umgebung zurückübertragen.</p>
</td>
  </tr>
  <tr>
    <td headers="NYCTraffic" deploylink><a href="/docs/services/StreamingAnalytics/?topic=StreamingAnalytics-starterapps_deploy" target="_blank">APP BEREITSTELLEN</a><br></td>
    <td headers="NYCTraffic"><a href="https://developer.ibm.com/streamsdev/docs/bluemix-streaming-analytics-starter-application/" target="_blank">Lernprogramm ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a></td>
    <td headers="NYCTraffic"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic" target="_blank">Download ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a></td>
  </tr>
</table>

*Tabelle 3. Beispiel-App 'NYC Traffic'*

## IBM Streams Runner for Apache Beam - Beispiel-Apps

<table summary="In der ersten Zeile dieser Tabelle wird die Beam-Anwendung 'TemperatureSample' beschrieben. Die zweite Zeile enthält einen Link zu einem Lernprogramm für die Bereitstellung der Beam-Anwendung 'TemperatureSample'.">
  <tr>
    <th id="TemperatureSample" colspan="3">Beam-App 'TemperatureSample'<br></th>
  </tr>
  <tr>
    <td headers="TemperatureSample" colspan="3">Diese Anwendung erfasst Temperaturmesswerte mehrerer Geräte. Diese Starter-App ist nur für [v2-Servicepläne](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) verfügbar. Die Anwendung unterteilt die Messwerte in 'gut' (gültig) und 'schlecht' (ungültig) auf der Basis eines bestimmten Schwellenwerts. Die ungültigen Werte werden gezählt, für die gültigen Werte wird eine Basisstatistik generiert und die Ergebnisse werden schließlich protokolliert. Die App 'TemperatureSample' kann über die Streaming Analytics-Konsole heruntergeladen werden.
</td>
  </tr>
  <tr>
    <td headers="TemperatureSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/sample/#running-the-temperaturesample-application" target="_blank">App bereitstellen ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a><br></td>
    <td headers="TemperatureSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/sample/#viewing-the-running-application" target="_blank">App anzeigen ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a></td>
  </tr>
</table>

*Tabelle 4. App 'TemperatureSample'*

<table summary="Die erste Zeile dieser Tabelle enthält eine Beschreibung der Beam-Beispielanwendung 'WordCount'. Die zweite Zeile enthält einen Link zu einem Lernprogramm für die Bereitstellung der Beispielanwendung 'WordCount'.">
  <tr>
    <th id="WordCountSample" colspan="3">Beispiel-App 'WordCount'<br></th>
  </tr>
  <tr>
    <td headers="WordCountSample" colspan="3">Die Apache Beam 2.0 Java SDK Quickstart-Beispielanwendung 'WordCount' erstellt Pipelines, die wiederverwendet und verwaltet werden können. Diese Pipelines lesen aus einer Textdatei, wenden Umsetzungen zur Aufbereitung an, zählen die Wörter und schreiben die Daten in eine Ausgabetextdatei.
</td>
  </tr>
  <tr>
    <td headers="WordCountSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/wordcount/" target="_blank">App bereitstellen ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a><br></td>
  </tr>
</table>

*Tabelle 5. Beispiel-App 'WordCount'*

<table summary="Die erste Zeile dieser Tabelle enthält eine Beschreibung der Beispielanwendung 'FileStreamSample'. Die zweite Zeile enthält einen Link zu einem Lernprogramm für die Bereitstellung der Anwendung 'FileStreamSample'.">
  <tr>
    <th id="FilterStreamSample" colspan="3">App 'FileStreamSample'<br></th>
  </tr>
  <tr>
    <td headers="FilterStreamSample" colspan="3">Mit der IBM® Streams Runner for Apache Beam-Beispielanwendung 'FileStreamSample' lernen Sie die Verwendung des {{site.data.keyword.Bluemix_notm}}-Objektspeichers für die Dateiein- und -ausgabe.
</td>
  </tr>
  <tr>
    <td headers="FilterStreamSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/objstor/" target="_blank">App bereitstellen ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")</a><br></td>
  </tr>
</table>

*Tabelle 6. App 'FileStreamSample'*
