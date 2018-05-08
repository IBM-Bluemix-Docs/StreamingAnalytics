---

copyright:
  years: 2015, 2018
lastupdated: "2018-04-24"

---

<!-- Attribute definitions -->
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics - Fehlerbehebung
{: #ts_StreamingAnalytics}

Hier finden Sie Antworten auf häufig gestellte Fragen zur Verwendung von {{site.data.keyword.streaminganalyticsshort}} unter {{site.data.keyword.Bluemix_short}}.
{:shortdesc}

## Wenn ich den Service starte, werde ich zur Eingabe von Berechtigungsnachweisen aufgefordert, um mich an der Konsole anmelden zu können.
{: #log_in_console}

Wenn Sie {{site.data.keyword.streaminganalyticsshort}} starten, werden Sie aufgefordert, Berechtigungsnachweise für die Anmeldung an der Servicekonsole einzugeben.
{:shortdesc}

Sie starten einen {{site.data.keyword.streaminganalyticsshort}}-Service, den Sie zuvor erstellt haben, und anstatt direkt Zugriff auf die Servicekonsole zu erhalten, wird eine Anmeldeseite angezeigt, auf der Sie zur Eingabe der Berechtigungsnachweise aufgefordert werden.
{: tsSymptoms}

Die Serviceinfrastruktur wurde aktualisiert und Ihr Browser-Cache verhindert, dass der Service die Aktualisierung aufgreift.
{: tsCauses}

Löschen Sie Ihren Browser-Cache, um sicherzustellen, dass Sie die aktuelle Version der Servicekonsole erhalten.
{: tsResolve}

## Meine Anwendung weist einen nicht einwandfreien Zustand auf
{: #app_unhealthy}

Sie können Ihre Anwendung nicht korrekt ausführen und der Allgemeinzustand ist `nicht einwandfrei`.
{:shortdesc}

Sie übergeben eine Anwendung an die Serviceinstanz, die Anwendung startet, schlägt dann aber sofort fehl und der Allgemeinzustand ist `nicht einwandfrei`. Der folgende Fehler ist in der Protokolldatei dokumentiert: `/lib64/libc.so.6: Version GLIBC_2.14 nicht gefunden`.
{: tsSymptoms}

Sie haben die Anwendung nicht mithilfe eines RHEL 7.x-Betriebssystems oder einer entsprechenden CentOS-Version kompiliert.
{: tsCauses}

Sie müssen die Anwendung in Red Hat Enterprise Linux (RHEL) 7.x erneut kompilieren, wenn Sie die [v2-Servicepläne](/docs/services/StreamingAnalytics/service_plans.html) verwenden, bzw. mit RHEL 6.5, wenn Sie [v1-Servicepläne](/docs/services/StreamingAnalytics/service_plans.html) verwenden. Verwenden Sie dabei Intel-Prozessoren. Übergeben Sie Ihre Anwendung erneut an die Serviceinstanz. Sie können die [{{site.data.keyword.streamsshort}} Quick Start Edition mit Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) herunterladen, wenn Sie nicht über eine kompatible Entwicklungsumgebung verfügen und wenn Sie die v2-Servicepläne verwenden. Wenn Sie die v1-Servicepläne verwenden, laden Sie die [{{site.data.keyword.streamsshort}} QSE ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window}.
{: tsResolve}
