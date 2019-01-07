---

copyright:
  years: 2015, 2018
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics - Haute disponibilité
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} permet une haute disponibilité dans vos applications. Si un problème est détecté sur l'un de vos noeuds d'application (ressources {{site.data.keyword.streamsshort}}), le noeud est automatiquement remplacé et tous les noeuds s'exécutant sur ce noeud sont migrés. Les travaux ne sont migrés et redémarrés que si l'instance comporte des noeuds d'applications multiples. Vous pouvez redimensionner l'instance en utilisant la [page des détails du service](/docs/services/StreamingAnalytics/r_service_dashboard.html) ou l'[{{site.data.keyword.streaminganalyticsshort}} API REST version 1![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} pour les [plans de service version 1](/docs/services/StreamingAnalytics/service_plans.html). Pour des plans de service version 2, utilisez l'[API REST version 2 ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window}
{:shortdesc}

Cette vidéo montre comment redimensionner votre instance à l'aide la page des détails du service :

<iframe width="560" height="315" title="Redimensionner l'instance" src="https://www.youtube.com/embed/zbZ9am9UhPw?rel=0" frameborder="0" allowfullscreen>Redimensionner l'instance</iframe>

## Régions cohérentes
En raison des exigences métier, certaines applications requièrent que tous les tuples soient traités au moins une fois. {{site.data.keyword.streamsshort}} a été amélioré avec des opérateurs et des annotations permettant la définition d'une région qui ne perd pas les tuples lors du traitement des flux. Les tuples qui se trouvent dans une région cohérente sont traités au moins une fois.

Vous pouvez exécuter et surveiller des applications Streams avec des régions cohérentes définies dans {{site.data.keyword.streaminganalyticsshort}}. Lorsque vous créez un service {{site.data.keyword.streaminganalyticsshort}}, l'instance est déjà configurée pour l'utilisation de régions cohérentes.

Une région cohérente est un sous-graphique dans lequel les états des opérateurs deviennent cohérents en traitant tous les tuples et toutes les marques de ponctuation dans des points définis sur un flux. Ainsi, les tuples contenus dans le sous-graphique peuvent être traités au moins une fois. Une opération DRAIN est régulièrement effectuée sur la région cohérente afin de la vider de ses tuples en cours. Tous les tuples contenus dans la région cohérente sont traités jusqu'à la fin du sous-graphique. L'état en mémoire des opérateurs est automatiquement sérialisé et stocké sur un point de contrôle pour chacun des opérateurs de la région.

Désormais, vous pouvez écrire des applications Java et SPL dans lesquelles le traitement des tuples est garanti et déployer ces applications dans {{site.data.keyword.streaminganalyticsshort}}.

Vous pouvez définir le début d'une région cohérente avec l'annotation `@consistent` pour un opérateur compatible. {{site.data.keyword.streamsshort}} détermine automatiquement la portée d'une région cohérente, mais vous pouvez modifier l'opérateur de fin de la région avec l'annotation `@autonomous`. La région cohérente définie établit périodiquement un état cohérent.

Consultez la [documentation {{site.data.keyword.streamsshort}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html) pour plus de détails sur l'utilisation de régions cohérentes dans les applications Streams.
