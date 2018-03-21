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

# Ambiente e strumenti di sviluppo
{: #c_beta_tooling}


Si applicano queste considerazioni all'ambiente e agli strumenti che utilizzi per sviluppare le tue applicazioni
per {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}} non include un ambiente di sviluppo {{site.data.keyword.streamsshort}} nel cloud o Streams Studio nel cloud. Sviluppa le tue applicazioni in un ambiente {{site.data.keyword.streamsshort}} istallato localmente e inviale
come bundle dell'applicazione. Se non disponi dell'ambiente di sviluppo, puoi scaricare la [{{site.data.keyword.streamsshort}} Quick Start Edition ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/), gratuitamente.
* Compila il bundle dell'applicazione in un ambiente Red Hat Enterprise Linux 6.5, o una versione CentOS equivalente, per garantire la compatibilità.

  **Nota:** se stai utilizzando i piani Beta-Entry e Beta-Enhanced, devi compilare il tuo bundle dell'applicazione in un ambiente RHEL 7 o in una versione CentOS equivalente. Puoi utilizzare la [{{site.data.keyword.streamsshort}} QSE per Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) se non disponi di un ambiente di sviluppo compatibile. Controlla la [Documentazione dei piani beta](/docs/services/StreamingAnalytics/beta_plans.html) per i dettagli.
* Nel tuo ambiente di sviluppo {{site.data.keyword.streamsshort}}, imposta la variabile di ambiente `JAVA_HOME` su $STREAMS_INSTALL/java.
