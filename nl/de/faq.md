---

copyright:
  years: 2015, 2017
lastupdated: "2017-12-15"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Häufige Fragen
{: #faq}

## Wie melde ich mich beim Streaming Analytics-Service an?
{: #signup notoc}  

Informationen zu den {{site.data.keyword.streaminganalyticsshort}}-Serviceplänen finden Sie auf der [{{site.data.keyword.Bluemix_short}}-Katalogseite](https://console.ng.bluemix.net/catalog/services/streaming-analytics).

## Welche Version des Streaming Analytics-Service verwende ich?
{: #version notoc}   

Verbesserungen werden in regelmäßigen Abständen an alle {{site.data.keyword.streaminganalyticsshort}}-Services per Push-Operation übertragen. Sie verwenden stets die neueste Version des verwalteten Service und es gibt keine Produktversion und keinen Produktänderungsstand, die bzw. den Sie im Auge behalten müssen.

## Welche Verwaltungsaufgaben übernimmt IBM?
{: #ibm_manage notoc}   

Die Installation, Software-Upgrades, das Erstellen und Verwalten von Domänen sowie die Hardwarewartung werden übernommen. Der Service umfasst eine Statusüberwachung rund um die Uhr.


## Für welche Aufgaben bin ich zuständig?  
{: #responsible notoc}

Sie schreiben die Anwendungen für die Ausführung in einer {{site.data.keyword.streaminganalyticsshort}}-Service- und Streams-Instanz lokal und stellen sicher, dass diese korrekt funktionieren und die Leistungsanforderungen erfüllen. Darüber hinaus sind Sie für eine gegebenenfalls angewandte anwendungsspezifische Überwachung verantwortlich. 

## Wird HA-Unterstützung (Hochverfügbarkeit) bereitgestellt?
{: #ha notoc}

Die Hochverfügbarkeit wird von IBM verwaltet. {{site.data.keyword.streaminganalyticsshort}} ist für die HA-Unterstützung konfiguriert. Falls es zu einer Funktionsübernahme kommt, stehen zusätzliche Serverressourcen zur Verfügung.

## Wie werden Sicherheitaspekte für den Streaming Analytics-Service gehandhabt?
{: #security notoc}  

Die Sicherheit wird vollständig von IBM verwaltet. Für jeden Service werden Berechtigungsnachweise generiert und Ihnen zur Verfügung gestellt. Sicherheitsupdates werden von IBM verwaltet und angewendet, sobald sie verfügbar sind.

## Muss ich einen Streaming Analytics-Service konfigurieren?  
{: #configure notoc}

Der Service wird erstellt und von IBM vollständig gewartet. Jeder Service besteht aus einem dedizierten Satz von Anwendungsknoten.

## Wie entwickle ich Streams-Anwendungen?
{: #streamsapp notoc}

Sie müssen Streams-Anwendungen lokal mithilfe der kostenfreien [{{site.data.keyword.streamsshort}} Quick Start Edition ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/) oder der [{{site.data.keyword.streamsshort}} Developer Edition ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://www.ibm.com/support/docview.wss?uid=swg24042775) entwickeln.

Falls Sie über eine lokale {{site.data.keyword.streamsshort}}-Installation verfügen, können Sie auch diese verwenden. Lokal entwickelte und kompilierte Anwendungen können dann nahtlos als Paket für einen Streams-Service in der Cloud bereitgestellt werden.

Wenn Sie jedoch Ihre Python-Anwendungen in der Cloud ausführen möchten, müssen Sie {{site.data.keyword.streamsshort}} nicht lokal installieren. Verwenden Sie einfach den `STREAMING\_ANALYTICS\_SERVICE`-Kontext, um Ihre Python-Anwendungen an den {{site.data.keyword.streaminganalyticsshort}}-Service zu übergeben. Sie können die Anwendungen in einer Python-Standardentwicklungsumgebung oder in einem interaktiven Jupyter-Notebook entwickeln, es muss jedoch Python Version 3.5 verwendet werden.

Eine Anleitung zur Entwicklung von Anwendungen finden Sie im [{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.streaminganalyticsshort}}-Entwicklerhandbuch ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/streamsdev/docs/bluemix-streaming-analytics-development-guide/).

## Kann ich mich direkt bei einem Streaming Analytics-Service-Host anmelden?
{: #host notoc}  

Nein. Eine direkte Anmeldung beim Server mit Telnet oder SSH (Secure Shell) wird nicht unterstützt. Sie können keine zusätzliche Software installieren und Sie können Software, bei der es sich nicht um Streams-Software handelt, nicht auf einem Streams-Host ausführen.

## Kann ich auf das Dateisystem des Streaming Analytics-Service zugreifen?
{: #filesystem notoc}  

Nur Ihre Streams-Anwendungen können direkt auf das Dateisystem eines Streams-Hosts zugreifen.

Es existieren cloudfähige Alternativen für Lösungen, die einen Mechanismus zur Interaktion von Streams mit anderen Lösungskomponenten benötigen. Sie können andere Quellen- und Zielprotokolle anstelle von Dateien verwenden. Ein Beispiel hierfür sind cloudbasierte Data-Stores.

## Wie können die Streaming Analytics-Serviceanwendungen auf die Unternehmensdaten meiner Organisation zugreifen?
{: #access notoc}  

Sie können den [{{site.data.keyword.Bluemix_notm}} Secure Gateway-Service](https://console.ng.bluemix.net/catalog/services/secure-gateway) verwenden, um eine sichere Verbindung zwischen Streams-Anwendungen und Ihrem Unternehmen herzustellen.

## Werden alle Features für lokale IBM Streams-Implementierungen auch vom Streaming Analytics-Service in der Cloud unterstützt?
{: #features notoc}

Einige der Features, die für den {{site.data.keyword.streaminganalyticsshort}}-Service nicht unterstützt werden, sind im Folgenden aufgeführt:

  - Administrative Aufgaben für eine Instanz, für die eine Domänenberechtigung erforderlich ist. Beispiel: Hinzufügen von benutzerdefinierten Host-Tags oder Erstellen einer Jobgruppe.
  - Konsistente Regionsprüfpunkte.
  - Einige der Toolkitoperatoren werden nicht unterstützt. Informationen hierzu finden Sie in [Unterstützte Toolkits und Adapter](/docs/services/StreamingAnalytics/compatible_toolkits.html).
  - Die Streams-JMX-API.

## Wo finde ich weitere Informationen zum Streaming Analytics-Service?
{: #roadmap notoc}

Der IBM developerWorks®-Artikel [Roadmap für den {{site.data.keyword.streaminganalyticsshort}}-Service in {{site.data.keyword.Bluemix_notm}} ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/streamsdev/docs/roadmap-for-streaming-analytics-service-on-bluemix/) enthält eine Anleitung dazu, wie Sie sich mit dem Service vertraut machen können, sowie Links zu informativen Blogs, Demos und Artikeln.
