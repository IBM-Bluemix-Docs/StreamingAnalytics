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

# Gestión de puntos finales de servicio
{: #manage_endpoints}

Utilizando un punto final interno, {{site.data.keyword.Bluemix_short}} Service Endpoint permite la conexión del servicio {{site.data.keyword.streaminganalyticsshort}} mediante la red interna de IBM Cloud.
{:shortdesc}

Ahora puede añadir un punto final interno para acceder y gestionar su instancia de servicio.

## Requisitos previos
{: #prereqs notoc}

Asegúrese de que cumpla con los siguientes requisitos:
- Cree la instancia de servicio utilizando [planes de contenedor v2](/docs/services/StreamingAnalytics/service_plans.html) que no sean Lite.
- Cree la instancia de servicio en las regiones de Reino Unido (RU)o Alemania (Frankfurt) de {{site.data.keyword.Bluemix_short}}.
- Habilite [Virtual Route Forwarding (VRF)](/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud) para su cuenta de {{site.data.keyword.Bluemix_short}}.


Para añadir un punto final interno:

1. En la página de detalles del servicio, pulse **Gestionar puntos finales**. Puede ver el punto final externo asignado a su instancia de servicio.
2. Pulse **Añadir punto final interno**. Se asigna un punto final interno a la instancia de servicio.
3. **Opcional.** Utilice el conmutador de punto final para habilitar o inhabilitar puntos finales según sea necesario.


Para obtener más información sobre los puntos finales de servicio, consulte la [documentación de {{site.data.keyword.Bluemix_short}} Service Endpoint](/docs/services/service-endpoint/getting-started.html#about){:new_window}.
