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

# Traitement des incidents dans Streaming Analytics
{: #ts_StreamingAnalytics}

Vous pouvez trouver ici les réponses aux questions courantes sur l'utilisation de {{site.data.keyword.streaminganalyticsshort}} dans {{site.data.keyword.Bluemix_short}}.
{:shortdesc}

## Quand je lance le service, je suis invité à entrer des données d'identification pour me connecter à la console
{: #log_in_console}

Lorsque vous lancez {{site.data.keyword.streaminganalyticsshort}}, vous êtes invité à indiquer vos donnée d'identification pour la connexion à la console de service.
{:shortdesc}

Vous lancez un service {{site.data.keyword.streaminganalyticsshort}} que vous aviez créé, mais au lieu d'accéder directement à la console de service, vous obtenez une page de connexion dans laquelle vous devez entrer des données d'identification.
{: tsSymptoms}

Une mise à jour a été effectuée dans l'infrastructure de service et le cache de votre navigateur empêche le service de récupérer cette mise à jour.
{: tsCauses}

Effacez le cache de votre navigateur afin de vous permettre d'obtenir la dernière version de la console de service.
{: tsResolve}

## Mon application est défaillante
{: #app_unhealthy}

Vous ne pouvez exécuter correctement votre application et son état de santé est `défaillant`.
{:shortdesc}

Vous soumettez une application à l'instance de service, l'application démarre puis échoue immédiatement après, avec un état de santé `défaillant`. L'erreur suivante apparaît dans le fichier journal : `/lib64/libc.so.6 : version GLIBC_2.14 introuvable`.
{: tsSymptoms}

Vous n'avez pas compilé l'application dans un système d'exploitation RHEL 7.x ou une version CentOS équivalente.
{: tsCauses}

Vous devez compiler vos applications sous Red Hat Enterprise Linux (RHEL) 7.x si vous utilisez les [plans de service version 2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans). Si vous utilisez les [plans de service version 1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans), vous devez compiler vos applications sous RHEL 6.5, utilisant des processeurs Intel. Soumettez à nouveau votre application à l'instance de service. Vous pouvez télécharger le produit [{{site.data.keyword.streamsshort}} Quick Start Edition avec Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) si vous ne disposez pas d'un environnement de développement compatible et que vous utilisez les plans de service version 2. Si vous utilisez des plans de service version 1, téléchargez le produit [{{site.data.keyword.streamsshort}} QSE ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}.
{: tsResolve}

## Mon application est défaillante après un redémarrage
{: #app_restart}

Votre application est défaillante après un redémarrage en raison d'une opération de maintenance du système ou de l'échec d'un scénario de reprise après incident.
{:shortdesc}

Votre instance de service contient plusieurs applications et l'une d'elles utilise une balise pour l'emplacement de l'opérateur. Lorsque l'application redémarre, les ressources des opérateurs sans balise sont acquises en premier et consomment l'intégralité du quota de ressources avant placement des opérateurs avec balise.
{: tsSymptoms}

Un redémarrage des pods à grande échelle (le plus souvent déclenché par des mises à jour de service) peut bloquer le redémarrage d'applications si celles-ci nécessitent un balisage particulier et que le quota de ressources a déjà été atteint. Dans certains cas, des redémarrages de pods à grande échelle peuvent provoquer l'échec de scénarios de reprise après incident.
{: tsCauses}

Vous devez augmenter votre quota de ressources ou libérer certaines ressources pour que les applications puissent acquérir des ressources avec les balises requises. Pour augmenter votre quota, accédez à la page des détails du service et augmentez la taille de votre instance. Pour libérer des ressources, annulez les travaux existants jusqu'à avoir libéré suffisamment de ressources pour correctement placer les applications.
{: tsResolve}
