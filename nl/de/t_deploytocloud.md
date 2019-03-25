---

copyright:
  years: 2015, 2019
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streams-Anwendungen in der Cloud bereitstellen
{: #t_deploytocloud}

Sie können Ihre {{site.data.keyword.streamsshort}}-Anwendungen für eine {{site.data.keyword.streaminganalyticsshort}}-Instanz bereitstellen, die in {{site.data.keyword.Bluemix_short}} ausgeführt wird.
{:shortdesc}

{{site.data.keyword.streamsshort}}-Anwendungen werden in {{site.data.keyword.streamsshort}} Processing Language (SPL), Java, Scala oder Python in einer {{site.data.keyword.streamsshort}}-Umgebung geschrieben. Sie können jetzt Streams-Python-Anwendungen ohne {{site.data.keyword.streamsshort}}-Umgebung entwickeln. Weitere Informationen finden Sie im Abschnitt [Bereitstellung von {{site.data.keyword.streamsshort}}-Python-Anwendungen für die Cloud](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_deploytocloud#t_deploypython)


{{site.data.keyword.streaminganalyticsshort}} enthält keine {{site.data.keyword.streamsshort}}-Entwicklungsumgebung in der Cloud, aber Sie können die Anwendungen, die Sie lokal entwickeln, in der Cloud bereitstellen.

Bevor Sie mit der Arbeit beginnen, müssen Sie den Popup-Blocker Ihres Browsers inaktivieren, um die {{site.data.keyword.streaminganalyticsshort}}-Konsole anzuzeigen.

Gehen Sie wie folgt vor, um Ihre {{site.data.keyword.streamsshort}}-Anwendungen für die Cloud bereitzustellen:

1. Richten Sie die Entwicklungsumgebung ein, um Ihre Anwendung zu entwickeln und zu testen.

	Wenn Sie eine {{site.data.keyword.streamsshort}}-Umgebung verwenden möchten, können Sie die [{{site.data.keyword.streamsshort}} Quick Start Edition ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window} für [v1-Servicepläne](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) herunterladen. Verwenden Sie die [{{site.data.keyword.streamsshort}} Quick Start Edition mit Docker ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi){:new_window} für [v2-Servicepläne](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans).

2. Entwickeln Sie Ihre Streaming-Anwendung in Ihrer Entwicklungsumgebung. In der {{site.data.keyword.streamsshort}}-Entwicklungsumgebung können Sie Streams Studio oder die Befehlszeilentools verwenden, um Ihre Anwendung zu entwickeln.

3. Stellen Sie sicher, dass Ihre Streaming-Anwendung in Ihrer Entwicklungsumgebung ordnungsgemäß ausgeführt wird.
**Hinweis:** Sie müssen die Anwendungen in Red Hat Enterprise Linux (RHEL) 7.x kompilieren, wenn Sie die v2-Servicepläne verwenden, bzw. mit RHEL 6.5, wenn Sie v1-Servicepläne verwenden.

4. Übergeben Sie das Anwendungsbundle (die Datei mit der Erweiterung .sab), die Ihrer SPL-, Java-, Scala- oder Python-Anwendung zugeordnet ist, an die Serviceinstanz in der Cloud. Verwenden Sie dazu eine der folgenden Methoden:
	* Verwenden Sie die {{site.data.keyword.streaminganalyticsshort}}-Konsole, um das Anwendungsbundle zu übergeben.

  * Erstellen Sie eine Anwendung in {{site.data.keyword.Bluemix_notm}} und fügen Sie die {{site.data.keyword.streamsshort}}-Anwendung zu dieser hinzu. Steuern Sie sie mithilfe der [{{site.data.keyword.streaminganalyticsshort}}-v1-REST-API ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} für [v1-Servicepläne](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) oder mithilfe der [{{site.data.keyword.streaminganalyticsshort}}-v2-REST-API ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window} für v2-Servicepläne.

Ihre Anwendung wurde jetzt in der Cloud bereitgestellt. Sie können Ihre Anwendung mit dem {{site.data.keyword.streaminganalyticsshort}}-Service überwachen. Sie haben auch die Möglichkeit, mehr als eine Anwendung (Dateien mit der Erweiterung .sab) an die Serviceinstanz zu übergeben. Dies können beliebig viele sein.

{{site.data.keyword.streamsshort}} unterstützt auch verschiedene Java™-Entwicklungskits, die Sie zur Entwicklung Ihrer Anwendungen verwenden können. Weitere Informationen zur Java-Unterstützung in {{site.data.keyword.streamsshort}} finden Sie in [Unterstützte Java-Entwicklungskits für die Anwendungsentwicklung ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.install.doc/doc/ibminfospherestreams-install-prerequisites-java-supported-sdks.html){:new_window}.

## Streams-Python-Anwendungen in der Cloud bereitstellen
{: #t_deploypython}

Stellen Sie Ihre {{site.data.keyword.streamsshort}}-Python-Anwendungen für einen {{site.data.keyword.streaminganalyticsshort}}-Service bereit, der in {{site.data.keyword.Bluemix_short}} ausgeführt wird. Sie benötigen dafür keine {{site.data.keyword.streamsshort}}-Installation.
{:shortdesc}

Mit der [{{site.data.keyword.streamsshort}}-Python-Anwendungs-API ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features){:new_window}, die im 'streamsx'-Paket enthalten ist, können Sie Python-Anwendungen für den {{site.data.keyword.streaminganalyticsshort}}-Service bereitstellen. Im Lernprogramm [Entwicklung für den {{site.data.keyword.streaminganalyticsshort}}-Service ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html){:new_window} wird anhand eines Beispiels veranschaulicht, wie eine einfache Python-Anwendung für den {{site.data.keyword.streaminganalyticsshort}} erstellt und bereitgestellt werden kann.

{{site.data.keyword.DSX_full}} unterstützt auch die Bereitstellung von Python-Anwendungen in interaktiven Jupyter-Notebooks. Weitere Informationen finden Sie in [Entwicklung von Python-Anwendungen für {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_develop_apps_python). 
