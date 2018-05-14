---

copyright:
  years: 2015, 2018
lastupdated: "2018-04-24"

---

<!-- Attribute definitions -->
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Resolução de problemas do Streaming Analytics
{: #ts_StreamingAnalytics}

É possível localizar as respostas a perguntas comuns sobre como usar o {{site.data.keyword.streaminganalyticsshort}} no {{site.data.keyword.Bluemix_short}}.
{:shortdesc}

## Ao ativar o serviço, sou solicitado por credenciais para efetuar login no console
{: #log_in_console}

Ao ativar o {{site.data.keyword.streaminganalyticsshort}}, você é solicitado por credenciais para efetuar login no console de serviço.
{:shortdesc}

Você ativa um serviço do {{site.data.keyword.streaminganalyticsshort}} que criou anteriormente e, em vez de acessar diretamente o console de serviço, verá uma página de login na qual serão solicitadas as credenciais.
{: tsSymptoms}

A infraestrutura de serviço foi atualizada e o cache do navegador está impedindo o serviço de coletar a atualização.
{: tsCauses}

Limpe o cache do navegador para certificar-se de obter a versão mais recente do console de serviço.
{: tsResolve}

## Meu aplicativo está unhealthy
{: #app_unhealthy}

Não é possível executar seu aplicativo corretamente e o status de funcionamento é `unhealthy`.
{:shortdesc}

Você envia um aplicativo para a instância de serviço, o aplicativo é iniciado, mas falha imediatamente e o status de funcionamento é `unhealthy`. O erro a seguir aparece no arquivo de log: `/lib64/libc.so.6: version GLIBC_2.14 not found`.
{: tsSymptoms}

O aplicativo não foi compilado usando um sistema operacional RHEL 7.x ou uma versão equivalente do CentOS.
{: tsCauses}

Será necessário recompilar o aplicativo no Red Hat Enterprise Linux (RHEL) 7.x ao usar os planos de serviços do
[v2](/docs/services/StreamingAnalytics/service_plans.html) ou com o RHEL 6.5 ao usar os planos de serviços do [v1](/docs/services/StreamingAnalytics/service_plans.html), usando
processadores Intel. Envie seu aplicativo para a instância de serviço novamente. Será possível fazer download do
[{{site.data.keyword.streamsshort}}
Quick Start Edition com o Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) se você não tiver um ambiente de desenvolvimento compatível e estiver usando os planos
de serviços da v2. Ao usar os planos de serviços da v1, faça download do [{{site.data.keyword.streamsshort}} QSE
![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window}.
{: tsResolve}
