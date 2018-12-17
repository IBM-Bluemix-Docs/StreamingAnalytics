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

# Alta disponibilidade do Streaming Analytics
{: #c_ha}

O {{site.data.keyword.streaminganalyticsshort}} permite alta disponibilidade para seus aplicativos. Se for detectado um problema em um de seus nós do aplicativo (recursos do {{site.data.keyword.streamsshort}}), o nó será substituído automaticamente e qualquer tarefa em execução nesse nó será migrada. As tarefas serão migradas e reiniciadas somente se a instância contiver múltiplos nós de aplicativo. É possível redimensionar a instância usando a [página de detalhes do serviço](/docs/services/StreamingAnalytics/r_service_dashboard.html) ou a [API de REST do {{site.data.keyword.streaminganalyticsshort}} v1 ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} para os [planos de serviço da v1](/docs/services/StreamingAnalytics/service_plans.html). Para planos de serviços da v2, use a API de REST do [v2 ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window}
{:shortdesc}

Este vídeo mostra como redimensionar a instância usando a página de detalhes do serviço:

<iframe width="560" height="315" title="Redimensionar instância" src="https://www.youtube.com/embed/zbZ9am9UhPw?rel=0" frameborder="0" allowfullscreen>Redimensionar instância</iframe>

## Regiões consistentes
Devido às necessidades de negócios, alguns aplicativos requerem que todas as tuplas sejam processadas pelo menos uma vez. O {{site.data.keyword.streamsshort}} é aprimorado com operadores e anotações que permitem a definição de uma região que não perca as tuplas durante o processamento de fluxos. As tuplas em uma região consistente são processadas pelo menos uma vez.

É possível executar e monitorar aplicativos Streams com regiões consistentes definidas no {{site.data.keyword.streaminganalyticsshort}}. Ao criar um serviço do {{site.data.keyword.streaminganalyticsshort}}, a instância já é configurada para usar regiões consistentes.

Uma região consistente é um subgráfico em que os estados dos operadores se tornam consistentes ao processar todas as tuplas e marcas de pontuação em pontos definidos em um fluxo. Isso permite que as tuplas dentro do subgráfico sejam processadas pelo menos uma vez. A região consistente é drenada periodicamente de suas tuplas atuais. Todas as tuplas na região consistente são processadas até o final do subgráfico. O estado contido na memória dos operadores é serializado e armazenado automaticamente no ponto de verificação para cada um dos operadores na região.

Agora é possível gravar os aplicativos Java e SPL que têm garantido o processamento de tupla e a implementação desses aplicativos no {{site.data.keyword.streaminganalyticsshort}}.

É possível definir o início de uma região compatível com a anotação `@consistent` em um operador capaz. O {{site.data.keyword.streamsshort}} determina o escopo da região consistente automaticamente, mas é possível mudar o operador final da região com a anotação `@autonomous`. A região consistente definida periodicamente estabelece um estado consistente.

Consulte a [Documentação do {{site.data.keyword.streamsshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html) para obter mais detalhes sobre o uso de regiões consistentes em aplicativos Streams.
