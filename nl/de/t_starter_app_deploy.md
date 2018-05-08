---

copyright:
  years: 2015, 2018
lastupdated: "2018-04-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Lernprogramm zur Einführung
{: #starterapps_deploy}

Streaming Analytics ist ein vollständig verwalteter Service, der Ihnen zeitaufwendige Installations-, Administrations- und Verwaltungsaufgaben abnimmt, sodass Sie mehr Zeit für die Entwicklung vobn Streaming-Anwendungen zur Verfügung haben. In diesem Lernprogramm zur Einführung lernen Sie, eine der {{site.data.keyword.streaminganalyticsshort}}-Starteranwendungen per Push-Operation an {{site.data.keyword.Bluemix_notm}} zu übermitteln und dort bereitzustellen.
{:shortdesc}


## Vorbereitung
{: #prereqs}

Führen Sie vor dem Bereitstellen der Starter-Apps diese Schritte aus:

* Nehmen Sie eine Registrierung für ein [{{site.data.keyword.Bluemix_notm}}-Konto ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://console.{DomainName}/registration){:new_window} vor.
* Erstellen Sie eine Instanz des {{site.data.keyword.streaminganalyticsshort}}-Service in Ihrer {{site.data.keyword.Bluemix_notm}}-Organisation. Sie können die Instanz direkt über die [{{site.data.keyword.streaminganalyticsshort}}-Seite im {{site.data.keyword.Bluemix_notm}}-Servicekatalog ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://console.{DomainName}/catalog/services/streaming-analytics/){:new_window} erstellen.  
* [Installieren Sie die {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://console.{DomainName}/docs/cli/reference/bluemix_cli/get_started.html#getting-started).



## Schritt 1: App erstellen und mit dem Service verbinden
{: #create_connect}

1. Erstellen Sie eine Anwendung in {{site.data.keyword.Bluemix_notm}}:

    a. Wählen Sie im {{site.data.keyword.Bluemix_notm}}-Menü **Cloud Foundry-Apps** aus und klicken Sie auf **Ressource erstellen**.

    b. Wählen Sie die {{site.data.keyword.sdk4node}}-Laufzeit für die Event Detection- oder Event Detection v2-Starter-Apps aus.

    Merken Sie sich den Namen, den Sie der Anwendung geben. Sie benötigen ihn zu einem späteren Zeitpunkt wieder.
1. Stellen Sie eine Verbindung von der {{site.data.keyword.streaminganalyticsshort}}-Serviceinstanz zu Ihrer Anwendung her und führen Sie ein erneutes Staging für die Anwendung durch.

## Schritt 2: Starteranwendung einrichten
{: #setup_app}

1. Wenn Sie die [v1-Servicepläne](/docs/services/StreamingAnalytics/service_plans.html) verwenden, laden Sie die Starter-App [Event Detection ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection) herunter. Laden Sie die Starter-App [Event Detection v2 ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://streams-github-samples.mybluemix.net/?get=QuickStart%2FBeta201801%2FEventDetectionV2) für [v2-Servicepläne](/docs/services/StreamingAnalytics/service_plans.html) herunter.

1. Benennen Sie das Verzeichnis so um, dass es dem Namen entspricht, den Sie Ihrer Anwendung in {{site.data.keyword.Bluemix_notm}} gegeben haben.

## Schritt 3: Starteranwendung bereitstellen
{: #deploy_app}

1. Rufen Sie das Verzeichnis der Starteranwendung auf:
  <pre><code>cd myapp</code></pre>
  {:pre}

1. Melden Sie sich bei {{site.data.keyword.Bluemix_notm}} an und legen Sie Ihre Zielorganisation fest, wenn Sie dazu aufgefordert werden:
  <pre><code>bx login</code></pre>
  {:pre}

1. Übertragen Sie die Anwendung mit einer Push-Operation an {{site.data.keyword.Bluemix_notm}}:
  <pre><code>bx app push myapp</code></pre>
  {:pre}

1. Navigieren Sie zur Seite mit der Anwendungsübersicht, auf die Sie über das {{site.data.keyword.Bluemix_notm}}-Dashboard gelangen, und prüfen Sie, ob Ihre Anwendung erfolgreich gestartet wurde.
1. Starten Sie Ihre Anwendung, sodass sie im Browser zu sehen ist. Die URL (oder "Route") zu Ihrer Anwendung finden Sie auf der Seite mit der Anwendungsübersicht.

## Weitere Schritte
{: #next_steps}

Nachdem die Anwendung nun ausgeführt wird, können Sie sie über die {{site.data.keyword.streaminganalyticsshort}}-Konsole überwachen. Rufen Sie das Service-Dashboard auf, wählen Sie Ihren {{site.data.keyword.streaminganalyticsshort}}-Service aus und klicken Sie auf **Starten**.
