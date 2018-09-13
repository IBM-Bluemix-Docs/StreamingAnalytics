---

copyright:
  years: 2015, 2018
lastupdated: "2018-07-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics - Hochverfügbarkeit
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} ermöglicht eine hohe Verfügbarkeit Ihrer Anwendungen. Wenn bei einem Ihrer Anwendungsknoten ({{site.data.keyword.streamsshort}}-Ressourcen) ein Problem festgestellt wird, wird der Knoten automatisch ersetzt und alle auf dem Knoten ausgeführten Jobs werden migriert. Jobs werden nur dann migriert und neu gestartet, wenn die Instanz mehrere Anwendungsknoten aufweist. Sie können die Größe der Instanz mithilfe des [Service-Dashboards](/docs/services/StreamingAnalytics/r_service_dashboard.html) oder mithilfe der [{{site.data.keyword.streaminganalyticsshort}}-v1-REST-API ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/apidocs/streaming-analytics-v1){:new_window} für [v1-Servicepläne](/docs/services/StreamingAnalytics/service_plans.html) ändern. Verwenden Sie für v2-Servicepläne die [v2-REST-API ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")https://console.bluemix.net/apidocs/streaming-analytics-v2).{:new_window}
{:shortdesc}

In diesem Video wird veranschaulicht, wie Sie die Größe der Instanz mithilfe des Service-Dashboards ändern können:

<iframe width="560" height="315" title="Größe der Instanz ändern" src="https://www.youtube.com/embed/zbZ9am9UhPw?rel=0" frameborder="0" allowfullscreen>Größe der Instanz ändern</iframe>

## Konsistente Regionen
Aufgrund von Geschäftsanforderungen ist es für einige Anwendungen erforderlich, dass alle Tupel mindestens einmal verarbeitet werden. Funktionale Erweiterungen für {{site.data.keyword.streamsshort}} umfassen Operatoren und Annotationen, die die Definition einer Region ermöglichen, bei der während der Streamverarbeitung keine Tupel verloren gehen. Tupel in einer konsistenten Region werden mindestens einmal verarbeitet.

Sie können Streams-Anwendungen mit definierten konsistenten Regionen in {{site.data.keyword.streaminganalyticsshort}} ausführen und überwachen. Wenn Sie einen {{site.data.keyword.streaminganalyticsshort}}-Service erstellen, ist die Instanz bereits für die Verwendung konsistenter Regionen konfiguriert.

Bei einer konsistenten Region handelt es sich um ein Unterdiagramm, in dem die Status der Operatoren konsistent werden, indem alle Tupel und Interpunktionszeichen innerhalb definierter Punkte in einem Stream verarbeitet werden. Auf diese Weise werden Tupel innerhalb des Unterdiagramms mindestens einmal verarbeitet. Für die konsistente Region findet in regelmäßigen Abständen eine Bereinigung der aktuelle Tupel statt. Alle Tupel in der konsistenten Region werden bis zum Ende des Unterdiagramms verarbeitet. Bei Operatoren mit speicherinternem Status wird automatisch eine Serialisierung und Speicherung vorgenommen. Dies erfolgt am Prüfpunkt für jeden Operator in der Region.

Sie können nun sowohl Java- als auch SPL-Anwendungen mit garantierter Tupelverarbeitung schreiben und in {{site.data.keyword.streaminganalyticsshort}} bereitstellen.

Sie können den Anfang einer konsistenten Region mit der Annotation `@consistent` bei einem geeigneten Operator definieren. {{site.data.keyword.streamsshort}} bestimmt den Bereich der konsistenten Region automatisch, Sie können jedoch den Endoperator der Region mit der Annotation `@autonomous` ändern. Die definierte konsistente Region stellt regelmäßig einen konsistenten Status her.

Die [{{site.data.keyword.streamsshort}}-Dokumentation ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.1/com.ibm.streams.dev.doc/doc/consistentregions.html) enthält weitere Details zur Verwendung konsistenter Regionen in Streams-Anwendungen.
