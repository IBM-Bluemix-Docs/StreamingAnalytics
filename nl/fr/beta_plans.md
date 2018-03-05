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

# Plans Beta-Entry et Beta-Enhanced 
{: #beta_plans}

Les nouveaux plans Beta-Entry et Beta-Enhanced du service {{site.data.keyword.streaminganalyticsshort}} incluent plusieurs améliorations et diffèrent des plans de service existants :
{:shortdesc}

**Nouvelle version d'[{{site.data.keyword.streamsshort}} QSE for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) :** {{site.data.keyword.streamsshort}} Quick Start Edition est une version gratuite d'{{site.data.keyword.streamsshort}}, qui n'a pas été conçue pour la production. Afin d'utiliser les plans Beta-Entry et Beta-Enhanced pour déployer des applications dans {{site.data.keyword.streaminganalyticsshort}}, vous devez compiler vos applications avec la version Red Hat Enterprise Linux (RHEL) 7 d'{{site.data.keyword.streamsshort}} QSE.
Consultez le document [Beta Development Guide ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/streamsdev/docs/cloud-beta-devguide/) pour apprendre à utiliser la nouvelle version de Streams QSE avec RHEL 7 dans un environnement Docker afin de compiler et de déployer vos applications avec les nouveaux plans bêta de {{site.data.keyword.streaminganalyticsshort}}.    

**API REST v2 de {{site.data.keyword.streaminganalyticsshort}} :** vous pouvez utiliser l'[API REST v2 de {{site.data.keyword.streaminganalyticsshort}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#introduction) pour gérer vos instances de service et vos travaux {{site.data.keyword.streamsshort}}. L'API v2 de {{site.data.keyword.streaminganalyticsshort}} n'est prise en charge que dans les instances de service créées avec l'un des nouveaux plans bêta. L'[API REST v1 ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://console.bluemix.net/apidocs/220-streaming-analytics?&language=node#introduction) n'est prise en charge que dans les instances existantes de {{site.data.keyword.streaminganalyticsshort}} et dans les nouvelles instances que vous créez avec les plans de service existants. 

**Nouvelles applications de démarrage et nouveaux modèles d'application :** étant donné que les nouveaux plans bêta requièrent l'exécution de Streams sous RHEL 7, de nombreux modèles d'application existants ne fonctionnent pas avec les nouveaux plans bêta. {{site.data.keyword.streaminganalyticsshort}} fournit un [nouvel ensemble d'applications de démarrage et de modèles d'application]( https://developer.ibm.com/streamsdev/docs/cloud-beta-samples/) pour que vous puissiez commencer à utiliser rapidement les nouveaux plans bêta. 

**Améliorations de la haute disponibilité :** évitez toute perte de données dans les applications de traitement de flux en définissant des régions cohérentes. {{site.data.keyword.streamsshort}} a été amélioré avec des opérateurs et des annotations permettant la définition d'une région qui ne perd pas les tuples lors du traitement des flux. Les tuples qui se trouvent dans une région cohérente sont traités au moins une fois. Si vous utilisez les plans de tarification Beta-Entry ou Beta-Enhanced, vous pouvez désormais exécuter et surveiller des applications Streams avec des [régions cohérentes définies dans {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/consistentregions.html). 

**Nouvelles fonctions d'identification des problèmes :** les plans Beta-Entry et Beta-Enhanced incluent plusieurs améliorations qui permettent d'identifier et de corriger rapidement les erreurs dans vos applications. Pour plus de détails, voir [New problem determination features in the beta version of the {{site.data.keyword.streaminganalyticsshort}} service ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe").](https://wp.me/p4IICn-4cx)

**Surveillance du comportement des opérateurs et traitement garanti des tuples dans le cloud :** {{site.data.keyword.streamsshort}} fournit des mesures qui permettent d'évaluer la santé des services {{site.data.keyword.streamsshort}} afin de diagnostiquer les problèmes de performance et d'analyser la capacité de traitement des demandes. Vous pouvez utiliser la console Streams dans {{site.data.keyword.streaminganalyticsshort}} pour [surveiller le comportement des opérateurs et assurer l'optimisation des ressources ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe").](https://wp.me/p4IICn-4bH)
