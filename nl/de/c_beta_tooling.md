---

copyright:
  years: 2015, 2018
lastupdated: "2017-12-15"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Entwicklungstools und Entwicklungsumgebung
{: #c_beta_tooling}


Die folgenden Überlegungen beziehen sich auf die Tools und die Umgebung, die Sie
zur Entwicklung Ihrer {{site.data.keyword.streaminganalyticsshort}}-Anwendungen verwenden.
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}} enthält keine {{site.data.keyword.streamsshort}}-Entwicklungsumgebung oder Streams Studio in der Cloud. Entwickeln Sie Ihre Anwendungen in einer lokal installierten {{site.data.keyword.streamsshort}}-Umgebung und übergeben Sie sie als Anwendungsbundles. Wenn Sie nicht über die Entwicklungsumgebung verfügen, können Sie die [{{site.data.keyword.streamsshort}} Quick Start Edition ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/) kostenfrei herunterladen.
* Kompilieren Sie das Anwendungsbundle in einer Red Hat Enterprise Linux 6.5-Umgebung oder einer funktional entsprechenden CentOS-Version, um die Kompatibilität sicherzustellen.

  **Hinweis:** Bei der Verwendung der Beta-Pläne 'Einstieg' und 'Erweitert' müssen Sie das Anwendungsbundle in einer RHEL 7-Umgebung oder einer äquivalenten CentOS-Version kompilieren. Sie können [{{site.data.keyword.streamsshort}} Quick Start Edition for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) verwenden, falls Sie nicht über eine kompatible Entwicklungsumgebung verfügen. Details hierzu finden Sie in der [Dokumentation zu den Beta-Plänen](/docs/services/StreamingAnalytics/beta_plans.html).

* Legen Sie in Ihrer {{site.data.keyword.streamsshort}}-Entwicklungsumgebung die Umgebungsvariable `JAVA_HOME` auf $STREAMS_INSTALL/java fest.
