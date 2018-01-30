---

copyright:
  years: 2015, 2017
lastupdated: "2017-12-15"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Alta disponibilidade do Streaming Analytics
{: #c_ha}

O {{site.data.keyword.streaminganalyticsshort}} permite alta disponibilidade para seus aplicativos. Se for detectado um problema em um de seus nós do aplicativo (recursos do {{site.data.keyword.streamsshort}}), o nó será substituído automaticamente e qualquer tarefa em execução nesse nó será migrada. As tarefas serão migradas e reiniciadas somente se a instância contiver múltiplos nós de aplicativo. É possível redimensionar a instância usando o [painel de serviço](/docs/services/StreamingAnalytics/r_service_dashboard.html) ou a [API de REST do {{site.data.keyword.streaminganalyticsshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://console.ng.bluemix.net/apidocs/220){:new_window}.
{:shortdesc}

Este vídeo mostra como redimensionar sua instância usando o painel de serviço:

<iframe width="560" height="315" src="https://www.youtube.com/embed/zbZ9am9UhPw?rel=0" frameborder="0" allowfullscreen>Redimensionar instância</iframe>
