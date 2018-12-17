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


# Visão geral do Streaming Analytics
{: #gettingstarted}

O {{site.data.keyword.streaminganalyticsfull}} foi desenvolvido com o {{site.data.keyword.streamsshort}}, uma plataforma analítica avançada que
pode ser usada para alimentar, analisar e correlacionar informações assim que chegam de diferentes tipos de origens de dados em tempo real. Ao criar uma instância do serviço {{site.data.keyword.streaminganalyticsshort}} você obtém sua própria instância do {{site.data.keyword.streamsshort}} em execução no {{site.data.keyword.Bluemix_short}}, pronta para executar seus aplicativos {{site.data.keyword.streamsshort}}.
{:shortdesc}

Inicie o {{site.data.keyword.streaminganalyticsshort}} imediatamente executando os [aplicativos iniciadores](/docs/services/StreamingAnalytics/t_starter_app_deploy.html){:new_window}.

Para iniciar o {{site.data.keyword.streaminganalyticsshort}}, use um dos métodos a seguir para enviar o pacote configurável do aplicativo (arquivo .sab) que está associado ao seu aplicativo SPL, Java™, Python ou Scala Streams:
* Use o botão **Enviar tarefa** no console do {{site.data.keyword.streaminganalyticsshort}}.
* Desenvolva um aplicativo no {{site.data.keyword.Bluemix_notm}} e inclua o aplicativo {{site.data.keyword.streamsshort}} nele. Controle-o usando a API de REST do [{{site.data.keyword.streaminganalyticsshort}} v1 ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} para os planos de serviços do [v1](/docs/services/StreamingAnalytics/service_plans.html) ou a API de REST do [{{site.data.keyword.streaminganalyticsshort}} v2 ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window} para os planos de serviços da v2.

Use {{site.data.keyword.streaminganalyticsshort}} com outros serviços, incluindo {{site.data.keyword.cloudant}}. Veja os [Tutoriais para se integrar com outros serviços do {{site.data.keyword.Bluemix_short}}](/docs/services/StreamingAnalytics/r_integrating_cloudant_rest.html){:new_window} para obter exemplos de funcionamento.

Se você deseja ir além com seus próprios aplicativos, é possível obter um ambiente de desenvolvimento do {{site.data.keyword.streamsshort}} e deve-se deixar seu aplicativo pronto para a nuvem. Se você não tiver um ambiente do {{site.data.keyword.streamsshort}}, será possível fazer download do [{{site.data.keyword.streamsshort}} Quick Start Edition com o Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) para os planos de serviços do [v2](/docs/services/StreamingAnalytics/service_plans.html) ou se estiver usando os planos de serviço do [v1](/docs/services/StreamingAnalytics/service_plans.html), será possível fazer download da imagem da VM do [{{site.data.keyword.streamsshort}} Quick Start Edition ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}.

Se você não estiver familiarizado com o desenvolvimento de
aplicativo do
{{site.data.keyword.streamsshort}},
haverá recursos para ajudá-lo a aprender. Para obter mais informações, consulte o [{{site.data.keyword.streamsshort}} Knowledge Center ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.welcome.doc/doc/kc-homepage.html){:new_window}

Se você já tem um aplicativo SPL que é executado no local, deve-se [deixar seu aplicativo pronto para a nuvem.![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/streamsdev/docs/getting-spl-application-ready-cloud/){:new_window}

**Nota:** deve-se compilar os aplicativos no Red Hat Enterprise Linux (RHEL) 7.x ao usar os planos de serviços da v2 ou com o RHEL 6.5 ao usar os planos de serviços da v1.
