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

# Ambiente e strumenti di sviluppo
{: #c_beta_tooling}


Si applicano queste considerazioni all'ambiente e agli strumenti che utilizzi per sviluppare le tue applicazioni
per {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}} non include un ambiente di sviluppo {{site.data.keyword.streamsshort}} nel cloud o Streams Studio nel cloud. Sviluppa le tue applicazioni in un ambiente {{site.data.keyword.streamsshort}} istallato localmente e inviale
come bundle dell'applicazione. Se non hai l'ambiente di sviluppo, puoi scaricare [{{site.data.keyword.streamsshort}} Quick Start Edition con Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) per i [piani di servizio v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) o, se stai utilizzando i [piani di servizio v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans), puoi scaricare l'[immagine della VM {{site.data.keyword.streamsshort}} Quick Start Edition ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}, gratuitamente.
* Compila le tue applicazioni in RHEL (Red Hat Enterprise Linux) 7.x se stai utilizzando i piani di servizio v2 o con RHEL 6.5 se stai utilizzando i piani di servizio v1, utilizzando i processori Intel.
* Nel tuo ambiente di sviluppo {{site.data.keyword.streamsshort}}, imposta la variabile di ambiente `JAVA_HOME` su $STREAMS_INSTALL/java.
