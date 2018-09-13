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

# Entwicklungstools und Entwicklungsumgebung
{: #c_beta_tooling}


Die folgenden Überlegungen beziehen sich auf die Tools und die Umgebung, die Sie
zur Entwicklung Ihrer {{site.data.keyword.streaminganalyticsshort}}-Anwendungen verwenden.
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}} enthält keine {{site.data.keyword.streamsshort}}-Entwicklungsumgebung oder Streams Studio in der Cloud. Entwickeln Sie Ihre Anwendungen in einer lokal installierten {{site.data.keyword.streamsshort}}-Umgebung und übergeben Sie sie als Anwendungsbundles. Wenn Sie nicht über die Entwicklungsumgebung verfügen, können Sie die [{{site.data.keyword.streamsshort}} Quick Start Edition mit Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) für [v2-Servicepläne](/docs/services/StreamingAnalytics/service_plans.html) herunterladen; wenn Sie [v1-Servicepläne](/docs/services/StreamingAnalytics/service_plans.html) verwenden, können Sie das [{{site.data.keyword.streamsshort}} Quick Start Edition-VM-Image ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window} kostenfrei herunterladen.
* Kompilieren Sie Ihre Anwendungen in Red Hat Enterprise Linux (RHEL) 7.x, wenn Sie die v2-Servicepläne verwenden, bzw. mit RHEL 6.5, wenn Sie v1-Servicepläne verwenden, und verwenden Sie dabei Intel-Prozessoren.
* Legen Sie in Ihrer {{site.data.keyword.streamsshort}}-Entwicklungsumgebung die Umgebungsvariable `JAVA_HOME` auf $STREAMS_INSTALL/java fest.
