---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-16"

subcollection: StreamingAnalytics

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

Avvii un servizio {{site.data.keyword.streaminganalyticsshort}} da te creato e, invece di accedere direttamente alla console del servizio, vedi una pagina di accesso in cui ti vengono richieste le credenziali.
{: tsSymptoms}

Si è verificato un aggiornamento nell'infrastruttura del servizio e la cache del tuo browser sta impedendo al servizio di rilevare l'aggiornamento.
{: tsCauses}

Pulisci la cache del browser per accertarti di ottenere l'ultima versione della console del servizio.
{: tsResolve}

## La mia applicazione è in uno stato di "unhealthy" (non integro)
{: #app_unhealthy}

Non puoi eseguire la tua applicazione correttamente e lo stato di integrità è `unhealthy`.
{:shortdesc}

Invii un'applicazione all'istanza del servizio, l'applicazione viene avviata ma si verifica immediatamente un suo malfunzionamento e lo stato di integrità è `unhealthy`. Nel file di log compare il seguente errore: `/lib64/libc.so.6: version GLIBC_2.14 not found`.
{: tsSymptoms}

Non hai compilato l'applicazione con un sistema operativo RHEL 7.x o una versione CentOS equivalente.
{: tsCauses}

Devi compilare la tua applicazione in RHEL (Red Hat Enterprise Linux) 7.x se stai utilizzando i [piani di servizio v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans). Se stai utilizzando i [piani di servizio v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans), devi compilare la tua applicazione con RHEL 6.5 con i processori Intel. Invia nuovamente la tua applicazione all'istanza del servizio. Puoi scaricare [{{site.data.keyword.streamsshort}} Quick Start Edition con Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) se non hai un ambiente di sviluppo compatibile e stai utilizzando i piani di servizio v2. Se stai utilizzando i piani di servizio v1, scarica  [{{site.data.keyword.streamsshort}} QSE ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}.
{: tsResolve}

## La mia applicazione è in uno stato di "unhealthy" (non integro) dopo il suo riavvio
{: #app_restart}

La tua applicazione è in uno stato di "unhealthy" (non integro) dopo il suo riavvio a causa di uno scenario di manutenzione del sistema o di ripristino da malfunzionamento.
{:shortdesc}

Hai più applicazioni nella tua istanza del servizio e una delle applicazioni utilizza una tag per il posizionamento dell'operatore. Una volta riavviata l'applicazione, le risorse per gli operatori senza tag vengono acquisite per prime e utilizzano tutta la tua quota di risorse prima che possano essere posizionati gli operatori con tag.
{: tsSymptoms}

Un riavvio di pod su larga scala, che nella maggior parte dei casi è attivato da aggiornamenti del servizio, può rendere impossibile il riavvio delle applicazioni se richiedono delle tag speciali e la quota di risorse è già stata raggiunta. In alcuni casi, i riavvii di pod su larga scala possono essere causati da scenari di ripristino da malfunzionamento.
{: tsCauses}

Devi aumentare la tua quota di risorse oppure liberare qualche risorsa in modo che le applicazioni possano acquisire risorse con le tag richieste. Per aumentare la tua quota, vai alla pagina dei dettagli del servizio e aumenta la dimensione della tua istanza. Per liberare delle risorse, annulla i lavori esistenti fino a liberare una quantità di risorse sufficiente per posizionare correttamente le applicazioni.
{: tsResolve}
