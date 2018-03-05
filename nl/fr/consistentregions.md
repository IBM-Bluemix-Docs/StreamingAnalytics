---

copyright:
  years: 2015, 2018
lastupdated: "2018-02-14"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}


# Améliorations de la haute disponibilité 
{: #consistentregions}

En raison des exigences métier, certaines applications requièrent que tous les tuples soient traités au moins une fois. {{site.data.keyword.streamsshort}} a été amélioré avec des opérateurs et des annotations permettant la définition d'une région qui ne perd pas les tuples lors du traitement des flux. Les tuples qui se trouvent dans une région cohérente sont traités au moins une fois. 


Si vous utilisez les plans de tarification Beta-Entry ou Beta-Enhanced, vous pouvez désormais exécuter et surveiller des applications Streams avec des régions cohérentes définies dans {{site.data.keyword.streaminganalyticsshort}}. Lorsque vous créez un service {{site.data.keyword.streaminganalyticsshort}} avec les plans Beta-Entry ou Beta-Enhanced, l'instance est déjà configurée pour l'utilisation de régions cohérentes. 

Une région cohérente est un sous-graphique dans lequel les états des opérateurs deviennent cohérents en traitant tous les tuples et toutes les marques de ponctuation dans des points définis sur un flux. Ainsi, les tuples contenus dans le sous-graphique peuvent être traités au moins une fois. Une opération DRAIN est régulièrement effectuée sur la région cohérente afin de la vider de ses tuples en cours. Tous les tuples contenus dans la région cohérente sont traités jusqu'à la fin du sous-graphique. L'état en mémoire des opérateurs est automatiquement sérialisé et stocké sur un point de contrôle pour chacun des opérateurs de la région.

Désormais, vous pouvez écrire des applications Java et SPL dans lesquelles le traitement des tuples est garanti et déployer ces applications dans {{site.data.keyword.streaminganalyticsshort}}. 

Vous pouvez définir le début d'une région cohérente avec l'annotation `@consistent` pour un opérateur compatible. {{site.data.keyword.streamsshort}} détermine automatiquement la portée d'une région cohérente, mais vous pouvez modifier l'opérateur de fin de la région avec l'annotation `@autonomous`. La région cohérente définie établit périodiquement un état cohérent. 

Consultez la [documentation d'{{site.data.keyword.streamsshort}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.1/com.ibm.streams.dev.doc/doc/consistentregions.html) pour plus de détails sur l'utilisation de régions cohérentes dans les applications Streams. 
