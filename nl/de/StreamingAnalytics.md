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

# Informationen zu Streaming Analytics
{: #about}

Sie können eine Echtzeitanalyse bewegter Daten im Rahmen Ihrer {{site.data.keyword.Bluemix_short}}-Anwendungen unter Verwendung von {{site.data.keyword.streaminganalyticsfull}} ausführen.
{:shortdesc}

Sie kennen {{site.data.keyword.streaminganalyticsshort}} noch nicht? Hier finden Sie eine [kurze Einführung in den Service ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/streamsdev/docs/streaming-analytics-now-available-bluemix-2/){:new_window}.

Der {{site.data.keyword.streaminganalyticsshort}}-Service bietet die folgenden Funktionen, mit denen Sie Ihre Daten in der Cloud bereitstellen, analysieren und überwachen können:

**Interaktive und programmgesteuerte Verwendung des Service:**

Sie können den Service interaktiv über die [{{site.data.keyword.streaminganalyticsshort}}-Konsole](/docs/services/StreamingAnalytics/c_streams_console.html) oder programmgesteuert über die [{{site.data.keyword.streaminganalyticsshort}}-v1-REST-API ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} verwenden, wenn Sie die [v1-Servicepläne](/docs/services/StreamingAnalytics/service_plans.html) nutzen. Verwenden Sie für [v2-Servicepläne](/docs/services/StreamingAnalytics/service_plans.html) die [{{site.data.keyword.streaminganalyticsshort}} v2-REST-API ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/apidocs/streaming-analytics-v2).

**Bereitstellung und Überwachung von SPL-, Java-, Scala- und Python-Anwendungen:**

Sie können {{site.data.keyword.streamsshort}}-Anwendungen in SPL, Java, Scala und Python schreiben. Mithilfe der {{site.data.keyword.streaminganalyticsshort}}-Konsole können Sie [diese Anwendungen bereitstellen und überwachen.](/docs/services/StreamingAnalytics/t_deploytocloud.html)

Wenn Sie Ihre Anwendungen in SPL schreiben möchten, sollten Sie wissen, dass {{site.data.keyword.streamsfull}} Processing Language (SPL) eine Programmiersprache ist, die zum Erstellen von Streamverarbeitungsanwendungen verwendet wird. Wenn Sie Ihre eigenen SPL-Anwendungen noch weitergehend einsetzen wollen, können Sie eine {{site.data.keyword.streamsshort}}-Entwicklungsumgebung einrichten und Sie müssen Ihre SPL-Apps für die Cloud vorbereiten.

Wenn Sie Python-Anwendungen ohne {{site.data.keyword.streamsshort}}-Entwicklungsumgebung erstellen und bereitstellen möchten, verwenden Sie die Service-Notebooks in {{site.data.keyword.DSX_short}} oder die Python-API von {{site.data.keyword.streamsshort}}. Weitere Informationen finden Sie im Abschnitt [Entwicklung von Python-Anwendungen für {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/t_develop_apps_python.html).

Sie können Beam-Anwendungen mit einer Streams-Ausführungskomponente in der lokalen Entwicklungsumgebung entwickeln und dann mithilfe des {{site.data.keyword.streaminganalyticsshort}}-Service bereitstellen und überwachen. Weitere Informationen zu Beam-Anwendungen mit Streams Runner finden Sie in [IBM Streams Runner for Apache Beam in {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/gs_beamrunner.html).


**Kompatibilität mit {{site.data.keyword.streamsshort}}-Operatoren:**

Die {{site.data.keyword.streamsshort}}-Operatoren im SPL-Standardtoolkit ([{{site.data.keyword.streamsshort}} Processing Language) sind mit {{site.data.keyword.streaminganalyticsshort}} kompatibel](/docs/services/StreamingAnalytics/compatible_toolkits.html).

## Zuständigkeiten in Streaming Analytics
{: #responsibilities notoc}

### Zuständigkeiten des Kunden
{: #clientresponsibilities notoc}

Der Kunde ist für Folgendes zuständig:

* Für das Überwachen, Konfigurieren und Verwalten der in seiner Instanz aktiven {{site.data.keyword.streamsshort}}-Jobs nach der Erstkonfiguration von {{site.data.keyword.streamsshort}} durch IBM. Der Kunde ist im Hinblick auf das Starten und Stoppen der Instanz und der unter der Instanz ausgeführten Jobs flexibel.
* Für das notwendige Entwickeln von Programmen und Anwendungen für den Service zur Analyse von Daten sowie zur Erkenntnisgewinnung im Hinblick auf diese Analyse. Der Kunde ist zudem für Qualität und Leistung dieser so entwickelten Programme oder Anwendungen verantwortlich. Programme können in SPL, Java oder anderen Sprachen entwickelt werden, und zwar mithilfe des {{site.data.keyword.streamsshort}} Topology-Features. Sie müssen entweder mit {{site.data.keyword.streamsshort}} Developer Edition oder mit {{site.data.keyword.streamsshort}} Quick Start Edition kompiliert werden, und zwar unter Verwendung des Betriebssystems, das auch für {{site.data.keyword.streaminganalyticsshort}} verwendet wird.
* Für das regelmäßige Prüfen des folgenden Links für den Abruf von Informationen zu einer geplanten, unterbrechungsfreien Ausfallzeit oder einer Ausfallzeit mit Unterbrechung: [https://developer.ibm.com/bluemix/support/#status ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/bluemix/support/#status){:new_window}.  
* Für das Sichern aller Daten, Metadaten, Konfigurationsdateien und Umgebungsparameter gemäß den Geschäftsanforderungen zur Sicherstellung der Kontinuität.
* Für das Wiederherstellen von Daten, Metadaten, Konfigurationsdateien und Umgebungsparametern aus einem Backup zur Sicherstellung der Kontinuität, falls es zu einem Ausfall eines beliebigen Typs kommt. Diese Ausfälle umfassen, sind jedoch nicht beschränkt auf Ausfälle eines Rechenzentrums oder Pods sowie auf Ausfälle von Servern, Festplatten oder Softwarekomponenten.

### Zuständigkeiten von IBM
{: #ibmresponsibilities notoc}

Im Rahmen von {{site.data.keyword.streaminganalyticsfull}} ist IBM für Folgendes zuständig:

* Für das Bereitstellen und Verwalten von Servern, Speicher und Netzinfrastruktur für die Kundeninstanz.
* Für das Bereitstellen einer Erstkonfiguration von {{site.data.keyword.streamsshort}} auf Basis der Anzahl der ausgewählten Knoten.
* Für das Bereitstellen und Verwalten einer Infrastruktur für Internet-Facing und einer internen Firewall zum Schutz und als Isolation.
* Für das Überwachen und Verwalten der folgenden Komponenten in {{site.data.keyword.streaminganalyticsshort}}:
	* Netzkomponenten
	* Server und deren lokaler Speicher
	* Infrastrukturbetriebssysteme
	* {{site.data.keyword.streamsshort}}-Management-Services
	* {{site.data.keyword.streamsshort}}-Instanzen
* Für das Bereitstellen von Wartungspatches einschließlich der entsprechenden Sicherheitspatches für die Infrastrukturbetriebssysteme und für {{site.data.keyword.streamsshort}}.
* Für das Durchführen einer regelmäßigen Wartung, für die es zu keiner Systemausfallzeit (unterbrechungsfreie Wartung) kommen sollte, sowie einer Wartung, für die es zu einer Systemausfallzeit samt Systemneustart (Wartung mit Unterbrechung) kommen kann; diese werden zu geplanten Zeiten durchgeführt, die unter [https://developer.ibm.com/bluemix/support/#status ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/bluemix/support/#status){:new_window} veröffentlicht werden.
* Alle Änderungen an den geplanten Wartungszeiten werden durch entsprechende Benachrichtigungen bekanntgemacht.
