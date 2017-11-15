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

# Usando os aplicativos iniciadores do Streaming Analytics
{: #starterapps}

Implemente e modifique os aplicativos iniciadores e aprenda rapidamente como usar o serviço {{site.data.keyword.streaminganalyticsshort}}:
{:shortdesc}

<table summary="Na primeira linha, essa tabela descreve o aplicativo iniciador do Stock Trades. A tabela inclui na segunda linha:
1. Na primeira coluna, um link para um vídeo sobre como implementar o aplicativo iniciador do Stock Trades. 2. Na segunda coluna, um link para fazer download diretamente do aplicativo iniciador do Stock Trades.
 ">
  <tr>
    <th colspan="3">Aplicativo de amostra Stock Trades<br></th>
  </tr>
  <tr>
    <td colspan="3">Esse aplicativo analisa um fluxo de cotações de estoque e produz uma média do balanço dos preços usando o operador <a href="https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$spl/op$spl.relational$Aggregate.html">Aggregate</a>.
É possível executar o aplicativo
iniciador sem modificação. Se você desejar experimentar mais com o serviço, também será possível modificar o código e enviar por push as mudanças de volta para o ambiente do {{site.data.keyword.Bluemix_short}}. A fonte completa para o aplicativo iniciador está <a href="https://github.com/IBMStreams/samples/tree/master/QuickStart/TradesApp">disponível no GitHub</a>.</p>
</td>
  </tr>
  <tr>
    <td><a href="https://developer.ibm.com/streamsdev/videos/getting-started-streaming-analytics-service-using-trades-starter-application/" target="_blank">IMPLEMENTAR O APP</a><br></td>
    <td><a href="https://github.com/IBMStreams/samples/raw/master/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab" target="_blank">FAZER O DOWNLOAD</a></td>
  </tr>
</table>

*Tabela 1. Aplicativo de amostra StockTrades*


<table summary="Esta tabela descreve, na primeira linha, o aplicativo de amostra Event Detection. A tabela inclui na segunda linha:
1. Na primeira coluna, um link para instruções sobre como implementar o aplicativo iniciador Event Detection. 2. Na segunda coluna, um link para tutoriais sobre como usar o aplicativo iniciador Event Detection. 3. Na terceira coluna, um link para fazer download diretamente do aplicativo iniciador Event Detection.
 ">
  <tr>
    <th colspan="3">Aplicativo de amostra Event Detection<br></th>
  </tr>
  <tr>
    <td colspan="3">O app Event Detection é implementado por meio do tempo de execução do <a href="https://console.ng.bluemix.net/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">{{site.data.keyword.sdk4node}}</a>.
O app fornece uma UI da web simples para exibir o status e os resultados da análise.
O app Node.js é ligado a uma instância do serviço do {{site.data.keyword.streaminganalyticsshort}}. O app controla o serviço por meio da API de REST do {{site.data.keyword.streaminganalyticsshort}}.
<p>É possível executar o aplicativo iniciador sem modificação.
Se você desejar experimentar mais com o serviço, também será possível modificar o código e enviar por push as mudanças de volta para o ambiente do {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">IMPLEMENTAR O APP</a><br></td>
    <td><a href="http://www.ibm.com/developerworks/library/ba-bluemix-detect-complex-events-from-data-stream-trs/index.html" target="_blank">TUTORIAL</a></td>
    <td><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection" target="_blank">FAZER O DOWNLOAD</a></td>
  </tr>
</table>

*Tabela 2. Aplicativo de amostra Event Detection*

<table summary="Esta tabela descreve, na primeira linha, o aplicativo de amostra New York Traffic. A tabela inclui na segunda linha:
1. Na primeira coluna, um link para instruções sobre como implementar o aplicativo de amostra New York Traffic. 2. Na segunda coluna, um link para tutoriais sobre como usar o aplicativo de amostra New York Traffic. 3. Na terceira coluna, um link para fazer download diretamente do aplicativo de amostra New York Traffic.">
  <tr>
    <th colspan="3">Aplicativo de amostra NYC Traffic<br></th>
  </tr>
  <tr>
    <td colspan="3">O aplicativo iniciador NYC Traffic é um aplicativo para o {{site.data.keyword.Bluemix_short}} que é gravado no Liberty for Java. Ele contém um aplicativo {{site.data.keyword.streamsshort}} que recupera dados públicos
dos sensores de tráfego da cidade de Nova York, calcula estatísticas agregadas e envia os resultados de volta para o aplicativo Liberty.
<p>É possível executar o aplicativo
iniciador sem modificação. Se você desejar experimentar mais com o serviço, também será possível modificar o código e enviar por push as mudanças de volta para o ambiente do {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">IMPLEMENTAR O APP</a><br></td>
    <td><a href="https://developer.ibm.com/streamsdev/docs/bluemix-streaming-analytics-starter-application/" target="_blank">TUTORIAL</a></td>
    <td><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic" target="_blank">FAZER O DOWNLOAD</a></td>
  </tr>
</table>

*Tabela 3. Aplicativo de amostra NYC Traffic*

## Aplicativos de amostra IBM Streams Runner for Apache Beam

<table summary="Essa tabela descreve na primeira linha o aplicativo TemperatureSample Beam. A tabela inclui na segunda linha um link para um tutorial sobre como implementar o aplicativo TemperatureSample Beam.
 ">
  <tr>
    <th colspan="3">Aplicativo Beam `TemperatureSample`<br></th>
  </tr>
  <tr>
    <td colspan="3">Este aplicativo captura leituras de temperatura de vários dispositivos. O aplicativo divide as leituras em leituras “boas” (válidas) e “ruins” (inválidas), com base em um limite específico. Ele conta as leituras ruins e gera algumas estatísticas básicas para as leituras boas e, finalmente, registra os resultados. É possível fazer download do aplicativo TemperatureSample no console do Streaming Analytics.
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3-sample/#running-the-temperaturesample-application" target="_blank">IMPLEMENTAR O APP</a><br></td>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3-sample/#viewing-the-running-application" target="_blank">VISUALIZAÇÃO DO APLICATIVO</a></td>
  </tr>
</table>

*Tabela 4. Aplicativo TemperatureSample*

<table summary="Esta tabela descreve na primeira linha o aplicativo de amostra WordCount Beam. A tabela inclui na segunda linha um link para um tutorial sobre como implementar o aplicativo de amostra WordCount.
 ">
  <tr>
    <th colspan="3">Aplicativo de amostra WordCount<br></th>
  </tr>
  <tr>
    <td colspan="3">O aplicativo de amostra WordCount da Iniciação Rápida de SDK Java do Apache Feixe 2.0 cria pipelines reutilizáveis e sustentáveis que podem ler em arquivos de texto, aplicar transformações para converter e contar as palavras em token e gravar os dados em um arquivo de texto de saída.
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3b-wordcount/" target="_blank">IMPLEMENTAR O APP</a><br></td>
  </tr>
</table>

*Tabela 5. Aplicativo de amostra `WordCount`*

<table summary="Esta tabela descreve na primeira linha o aplicativo de amostra `FileStreamSample`. A tabela inclui na segunda linha um link para um tutorial sobre como implementar o aplicativo`FileStreamSample`.
 ">
  <tr>
    <th colspan="3">Aplicativo FileStreamSample<br></th>
  </tr>
  <tr>
    <td colspan="3">É possível usar o aplicativo de amostra IBM® Streams Runner for Apache Beam FileStreamSample para aprender a usar o armazenamento de objeto do {{site.data.keyword.Bluemix_notm}} para entrada e saída de arquivo.
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-5b-objstor/" target="_blank">IMPLEMENTAR O APP</a><br></td>
  </tr>
</table>

*Tabela 6. Aplicativo `FileStreamSample`*
