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

# V1 e v2 planos de serviço
{: #service_plans}

{{site.data.keyword.streaminganalyticsshort}} agora está em execução em uma infraestrutura baseada em contêiner do Kubernetes que fornece vantagens de segurança e disponibilidade para o serviço.
{:shortdesc}

É possível acessar essa nova infraestrutura baseada em contêiner com os planos de serviço v2. É possível escolher o plano do {{site.data.keyword.streaminganalyticsshort}} que seja mais adequado ao trabalho que precisa fazer:


<table summary="Esta tabela fornece uma lista de planos de serviços que podem ser usados para criar o seu serviço do {{site.data.keyword.streaminganalyticsshort}}. A tabela lista todos os planos de serviços para os conjuntos de planos da v1 e da v2 e fornece uma lista de recursos para cada conjunto.">
  <tr>
    <th>Plano de Serviço definido<br></th>
    <th>Plano de nomes<br></th>
    <th>Recursos disponíveis<br></th>
  </tr>
  <tr>
    <td width="15%">
    Planos de serviço da v1 (descontinuados)    
    </td>
    <td width="35%">
    <ul>
      <li>Lite VM</li>
      <li>Entrada da VM de Hora</li>
      <li>Entrada VM Mensal</li>
      <li>Hora da VM Aprimorada</li>
      <li>Aprimorado VM Mensal</li>
      <li>Assinatura VM Aprimorada</li>
      <li>Premium VM Mensal</li>
      <li>Premium VM Assinatura</li>
    </ul>
    </td>
    <td>
      <ul>
        <li>Requer a compilação do aplicativo Streams em um sistema operacional Red Hat Enterprise Linux (RHEL) 6.5 ou uma versão equivalente do CentOS.</li>
        <li>Executa em uma infraestrutura VM baseada.</li>
        <li>Suporta v1 e v2 APIs REST.<br></li>
        <li>Suporta autenticação IAM e autenticação de credenciais do usuário.</li>
        <li>Suporta [{{site.data.keyword.streamsshort}} imagem da VM do Quick Start Edition ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-linux/)
      </ul>    
    </td>
  </tr>
  <tr>
    <td>
    V2 planos de serviço
    </td>
    <td>
      <ul>
        <li>Lite</li>
        <li>Contêiner de entrada por hora</li>
        <li>Contêiner de Entrada Mensal</li>
        <li>Assinatura de contêiner de entrada</li>
        <li>Hora do Contêiner Aprimorada</li>
        <li>Contêiner Enhanced Mensal</li>
        <li>Assinatura de contêiner aprimorada</li>
        <li>Hora do Contêiner Premium</li>
        <li>Premium Contêiner Mensal</li>
        <li>Assinatura de contêiner Premium</li>
      </ul>
    </td>
    <td>
    <ul>
      <li>Requer que você compile seu aplicativo Streams em um sistema operacional RHEL 7.x ou uma versão equivalente do CentOS.</li>
      <li>É executado em uma infraestrutura baseada em contêiner.</li>
      <li>Suporta v2 APIs REST.<br></li>
      <li>Suporta autenticação do IAM.</li>
      <li>Suporta os terminais de serviço para planos de serviço não Lite</li>
      <li>Suporta o [{{site.data.keyword.streamsshort}} Quick Start Edition com o Docker ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-docker/)</li>
    </ul>
    </td>
  </tr>
</table>

*Tabela 1. Planos de serviços do {{site.data.keyword.streaminganalyticsshort}} v1 e v2*

## Diferenças entre planos de serviços da v1 e v2

Os recursos a seguir são suportados apenas nos planos de serviços da v1:

* [v1 REST API](https://{DomainName}/apidocs/streaming-analytics-v1). Na infraestrutura v2, deve-se usar a API de REST do [{{site.data.keyword.streaminganalyticsshort}} v2](https://{DomainName}/apidocs/streaming-analytics-v2)
* Aplicativos de amostra NYC Traffic e Event Detection v1. Consulte [Aplicativos de amostra](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps) para obter uma lista de aplicativos que podem ser usados para iniciar o {{site.data.keyword.streaminganalyticsshort}} na infraestrutura v2 baseada em contêiner.
* Compatibilidade de alguns kits. Consulte [Kits de ferramentas compatíveis](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-compatible_toolkits) para obter uma lista de kits de ferramentas compatíveis com a nova infraestrutura baseada em contêiner.

## Variável de ambiente VCAP_SERVICES para planos de serviço v1
{: #vcap_services}

As credenciais de serviço do {{site.data.keyword.streaminganalyticsshort}} e a variável de ambiente VCAP_SERVICES para planos de serviços v1 incluem as informações de VCAP que são necessárias para usar a API de REST do {{site.data.keyword.streaminganalyticsshort}} v1. As informações de VCAP fornecem a URL de REST, o ID da instância de serviço, o ID de ligação e as credenciais para cada API de REST do {{site.data.keyword.streaminganalyticsshort}} v1.  
{:shortdesc}

 Quando uma instância de serviço do {{site.data.keyword.streaminganalyticsshort}} é provisionada e ligada a um aplicativo no {{site.data.keyword.Bluemix_notm}}, as informações do VCAP da instância de serviço ficam disponíveis para o ambiente de aplicativos do {{site.data.keyword.Bluemix_notm}}. É possível localizar essas informações na variável de ambiente VCAP_SERVICES. Quando uma instância de serviço do {{site.data.keyword.streaminganalyticsshort}} é provisionada sem especificar um aplicativo no {{site.data.keyword.Bluemix_notm}} para o qual ligar, as credenciais de serviço são criadas automaticamente. As credenciais de serviço do {{site.data.keyword.streaminganalyticsshort}} podem ser acessadas por meio da página de detalhes do serviço.


As credenciais de serviço do {{site.data.keyword.streaminganalyticsshort}} e a variável de ambiente VCAP_SERVICES incluem informações conforme apresentado no exemplo a seguir:

<pre><code>
{
  "streaming-analytics": [
    {
      "name": "NYCTrafficStreaming Analytics-t6",
      "label": "streaming-analytics",
      "plan": "Standard",
      "credentials": {
        "status_path": "/jax-rs/streams/status/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "size_path": "/jax-rs/streams/size/service_instances/0fb17393-90eb-4066-96b6-df1ac9860743/service_bindings/b37b89df-b0d7-464e-b7d9-3db607a26550",
        "start_path": "/jax-rs/streams/start/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "stop_path": "/jax-rs/streams/stop/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "resources_path": "/jax-rs/resources/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "jobs_path": "/jax-rs/jobs/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "rest_host": "{rest_url}",
        "rest_port": "443",
        "rest_url": "{rest_url}",
        "userid": "xxx",
        "password": "yyy"
      }
    }
  ]
}	  
</code></pre>

Para obter mais informações sobre a API de REST da v1, consulte a [documentação da API de REST da v1 ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window}.

## Variável de ambiente VCAP_SERVICES para planos de serviços da v2
{: #v2_vcap_services}

As credenciais de serviço do {{site.data.keyword.streaminganalyticsshort}} e a variável de ambiente VCAP_SERVICES para planos de serviço v2 incluem as informações do VCAP que devem ser usadas com a API de REST do {{site.data.keyword.streaminganalyticsshort}} v2. As informações de VCAP fornecem a URL de REST da v2, o ID de serviço e as credenciais para acessar a API de REST do {{site.data.keyword.streaminganalyticsshort}} v2.  
{:shortdesc}

As credenciais de serviço e a variável de ambiente VCAP_SERVICES do {{site.data.keyword.streaminganalyticsshort}} para planos de serviços da v2 incluem informações, conforme apresentadas no exemplo a seguir:

<pre><code>
    {
      "Apikey": "aaaabbbbb1111222ABCDEFgh567appjurHKyY",
      "iam_apikey_description": "Auto generated apikey during resource-key operation for Instance - crn:v1:bluemix:public:streaming-analytics:us-south:a/aaabbbb120110ab123d456e78a0b78910:12e3456e-102f-47e0-9600-4313d496e07a::",
      "iam_apikey_name": "auto-generated-apikey-ab12c34d-e5d6-7890-123f-45dcece304df",
      "Iam_role_crn": "crn:v1 :bluemix:public:iam ::::serviceRole :Manager",
      "Iam_serviceid_crn": "crn:v1 :bluemix:public:iam-identity ::a/b123bb45670ab123d123e12d0a12345: :serviceid: ServiceId-a1234b5c-678d-9f6f-bdb4-16c23935efb5",
      "v2_rest_url": "{rest_url}/v2/streaming_analytics/a1234b5c-678d-9f6f-bdb4-16c23935efb5"
    }
</code></pre>

Para obter mais informações sobre a API de REST da v2, consulte a [documentação da API de REST da v2 ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window}.
