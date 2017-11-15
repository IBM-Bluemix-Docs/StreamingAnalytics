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

# IBM Streams Runner for Apache Beam in Streaming Analytics
{: #gs_beamrunner}

Wenn Sie über eine {{site.data.keyword.streamsshort}}-Entwicklungsumgebung verfügen, können Sie nun Beam-Anwendungen lokal in Ihrer Umgebung entwickeln und diese Apps anschließend an den {{site.data.keyword.streaminganalyticsshort}}-Service in {{site.data.keyword.Bluemix_notm}} übergeben.{{site.data.keyword.streamsshort}} Runner for Apache Beam führt Beam-Pipelines in einer {{site.data.keyword.streamsshort}}-Umgebung aus. Eine Beam-Anwendung, die mit Streams Runner gestartet wird, wird in eine Streams Application Bundle-Datei (SAB-Datei) umgesetzt, die Sie dann in {{site.data.keyword.streaminganalyticsshort}} bereitstellen und überwachen können.


Als ersten Schritt verwenden Sie die [Beispielanwendungen](/docs/services/StreamingAnalytics/c_starterapps.html), um sich mit der Übergabe und Überwachung einer Beam-Anwendung im {{site.data.keyword.streaminganalyticsshort}}-Service vertraut zu machen. Sie können die Beispielanwendungen von der {{site.data.keyword.streaminganalyticsshort}}-Konsole herunterladen.

Lesen Sie die [{{site.data.keyword.streamsshort}} Runner for Apache Beam-Dokumentation](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/), in der Sie Tabellen finden, die die Kompatibilität von Streams Runner mit der [Beam-Funktionsmatrix] veranschaulichen. [IBM Streams Runner for Apache Beam installieren](http://bit.ly/2zFDpPr) enthält eine Anleitung zur Installation des `com.ibm.streams.beam`-Toolkits in Ihrer Streams-Umgebung für die Erstellung von Beam-Anwendungen zur Übergabe und Überwachung in {{site.data.keyword.streaminganalyticsshort}}.

Grundlegende Kenntnisse der Beam-Programmierung sind von Vorteil, jedoch nicht erforderlich; auf der [Apache Beam-Website](https://beam.apache.org/documentation/){:new_window} stehen nützliche Informationen auf der Seite [Apache Beam Java SDK Quickstart](https://beam.apache.org/get-started/quickstart-java/){:new_window} sowie weitere Dokumente zur Verfügung.
