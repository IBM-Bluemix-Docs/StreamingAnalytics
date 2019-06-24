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

# Alta disponibilidade e recuperação de desastre
{: #c_ha}

O {{site.data.keyword.streaminganalyticsshort}} está altamente disponível dentro de uma localização do {{site.data.keyword.Bluemix_notm}} (por exemplo, Dallas, Washington DC, Londres, Frankfurt). No entanto, a recuperação de potenciais desastres que afetam uma região inteira do {{site.data.keyword.Bluemix_notm}} requer planejamento e preparação.
{:shortdesc}


Você é responsável por entender sua configuração, customização e uso do serviço. Você também é responsável por estar pronto para recriar uma instância do serviço em uma nova localização do {{site.data.keyword.Bluemix_notm}} e por reimplementar seus aplicativos nessa localização. Consulte
[Como assegurar tempo de inatividade zero?](/docs/services/overview?topic=overview-zero-downtime#zero-downtime) para saber mais sobre os padrões de alta disponibilidade e de recuperação de desastre no {{site.data.keyword.Bluemix_notm}}. Também é possível localizar informações sobre [Acordos de Nível de Serviço](/docs/services/overview?topic=overview-zero-downtime#zero-downtime#SLAs).

## Alta disponibilidade

O {{site.data.keyword.streaminganalyticsshort}} permite alta disponibilidade para seus aplicativos. Seus aplicativos são implementados em contêineres Docker que são executados em clusters Kubernetes. Para gravar aplicativos altamente disponíveis, deve-se entender como esses contêineres funcionam para assegurar a alta disponibilidade:

* Os recursos de aplicativo são contêineres com CPU e memória alocados de acordo com seu plano de serviço.
* Durante uma falha de hardware ou de software, os contêineres podem se mover. Quando os contêineres são movidos, os elementos de processamento são reiniciados.
* Durante a manutenção planejada, os contêineres podem se mover (elementos de processamento são reiniciados).

Portanto, ao gravar seus aplicativos, deve-se considerar que os contêineres podem se mover ocasionalmente. Além disso, considere os itens a seguir:
* Assegure-se de que os elementos de processamento sejam reinicializáveis e realocáveis.
* Assegure-se de que seu aplicativo possa tolerar a reinicialização de alguns ou de todos os seus elementos de processamento (PEs), em qualquer ordem.
* Assegure-se de que os operadores sink e source em seu aplicativo Streams estejam configurados para restabelecer as conexões quando seu elemento de processamento for reiniciado.

Consulte o [Guia de desenvolvimento do {{site.data.keyword.streaminganalyticsshort}}](https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/#troubleshooting) para obter exemplos de como solucionar problemas de seu aplicativo.

Para implementar a alta disponibilidade, os aplicativos Streams são ativados para garantir o processamento de todas as tuplas. Para alcançar um processamento de tupla garantido, um ponto de verificação é estabelecido periodicamente para todos os operadores em uma região consistente. Após a falha de um aplicativo, todos os operadores são retrocedidos para os estados de pontos de verificação bem-sucedidos mais recentes.
O {{site.data.keyword.streaminganalyticsshort}} permite o uso de regiões consistentes.

### Processamento de tupla garantido
Devido às necessidades de negócios, alguns aplicativos requerem que todas as tuplas sejam processadas pelo menos uma vez. O {{site.data.keyword.streamsshort}} é aprimorado com operadores e anotações que permitem a definição de uma região que não perde tuplas durante o processamento de fluxos. As tuplas em uma região consistente são processadas pelo menos uma vez.

Se qualquer falha de aplicativo for detectada dentro de uma região consistente, o {{site.data.keyword.streaminganalyticsshort}} poderá configurar o aplicativo de volta para o último estado consistente (também conhecido como ponto de verificação) e direcionar as origens de dados do aplicativo para reproduzir tuplas desse ponto em diante.

É possível executar e monitorar aplicativos Streams com regiões consistentes definidas no {{site.data.keyword.streaminganalyticsshort}}. Quando você cria um serviço {{site.data.keyword.streaminganalyticsshort}}, a instância já está configurada para permitir o uso de regiões consistentes.

Uma região consistente é um subgráfico no qual os estados dos operadores se tornam consistentes por meio do processamento de todas as tuplas e marcas de pontuação dentro de pontos definidos em um fluxo. Isso permite que as tuplas dentro do subgráfico sejam processadas pelo menos uma vez. Periodicamente, as tuplas atuais são drenadas da região consistente. Todas as tuplas na região consistente são processadas até o final do subgráfico. O estado na memória dos operadores é serializado automaticamente e armazenado no ponto de verificação para cada um dos operadores na região.

É possível gravar aplicativos Java, SPL e Python que têm o processamento de tupla garantido e implementar esses aplicativos no {{site.data.keyword.streaminganalyticsshort}}.

É possível definir o início de uma região consistente com a anotação `@consistent` em um operador capaz. O {{site.data.keyword.streamsshort}} determina o escopo da região consistente automaticamente, mas é possível mudar o operador final da região com a anotação `@autonomous`. A região consistente definida periodicamente estabelece um estado consistente.

Consulte a [documentação do {{site.data.keyword.streamsshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html) para obter mais detalhes sobre o uso das regiões consistentes em aplicativos Streams.

## Recuperação de Desastres
O {{site.data.keyword.streaminganalyticsshort}} é um serviço GA oferecido em múltiplas regiões do {{site.data.keyword.Bluemix_notm}}. O {{site.data.keyword.streaminganalyticsshort}} não armazena dados do usuário no {{site.data.keyword.Bluemix_notm}}.

Com base em seus requisitos de negócios, selecione uma das estratégias de recuperação de desastre a seguir:
* Se você não precisar de nenhuma interrupção em seu aplicativo:
  1. Crie instâncias do {{site.data.keyword.streaminganalyticsshort}} em múltiplas regiões do {{site.data.keyword.Bluemix_notm}}.
  2. Envie seu aplicativo para múltiplas regiões.


* Se você precisar de uma interrupção mínima em seu aplicativo:
  1. Crie instâncias do {{site.data.keyword.streaminganalyticsshort}} em múltiplas regiões do {{site.data.keyword.Bluemix_notm}}.
  2. Monitore o seu aplicativo usando a [API de REST de serviço](https://ibm.co/2Gt9mB6) e dinamicamente alterne sua carga de trabalho para uma nova região, conforme necessário.

**Nota**: cada região consistente está ligada à região do {{site.data.keyword.Bluemix_notm}}. Em um cenário de recuperação de desastre, as regiões consistentes em um aplicativo não têm nenhuma função.
