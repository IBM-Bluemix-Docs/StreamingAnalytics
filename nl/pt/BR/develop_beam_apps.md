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

# Implementando aplicativos Beam no Streaming Analytics
{: #develop_beam_apps}

Agora é possível desenvolver aplicativos Beam em seu ambiente de desenvolvimento local do {{site.data.keyword.streamsshort}} e implementar esses aplicativos no {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

O {{site.data.keyword.streamsshort}} Runner for Apache Beam executa pipelines do Beam em um ambiente do {{site.data.keyword.streamsshort}}. Um aplicativo Beam que é ativado com o Streams Runner é convertido em um arquivo Streams Application Bundle (SAB), que pode, então, ser implementado e monitorado no {{site.data.keyword.streaminganalyticsshort}}.

Para enviar um aplicativo Beam para o serviço {{site.data.keyword.streaminganalyticsshort}} no {{site.data.keyword.Bluemix_notm}}, deve-se criar um arquivo VCAP formatado por JSON que contenha credenciais e outras informações para o serviço.

1. Em seu ambiente local do Streams, navegue para a subpasta de amostras na qual você instalou o kit de ferramentas ($STREAMS_BEAM_RUNNER/samples) e copie o arquivo template.vcap em um novo arquivo. Dê ao arquivo um nome significativo e uma extensão de arquivo de .vcap.
1. [Copie as credenciais do serviço {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/r_vcap_services.html) e cole a credenciais no arquivo VCAP que você criou, substituindo a linha a seguir:
```
 <REMOVE THIS LINE AND INSERT CREDENTIALS HERE>
 ```
1. Verifique se o aplicativo Beam é executado adequadamente em seu ambiente de desenvolvimento. Ao ativar seu aplicativo Beam com o Streams Runner, o aplicativo é convertido em um arquivo Streams Application Bundle (SAB).
1. Envie o arquivo SAB que está associado ao aplicativo Beam para {{site.data.keyword.streaminganalyticsshort}}

Agora seu aplicativo está implementado na nuvem. É possível monitorar seu aplicativo usando o serviço {{site.data.keyword.streaminganalyticsshort}}.

Para obter mais detalhes sobre como implementar e monitorar seus aplicativos Beam no {{site.data.keyword.streaminganalyticsshort}}, veja [Streams Runner for Apache Beam ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/).
