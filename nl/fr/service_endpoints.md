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

# Gestion des noeuds finaux de service
{: #manage_endpoints}

En utilisant un noeud final privé, le noeud final de service {{site.data.keyword.Bluemix_short}} active la connexion au service {{site.data.keyword.streaminganalyticsshort}} via le réseau {{site.data.keyword.Bluemix_notm}} interne.
{:shortdesc}

Vous pouvez désormais ajouter un noeud final privé pour accéder à votre instance de service et la gérer.

## Prérequis
{: #prereqs notoc}

Vérifiez que les conditions suivantes sont remplies :
- Créez votre instance de service en utilisant des [plans de conteneur version 2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) non Lite.
- Activez [Virtual Route Forwarding (VRF)](/docs/infrastructure/direct-link?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud) pour votre compte {{site.data.keyword.Bluemix_notm}}.


Pour ajouter un noeud final privé :

1. Sur la page des détails du service, cliquez sur **Gérer les noeuds finaux**. Vous pouvez voir le noeud final public affecté à votre instance de service.
2. Cliquez sur **Ajouter un noeud final privé**. Un noeud final privé est affecté à votre instance de service.
3. **Facultatif** Au besoin, utilisez le bouton de bascule des noeuds finaux pour les activer ou les désactiver.


Pour plus d'informations sur les noeuds finaux de service, voir la [documentation relative aux noeuds finaux de service {{site.data.keyword.Bluemix_notm}}](/docs/services/service-endpoint?topic=service-endpoint-about#about){:new_window}.
