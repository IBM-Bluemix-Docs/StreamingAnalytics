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

# Serviceendpunkte verwalten
{: #manage_endpoints}

Mithilfe eines privaten Endpunkts ermöglicht {{site.data.keyword.Bluemix_short}} Service Endpoint die Herstellung einer Verbindung zum {{site.data.keyword.streaminganalyticsshort}}-Service über das interne {{site.data.keyword.Bluemix_notm}}-Netz.
{:shortdesc}

Es ist nun möglich, einen privaten Endpunkt hinzuzufügen, über den Sie auf die Serviceinstanz zugreifen und diese verwalten können.

## Voraussetzungen
{: #prereqs notoc}

Stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
- Erstellung der Serviceinstanz mit den [v2-Containerplänen](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) (keine Lite-Pläne).
- Aktivierung von [Virtual Route Forwarding (VRF)](/docs/infrastructure/direct-link?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud) für Ihr {{site.data.keyword.Bluemix_notm}}-Konto.


Gehen Sie wie folgt vor, um einen privaten Endpunkt hinzuzufügen:

1. Klicken Sie auf der Servicedetailseite auf **Endpunkte verwalten**. Sie Ihrer Serviceinstanz zugewiesenen öffentlichen Endpunkte werden angezeigt.
2. Klicken Sie auf **Privaten Endpunkt hinzufügen**. Ein privater Endpunkt wird Ihrer Serviceinstanz zugewiesen.
3. **Optional.** Mithilfe der Option zum Aktivieren/Inaktivieren von Endpunkten können Sie bei Bedarf zur entsprechenden Einstellung wechseln.


Weitere Informationen zu Serviceendpunkten finden Sie in der [{{site.data.keyword.Bluemix_notm}} Service Endpoint-Dokumentation](/docs/services/service-endpoint?topic=service-endpoint-about#about){:new_window}.
