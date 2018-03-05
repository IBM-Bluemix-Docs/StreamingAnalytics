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

# Planos Beta-Entry e Beta-Enhanced
{: #beta_plans}

Os novos planos Beta-Entry e Beta-Enhanced do serviço {{site.data.keyword.streaminganalyticsshort}} incluem vários aprimoramentos e diferenças dos planos de serviços existentes:
{:shortdesc}

**Novo [{{site.data.keyword.streamsshort}} QSE for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi):** A {{site.data.keyword.streamsshort}} Quick Start Edition é uma versão gratuita de não produção do {{site.data.keyword.streamsshort}}. Para usar os planos Beta-Entry e Beta-Enhanced para implementar aplicativos para o {{site.data.keyword.streaminganalyticsshort}}, deve-se compilar seus aplicativos usando o Red Hat Enterprise Linux (RHEL) versão 7 do {{site.data.keyword.streamsshort}} QSE.
Veja o [Guia de Desenvolvimento Beta ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/streamsdev/docs/cloud-beta-devguide/) para saber como usar o novo Streams QSE com o RHEL 7 em execução em um ambiente do Docker para compilar e implementar seus aplicativos com os novos planos beta do{{site.data.keyword.streaminganalyticsshort}}.   

**{{site.data.keyword.streaminganalyticsshort}} API de REST v2:** é possível usar a[{{site.data.keyword.streaminganalyticsshort}} API de REST v2 ![Ícone de link externo](../../icons/launch-glyph.svg "ìcone de link externo")](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#introduction) para gerenciar suas instâncias de serviço e as tarefas do {{site.data.keyword.streamsshort}}. A API v2 do {{site.data.keyword.streaminganalyticsshort}} é suportada apenas em instâncias de serviço criadas com um dos novos planos beta. A [ API de REST v1 ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://console.bluemix.net/apidocs/220-streaming-analytics?&language=node#introduction) é suportada apenas em instâncias existentes do {{site.data.keyword.streaminganalyticsshort}} e em quaisquer novas instâncias criadas com os planos de serviços existentes.

**Novos aplicativos iniciadores e de amostra:** como os planos novos beta requerem a execução do Streams no RHEL 7, muitos dos aplicativos de amostra existentes não funcionam com os novos planos beta. O {{site.data.keyword.streaminganalyticsshort}} fornece um [novo conjunto de aplicativos iniciadores e de amostra]( https://developer.ibm.com/streamsdev/docs/cloud-beta-samples/) para introduzi-lo rapidamente aos novos planos beta.

**Aprimoramentos de alta disponibilidade:** evite perda de dados em aplicativos de processamento de fluxos definindo regiões consistentes. O {{site.data.keyword.streamsshort}} é aprimorado com operadores e anotações que permitem a definição de uma região que não perca as tuplas durante o processamento de fluxos. As tuplas em uma região consistente são processadas pelo menos uma vez.
Se você usa os planos de precificação Beta-Entry ou Beta-Enhanced, agora é possível executar e monitorar aplicativos Streams com [regiões consistentes definidas no {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/consistentregions.html).

**Novos recursos de determinação de problema:** os planos Beta-Entry e Beta-Enhanced incluem vários aprimoramentos para ajudá-lo a localizar e corrigir rapidamente erros em seus aplicativos. Para obter mais detalhes, consulte [O {{site.data.keyword.streaminganalyticsshort}} Console oferece mais maneiras de localizar e corrigir erros (planos Beta) ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo").](https://wp.me/p4IICn-4cx)

**Monitorando como os operadores se comportam e garantindo o processamento da tupla na nuvem:** o {{site.data.keyword.streamsshort}} fornece métricas para ajudar a avaliar o funcionamento de serviços do {{site.data.keyword.streamsshort}} para auxiliar no diagnóstico de problemas de desempenho e para analisar o rendimento das solicitações. É possível usar o Streams Console em {{site.data.keyword.streaminganalyticsshort}} para [monitorar como os operadores se comportam e garantir a otimização de recursos ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo").](https://wp.me/p4IICn-4bH)
