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

# Beam-Anwendungen in Streaming Analytics bereitstellen
{: #develop_beam_apps}

Sie können jetzt Beam-Anwendungen in Ihrer lokalen {{site.data.keyword.streamsshort}}-Entwicklungsumgebung entwickeln und diese Anwendungen in {{site.data.keyword.streaminganalyticsshort}} bereitstellen.
{:shortdesc}

{{site.data.keyword.streamsshort}} Runner for Apache Beam führt Beam-Pipelines in einer {{site.data.keyword.streamsshort}}-Umgebung aus. Eine Beam-Anwendung, die mit Streams Runner gestartet wird, wird in eine Streams Application Bundle-Datei (SAB-Datei) umgesetzt, die Sie dann in {{site.data.keyword.streaminganalyticsshort}} bereitstellen und überwachen können.

Um eine Beam-Anwendung an den {{site.data.keyword.streaminganalyticsshort}}-Service in {{site.data.keyword.Bluemix_notm}} zu übergeben, müssen Sie eine mit JSON formatierte VCAP-Datei erstellen, die Berechtigungsnachweise und weitere Informationen für den Service enthält.

1. Navigieren Sie in der lokalen Streams-Umgebung zum Unterordner mit den Beispielen, in dem das Toolkit installiert wurde ($STREAMS_BEAM_RUNNER/samples), und kopieren Sie die Datei 'template.vcap' in eine neue Datei. Benennen Sie die Datei mit einem aussagekräftigen Dateinamen und der Dateierweiterung .vcap.
1. [Kopieren Sie die Berechtigungsnachweise des {{site.data.keyword.streaminganalyticsshort}}-Service](/docs/services/StreamingAnalytics/r_vcap_services.html) und fügen Sie sie in die erstellte VCAP-Datei ein, wobei Sie die folgende Zeile ersetzen:
```
 <REMOVE THIS LINE AND INSERT CREDENTIALS HERE>
 ```
1. Stellen Sie sicher, dass Ihre Beam-Anwendung in Ihrer Entwicklungsumgebung ordnungsgemäß ausgeführt wird. Beim Starten der Beam-Anwendung mit Streams Runner wird die Anwendung in eine Streams Application Bundle-Datei (SAB-Datei) umgesetzt.
1. Übergeben Sie die SAB-Datei, die Ihrer Beam-Anwendung zugeordnet ist, an {{site.data.keyword.streaminganalyticsshort}}.

Ihre Anwendung wurde jetzt in der Cloud bereitgestellt. Sie können Ihre Anwendung überwachen, indem Sie den {{site.data.keyword.streaminganalyticsshort}}-Service verwenden.

Weitere Details zur Bereitstellung und Überwachung der Beam-Anwendung in {{site.data.keyword.streaminganalyticsshort}} finden Sie in [Streams Runner for Apache Beam ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/).
