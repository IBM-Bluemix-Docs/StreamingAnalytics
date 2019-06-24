---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-16"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# A propos de Streaming Analytics
{: #about}

Vous pouvez effectuer une analyse en temps réel sur des données en mouvement dans le cadre de vos applications {{site.data.keyword.Bluemix_short}} à l'aide d'{{site.data.keyword.streaminganalyticsfull}}.
{:shortdesc}

Vous utilisez {{site.data.keyword.streaminganalyticsshort}} pour la première fois ? Découvrez une [rapide introduction au service ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/streamsdev/docs/streaming-analytics-now-available-bluemix-2/){:new_window}.

Le service {{site.data.keyword.streaminganalyticsshort}} fournit les fonctionnalités ci-après pour déployer, analyser et surveiller vos données sur le cloud :

**Utilisation interactive et par programme du service :**

Vous pouvez utiliser le service interactivement via la [console {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-console#console), ou à l'aide d'un programme via l'[API REST {{site.data.keyword.streaminganalyticsshort}} version 1 ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} si vous utilisez les [plans de service version 1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans). Pour des [plans de service version 2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans), utilisez l'[{{site.data.keyword.streaminganalyticsshort}}API REST version 2 ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/apidocs/streaming-analytics-v2)

**Déploiement et surveillance des applications SPL, Java, Scala et Python :**

Vous pouvez écrire des applications {{site.data.keyword.streamsshort}} en SPL, Java, Scala et Python. [Déployez et surveillez ces applications](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_deploytocloud) à l'aide de la console {{site.data.keyword.streaminganalyticsshort}}.

Si vous voulez écrire vos applications en SPL, sachez qu'{{site.data.keyword.streamsfull}} Processing Language (SPL) est un langage de programmation utilisé pour créer des applications de traitement de flux. Si vous voulez aller plus loin avec vos propres applications SPL, vous pouvez obtenir un environnement de développement {{site.data.keyword.streamsshort}} et vous devez faire en sorte que vos applications SPL soient prêtes pour le cloud.

Pour créer et déployer des applications Python sans environnement de développement {{site.data.keyword.streamsshort}}, utilisez les fichiers notebook de service dans {{site.data.keyword.DSX_short}} ou l'API Python {{site.data.keyword.streamsshort}}. Pour plus d'informations, voir [Développement d'applications Python pour {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_develop_apps_python).

Vous pouvez développer des applications Beam avec Streams Runner dans votre environnement de développement local, et ensuite les déployer et les surveiller à l'aide du service {{site.data.keyword.streaminganalyticsshort}}. Pour plus d'informations sur les applications Beam avec Streams Runner, voir [IBM Streams Runner for Apache Beam dans {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-gs_beamrunner).


**Compatibilité avec les opérateurs {{site.data.keyword.streamsshort}} :**

Les opérateurs {{site.data.keyword.streamsshort}} du kit d'outils standard [{{site.data.keyword.streamsshort}} Processing Language (SPL) sont compatibles](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-compatible_toolkits) avec {{site.data.keyword.streaminganalyticsshort}}.

## Responsabilités Streaming Analytics
{: #responsibilities notoc}

### Responsabilités du client
{: #clientresponsibilities notoc}

Le client est responsable des actions suivantes :

* Suivi de la configuration IBM initiale d'{{site.data.keyword.streamsshort}}, surveillance, configuration et gestion des travaux {{site.data.keyword.streamsshort}} qui s'exécutent dans son instance. Le client peut démarrer et arrêter l'instance et démarrer et arrêter les travaux s'exécutant sur l'instance.
* Au besoin, développement de programmes et d'applications sur le service pour analyser les données et en tirer des renseignements utiles. Le client est aussi responsable de la qualité et des performances des programmes et applications ainsi développés. Les programmes peuvent être développés en SPL, Java ou d'autres langages pris en charge, via la fonction {{site.data.keyword.streamsshort}} Topology. Ils doivent être compilés à l'aide d'{{site.data.keyword.streamsshort}} Developer Edition ou d'{{site.data.keyword.streamsshort}} Quick Start Edition, avec le même système d'exploitation que celui utilisé pour {{site.data.keyword.streaminganalyticsshort}}.
* Vérification périodique du lien suivant, pour être informé d'une période d'indisponibilité planifiée, avec ou sans interruption - [https://developer.ibm.com/bluemix/support/#status ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/bluemix/support/#status){:new_window}  
* Sauvegarde de toutes les données, métadonnées, fichiers de configuration et paramètres d'environnement, en fonction des exigences métier, afin d'assurer une continuité.
* Restauration des données, métadonnées, fichiers de configuration et paramètres d'environnement depuis une sauvegarde, afin d'assurer une continuité, dans l'éventualité d'un incident, quel qu'en soit son type (par exemple, un incident survenant dans un centre de données, un pod, un serveur, un disque dur ou un logiciel).

### Responsabilités d'IBM
{: #ibmresponsibilities notoc}

Dans le cadre d'{{site.data.keyword.streaminganalyticsfull}}, IBM est responsable des actions suivantes :

* Fournir et gérer une infrastructure de serveurs, de stockage et de mise en réseau pour l'instance client.
* Fournir une configuration initiale d'{{site.data.keyword.streamsshort}} sur le nombre de ressources sélectionnées.
* Fournir et gérer une infrastructure pour Internet et un pare-feu interne pour la protection et l'isolation.
* Surveiller et gérer les composants ci-après sur {{site.data.keyword.streaminganalyticsshort}} :
	* Composants réseau
	* Serveurs et espace de stockage local associé
	* Systèmes d'exploitation des infrastructures
	* Services de gestion {{site.data.keyword.streamsshort}}
	* Instances {{site.data.keyword.streamsshort}}
* Fournir des correctifs de maintenance, incluant les correctifs de sécurité appropriés pour les systèmes d'exploitation des infrastructures et {{site.data.keyword.streamsshort}}.
* Effectuer d'une part une maintenance régulière ne devant provoquer aucune période d'indisponibilité du système (maintenance “sans interruption”), et d'autre part une maintenance pouvant générer une période d'indisponibilité du système ainsi qu'un redémarrage (maintenance “avec interruption”), à des dates précises, planifiées et publiées sur [https://developer.ibm.com/bluemix/support/#status ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/bluemix/support/#status){:new_window}
* Tout changement dans les dates et heures de la maintenance planifiée est publié, avec un avis préalable approprié.
