---

copyright:
  years:  2017
lastupdated: "2018-07-24"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Authentification dans Identity and Access Management

L'accès aux instances de service {{site.data.keyword.streaminganalyticsshort}} pour les utilisateurs de votre compte est contrôlé par {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM). Pour gérer votre service {{site.data.keyword.streaminganalyticsshort}}, vous devez utiliser un jeton d'authentification.

## Extraction des jetons d'accès IAM

### Prérequis

a. Vous devez disposer d'un IBMid valide.

b. Téléchargez et installez l'interface de ligne de commande [{{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/cli/reference/bluemix_cli/get_started.html#getting-started).

### Etape 1. Connectez-vous à l'interface de ligne de commande {{site.data.keyword.Bluemix_notm}}.

```
bx api https://api.ng.bluemix.net
bx login
<entrez vos données d'identification>

<Si vous disposez de plusieurs comptes {{site.data.keyword.Bluemix_notm}}, vous serez invité à en choisir un pour la session en cours. De même, vous devrez choisir une organisation et un espace dans {{site.data.keyword.Bluemix_notm}}.>
```

### Etape 2. Récupérez le jeton d'accès IAM.

```
bx iam oauth-tokens
```

Deux jetons sont générés : un nommé `IAM token` et l'autre `UAA token`. Utilisez `IAM token` pour passer des appels d'API REST.
