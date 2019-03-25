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

# Implementando aplicativos Streams na nuvem
{: #t_deploytocloud}

É possível implementar seus aplicativos {{site.data.keyword.streamsshort}} para uma instância do {{site.data.keyword.streaminganalyticsshort}} que está em execução no {{site.data.keyword.Bluemix_short}}.
{:shortdesc}

Os aplicativos {{site.data.keyword.streamsshort}} são gravados em {{site.data.keyword.streamsshort}} Processing Language (SPL), SPL, Java, Scala ou Python em um ambiente {{site.data.keyword.streamsshort}}. Agora é possível desenvolver aplicativos Streams Python sem um ambiente {{site.data.keyword.streamsshort}}. Consulte [Implementando aplicativos {{site.data.keyword.streamsshort}} Python para a nuvem](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_deploytocloud#t_deploypython)


O {{site.data.keyword.streaminganalyticsshort}} não inclui um ambiente de desenvolvimento do {{site.data.keyword.streamsshort}} na nuvem, mas é possível implementar localmente na nuvem os aplicativos que você desenvolve.

Antes de iniciar, desative o bloqueador de pop-up de seu navegador para exibir o console do {{site.data.keyword.streaminganalyticsshort}}.

Para implementar os seus aplicativos {{site.data.keyword.streamsshort}} na nuvem:

1. Configure seu ambiente de desenvolvimento para desenvolver e testar seu aplicativo.

	Se desejar usar um ambiente do {{site.data.keyword.streamsshort}}, será possível fazer download do [{{site.data.keyword.streamsshort}} Quick Start Edition ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window} para [planos de serviço v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans). Use o [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi){:new_window} para [planos de serviço v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans).

2. Desenvolva seu aplicativo de fluxo em seu ambiente de desenvolvimento. No ambiente de desenvolvimento do {{site.data.keyword.streamsshort}}, é possível usar o Streams Studio ou as ferramentas de linha de comandos para desenvolver seu aplicativo.

3. Verifique se o seu aplicativo de fluxo está sendo executado adequadamente em seu ambiente de desenvolvimento.
**Nota:** deve-se compilar os aplicativos no Red Hat Enterprise Linux (RHEL) 7.x ao usar os planos de serviços da v2 ou com o RHEL 6.5 ao usar os planos de serviços da v1.

4. Envie o pacote configurável do aplicativo (arquivo .sab) que está associado ao aplicativo SPL, Java, Scala ou Python para a instância de serviço na nuvem usando um destes métodos:
	* Use o console do {{site.data.keyword.streaminganalyticsshort}} para enviar o pacote configurável do aplicativo.

  * Crie um aplicativo no {{site.data.keyword.Bluemix_notm}} e inclua o aplicativo {{site.data.keyword.streamsshort}} nele. Controle-o usando a API de REST do [{{site.data.keyword.streaminganalyticsshort}} v1 ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} para os planos de serviços do [v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) ou a API de REST do [{{site.data.keyword.streaminganalyticsshort}} v2 ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window} para os planos de serviços da v2.

Agora seu aplicativo está implementado na nuvem. É possível monitorar seu aplicativo no serviço do {{site.data.keyword.streaminganalyticsshort}}. Também é possível enviar mais de um aplicativo (arquivos .sab) para sua instância de serviço. Quantas
você quiser.

O {{site.data.keyword.streamsshort}} também suporta vários Java™ Development Kits que podem ser usados
para desenvolver os seus aplicativos. Para obter mais informações sobre o suporte Java no {{site.data.keyword.streamsshort}}, veja [Java Development Kits suportados para desenvolvimento de aplicativo ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.install.doc/doc/ibminfospherestreams-install-prerequisites-java-supported-sdks.html){:new_window}.

## Implementando aplicativos Streams Python na nuvem
{: #t_deploypython}

Implemente seus aplicativos {{site.data.keyword.streamsshort}} Python em um serviço {{site.data.keyword.streaminganalyticsshort}} que esteja em execução no {{site.data.keyword.Bluemix_short}}. Não é necessário ter uma instalação do {{site.data.keyword.streamsshort}}.
{:shortdesc}

Com a [API do aplicativo {{site.data.keyword.streamsshort}} Python ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features){:new_window}, que está incluída no pacote streamsx, é possível implementar aplicativos Python no serviço do {{site.data.keyword.streaminganalyticsshort}}. Consulte o tutorial [Desenvolvendo para o serviço {{site.data.keyword.streaminganalyticsshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html){:new_window} para obter um exemplo de como criar e implementar um aplicativo Python simples para o serviço {{site.data.keyword.streaminganalyticsshort}}.

O {{site.data.keyword.DSX_full}} também suporta o envio de aplicativos Python nos blocos de notas interativos do Jupyter. Para obter mais informações, consulte [Desenvolvendo aplicativos Python para o {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_develop_apps_python).
