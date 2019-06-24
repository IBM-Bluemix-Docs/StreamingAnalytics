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

# Gestione degli endpoint del servizio
{: #manage_endpoints}

Utilizzando un endpoint privato, l'endpoint del servizio {{site.data.keyword.Bluemix_short}} consente la connessione al servizio {{site.data.keyword.streaminganalyticsshort}} tramite la rete {{site.data.keyword.Bluemix_notm}} interna.
{:shortdesc}

Puoi ora aggiungere un endpoint privato per accedere e gestire la tua istanza del servizio.

## Prerequisiti
{: #prereqs notoc}

Assicurati di soddisfare i seguenti requisiti:
- Crea la tua istanza del servizio utilizzando i [piani del contenitore v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) non Lite.
- Abilita il [VRF (Virtual Route Forwarding)](/docs/infrastructure/direct-link?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud) per il tuo account {{site.data.keyword.Bluemix_notm}}.


Per aggiungere un endpoint privato:

1. Nella pagina dei dettagli del servizio, fai clic su **Manage endpoints**. Puoi vedere l'endpoint privato assegnato alla tua istanza del servizio.
2. Fai cli su **Add private endpoint**. Viene assegnato un endpoint privato alla tua istanza del servizio.
3. **Facoltativo.** Utilizza il pulsante di attivazione per abilitare o disabilitare gli endpoint come necessario.


Per ulteriori informazioni sugli endpoint del servizio, consulta la [documentazione dell'endpoint del servizio {{site.data.keyword.Bluemix_notm}}](/docs/services/service-endpoint?topic=service-endpoint-about#about){:new_window}.
