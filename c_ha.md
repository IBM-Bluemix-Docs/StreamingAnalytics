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

# Streaming Analytics high availability
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} enables high availability for your applications. If an issue is detected on one of your application nodes ({{site.data.keyword.streamsshort}} resources), the node is automatically replaced and any jobs running on that node are migrated. Jobs are only migrated and restarted if the instance contains multiple application nodes. You can resize the instance by using the [service dashboard](/docs/services/StreamingAnalytics/r_service_dashboard.html) or the [{{site.data.keyword.streaminganalyticsshort}} REST API ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.ng.bluemix.net/apidocs/220){:new_window}.
{:shortdesc}

This video shows how to resize your instance using the service dashboard:

<iframe width="560" height="315" src="https://www.youtube.com/embed/zbZ9am9UhPw?rel=0" frameborder="0" allowfullscreen>Resize instance</iframe>
