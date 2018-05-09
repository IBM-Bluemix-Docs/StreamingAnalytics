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

# Risoluzione dei problemi di Streaming Analytics
{: #ts_StreamingAnalytics}

Puoi trovare le risposte a domande comuni sull'utilizzo di {{site.data.keyword.streaminganalyticsshort}} in {{site.data.keyword.Bluemix_short}}.
{:shortdesc}

## Quando avvio il servizio, mi vengono richieste le credenziali per accedere alla console
{: #log_in_console}

Quando avvii {{site.data.keyword.streaminganalyticsshort}}, ti vengono richieste le credenziali
per accedere alla console del servizio.
{:shortdesc}

Avvii un servizio {{site.data.keyword.streaminganalyticsshort}} creato in precedenza e, invece di accedere direttamente alla console del servizio, viene visualizzata una pagina di accesso in cui ti vengono richieste le credenziali.
{: tsSymptoms}

L'infrastruttura del servizio è stata aggiornata e la cache del tuo browser impedisce
al servizio di eseguire l'aggiornamento.
{: tsCauses}

Pulisci la cache del browser per essere sicuro di ottenere l'ultima versione della console del servizio.
{: tsResolve}

## La mia applicazione è in uno stato di "unhealthy" (non integro)
{: #app_unhealthy}

Non puoi eseguire la tua applicazione correttamente e lo stato di integrità è `unhealthy`.
{:shortdesc}

Invii un'applicazione all'istanza del servizio, l'applicazione viene avviata ma si verifica immediatamente un suo malfunzionamento e lo stato di integrità è `unhealthy`. Nel file di log compare il seguente errore: `/lib64/libc.so.6: version GLIBC_2.14 not found`.
{: tsSymptoms}

Non hai compilato l'applicazione utilizzando un sistema operativo RHEL 7.x o una versione CentOS equivalente.
{: tsCauses}

Devi ricompilare la tua applicazione in RHEL (Red Hat Enterprise Linux) 7.x se stai utilizzando i [piani di servizio v2](/docs/services/StreamingAnalytics/service_plans.html) o con RHEL 6.5 se stai utilizzando i [piani di servizio v1](/docs/services/StreamingAnalytics/service_plans.html), utilizzando i processori Intel. Invia nuovamente la tua applicazione all'istanza del servizio. Puoi scaricare [{{site.data.keyword.streamsshort}} Quick Start Edition con Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) se non hai un ambiente di sviluppo compatibile e stai utilizzando i piani di servizio v2. Se stai utilizzando i piani di servizio v1, scarica  [{{site.data.keyword.streamsshort}} QSE ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window}.
{: tsResolve}
