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

# Unterstützte Toolkits und Adapter
{: #compatible_toolkits}

Diese Analysetoolkits und Adapter werden von {{site.data.keyword.streaminganalyticsshort}} unterstützt.
{:shortdesc}

| Toolkits                        | Beschreibung							                  |
| --------------------------------| --------------------------|
| [Complex Event Processing (CEP) ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://ibm.co/2zOwODa)    |	Stellt den Operator 'MatchRegex' bereit, der das Complex Event Processing ermöglicht.  		 |
| [Datetime ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://ibmstreams.github.io/streamsx.datetime/)	|	Gruppe von Dienstprogrammen zur Verarbeitung von Datums-, Uhrzeit- und Zeitmarkenangaben.	 |
| [HBase![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.hbase/)        | Ermöglicht es Streams-Anwendungen, eine Verbindung zur Apache HBase herzustellen.	 	   |
| [HDFS ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.hdfs/)          | Stellt Operatoren und Funktionen bereit, die mit Hadoop Distributed File System interagieren.	|
| [Internet (Inet) ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.inet)|  Richtet den Fokus auf die Interaktion mit Daten, die im Netz gehostet werden.				       |
| [IoT ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.iot/)            | Bietet die Integration mit Internet of Things (IoT) mit IBM Watson IoT Platform, entweder in {{site.data.keyword.Bluemix_notm}} oder lokal ({{site.data.keyword.streamsshort}}). |
| [JDBC ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.jdbc/)          | Ermöglicht es Streams-Anwendungen, über JDBC mit Datenbanken zu arbeiten.		   |
| [JSON ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.json/)          | Hier finden Sie Informationen zum Konvertieren von Daten aus dem JSON-Format in das Streams-Tupelformat und zurück.   		|
| [Kafka ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://ibmstreams.github.io/streamsx.kafka/)       | Ermöglicht Streams-Anwendungen die einfache Integration mit Apache Kafka. 	 |
| [MessageHub ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://ibmstreams.github.io/streamsx.messagehub/) | Ermöglicht es Streams-Anwendungen, mit MessageHub zu arbeiten.			     |
| [Messaging ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://ibmstreams.github.io/streamsx.messaging/)   |  	Richtet den Fokus auf die Interaktion mit den gängigen Nachrichtenübertragungssystemen wie Kafka, MQTT, JMS und XMS.	<br>**Hinweis**: Um JMSSource, JMSSink, XMSSource oder XMSSink mit WebSphere MQ verwenden zu können, führen Sie die folgenden Schritte in Ihrer Entwicklungsumgebung aus: <br>1. Navigieren Sie zu [IBMStreams on GitHub ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://github.com/IBMStreams){:new_window} und laden Sie das Messaging Toolkit (com.ibm.streamsx.messaging) Version 3.0.0 oder höher in Ihre Entwicklungsumgebung herunter.<br>2. Verwenden Sie das Toolkit in Version 5.1.0 oder höher, um einen Build Ihrer Anwendung zu erstellen.<br>3. Stellen Sie die erforderliche Datei mit der Erweiterung `.bindings` in das Verzeichnis `/etc` Ihrer Anwendung, um sie in das {{site.data.keyword.streamsshort}}-Anwendungsbundle aufzunehmen.	    |
| [Mining ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://ibm.co/2y3i5au)              	   	            |  Enthält Operatoren, mit denen Datenströme mithilfe von Modellen gefiltert werden können. <br> **Einschränkung:** Dieses Toolkit wird nicht unterstützt, wenn Sie die [v2-Servicepläne](/docs/services/StreamingAnalytics/service_plans.html) verwenden, da das Anwendungsbundle in einer RHEL 7-Umgebung oder einer äquivalenten CentOS-Version kompiliert werden muss. 	     |
| [RabbitMQ ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://ibmstreams.github.io/streamsx.rabbitmq/)     |  Stellt Operatoren bereit, die es der Streams-Anwendung ermöglichen, Rabbit MQ-Nachrichten zu lesen und zu senden.  |
| [R-project ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://ibm.co/2h7D9lu)          	   	              |   Enthält den Operator 'RScript', den Sie verwenden können, um R-Befehle auszuführen und um komplexe Data-Mining-Algorithmen zur Erkennung relevanter Muster in Datenstreams anzuwenden.			     |
| [Topology ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.topology/)      | Hier finden Sie Informationen zum Erstellen von Python-Streaming-Anwendungen für den {{site.data.keyword.streaminganalyticsshort}}-Service auf der {{site.data.keyword.Bluemix_notm}}-Plattform und in {{site.data.keyword.streamsshort}}.		     |
| [DPS ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.dps/) |	 Ermöglicht es mehreren Anwendungen, die Verarbeitungselemente (Processing Elements, PE) auf einer oder mehreren Maschinen ausführen, anwendungsspezifische Statusinformationen gemeinsam zu nutzen.<br>**Einschränkung:** Nur REDIS wird als Datenbank-Back-End unterstützt.	| 	 	 	
| [Geospatial ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://ibm.co/2h9x0VR) 	     |	Enthält Operatoren und Funktionen, die die effiziente Verarbeitung und Indexierung von Positionsdaten vereinfachen.<br>**Einschränkung:** Operatoren, die den Modus für gemeinsam genutzte Karten verwenden, werden nicht unterstützt (`MapStore`, `PointMapMatcher` im Modus für gemeinsam genutzte Karten).		 |
| [TEDA ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://ibm.co/2z9DS00)	   | 	Bietet eine Reihe von generischen Operatoren, die in Telekommunikationsanwendungen genutzt werden, und stellt ein Anwendungsframework zur Verfügung, mit dem Sie neue File-to-File-Anwendungen einrichten können. Führen Sie als ersten Schritt die [TEDA-Lernprogramme![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.tutorial.teda/) aus. Alle Operatoren und Funktionen des Toolkits werden unterstützt. <br>**Einschränkung:** Das Anwendungsframework wird nicht unterstützt.	 	 |
| [TimeSeries ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://ibm.co/2zEPILZ)	 	  | Mit den Operatoren und Funktionen im TimeSeries Toolkit können Zeitreihendaten aufbereitet, analysiert und modelliert werden. <br>**Einschränkung:** Veraltete Operatoren werden nicht unterstützt.	   |
| [{{site.data.keyword.cos_short}} ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://bit.ly/2Ggp03T)	 	  | Stelle einfache Operatoren und native Funktionen für Datenlese- und -schreibvorgänge in {{site.data.keyword.cos_short}} bereit. Das Toolkit unterstützt mit S3 kompatibles {{site.data.keyword.cos_short}}.	   |

*Tabelle 1. Unterstützte Toolkits*

## Sonstige Toolkits und Operatoren
{: #other_operators}

Auch andere Operatoren einschließlich der Toolkitoperatoren, die Sie für Ihre eigenen Anforderungen entwickelt haben, können von {{site.data.keyword.streaminganalyticsshort}} unterstützt werden.
{:shortdesc}

Toolkits müssen die folgenden Kriterien erfüllen, um mit {{site.data.keyword.streaminganalyticsshort}} kompatibel zu sein:

1. Sie setzen keine zusätzlich vorinstallierte Software auf den Anwendungsknoten Ihrer Serviceinstanz voraus.
2. Alle Konfigurationsinformationen, die für das Toolkit benötigt werden, können mithilfe des Toolkits in das Anwendungsbundle integriert werden.
