---

copyright:
  years: 2015, 2018
lastupdated: "2018-02-14"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Desenvolvendo aplicativos Python no Streaming Analytics
{: #t_develop_apps_python}

Agora é possível desenvolver aplicativos Python no IBM Data Science Experience (DSX) ou em seu ambiente de desenvolvimento Python local e implementar esses aplicativos no {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

Desenvolva e implemente seus aplicativos Python no {{site.data.keyword.Bluemix_short}} usando o serviço {{site.data.keyword.streaminganalyticsshort}} e um destes métodos:


## Desenvolvendo aplicativos Streams Python em DSX
{: #t_develop_python_dsx}

Se você não tem um ambiente de desenvolvimento Python, a maneira mais fácil de começar é usar nossos blocos de notas em DSX e criar aplicativos Python de amostra para o serviço {{site.data.keyword.streaminganalyticsshort}}. Esses blocos de notas fornecem as etapas e as amostras de código para criar e implementar aplicativos Python simples para o serviço {{site.data.keyword.streaminganalyticsshort}} dentro do ambiente Python DSX:

* [Hello World! ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039ca9c6e8): crie um aplicativo Hello World! simples para introdução e, em seguida, implemente o aplicativo em uma instância do serviço {{site.data.keyword.streaminganalyticsshort}}.

* [Demo Healthcare ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039cad29a6): crie um aplicativo que alimente e analise dados de fluxo de um feed e, em seguida, visualize os dados no bloco de notas. Finalmente, envie esse aplicativo para a instância de serviço {{site.data.keyword.streaminganalyticsshort}}.

* [Demo Neural Net ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039ca60bb7): crie um conjunto de dados de amostra, crie um modelo para os dados de amostra, use esse modelo em um aplicativo de fluxo, visualize os dados de fluxo e, por último, envie o aplicativo de fluxo para o serviço {{site.data.keyword.streaminganalyticsshort}}.

## Desenvolvendo aplicativos em seu ambiente Python local
 {: #t_develop_python_api}

 O [Python Application API {{site.data.keyword.streamsshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features), que está incluído no pacote streamsx, permite criar aplicativos de processamento de fluxo usando classes ou funções de chamada do Python. Use a API do aplicativo Python para definir e enviar o aplicativo para o serviço.

Comece seguindo as etapas no tutorial [Desenvolvendo para o serviço {{site.data.keyword.streaminganalyticsshort}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html) para criar um aplicativo de amostra em seu ambiente Python local e implementá-lo no serviço {{site.data.keyword.streaminganalyticsshort}}.

Para se aprofundar no {{site.data.keyword.streamsshort}} Python Application API, conclua [este curso on-line ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/courses/all/streaming-analytics-basics-python-developers/){:new_window} e aprenda as noções básicas do {{site.data.keyword.streaminganalyticsshort}} para desenvolvedores de Python.
