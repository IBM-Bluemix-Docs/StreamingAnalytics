---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-16"

subcollection: StreamingAnalytics

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

Você ativa um serviço do {{site.data.keyword.streaminganalyticsshort}} que criou e em vez de acessar diretamente o console de serviço, você vê uma página de login em que são solicitadas as credenciais.
{: tsSymptoms}

Houve uma atualização na infraestrutura de serviço e seu cache do navegador está impedindo o serviço de selecionar a atualização.
{: tsCauses}

Limpe o cache do seu navegador para certificar-se de obter a versão mais recente do console de serviço.
{: tsResolve}

## Meu aplicativo está unhealthy
{: #app_unhealthy}

Não é possível executar seu aplicativo corretamente e o status de funcionamento é `unhealthy`.
{:shortdesc}

Você envia um aplicativo para a instância de serviço, o aplicativo é iniciado, mas falha imediatamente e o status de funcionamento é `unhealthy`. O erro a seguir aparece no arquivo de log: `/lib64/libc.so.6: version GLIBC_2.14 not found`.
{: tsSymptoms}

Você não compilou o aplicativo com um sistema operacional RHEL 7.x ou uma versão equivalente do CentOS.
{: tsCauses}

Deve-se compilar seu aplicativo no Red Hat Enterprise Linux (RHEL) 7.x se você estiver usando os [planos de serviço v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans). Se você estiver usando os [planos de serviço v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans), deve-se compilar o aplicativo com o RHEL 6.5 com processadores Intel. Envie seu aplicativo para a instância de serviço novamente. É possível fazer download do [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) se não tiver um ambiente de desenvolvimento compatível e estiver usando os planos de serviço v2. Ao usar os planos de serviços da v1, faça download do [{{site.data.keyword.streamsshort}} QSE
![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}.
{: tsResolve}

## Meu aplicativo não está funcionando bem após ser reiniciado
{: #app_restart}

Seu aplicativo não está funcionando bem após ser reiniciado devido à manutenção do sistema ou ao cenário de recuperação de falha.
{:shortdesc}

Você possui múltiplos aplicativos em sua instância de serviço e um dos aplicativos utiliza uma tag para posicionamento do operador. Após o aplicativo ser reiniciado, os recursos para operadores não identificados são adquiridos primeiro e consomem toda a sua cota de recursos antes de os operadores identificados poderem ser posicionados.
{: tsSymptoms}

Uma reinicialização de pod de grande escala, que é mais frequentemente acionada por atualizações de serviço, pode fazer com que os aplicativos não consigam reiniciar se requererem identificação especial e a cota de recurso já tiver sido atendida. Em alguns casos, reinicializações de pod de grande escala podem ser causados por cenários de recuperação de falha.
{: tsCauses}

É necessário aumentar sua cota de recursos ou liberar alguns recursos para que os aplicativos possam adquirir recursos com as tags necessárias. Para aumentar a sua cota, acesse a página de detalhes do serviço e aumente o tamanho da sua instância. Para liberar recursos, cancele as tarefas existentes até que recursos suficientes sejam liberados para posicionar adequadamente os aplicativos.
{: tsResolve}
