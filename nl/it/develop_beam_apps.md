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

# Distribuzione delle applicazioni Beam in Streaming Analytics
{: #develop_beam_apps}

Puoi ora sviluppare applicazioni Beam nel tuo ambiente di sviluppo {{site.data.keyword.streamsshort}} locale e distribuire queste applicazioni in {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

{{site.data.keyword.streamsshort}} Runner for Apache Beam esegue le pipeline in un ambiente {{site.data.keyword.streamsshort}}. Un'applicazione Beam avviata con Streams Runner viene tradotta in un file SAB (Streams Application Bundle) che puoi distribuire e monitorare in {{site.data.keyword.streaminganalyticsshort}}.

Per inviare un'applicazione Beam al tuo servizio {{site.data.keyword.streaminganalyticsshort}} su {{site.data.keyword.Bluemix_notm}}, devi creare un file VCAP formattato JSON che ospita le credenziali e le altre informazioni sul servizio.

1. Nel tuo ambiente locale Streams, passa alla cartella secondaria degli esempi in cui hai installato il toolkit ($STREAMS_BEAM_RUNNER/samples) e copia il file template.vcap in un nuovo file. Fornisci al file un nome significativo e un estensione di .vcap.
1. [Copia le credenziali del tuo servizio {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/r_vcap_services.html) e incollale nel file VCAP che hai creato, sostituendo la seguente riga:
```
 <REMOVE THIS LINE AND INSERT CREDENTIALS HERE>
 ```
1. Verifica che la tua applicazione Beam venga eseguita correttamente nel tuo ambiente di sviluppo. Quando avvii la tua applicazione Beam con Streams Runner, viene tradotta in un file SAB (Streams Application Bundle).
1. Invia il file SAB associato alla tua applicazione Beam a {{site.data.keyword.streaminganalyticsshort}}

La tua applicazione è ora distribuita nel cloud. Puoi monitorarla utilizzando il servizio
{{site.data.keyword.streaminganalyticsshort}}.

Per ulteriori dettagli sulla distribuzione e sul monitoraggio delle tue applicazioni Beam in {{site.data.keyword.streaminganalyticsshort}}, consulta [Streams Runner for Apache Beam ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/).
