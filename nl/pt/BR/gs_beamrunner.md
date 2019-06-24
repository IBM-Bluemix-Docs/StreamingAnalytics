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

# IBM Streams Runner for Apache Beam in Streaming Analytics
{: #gs_beamrunner}

Se você tiver um ambiente de desenvolvimento do {{site.data.keyword.streamsshort}}, agora será possível desenvolver aplicativos Beam localmente em seu ambiente e, em seguida, enviar esses aplicativos para o serviço {{site.data.keyword.streaminganalyticsshort}} no {{site.data.keyword.Bluemix_notm}}. O {{site.data.keyword.streamsshort}} Runner for Apache Beam executa pipelines do Beam em um ambiente do {{site.data.keyword.streamsshort}}. Um aplicativo Beam que é ativado com o Streams Runner é convertido em um arquivo Streams Application Bundle (SAB), que pode, então, ser implementado e monitorado no {{site.data.keyword.streaminganalyticsshort}}.


Inicie usando os [aplicativos de amostra](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps) para saber como enviar e monitorar um aplicativo Beam no serviço {{site.data.keyword.streaminganalyticsshort}}. É possível fazer download dos aplicativos de amostra no console do {{site.data.keyword.streaminganalyticsshort}}.

Consulte a [Documentação do {{site.data.keyword.streamsshort}} Runner for Apache Beam ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/){:new_window} para ver as tabelas que mostram como o Streams Runner se ajusta à [Matriz de compatibilidade do Beam](https://beam.apache.org/documentation/runners/capability-matrix/). Veja [Instalando o IBM Streams Runner for Apache Beam ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://bit.ly/2zFDpPr){:new_window} para obter instruções sobre como instalar o kit de ferramentas `com.ibm.streams.beam` em seu ambiente do Streams para criar aplicativos Beam que podem ser enviados e monitorados no {{site.data.keyword.streaminganalyticsshort}}.

Alguma familiaridade com a programação Beam é útil, mas não necessária; o [website Apache Beam ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://beam.apache.org/documentation/){:new_window} tem uma página útil [Iniciação rápida do Apache Beam Java SDK ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://beam.apache.org/get-started/quickstart-java/){:new_window} e outras documentações.
