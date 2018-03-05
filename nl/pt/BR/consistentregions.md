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


# Aprimoramentos de alta disponibilidade
{: #consistentregions}

Devido às necessidades de negócios, alguns aplicativos requerem que todas as tuplas sejam processadas pelo menos uma vez. O {{site.data.keyword.streamsshort}} é aprimorado com operadores e anotações que permitem a definição de uma região sem que essa perca as tuplas durante o processamento de fluxos. As tuplas em uma região consistente são processadas pelo menos uma vez.


Se você usa os planos de precificação Beta-Entry ou Beta-Enhanced, agora é possível executar e monitorar aplicativos Streams com regiões consistentes definidas no {{site.data.keyword.streaminganalyticsshort}}.Quando você cria um serviço {{site.data.keyword.streaminganalyticsshort}} com os planos Beta-Entry ou Beta-Enhanced, a instância já está configurada para usar regiões consistentes.

Uma região consistente é um subgráfico em que os estados dos operadores se tornam consistentes ao processar todas as tuplas e marcas de pontuação em pontos definidos em um fluxo. Isso permite que as tuplas dentro do subgráfico sejam processadas pelo menos uma vez. A região consistente é drenada periodicamente de suas tuplas atuais. Todas as tuplas na região consistente são processadas até o final do subgráfico. O estado contido na memória dos operadores é serializado e armazenado automaticamente no ponto de verificação para cada um dos operadores na região.

Agora é possível gravar os aplicativos Java e SPL que têm garantido o processamento de tupla e a implementação desses aplicativos no {{site.data.keyword.streaminganalyticsshort}}.

É possível definir o início de uma região compatível com a anotação `@consistent` em um operador capaz. O {{site.data.keyword.streamsshort}} determina o escopo da região consistente automaticamente, mas é possível mudar o operador final da região com a anotação `@autonomous`. A região consistente definida periodicamente estabelece um estado consistente.

Veja a [ documentação do {{site.data.keyword.streamsshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.1/com.ibm.streams.dev.doc/doc/consistentregions.html) para obter mais detalhes sobre como usar regiões consistente em aplicativos Streams.
