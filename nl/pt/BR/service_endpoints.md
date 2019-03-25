---

copyright:
  years: 2015, 2019
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Gerenciando os terminais em serviço
{: #manage_endpoints}

Usando um terminal interno, o {{site.data.keyword.Bluemix_short}} Service Endpoint permite a conexão com o serviço do {{site.data.keyword.streaminganalyticsshort}} por meio da rede interna do IBM Cloud.
{:shortdesc}

Agora, é possível incluir um terminal interno para acessar e gerenciar sua instância de serviço.

## Pré-requisitos
{: #prereqs notoc}

Assegure-se de atender aos requisitos a seguir:
- Crie a sua instância de serviço usando os [planos do contêiner da v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) não Lite.
- Crie a sua instância de serviço nas regiões do Reino Unido (Londres) ou da Alemanha (Frankfurt) do {{site.data.keyword.Bluemix_short}}.
- Ative o [Virtual Route Forwarding (VRF)](/docs/infrastructure/direct-link?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud) para a sua conta do {{site.data.keyword.Bluemix_short}}.


Para incluir um terminal interno:

1. Na página de detalhes do serviço, clique em **Gerenciar terminais**. É possível ver o terminal externo designado para a sua instância de serviço.
2. Clique em **Incluir terminal interno**. Um terminal interno é designado para a sua instância de serviço.
3. **Opcional.** Use a alternância de terminal para ativar ou desativar os terminais, conforme necessário.


Para obter mais informações sobre os terminais em serviço, consulte a [documentação do {{site.data.keyword.Bluemix_short}} Service Endpoint](/docs/services/service-endpoint?topic=about){:new_window}.
