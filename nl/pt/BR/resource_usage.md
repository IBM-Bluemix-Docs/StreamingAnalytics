---

copyright:
  years: 2015, 2018
lastupdated: "2018-04-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}


# Uso do Recurso
{: #resourceusage}

O {{site.data.keyword.streaminganalyticsshort}} possui uma série de comportamentos e políticas para garantir a alocação e o uso apropriado de recursos.

## Visualizando e editando recursos de instância
É possível visualizar e editar o número de recursos autorizados para a instância no painel de serviços ou usar a API de REST
do v1 para [os planos de serviços da v1](/docs/services/StreamingAnalytics/service_plans.html) ou a
[{{site.data.keyword.streaminganalyticsshort}}
API de REST da v2](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#get-a-streaming-analytics-instance) para os [planos de serviços da v2](/docs/services/StreamingAnalytics/service_plans.html).

## Alocação de recurso
- Os recursos são alocados automaticamente para a instância quando você envia uma tarefa que é executada com êxito.
- Os recursos são removidos da instância se não há tarefas em execução no recurso. Por exemplo, você tem duas tarefas, em que a tarefa 1 está em execução no recurso 1 e a tarefa 2 está em execução no recurso 1 e no recurso 2. Se a tarefa 2 é cancelada, o recurso 1 permanece na instância enquanto o recurso 2 é removido.
- Ao enviar uma tarefa, ela é colocada em um novo recurso se a instância não atingiu seu limite de alocação.
- Quando uma instância está usando todos os seus recursos autorizados, novas tarefas são planejadas em recursos existentes.

## Restrições de recursos

As restrições de recursos podem ser usadas para controlar a alocação e o uso de recursos. Por exemplo, usando as restrições de recursos é possível especificar que duas tarefas utilizam um único recurso, em vez de serem separadas em dois recursos.
