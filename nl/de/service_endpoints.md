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

# Serviceendpunkte verwalten
{: #manage_endpoints}

Mithilfe eines internen Endpunkts ermöglicht {{site.data.keyword.Bluemix_short}} Service Endpoint die Herstellung einer Verbindung zum {{site.data.keyword.streaminganalyticsshort}}-Service über das interne IBM Cloud-Netz.
{:shortdesc}

Es ist nun möglich, einen internen Endpunkt hinzuzufügen, über den Sie auf die Serviceinstanz zugreifen und diese verwalten können. 

## Voraussetzungen
{: #prereqs notoc}

Stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
- Erstellung der Serviceinstanz mit den [v2-Containerplänen](/docs/services/StreamingAnalytics/service_plans.html) (keine Lite-Pläne).
- Erstellung der Serviceinstanz in den {{site.data.keyword.Bluemix_short}}-Regionen 'Vereinigtes Königreich (London)' oder 'Deutschland (Frankfurt)'.
- Aktivierung von [Virtual Route Forwarding (VRF)](/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud) für Ihr {{site.data.keyword.Bluemix_short}}-Konto.


Gehen Sie wie folgt vor, um einen internen Endpunkt hinzuzufügen:

1. Klicken Sie auf der Servicedetailseite auf **Endpunkte verwalten**. Sie Ihrer Serviceinstanz zugewiesenen externen Endpunkte werden angezeigt. 
2. Klicken Sie auf **Internen Endpunkt hinzufügen**. Ein interner Endpunkt wird Ihrer Serviceinstanz zugewiesen. 
3. **Optional.** Mithilfe der Option zum Aktivieren/Inaktivieren von Endpunkten können Sie bei Bedarf zur entsprechenden Einstellung wechseln.


Weitere Informationen zu Serviceendpunkten finden Sie in der [{{site.data.keyword.Bluemix_short}} Service Endpoint-Dokumentation](/docs/services/service-endpoint/getting-started.html#about){:new_window}.
