---

copyright:
  years: 2015, 2018
lastupdated: "2018-02-14"

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

# Traitement des incidents dans Streaming Analytics
{: #ts_StreamingAnalytics}

Vous pouvez trouver ici les réponses aux questions courantes sur l'utilisation de {{site.data.keyword.streaminganalyticsshort}} dans {{site.data.keyword.Bluemix_short}}.
{:shortdesc}

## Quand je lance le service, je suis invité à entrer des données d'identification pour me connecter à la console
{: #log_in_console}

Lorsque vous lancez {{site.data.keyword.streaminganalyticsshort}}, vous êtes invité à indiquer vos donnée d'identification pour la connexion à la console de service.
{:shortdesc}

Vous lancez un service {{site.data.keyword.streaminganalyticsshort}} que vous aviez créé précédemment, mais à la place d'un accès direct à la console de service, une page de connexion s'affiche, dans laquelle vous devez entrer des données d'identification.
{: tsSymptoms}

L'infrastructure de service a été mise à jour et le cache de votre navigateur empêche le service de récupérer cette mise à jour.
{: tsCauses}

Effacez le cache de votre navigateur pour être sûr d'obtenir la dernière version de la console de service.
{: tsResolve}

## Mon application est défaillante
{: #app_unhealthy}

Vous ne pouvez exécuter correctement votre application et son état de santé est `défaillant`.
{:shortdesc}

Vous soumettez une application à l'instance de service, l'application démarre puis échoue immédiatement après, avec un état de santé `défaillant`. L'erreur suivante apparaît dans le fichier journal : `/lib64/libc.so.6 : version GLIBC_2.14 introuvable`.
{: tsSymptoms}

Vous n'avez pas compilé l'application en utilisant le système d'exploitation RHEL 6.5 ou une version CentOS équivalente.
{: tsCauses}

Vous devez recompiler votre application sur un système d'exploitation Red Hat Enterprise Linux (RHEL) 6.5 ou une version CentOS équivalente, avec des processeurs Intel. Soumettez à nouveau votre application à l'instance de service.

**Remarque :** si vous utilisez les plans Beta-Entry et Beta-Enhanced, vous devez compiler votre bundle d'applications dans un environnement RHEL 7 ou une version CentOS équivalente. Vous pouvez utiliser [{{site.data.keyword.streamsshort}} Quick Start Edition for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) si vous ne disposez pas d'un environnement de développement compatible. Consultez la [documentation relative aux plans bêta](/docs/services/StreamingAnalytics/beta_plans.html) pour des détails.
{: tsResolve}
