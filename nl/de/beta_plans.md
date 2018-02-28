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

# Beta-Pläne 'Einstieg' und 'Erweitert'
{: #beta_plans}

Die neuen Beta-Pläne 'Einstieg' und 'Erweitert' des {{site.data.keyword.streaminganalyticsshort}}-Service enthalten eine Reihe funktionaler Erweiterungen und Änderungen gegenüber den vorhandenen Serviceplänen:
{:shortdesc}

**Neue [Die {{site.data.keyword.streamsshort}} Quick Start Edition für Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi):** {{site.data.keyword.streamsshort}} Quick Start Edition ist eine gebührenfreie, nicht für Produktionsumgebungen konzipierte Version von {{site.data.keyword.streamsshort}}. Wenn Sie die Beta-Pläne 'Einstieg' und 'Erweitert' für die Bereitstellung von Anwendungen in {{site.data.keyword.streaminganalyticsshort}} verwenden möchten, müssen Sie die Anwendungen mit der Red Hat Enterprise Linux (RHEL) 7-Version der {{site.data.keyword.streamsshort}} Quick Start Edition kompilieren. In der Veröffentlichung [Beta Development Guide ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/streamsdev/docs/cloud-beta-devguide/) finden Sie Informationen zur Verwendung der neuen Streams Quick Start Edition mit RHEL 7 in einer Docker-Umgebung zum Kompilieren und Bereitstellen Ihrer Anwendungen im Rahmen der neuen {{site.data.keyword.streaminganalyticsshort}}-Beta-Pläne.   

**{{site.data.keyword.streaminganalyticsshort}} v2-REST-API:** Mit der [{{site.data.keyword.streaminganalyticsshort}} v2-REST-API ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#introduction) können Sie Ihre Serviceinstanzen und {{site.data.keyword.streamsshort}}-Jobs verwalten. Die {{site.data.keyword.streaminganalyticsshort}} v2-API wird nur für Serviceinstanzen unterstützt, die im Rahmen eines der neuen Beta-Pläne erstellt wurden. Die [v1-REST-API ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/apidocs/220-streaming-analytics?&language=node#introduction) wird nur für vorhandene {{site.data.keyword.streaminganalyticsshort}}-Instanzen und neue Instanzen unterstützt, die im Rahmen der vorhandenen Servicepläne erstellt werden.

**Neue Starter- und Beispielanwendungen:** Da für die neuen Beta-Pläne die Ausführung von Streams mit RHEL 7 erforderlich ist, können einige der vorhandenen Beispielanwendungen mit den neuen Beta-Plänen nicht verwendet werden. {{site.data.keyword.streaminganalyticsshort}} stellt [neue Starter- und Beispielanwendungen]( https://developer.ibm.com/streamsdev/docs/cloud-beta-samples/) bereit, die einen schnellen Einstieg in die neuen Beta-Pläne ermöglichen.

**Funktionale Erweiterungen bei der Hochverfügbarkeit:** Durch die Definition konsistenter Regionen können Sie Datenverluste in Streams-verarbeitenden Anwendungen vermeiden. Funktionale Erweiterungen für {{site.data.keyword.streamsshort}} umfassen Operatoren und Annotationen, die die Definition einer Region ermöglichen, bei der während der Streamverarbeitung keine Tupel verloren gehen. Tupel in einer konsistenten Region werden mindestens einmal verarbeitet.
Wenn Sie den Beta-Preisstrukturplan 'Einstieg' oder 'Erweitert' verwenden, können Sie nun Streams-Anwendungen mit [definierten konsistenten Regionen in {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/consistentregions.html) ausführen und überwachen.

**Neue Problembestimmungsfeatures:** Die Beta-Pläne 'Einstieg' und 'Erweitert' enthalten eine Reihe funktionaler Erweiterungen, die Sie bei der schnellen Fehlerbestimmung und -behebung in Ihren Anwendungen unterstützen. Weitere Details finden Sie im Abschnitt [Die {{site.data.keyword.streaminganalyticsshort}}-Konsole bietet zusätzliche Möglichkeiten zum Suchen und Beheben von Fehlern (Beta-Pläne) ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link").](https://wp.me/p4IICn-4cx)

**Überwachung des Operatorverhaltens und garantierte Tupelverarbeitung in der Cloud:** {{site.data.keyword.streamsshort}} stellt Metriken bereit, mit denen Sie den Status der {{site.data.keyword.streamsshort}}-Services auswerten, Leistungsprobleme diagnostizieren und den Durchsatz von Anforderungen analysieren können. Sie können die Streams-Konsole in {{site.data.keyword.streaminganalyticsshort}} verwenden, um [das Verhalten von Operatoren zu überwachen und die Ressourcenoptimierung sicherzustellen ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link").](https://wp.me/p4IICn-4bH)
