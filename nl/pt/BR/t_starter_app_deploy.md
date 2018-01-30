---

copyright:
  years: 2015, 2017
lastupdated: "2017-12-15"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Tutorial Introdução
{: #starterapps_deploy}

O Streaming Analytics é um serviço totalmente gerenciado que libera você de demoradas tarefas de instalação, administração e gerenciamento, dando mais tempo para desenvolver aplicativos de fluxo. Neste tutorial de introdução, você enviará por push e implementará um dos aplicativos iniciadores do {{site.data.keyword.streaminganalyticsshort}} para {{site.data.keyword.Bluemix_notm}}.
{:shortdesc}


## Antes de iniciar
{: #prereqs}

Antes de implementar os apps iniciadores, deve-se seguir estas etapas:

* Registre-se para uma conta do [{{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://console.{DomainName}/registration){:new_window}
* Crie uma instância do serviço {{site.data.keyword.streaminganalyticsshort}} em sua organização do {{site.data.keyword.Bluemix_notm}}. É possível criar a instância diretamente na página do [{{site.data.keyword.streaminganalyticsshort}} no Catálogo de serviços do {{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://console.{DomainName}/catalog/services/streaming-analytics/){:new_window}.  
* [Instale o {{site.data.keyword.Bluemix_notm}} CLI ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://console.stage1.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).



## Etapa 1: Criar o app e conectá-lo ao seu serviço
{: #create_connect}

1. Crie um aplicativo no {{site.data.keyword.Bluemix_notm}}:

    a. No menu {{site.data.keyword.Bluemix_notm}}, selecione **Apps Cloud Foundry** e clique em **Criar recurso**.

    b. Selecione seu tempo de execução do aplicativo:
  	* Para implementar o app iniciador Event Detection, crie um aplicativo com o tempo de execução do {{site.data.keyword.sdk4node}}.
  	* Para implementar o app iniciador NYC Traffic, crie um aplicativo com o tempo de execução do Liberty for Java™.

  Lembre-se do nome que você deu ao aplicativo; você precisará dele posteriormente.
1. Conecte a instância de serviço do {{site.data.keyword.streaminganalyticsshort}} ao seu aplicativo e remonte o aplicativo.

## Etapa 2: Configurar o aplicativo iniciador
{: #setup_app}

1. Faça download do aplicativo iniciador [Event Detection ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection) ou [NYC Traffic ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic).

1. Renomeie o diretório para corresponder ao nome que você forneceu ao seu aplicativo no {{site.data.keyword.Bluemix_notm}}.

## Etapa 3: Implementar o aplicativo iniciador
{: #deploy_app}

1. Acesse o diretório do aplicativo iniciador:
  <pre><code>cd myapp</code></pre>
  {:pre}

1. Efetue login no {{site.data.keyword.Bluemix_notm}} e configure a sua organização de destino quando solicitado:
  <pre><code>  bx login
  </code></pre>
  {:pre}

1. Envie por push seu aplicativo para o {{site.data.keyword.Bluemix_notm}}:
  <pre><code>bx app push myapp</code></pre>
  {:pre}

1. Acesse a página de visão geral do aplicativo, acessível por meio do painel do {{site.data.keyword.Bluemix_notm}}, para verificar se o seu
aplicativo foi iniciado com êxito.
1. Ative seu aplicativo para vê-lo em seu navegador. É possível localizar (ou "rotear") a URL do aplicativo
            na página de visão geral do aplicativo.

## Etapas Seguintes
{: #next_steps}

Agora que seu aplicativo está sendo executado, é possível monitorar o aplicativo no console do {{site.data.keyword.streaminganalyticsshort}}. Acesse o painel de serviço, selecione o serviço {{site.data.keyword.streaminganalyticsshort}} e clique em **Ativar**.
