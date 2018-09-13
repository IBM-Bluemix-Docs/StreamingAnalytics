---

copyright:
  years: 2015, 2018
lastupdated: "2018-07-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Desenvolvendo aplicativos Python no Streaming Analytics
{: #t_develop_apps_python}

Agora é possível desenvolver aplicativos Python no {{site.data.keyword.DSX_full}} ou em seu ambiente de
desenvolvimento Python local e implementar esses aplicativos no {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

Desenvolver e implementar seus aplicativos Python no {{site.data.keyword.Bluemix_short}} com o serviço do {{site.data.keyword.streaminganalyticsshort}} com um destes métodos:


## Desenvolvendo aplicativos Streams Python no Watson Studio
{: #t_develop_python_dsx}

Se você não tiver um ambiente de desenvolvimento Python, a forma mais fácil de começar será usar os blocos de notas do {{site.data.keyword.streamsshort}} no {{site.data.keyword.DSX_short}} e criar aplicativos Python de amostra. Esses blocos de notas fornecem as etapas e as amostras de código para criar e implementar aplicativos Python simples para o serviço
do {{site.data.keyword.streaminganalyticsshort}} dentro do ambiente Python do {{site.data.keyword.DSX_short}}:

* [Hello World! ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039ca9c6e8): crie um aplicativo Hello World! simples para introdução e, em seguida, implemente o aplicativo em uma instância do serviço {{site.data.keyword.streaminganalyticsshort}}.

* [Demo Healthcare ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039cad29a6): crie um aplicativo que alimente e analise dados de fluxo de um feed e, em seguida, visualize os dados no bloco de notas. Finalmente, envie esse aplicativo para a instância de serviço do {{site.data.keyword.streaminganalyticsshort}}.

* [Neural Net Demo ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039ca60bb7): crie um conjunto de dados de amostra, crie um modelo de dados, use esse modelo em um aplicativo de amostra, visualize os dados de fluxo e envie o aplicativo de fluxo para o serviço.

## Desenvolvendo aplicativos em seu ambiente Python local
 {: #t_develop_python_api}

Com a [API do aplicativo {{site.data.keyword.streamsshort}} Python![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features), que está incluída no pacote streamsx, é possível criar aplicativos de processamento de fluxo com classes ou funções que podem ser chamadas pelo Python. Use a API do aplicativo Python para definir e enviar o aplicativo para o serviço.

Comece seguindo as etapas no tutorial [Desenvolvendo para o serviço {{site.data.keyword.streaminganalyticsshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html). Nesse tutorial, você cria um aplicativo de amostra em seu ambiente Python local e implementa-o no serviço do {{site.data.keyword.streaminganalyticsshort}}.

Para se aprofundar no {{site.data.keyword.streamsshort}} Python Application API, conclua [este curso on-line ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/courses/all/streaming-analytics-basics-python-developers/){:new_window} e aprenda as noções básicas do {{site.data.keyword.streaminganalyticsshort}} para desenvolvedores de Python.
