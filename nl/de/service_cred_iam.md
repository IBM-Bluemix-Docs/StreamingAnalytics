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


# Identity and Access Management-Authentifizierung
{: #iam}

Der Zugriff auf {{site.data.keyword.streaminganalyticsshort}}-Serviceinstanzen für Benutzer in Ihrem Konto wird mithilfe von {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) gesteuert. Zur Verwaltung Ihres {{site.data.keyword.streaminganalyticsshort}}-Service müssen Sie ein Authentifizierungstoken verwenden.

## IAM-Zugriffstoken abrufen

### Voraussetzungen

a. Sie benötigen eine gültige IBMid.

b. Laden Sie die [{{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle (CLI)](/docs/cli?topic=cloud-cli-install-ibmcloud-cli#install-ibmcloud-cli) herunter und installieren Sie sie.

### Schritt 1. Melden Sie sich bei der {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle an.

```
bx api https://api.ng.bluemix.net
bx login
<Berechtigungsnachweise eingeben>

<Wenn Sie Mitglied mehrerer {{site.data.keyword.Bluemix_notm}}-Konten sind, werden Sie dazu aufgefordert, ein Konto für die aktuelle Sitzung auszuwählen. Darüber hinaus müssen Sie eine Organisation und einen Bereich in {{site.data.keyword.Bluemix_notm}} auswählen.>
```

### Schritt 2. Rufen Sie das IAM-Zugriffstoken ab.

```
bx iam oauth-tokens
```

Es werden zwei Tokens erstellt: ein `IAM-Token` und ein `UAA-Token`. Verwenden Sie das `IAM-Token` für REST-API-Aufrufe.
