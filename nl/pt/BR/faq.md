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

# Perguntas Frequentes
{: #faq}

## Como se inscrever para o serviço Streaming Analytics?
{: #signup notoc}  

Para obter informações sobre os planos de serviços do {{site.data.keyword.streaminganalyticsshort}}, veja a [página do catálogo do {{site.data.keyword.Bluemix_short}}](https://console.ng.bluemix.net/catalog/services/streaming-analytics).

## Qual versão do serviço Streaming Analytics eu estou usando?
{: #version notoc}   

Melhorias são enviadas por push regularmente para todos os serviços do {{site.data.keyword.streaminganalyticsshort}}. Você sempre usa a versão mais recente do serviço gerenciado e não há nenhuma versão ou nível do produto para controlar.

## O que a IBM gerencia para mim?
{: #ibm_manage notoc}   

Manipulamos a instalação, os upgrades de software, a criação e o gerenciamento de domínios e a manutenção de hardware. O serviço inclui monitoramento de funcionamento 24 x 7.


## Por quais tarefas eu sou responsável?  
{: #responsible notoc}

Grave os aplicativos que serão executados em um serviço {{site.data.keyword.streaminganalyticsshort}} e na instância do Streams no local e assegure que eles estejam funcionando corretamente e atendendo aos requisitos de desempenho. Você também é responsável por qualquer monitoramento específico do aplicativo.

## A alta disponibilidade (HA) é suportada?
{: #ha notoc}

A alta disponibilidade é gerenciada pela IBM. O {{site.data.keyword.streaminganalyticsshort}} está configurado para suportar HA. Recursos adicionais do servidor estão no local no evento de um failover. 

## Como a segurança é gerenciada para o serviço Streaming Analytics?
{: #security notoc}  

A segurança é totalmente gerenciada pela IBM. As credenciais são geradas para cada serviço e são fornecidas a você. As atualizações de segurança são gerenciadas e aplicadas pela IBM imediatamente depois que elas se tornam disponíveis.

## Preciso configurar um serviço Streaming Analytics?  
{: #configure notoc}

O serviço é criado e totalmente gerenciado pela IBM. Cada serviço consiste em um conjunto dedicado de nós do aplicativo.

## Como desenvolver aplicativos Streams?
{: #streamsapp notoc}

Deve-se desenvolver aplicativos Streams localmente usando o Streams [{{site.data.keyword.streamsshort}} Quick Start Edition gratuitamente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/) ou o [{{site.data.keyword.streamsshort}} Developer Edition ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://www.ibm.com/support/docview.wss?uid=swg24042775).

Também será possível usar a instalação do {{site.data.keyword.streamsshort}} no local, se você tiver uma. Os aplicativos que você desenvolve e compila localmente podem ser facilmente implementados como um pacote configurável para um serviço Streams na nuvem.

Mas se você deseja executar seus aplicativos Python na nuvem, não precisa instalar o {{site.data.keyword.streamsshort}} no local. Basta usar o contexto `STREAMING\_ANALYTICS\_SERVICE` para enviar seus aplicativos Python para o serviço {{site.data.keyword.streaminganalyticsshort}}. É possível desenvolver os aplicativos em um ambiente de desenvolvimento Python padrão ou em um bloco de notas interativo Jupyter, mas deve-se usar o Python 3.5.

Para obter orientação sobre o desenvolvimento de aplicativos, veja o [Guia de desenvolvimento do {{site.data.keyword.Bluemix_notm}} {{site.data.keyword.streaminganalyticsshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/streamsdev/docs/bluemix-streaming-analytics-development-guide/).

## Posso me conectar a um host do serviço Streaming Analytics diretamente?
{: #host notoc}  

Não. Um login direto para o servidor com Telnet ou um Shell Seguro (ssh) não é suportado. Não é possível instalar software adicional ou executar software não Streams em um host do Streams.

## Posso acessar o sistema de arquivos no serviço Streaming Analytics?
{: #filesystem notoc}  

Somente os aplicativos Streams podem acessar diretamente o sistema de arquivos em um host do Streams.

Existem alternativas prontas para nuvem para soluções que precisam de um mecanismo para o Streams para interagir com outros componentes da solução. É possível usar outros protocolos de origem e sorvedouro em vez de arquivos. Por exemplo, armazenamentos de dados baseados em nuvem.

## Como os aplicativos de serviço do Streaming Analytics podem acessar dados corporativos da minha organização?
{: #access notoc}  

É possível usar o [{{site.data.keyword.Bluemix_notm}} Secure Gateway Service](https://console.ng.bluemix.net/catalog/services/secure-gateway) para conectar aplicativos de fluxos com segurança à sua empresa.

## Todos os recursos para o IBM Streams no local são suportados pelo serviço Streaming Analytics na nuvem?
{: #features notoc}

Alguns dos recursos que não são suportados para o serviço {{site.data.keyword.streaminganalyticsshort}} incluem os seguintes:

  - Tarefas administrativas para uma instância que requerem autoridade de domínio. Por exemplo, incluir tags customizadas de host ou criar um grupo de tarefas.
  - Pontos de verificação de região consistentes.
  - Alguns dos operadores do kit de ferramentas não são suportados. Para obter informações, veja [Kits de ferramentas e adaptadores suportados](/docs/services/StreamingAnalytics/compatible_toolkits.html).
  - O Streams JMX API.

## Onde posso aprender mais sobre o serviço Streaming Analytics?
{: #roadmap notoc}

O artigo do IBM developerWorks®, [Roteiro para o serviço {{site.data.keyword.streaminganalyticsshort}} no {{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/streamsdev/docs/roadmap-for-streaming-analytics-service-on-bluemix/), tem orientação para aprender sobre o serviço, além de links para blogs informativos, demos e artigos.
