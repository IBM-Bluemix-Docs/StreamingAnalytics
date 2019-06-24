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

# Hochverfügbarkeit und Disaster-Recovery
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} ist innerhalb eines {{site.data.keyword.Bluemix_notm}}-Standorts (z. B. Dallas, Washington DC, London, Frankfurt) hoch verfügbar. Die mögliche Disaster-Recovery für eine gesamte {{site.data.keyword.Bluemix_notm}}-Region Standort setzt jedoch Planung und  Vorbereitung voraus.
{:shortdesc}


Sie müssen selbst dafür sorgen, dass Sie Ihre Konfiguration, Ihre Anpassung und Ihre Nutzung des Service kennen. Sie sind ebenfalls dafür verantwortlich, alle Vorbereitungen für die erneute Erstellung einer Instanz des Service an einem neuen {{site.data.keyword.Bluemix_notm}}-Standord und erneute Bereitstellung der Anwendungen an diesem Standort zu treffen. In [Wie kann sichergestellt werden, dass keine Ausfallzeiten auftreten?](/docs/services/overview?topic=overview-zero-downtime#zero-downtime) finden Sie weitere Informationen zu den Standards für die Hochverfügbarkeit und die Disaster-Recovery in {{site.data.keyword.Bluemix_notm}}. Darüber hinaus stehen Informationen zu [Service Level Agreements](/docs/services/overview?topic=overview-zero-downtime#zero-downtime#SLAs) zur Verfügung. 

## Hochverfügbarkeit

{{site.data.keyword.streaminganalyticsshort}} ermöglicht eine hohe Verfügbarkeit Ihrer Anwendungen. Ihre Anwendungen werden in Docker-Containern bereitgestellt, die in Kubernetes-Clustern ausgeführt werden. Zum Entwickeln hoch verfügbarer Anwendungen benötigen Sie Kenntnisse über die Funktionsweise dieser Container, mit der die Hochverfügbarkeit sichergestellt wird. 

* Bei Anwendungsressourcen handelt es sich um Container, deren CPU und Speicher anhand Ihres Serviceplans zugeordnet werden. 
* Während eines Hardware- oder Softwareausfalls können Container verschoben werden. Beim Verschieben von Containern werden Verarbeitungselemente erneut gestartet. 
* Während geplanter Wartungsarbeiten können Container verschoben werden (Verarbeitungselemente werden erneut gestartet). 

Aus diesem Grund müssen Sie beim Schreiben von Anwendungen berücksichtigen, dass Container gelegentlich verschoben werden können. Berücksichtigen Sie darüber hinaus die folgenden Aspekte: 
* Stellen Sie sicher, dass die Verarbeitungselemente wiederanlauffähig und verschiebbar sind. 
* Stellen Sie sicher, dass die Anwendung das erneute Starten einiger oder aller zugehörigen Verarbeitungselemente toleriert. Die Reihenfolge des Wiederanlaufs darf dabei keine Rolle spielen. 
* Stellen Sie sicher, dass die Quellen- und Zieloperatoren in Ihrer Streams-Anwendung so konfiguriert sind, dass sie Verbindungen erneut herstellen, wenn das zugehörige Verarbeitungselement erneut gestartet wird. 

Im [Entwicklerhandbuch zu {{site.data.keyword.streaminganalyticsshort}}](https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/#troubleshooting) finden Sie Beispiele zur Fehlerbehebung für Ihre Anwendung. 

Zur Implementierung der Hochverfügbarkeit wurde für Streams-Anwendungen die garantierte Verarbeitung aller Tupel aktiviert. Um eine garantierte Tupelverarbeitung zu erreichen, wird für alle Operatoren innerhalb einer konsistenten Region in regelmäßigen Abständen ein Prüfpunkt eingerichtet. Wenn ein Anwendungsfehler auftritt, werden alle Operatoren auf den letzten erfolgreichen Prüfpunktstatus zurückgesetzt.
{{site.data.keyword.streaminganalyticsshort}} ermöglicht die Verwendung konsistenter Regionen. 

### Garantierte Tupelverarbeitung
Aufgrund von Geschäftsanforderungen ist es für einige Anwendungen erforderlich, dass alle Tupel mindestens einmal verarbeitet werden. Funktionale Erweiterungen für {{site.data.keyword.streamsshort}} umfassen Operatoren und Annotationen, die die Definition einer Region ermöglichen, bei der während der Streamverarbeitung keine Tupel verloren gehen. Tupel in einer konsistenten Region werden mindestens einmal verarbeitet.

Wenn innerhalb einer konsistenten Region ein Anwendungsfehler festgestellt wird, kann {{site.data.keyword.streaminganalyticsshort}} die Anwendung auf den letzten konsistenten Status (d. h. Prüfpunkt) zurücksetzen und die Anwendungsdatenquellen anweisen, Tupel von diesem Punkt an zu wiederholen. 

Sie können Streams-Anwendungen mit definierten konsistenten Regionen in {{site.data.keyword.streaminganalyticsshort}} ausführen und überwachen. Wenn Sie einen {{site.data.keyword.streaminganalyticsshort}}-Service erstellen, ist die Instanz bereits so konfiguriert, dass sie die Verwendung konsistenter Regionen zulässt. 

Bei einer konsistenten Region handelt es sich um ein Unterdiagramm, in dem die Status der Operatoren konsistent werden, indem alle Tupel und Interpunktionszeichen innerhalb definierter Punkte in einem Stream verarbeitet werden. Auf diese Weise werden Tupel innerhalb des Unterdiagramms mindestens einmal verarbeitet. Für die konsistente Region findet in regelmäßigen Abständen eine Bereinigung der aktuelle Tupel statt. Alle Tupel in der konsistenten Region werden bis zum Ende des Unterdiagramms verarbeitet. Bei Operatoren mit speicherinternem Status wird automatisch eine Serialisierung und Speicherung vorgenommen. Dies erfolgt am Prüfpunkt für jeden Operator in der Region.

Sie können Java-, SPL- und Python-Anwendungen mit garantierter Tupelverarbeitung schreiben und in {{site.data.keyword.streaminganalyticsshort}} bereitstellen. 

Sie können den Anfang einer konsistenten Region mit der Annotation `@consistent` bei einem geeigneten Operator definieren. {{site.data.keyword.streamsshort}} bestimmt den Bereich der konsistenten Region automatisch, Sie können jedoch den Endoperator der Region mit der Annotation `@autonomous` ändern. Die definierte konsistente Region stellt regelmäßig einen konsistenten Status her.

Die [{{site.data.keyword.streamsshort}}-Dokumentation ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html) enthält weitere Details zur Verwendung konsistenter Regionen in Streams-Anwendungen.

## Disaster-Recovery
{{site.data.keyword.streaminganalyticsshort}} ist ein GA-Service, der in mehreren {{site.data.keyword.Bluemix_notm}}-Regionen angeboten wird. {{site.data.keyword.streaminganalyticsshort}} speichert keine Benutzerdaten in {{site.data.keyword.Bluemix_notm}}. 

Wählen Sie auf der Basis der jeweiligen Geschäftsanforderungen eine der folgenden Disaster-Recovery-Strategien aus:
* Wenn eine unterbrechungsfreie Ausführung der Anwendung erforderlich ist:
  1. Erstellen Sie Instanzen von {{site.data.keyword.streaminganalyticsshort}} in mehreren {{site.data.keyword.Bluemix_notm}}-Regionen. 
  2. Übergeben Sie Ihre Anwendung an mehrere Regionen. 


* Wenn nur eine minimale Unterbrechung der Anwendung zulässig ist:
  1. Erstellen Sie Instanzen von {{site.data.keyword.streaminganalyticsshort}} in mehreren {{site.data.keyword.Bluemix_notm}}-Regionen. 
  2. Überwachen Sie die Anwendung mithilfe der [Service-REST-API](https://ibm.co/2Gt9mB6) und verlagern Sie die Workload bei Bedarf dynamisch in eine neue Region. 

**Hinweis**: Für jede konsistente Region besteht eine Bindung zur {{site.data.keyword.Bluemix_notm}}-Region. In einem Disaster-Recovery-Szenario ist konsistenten Regionen in einer Anwendung keine Rolle zugewiesen. 
