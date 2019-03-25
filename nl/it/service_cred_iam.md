---

copyright:
  years:  2015, 2019
lastupdated: "2018-12-06"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Autenticazione IAM (Identity and Access Management)
{: #iam}

L'accesso alle istanze del servizio {{site.data.keyword.streaminganalyticsshort}} per gli utenti nel tuo account è controllato da{{site.data.keyword.Bluemix_notm}} IAM (Identity and Access Management). Per gestire il tuo servizio {{site.data.keyword.streaminganalyticsshort}}, devi utilizzare un token di autenticazione.

## Richiamo dei token di accesso IAM

### Prerequisiti

a. Devi disporre di un ID IBM valido.

b. Scarica e installa la [CLI {{site.data.keyword.Bluemix_notm}}](/docs/cli?topic=cloud-cli-install-ibmcloud-cli#install-ibmcloud-cli).

### Passo 1. Esegui l'accesso alla CLI {{site.data.keyword.Bluemix_notm}}.

```
bx api https://api.ng.bluemix.net
bx login
<enter your credentials>

<Se fai parte di più account {{site.data.keyword.Bluemix_notm}}, ti verrà chiesto di scegliere un account per la sessione corrente. Dovrai inoltre scegliere un'organizzazione e uno spazio in {{site.data.keyword.Bluemix_notm}}.>
```

### Passo 2. Recupera il token di accesso IAM.

```
bx iam oauth-tokens
```

Vengono prodotti due token: uno denominato `IAM token` e l'altro denominato `UAA token`. Utilizza `IAM token` per effettuare le chiamate API REST.
