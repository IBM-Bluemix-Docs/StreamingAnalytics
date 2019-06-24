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

# Gestión de puntos finales de servicio
{: #manage_endpoints}

Utilizando un punto final privado, {{site.data.keyword.Bluemix_short}} Service Endpoint permite la conexión al servicio {{site.data.keyword.streaminganalyticsshort}} a través de una red interna de {{site.data.keyword.Bluemix_notm}}.
{:shortdesc}

Ahora puede añadir un punto final privado para acceder y gestionar su instancia de servicio.

## Requisitos previos
{: #prereqs notoc}

Asegúrese de que cumpla con los siguientes requisitos:
- Cree la instancia de servicio utilizando [planes de contenedor v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) que no sean Lite.
- Habilite [Virtual Route Forwarding (VRF)](/docs/infrastructure/direct-link?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud) para su cuenta de {{site.data.keyword.Bluemix_notm}}.


Para añadir un punto final privado:

1. En la página de detalles del servicio, pulse **Gestionar puntos finales**. Puede ver el punto final público asignado a su instancia de servicio.
2. Pulse **Añadir punto final privado**. Se asigna un punto final privado a la instancia de servicio.
3. **Opcional.** Utilice el conmutador de punto final para habilitar o inhabilitar puntos finales según sea necesario.


Para obtener más información sobre los puntos finales de servicio, consulte la [documentación de {{site.data.keyword.Bluemix_notm}} Service Endpoint](/docs/services/service-endpoint?topic=service-endpoint-about#about){:new_window}.
