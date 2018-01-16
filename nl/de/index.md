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


# Streaming Analytics - Übersicht
{: #gettingstarted}

{{site.data.keyword.streaminganalyticsfull}} basiert auf der Technologie von {{site.data.keyword.streamsshort}}, einer zukunftsweisenden Analyseplattform, die Sie verwenden können, um Informationen zu erfassen, zu analysieren und zu korrelieren, die in Echtzeit aus verschiedenen Arten von Datenquellen abgerufen werden. Wenn Sie eine Instanz des {{site.data.keyword.streaminganalyticsshort}}-Service erstellen, erhalten Sie so eine eigene Instanz von {{site.data.keyword.streamsshort}}, die in {{site.data.keyword.Bluemix_short}} ausgeführt wird und somit bereit ist, Ihre {{site.data.keyword.streamsshort}}-Anwendungen auszuführen.
{:shortdesc}

Sie können sofort mit der Verwendung von {{site.data.keyword.streaminganalyticsshort}} beginnen, indem Sie die [Starteranwendungen](/docs/services/StreamingAnalytics/t_starter_app_deploy.html){:new_window} ausführen.

Als ersten Schritt bei der Arbeit mit {{site.data.keyword.streaminganalyticsshort}} verwenden Sie eine der folgenden Methoden, um die Anwendungsbundledatei (die Datei mit der Erweiterung .sab) zu übergeben, die Ihrer SPL-, Java™-, Python- oder Scala Streams-Anwendung zugeordnet ist:
* Verwenden Sie die Schaltfläche **Job übergeben** in der {{site.data.keyword.streaminganalyticsshort}}-Konsole.
* Entwickeln Sie eine Anwendung in {{site.data.keyword.Bluemix_notm}} und fügen Sie die {{site.data.keyword.streamsshort}}-Anwendung hinzu. Steuern Sie sie mithilfe der [{{site.data.keyword.streaminganalyticsshort}}-REST-API ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://console.ng.bluemix.net/apidocs/220){:new_window}.

Sie können {{site.data.keyword.streaminganalyticsshort}} zusammen mit anderen {{site.data.keyword.Bluemix_short}}-Services verwenden, z. B. mit {{site.data.keyword.cloudant}} und {{site.data.keyword.messagehub}}. In den [Lernprogrammen für die Integration mit anderen {{site.data.keyword.Bluemix_short}}-Services](/docs/services/StreamingAnalytics/r_integrating_cloudant_rest.html){:new_window} finden Sie Beispiele, die Ihnen beim Einstieg helfen.

Wenn Sie Ihre eigenen Anwendungen noch weitergehend einsetzen wollen, können Sie eine {{site.data.keyword.streamsshort}}-Entwicklungsumgebung einrichten und Sie müssen Ihre Anwendung für die Cloud vorbereiten. Wenn Sie nicht über eine {{site.data.keyword.streamsshort}}-Umgebung verfügen, können Sie die {{site.data.keyword.streamsshort}} Quick Start Edition kostenfrei von der [{{site.data.keyword.streamsshort}}-Produktseite herunterladen. ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/analytics/us/en/technology/stream-computing/#products)

Wenn Sie keine Erfahrung mit der Entwicklung von {{site.data.keyword.streamsshort}}-Anwendungen haben, können Sie sich hierüber anhand der zur Verfügung stehenden Ressourcen informieren. Weitere Informationen finden Sie im [{{site.data.keyword.streamsshort}} Knowledge Center ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.2.0/com.ibm.streams.welcome.doc/doc/kc-homepage.html){:new_window}

Wenn Sie bereits über eine SPL-Anwendung verfügen, die Sie lokal ausführen, müssen Sie [Ihre Anwendung für die Cloud vorbereiten. ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/streamsdev/docs/getting-spl-application-ready-cloud/){:new_window}

**Anmerkung:** Sie müssen Ihre Anwendungen unter Red Hat Enterprise Linux (RHEL) 6.5 oder einer entsprechenden CentOS-Version mit Intel-Prozessoren kompilieren.
