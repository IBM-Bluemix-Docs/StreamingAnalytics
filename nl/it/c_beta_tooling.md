---

copyright:
  years: 2015, 2017
lastupdated: "2017-10-27"

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
come bundle dell'applicazione. Se non disponi dell'ambiente di sviluppo, puoi scaricare []{{site.data.keyword.streamsshort}} Quick Start Edition](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/), gratuitamente.
* Compila il bundle dell'applicazione in un ambiente Red Hat Enterprise Linux 6.5, o una versione CentOS equivalente, per garantire la compatibilità.
* Nel tuo ambiente di sviluppo {{site.data.keyword.streamsshort}}, imposta la variabile di ambiente `JAVA_HOME` su $STREAMS_INSTALL/java.
