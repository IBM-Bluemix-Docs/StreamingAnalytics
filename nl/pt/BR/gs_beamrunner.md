---

copyright:
  years: 2015, 2017
lastupdated: "2017-10-27"

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


Inicie usando os [aplicativos de amostra](/docs/services/StreamingAnalytics/c_starterapps.html) para saber como enviar e monitorar um aplicativo Beam no serviço {{site.data.keyword.streaminganalyticsshort}}. É possível fazer download dos aplicativos de amostra no console do {{site.data.keyword.streaminganalyticsshort}}.

Confira a [{{site.data.keyword.streamsshort}} Documentação do Runner for Apache Beam](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/) para ver as tabelas que mostram como o Streams Runner se encaixa na [matriz de capacidade do Beam]. Consulte [Instalando o IBM Streams Runner for Apache Beam](http://bit.ly/2zFDpPr) para obter instruções sobre como instalar o kit de ferramentas `com.ibm.streams.beam` em seu ambiente do Streams para criar aplicativos Beam que podem ser enviados e monitorados no {{site.data.keyword.streaminganalyticsshort}}.

Alguma familiaridade com a programação do Beam é útil, embora não seja necessária; o [website do Apache Beam](https://beam.apache.org/documentation/){:new_window} possui uma página útil de [Iniciação rápida do SDK Java do Apache Beam](https://beam.apache.org/get-started/quickstart-java/){:new_window} e outra documentação.
