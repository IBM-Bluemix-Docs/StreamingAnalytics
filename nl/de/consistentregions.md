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


# Funktionale Erweiterungen bei der Hochverfügbarkeit
{: #consistentregions}

Aufgrund von Geschäftsanforderungen ist es für einige Anwendungen erforderlich, dass alle Tupel mindestens einmal verarbeitet werden. Funktionale Erweiterungen für {{site.data.keyword.streamsshort}} umfassen Operatoren und Annotationen, die die Definition einer Region ermöglichen, bei der während der Streamverarbeitung keine Tupel verloren gehen. Tupel in einer konsistenten Region werden mindestens einmal verarbeitet.


Wenn Sie den Beta-Preisstrukturplan 'Einstieg' oder 'Erweitert' verwenden, können Sie nun Streams-Anwendungen mit definierten konsistenten Regionen in {{site.data.keyword.streaminganalyticsshort}} ausführen und überwachen. Wenn Sie einen {{site.data.keyword.streaminganalyticsshort}}-Service im Rahmen des Beta-Plans 'Einstieg' oder 'Erweitert' erstellen, ist die Instanz bereits für die Verwendung konsistenter Regionen konfiguriert.

Bei einer konsistenten Region handelt es sich um ein Unterdiagramm, in dem die Status der Operatoren konsistent werden, indem alle Tupel und Interpunktionszeichen innerhalb definierter Punkte in einem Stream verarbeitet werden. Auf diese Weise werden Tupel innerhalb des Unterdiagramms mindestens einmal verarbeitet. Für die konsistente Region findet in regelmäßigen Abständen eine Bereinigung der aktuelle Tupel statt. Alle Tupel in der konsistenten Region werden bis zum Ende des Unterdiagramms verarbeitet. Bei Operatoren mit speicherinternem Status wird automatisch eine Serialisierung und Speicherung vorgenommen. Dies erfolgt am Prüfpunkt für jeden Operator in der Region.

Sie können nun sowohl Java- als auch SPL-Anwendungen mit garantierter Tupelverarbeitung schreiben und in {{site.data.keyword.streaminganalyticsshort}} bereitstellen.

Sie können den Anfang einer konsistenten Region mit der Annotation `@consistent` bei einem geeigneten Operator definieren. {{site.data.keyword.streamsshort}} bestimmt den Bereich der konsistenten Region automatisch, Sie können jedoch den Endoperator der Region mit der Annotation `@autonomous` ändern. Die definierte konsistente Region stellt regelmäßig einen konsistenten Status her.

Die [{{site.data.keyword.streamsshort}}-Dokumentation ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.1/com.ibm.streams.dev.doc/doc/consistentregions.html) enthält weitere Details zur Verwendung konsistenter Regionen in Streams-Anwendungen.
