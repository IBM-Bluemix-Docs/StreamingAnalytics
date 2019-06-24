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

# Haute disponibilité et reprise après incident
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} est hautement disponible au sein d'un emplacement {{site.data.keyword.Bluemix_notm}} (par exemple, Dallas, Washington DC, Londres, Francfort). Cependant, la reprise après incidents qui affectent l'intégralité d'une région {{site.data.keyword.Bluemix_notm}} nécessite planification et préparation.
{:shortdesc}


Vous êtes responsable de la compréhension de votre configuration, de la personnalisation et de l'utilisation du service. Vous devez également être prêt à recréer une instance du service dans le nouvel emplacement {{site.data.keyword.Bluemix_notm}} et à redéployer votre applications dans cet emplacement. Voir [Comment garantir une disponibilité permanente ?](/docs/services/overview?topic=overview-zero-downtime#zero-downtime) pour en savoir plus sur les normes relatives à la haute disponibilité et à la reprise après incident dans {{site.data.keyword.Bluemix_notm}}. Vous pouvez également consultez les informations sur les [Accords sur les niveaux de service (SLA)](/docs/services/overview?topic=overview-zero-downtime#zero-downtime#SLAs).

## Haute disponibilité

{{site.data.keyword.streaminganalyticsshort}} permet une haute disponibilité dans vos applications. Vos applications sont déployées dans des conteneurs Docker qui s'exécutent dans des clusters Kubernetes. Pour développer des applications à haute disponibilité, vous devez comprendre comment fonctionnent ces conteneurs afin de garantir la haute disponibilité :

* Les ressources d'application sont des conteneurs auxquels l'utilisation de l'UC et de la mémoire est attribuée selon votre plan de service.
* En cas de défaillance matérielle ou logicielle, des conteneurs peuvent être déplacés. Lorsque des conteneurs sont déplacés, des éléments de processus sont redémarrés.
* Lors d'une maintenance planifiée, des conteneurs peuvent être déplacés (des éléments de processus sont redémarrés).

Par conséquent, lors de l'écriture de vos applications, vous devez tenir compte du fait que des conteneurs peuvent parfois être déplacés. Tenez également compte des éléments suivants :
* Vérifiez que les éléments de processus peuvent être redémarrés et relocalisés.
* Vérifiez que votre application accepte le redémarrage de certains ou de tous les éléments de processus, dans n'importe quel ordre.
* Vérifiez que les opérateurs source et d'évacuation de votre application Streams sont configurés de manière à rétablir les connexions au moment où leur élément de processus redémarre.

Consultez le [guide de développement {{site.data.keyword.streaminganalyticsshort}}](https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/#troubleshooting) pour des exemples qui montrent comment traiter les incidents liés à votre application.

Pour implémenter la haute disponibilité, des applications Streams sont activées afin de garantir le traitement de tous les tuples. Pour un traitement de n-uplet garanti, un point de contrôle est régulièrement mis en place pour tous les opérateurs dans une région cohérente. Lors de l'échec d'une application, tous les opérateurs sont ramenés aux états du dernier point de contrôle sans incident.
{{site.data.keyword.streaminganalyticsshort}} autorise l'utilisation de régions cohérentes.

### Traitement de n-uplet garanti
En raison des exigences métier, certaines applications requièrent que tous les tuples soient traités au moins une fois. {{site.data.keyword.streamsshort}} a été amélioré avec des opérateurs et des annotations permettant la définition d'une région qui ne perd pas les tuples lors du traitement des flux. Les tuples qui se trouvent dans une région cohérente sont traités au moins une fois.

Si un échec d'application est détecté dans une région cohérentes, {{site.data.keyword.streaminganalyticsshort}} peut redéfinir l'application à son dernier état de cohérence (point de contrôle a.k.a.) et rediriger les sources de données d'application de manière à réexécuter les tuples à partir de ce point.

Vous pouvez exécuter et surveiller des applications Streams avec des régions cohérentes définies dans {{site.data.keyword.streaminganalyticsshort}}. Lorsque vous créez un service {{site.data.keyword.streaminganalyticsshort}}, l'instance est déjà configurée pour autoriser l'utilisation de régions cohérentes.

Une région cohérente est un sous-graphique dans lequel les états des opérateurs deviennent cohérents en traitant tous les tuples et toutes les marques de ponctuation dans des points définis sur un flux. Ainsi, les tuples contenus dans le sous-graphique peuvent être traités au moins une fois. Une opération DRAIN est régulièrement effectuée sur la région cohérente afin de la vider de ses tuples en cours. Tous les tuples contenus dans la région cohérente sont traités jusqu'à la fin du sous-graphique. L'état en mémoire des opérateurs est automatiquement sérialisé et stocké sur un point de contrôle pour chacun des opérateurs de la région.

Vous pouvez écrire des applications Java, SPL et Python dans lesquelles le traitement des tuples est garanti et déployer ces applications dans {{site.data.keyword.streaminganalyticsshort}}.

Vous pouvez définir le début d'une région cohérente avec l'annotation `@consistent` pour un opérateur compatible. {{site.data.keyword.streamsshort}} détermine automatiquement la portée d'une région cohérente, mais vous pouvez modifier l'opérateur de fin de la région avec l'annotation `@autonomous`. La région cohérente définie établit périodiquement un état cohérent.

Consultez la [documentation {{site.data.keyword.streamsshort}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html) pour plus de détails sur l'utilisation de régions cohérentes dans les applications Streams. 

## Reprise après incident
{{site.data.keyword.streaminganalyticsshort}} est un service de disponibilité générale offert dans plusieurs régions {{site.data.keyword.Bluemix_notm}}. {{site.data.keyword.streaminganalyticsshort}} ne stocke aucune donnée utilisateur dans {{site.data.keyword.Bluemix_notm}}.

En fonction de vos exigences professionnelles, sélectionnez l'une des stratégies de reprise après incident suivantes :
* Pour que votre application ne subisse aucune interruption :
  1. Créez des instances {{site.data.keyword.streaminganalyticsshort}} dans plusieurs régions {{site.data.keyword.Bluemix_notm}}.
  2. Soumettez votre application à plusieurs régions.


* Pour un minimum d'interruption de votre application :
  1. Créez des instances {{site.data.keyword.streaminganalyticsshort}} dans plusieurs régions {{site.data.keyword.Bluemix_notm}}.
  2. Surveillez votre application à l'aide de l'[API REST de service](https://ibm.co/2Gt9mB6) et, au besoin, déplacez dynamiquement votre charge de travail vers une nouvelle région.

**Remarque** : chaque région cohérente est liée à une région {{site.data.keyword.Bluemix_notm}}. Dans un scénario de reprise après incident, les régions cohérentes d'une application n'ont aucun rôle.
