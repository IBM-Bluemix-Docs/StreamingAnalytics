---

copyright:
  years: 2015, 2019
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}


# Utilisation des ressources
{: #resourceusage}

{{site.data.keyword.streaminganalyticsshort}} dispose d'une série de comportements et de règles assurant une allocation et une utilisation appropriées des ressources.

## Affichage et édition des ressources d'instance
Vous pouvez afficher et éditer le nombre de ressources autorisées pour l'instance sur la page des détails du service ou l'API REST version 1 pour les [plans de service version 1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans). Vous devez utiliser l'API REST [{{site.data.keyword.streaminganalyticsshort}} v2](https://{DomainName}/apidocs/streaming-analytics-v2#get-a-streaming-analytics-instance) pour les [plans de service version 2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans).

## Allocation des ressources
- Les ressources sont allouées automatiquement à l'instance lorsque vous soumettez à un travail qui s'exécute correctement.
- Les ressources sont retirées de l'instance si aucun travail ne s'exécute sur la ressource. Par exemple, vous disposez de deux travaux : le premier s'exécute sur la ressource 1 et le deuxième sur la ressource 1 et sur la ressource 2. Si le deuxième travail est annulé, la ressource 1 est conservée dans l'instance alors que la ressource 2 est retirée.
- Lorsque vous soumettez un travail, celui-ci est placé sur une nouvelle ressource si l'instance n'a pas atteint sa limite d'allocation.
- Lorsqu'une instance utilise toutes ses ressources autorisées, les nouveaux travaux sont planifiés sur les ressources existantes.

## Contraintes relatives aux ressources

Des contraintes relatives aux ressources peuvent être utilisées pour contrôler l'allocation et l'utilisation des ressources. Par exemple, vous pouvez spécifier que deux travaux utilisent une ressource unique au lieu de deux ressources distinctes.
