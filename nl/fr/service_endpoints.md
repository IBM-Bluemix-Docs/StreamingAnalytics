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

# Gestion des noeuds finaux de service
{: #manage_endpoints}

En utilisant un noeud final interne, le noeud final de service {{site.data.keyword.Bluemix_short}} active la connexion au service {{site.data.keyword.streaminganalyticsshort}} via le réseau IBM Cloud interne.
{:shortdesc}

Vous pouvez maintenant ajouter un noeud final interne pour accéder à votre instance de service et a gérer.

## Prérequis
{: #prereqs notoc}

Vérifiez que les conditions suivantes sont remplies :
- Créez votre instance de service en utilisant des [plans de conteneur version 2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) non Lite.
- Créez votre instance de service dans les régions {{site.data.keyword.Bluemix_short}} Royaume-Uni (Londres) ou Allemagne (Francfort).
- Activez [Virtual Route Forwarding (VRF)](/docs/infrastructure/direct-link?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud) pour votre compte {{site.data.keyword.Bluemix_short}}.


Pour ajouter un noeud final interne :

1. Sur la page des détails du service, cliquez sur **Gérer les noeuds finaux**. Vous pouvez voir le noeud final externe affecté à votre instance de service.
2. Cliquez sur **Ajouter un noeud final interne**. Un noeud final interne est affecté à votre instance de service.
3. **Facultatif** Au besoin, utilisez le bouton de bascule des noeuds finaux pour les activer ou les désactiver.


Pour plus d'informations sur les noeuds finaux de service, voir la [documentation relative aux noeuds finaux de service {{site.data.keyword.Bluemix_short}}](/docs/services/service-endpoint?topic=about){:new_window}.
