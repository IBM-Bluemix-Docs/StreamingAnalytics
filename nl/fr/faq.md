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
{:faq: data-hd-content-type='faq'}

# Foire aux questions
{: #faq}

## Comment s'inscrire au service Streaming Analytics ?
{: #signup notoc}
{: faq}  

Pour plus d'informations sur les plans de service {{site.data.keyword.streaminganalyticsshort}}, voir le catalogue [{{site.data.keyword.Bluemix_short}}](https://{DomainName}/catalog/services/streaming-analytics).

## Quelle est la version du service Streaming Analytics que j'utilise ?
{: #version notoc}
{: faq}   

Des améliorations sont apportées régulièrement à tous les services {{site.data.keyword.streaminganalyticsshort}}. Vous utilisez toujours la version la plus récente du service géré et vous n'avez pas à assurer le suivi de la version ou du niveau du produit.

## Quelles sont les tâches qu'IBM gère pour moi ?
{: #ibm_manage notoc}
{: faq}   

Nous assurons l'installation, les mises à jour de logiciel, la création et la gestion des domaines ainsi que la maintenance du matériel. Le service inclut une surveillance de l'état de santé 24h/24 et 7j/7.


## Quelles sont les tâches qui m'incombent ?  
{: #responsible notoc}
{: faq}

Vous écrivez les applications qui s'exécuteront dans un service {{site.data.keyword.streaminganalyticsshort}} et une instance Streams sur site et vous vous assurez qu'elles fonctionnent correctement et qu'elles répondent aux exigences en matière de performances. Vous êtes également chargé de surveiller tout ce qui est propre à l'application.

## La haute disponibilité est-elle prise en charge ?
{: #ha notoc}
{: faq}

La haute disponibilité est gérée par IBM. {{site.data.keyword.streaminganalyticsshort}} est configuré pour prendre en charge la haute disponibilité. D'autres ressources serveur sont en place en cas de basculement.

## Comment la sécurité est-elle gérée pour le service Streaming Analytics ?
{: #security notoc}
{: faq}   

La sécurité est entièrement gérée par IBM. Des données d'identification sont générées pour chaque service et vous sont fournies. Les mises à jour de sécurité sont gérées et appliquées par IBM rapidement après leur mise à disposition.

## Dois-je configurer un service Streaming Analytics ?  
{: #configure notoc}
{: faq}

Le service est créé et entièrement géré par IBM. Chaque service est constitué d'un ensemble dédié de noeuds d'application.

## Comment développer des applications Streams ?
{: #streamsapp notoc}
{: faq}

Vous devez développer des applications Streams localement à l'aide du produit gratuit Streams [{{site.data.keyword.streamsshort}} Quick Start Edition avec Docker ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-docker/) pour les [plans de service version 2](/docs/services/StreamingAnalytics/service_plans.html) ou, si vous utilisez des [plans de service version 1](/docs/services/StreamingAnalytics/service_plans.html), vous pouvez télécharger l'[image de machine virtuelle {{site.data.keyword.streamsshort}} Quick Start Edition![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}.

Vous pouvez également utiliser l'installation d'{{site.data.keyword.streamsshort}} sur site, le cas échéant. Les applications que vous développez et compilez localement peuvent ensuite être déployées en toute transparence sous la forme d'un bundle dans un service Streams dans le cloud.

Toutefois, si vous voulez exécuter vos applications Python dans le cloud, il n'est pas nécessaire d'installer {{site.data.keyword.streamsshort}} sur site. Utilisez simplement le contexte `STREAMING\_ANALYTICS\_SERVICE` pour soumettre vos applications Python au service {{site.data.keyword.streaminganalyticsshort}}. Vous pouvez développer les applications dans un environnement de développement Python standard ou dans un bloc-notes interactif Jupyter, mais vous devez utiliser Python 3.5.

Pour plus d'informations sur le développement d'applications, voir le manuel [{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.streaminganalyticsshort}} Development Guide ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/streamsdev/?p=16589&post_type=doc&preview=1&_ppp=7ad76a418b).

## Puis-je me connecter directement à un hôte de service Streaming Analytics ?
{: #host notoc}  
{: faq}

Non. La connexion directe au serveur via une session Telnet ou Secure Shell (ssh) n'est pas prise en charge. Vous ne pouvez pas installer de logiciels supplémentaires ni exécuter des logiciels non Streams sur un hôte Streams.

## Puis-je accéder au système de fichiers dans le service Streaming Analytics ?
{: #filesystem notoc}
{: faq}   

Seules vos applications Streams peuvent accéder directement au système de fichiers sur un hôte Streams.

Il existe des alternatives prêtes pour le cloud pour les solutions nécessitant un mécanisme pour que Streams puisse interagir avec d'autres composants de solution. Vous pouvez utiliser d'autres protocoles source et collecteur à la place de fichiers. Par exemple, des magasins de données basés sur le cloud.

## Comment les applications du service Streaming Analytics peuvent-elles accéder aux données d'entreprise de mon organisation ?
{: #access notoc}  

Vous pouvez utiliser le [service {{site.data.keyword.Bluemix_notm}} Secure Gateway](https://{DomainName}/catalog/services/secure-gateway) pour connecter en toute sécurité des applications Streams à votre entreprise.

## Les fonctions pour IBM Streams sur site sont-elles toutes prises en charge par le service Streaming Analytics dans le cloud ?
{: #features notoc}

Certaines fonctions ne sont pas prises en charge pour le service {{site.data.keyword.streaminganalyticsshort}}, notamment :

  - Les tâches administratives d'une instance qui nécessitent des droits sur le domaine. Par exemple, l'ajout de balises d'hôte personnalisées ou la création d'un groupe de travaux.
  - Les points de contrôle de région cohérente.
  - Certains des opérateurs de kit d'outils. Pour plus d'informations, voir [Kits d'outils et adaptateurs pris en charge](/docs/services/StreamingAnalytics/compatible_toolkits.html).
  - L'API JMX Streams.

## Où puis-je obtenir davantage d'informations sur le service Streaming Analytics ?
{: #roadmap notoc}

L'article IBM developerWorks® intitulé [Roadmap for {{site.data.keyword.streaminganalyticsshort}} Service on {{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/streamsdev/docs/roadmap-for-streaming-analytics-service-on-bluemix/) comporte des conseils sur le service ainsi que des liens vers des blogues, des démonstrations et des articles.
