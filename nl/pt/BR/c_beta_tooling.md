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

# Ferramentas de desenvolvimento e ambiente
{: #c_beta_tooling}


Estas considerações se aplicam às ferramentas e ao ambiente usado para desenvolver seus aplicativos para o {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}


* O {{site.data.keyword.streaminganalyticsshort}} não inclui um ambiente de desenvolvimento do {{site.data.keyword.streamsshort}} na nuvem ou o Streams Studio na nuvem. Desenvolva os seus aplicativos em um ambiente do {{site.data.keyword.streamsshort}} instalado localmente e envie-os como pacotes configuráveis do aplicativo. Se você não tiver o ambiente de desenvolvimento, faça o download do [{{site.data.keyword.streamsshort}} Quick Start Edition com o Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) para planos de serviços do [v2 ](/docs/services/StreamingAnalytics/service_plans.html) ou, se estiver usando os planos de serviços do [v1](/docs/services/StreamingAnalytics/service_plans.html), faça o download da imagem da VM do [{{site.data.keyword.streamsshort}} Quick Start Edition ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window}, gratuitamente.
* Compile os aplicativos no Red Hat Enterprise Linux (RHEL) 7.x ao usar os planos de serviços da v2 ou com o RHEL 6.5 ao usar os planos de serviços da v1, usando processadores Intel.
* Em seu ambiente de desenvolvimento do {{site.data.keyword.streamsshort}}, configure a variável de ambiente `JAVA_HOME` como $STREAMS_INSTALL/java.
