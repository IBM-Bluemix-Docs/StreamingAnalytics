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

# Streaming Analytics ad alta disponibilità
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} abilita
l'alta disponibilità per le tue applicazioni. Se viene rilevato un problema su uno dei nodi della tua applicazione,
(risorse {{site.data.keyword.streamsshort}}), il nodo viene
automaticamente sostituito e ogni lavoro in esecuzione su tale nodo viene migrato. I lavori vengono migrati e riavviati
solo se l'istanza contiene più nodi di applicazione. Puoi ridimensionare l'istanza utilizzando il [dashboard del servizio](/docs/services/StreamingAnalytics/r_service_dashboard.html) o l'[{{site.data.keyword.streaminganalyticsshort}}API REST ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://console.ng.bluemix.net/apidocs/220){:new_window}.
{:shortdesc}

Questo video mostra come ridimensionare la tua istanza utilizzando il dashboard del servizio:

<iframe width="560" height="315" src="https://www.youtube.com/embed/zbZ9am9UhPw?rel=0" frameborder="0" allowfullscreen>Ridimensiona istanza</iframe>
