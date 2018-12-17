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

# Aplicativos de Amostra
{: #starterapps}

Implemente e modifique os aplicativos Starter e aprenda rapidamente a usar o serviço do {{site.data.keyword.streaminganalyticsshort}}. Observe que os planos de serviço da v2 requerem que o Streams execute no RHEL 7. O {{site.data.keyword.streaminganalyticsshort}} fornece um [conjunto de aplicativos Starter e de amostra](https://developer.ibm.com/streamsdev/docs/starter-sample-apps-v2-plans/) para introduzi-lo rapidamente aos planos de serviços da v2. Os aplicativos de amostra EventDetection e NYCTraffic não funcionam com os planos de serviços da v2.
{:shortdesc}


<table summary="Na primeira linha, essa tabela descreve o aplicativo iniciador do Stock Trades. A tabela inclui na segunda linha:
1. Na primeira coluna, um link para um vídeo sobre como implementar o aplicativo iniciador do Stock Trades. 2. Na segunda coluna, um link para fazer download diretamente do aplicativo iniciador do Stock Trades.
 ">
  <tr>
    <th id="stocktrades" colspan="3">Aplicativo de amostra Stock Trades<br></th>
  </tr>
  <tr>
    <td headers="stocktrades" colspan="3">Este aplicativo analisa um fluxo de cotações de estoque e produz uma média contínua dos preços usando o operador de <a href="https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$spl/op$spl.relational$Aggregate.html">Agregação ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a>.
É possível executar o aplicativo iniciador sem modificação. Se você desejar experimentar mais com o serviço, também será possível modificar o código e enviar por push as mudanças de volta para o ambiente do {{site.data.keyword.Bluemix_short}}. A origem integral para o aplicativo iniciador está <a href="https://github.com/IBMStreams/samples/tree/master/QuickStart/TradesApp">disponível no GitHub ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a>.</p>
</td>
  </tr>
  <tr>
    <td headers="stocktrades"><a href="https://developer.ibm.com/streamsdev/videos/getting-started-streaming-analytics-service-using-trades-starter-application/" target="_blank">IMPLEMENTAR O APP ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a><br></td>
    <td headers="stocktrades"><a href="https://github.com/IBMStreams/samples/raw/master/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab" target="_blank">DOWNLOAD ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a></td>
  </tr>
</table>

*Tabela 1. Aplicativo de amostra StockTrades*


<table summary="Essa tabela descreve, na primeira linha, o aplicativo de amostra Event Detection v2. A tabela inclui na segunda linha:
1. Na primeira coluna, um link para instruções sobre como implementar o aplicativo iniciador Event Detection v2. 2. Na segunda coluna, um link para tutoriais sobre como usar o aplicativo iniciador Event Detection. 3. Na terceira coluna, um link para fazer download diretamente do aplicativo iniciador Event Detection.
">
  <tr>
    <th id="EventDetection2" colspan="3">Aplicativo de amostra Event Detection v2<br></th>
  </tr>
  <tr>
    <td colspan="3" headers="EventDetection2">O app Event Detection v2 é implementado por meio do tempo de execução do <a href="https://{DomainName}/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">SDK for Node.js ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a>. Esse aplicativo Starter é compatível apenas com os [planos de serviços da v2](/docs/services/StreamingAnalytics/service_plans.html).
O app fornece uma UI da web simples para exibir o status e os resultados da análise.
O app Node.js é ligado a uma instância do serviço do {{site.data.keyword.streaminganalyticsshort}}. O aplicativo controla o serviço por meio da API de REST do {{site.data.keyword.streaminganalyticsshort}} v2.
<p>É possível executar o aplicativo iniciador sem modificação.
Se você desejar experimentar mais com o serviço, também será possível modificar o código e enviar por push as mudanças de volta para o ambiente do {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td headers="EventDetection2"><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">IMPLEMENTAR O APP</a><br></td>
    <td headers="EventDetection2"><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">TUTORIAL ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a></td>
    <td headers="EventDetection2"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetectionV2" target="_blank">DOWNLOAD ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a></td>
  </tr>
</table>

*Tabela 2. Aplicativo de amostra Event Detection v2*
<table summary="Esta tabela descreve, na primeira linha, o aplicativo de amostra Event Detection. A tabela inclui na segunda linha:
1. Na primeira coluna, um link para instruções sobre como implementar o aplicativo iniciador Event Detection. 2. Na segunda coluna, um link para tutoriais sobre como usar o aplicativo iniciador Event Detection. 3. Na terceira coluna, um link para fazer download diretamente do aplicativo iniciador Event Detection.
 ">
  <tr>
    <th id="EventDetection1" colspan="3">Aplicativo de amostra Event Detection<br></th>
  </tr>
  <tr>
    <td headers="EventDetection1" colspan="3">O app Event Detection é implementado por meio do tempo de execução do <a href="https://{DomainName}/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">SDK for Node.js ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a>. Esse aplicativo Starter é compatível apenas com os [planos de serviços da v1](/docs/services/StreamingAnalytics/service_plans.html). O app fornece uma UI da web simples para exibir o status e os resultados da análise.
O app Node.js é ligado a uma instância do serviço do {{site.data.keyword.streaminganalyticsshort}}. O app controla o serviço por meio da API de REST do {{site.data.keyword.streaminganalyticsshort}}.
<p>É possível executar o aplicativo iniciador sem modificação.
Se você desejar experimentar mais com o serviço, também será possível modificar o código e enviar por push as mudanças de volta para o ambiente do {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td headers="EventDetection1"><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">IMPLEMENTAR O APP</a><br></td>
    <td headers="EventDetection1"><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">TUTORIAL ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a></td>
    <td headers="EventDetection1"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection" target="_blank">DOWNLOAD ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a></td>
  </tr>
</table>

*Tabela 2. Aplicativo de amostra Event Detection*

<table summary="Esta tabela descreve, na primeira linha, o aplicativo de amostra New York Traffic. A tabela inclui na segunda linha:
1. Na primeira coluna, um link para instruções sobre como implementar o aplicativo de amostra New York Traffic. 2. Na segunda coluna, um link para tutoriais sobre como usar o aplicativo de amostra New York Traffic. 3. Na terceira coluna, um link para fazer download diretamente do aplicativo de amostra New York Traffic.">
  <tr>
    <th id="NYCTraffic" colspan="3">Aplicativo de amostra NYC Traffic<br></th>
  </tr>
  <tr>
    <td headers="NYCTraffic" colspan="3">O aplicativo iniciador NYC Traffic é um aplicativo para o {{site.data.keyword.Bluemix_short}} que é gravado no Liberty for Java. Ele contém um aplicativo {{site.data.keyword.streamsshort}} que recupera dados públicos dos sensores de tráfego da cidade de Nova York, calcula estatísticas agregadas e envia os resultados de volta para o aplicativo Liberty. Esse aplicativo Starter é compatível apenas com os [planos de serviços da v1](/docs/services/StreamingAnalytics/service_plans.html).
<p>É possível executar o aplicativo iniciador sem modificação. Se você desejar experimentar mais com o serviço, também será possível modificar o código e enviar por push as mudanças de volta para o ambiente do {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td headers="NYCTraffic" deploylink><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">IMPLEMENTAR O APP</a><br></td>
    <td headers="NYCTraffic"><a href="https://developer.ibm.com/streamsdev/docs/bluemix-streaming-analytics-starter-application/" target="_blank">TUTORIAL ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a></td>
    <td headers="NYCTraffic"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic" target="_blank">DOWNLOAD ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a></td>
  </tr>
</table>

*Tabela 3. Aplicativo de amostra NYC Traffic*

## Aplicativos de amostra IBM Streams Runner for Apache Beam

<table summary="Essa tabela descreve na primeira linha o aplicativo TemperatureSample Beam. A tabela inclui na segunda linha um link para um tutorial sobre como implementar o aplicativo TemperatureSample Beam.
 ">
  <tr>
    <th id="TemperatureSample" colspan="3">App TemperatureSample Beam<br></th>
  </tr>
  <tr>
    <td headers="TemperatureSample" colspan="3">Este aplicativo captura leituras de temperatura de vários dispositivos. Esse aplicativo Starter está disponível apenas para os [planos de serviços da v2](/docs/services/StreamingAnalytics/service_plans.html). O aplicativo divide as leituras em leituras “boas” (válidas) e “ruins” (inválidas), com base em um limite específico. Ele conta as leituras ruins e gera algumas estatísticas básicas para as leituras boas e, finalmente, registra os resultados. É possível fazer download do aplicativo TemperatureSample no console do Streaming Analytics.
</td>
  </tr>
  <tr>
    <td headers="TemperatureSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/sample/#running-the-temperaturesample-application" target="_blank">IMPLEMENTAR O APP ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a><br></td>
    <td headers="TemperatureSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/sample/#viewing-the-running-application" target="_blank">VISUALIZAR O APP ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a></td>
  </tr>
</table>

*Tabela 4. Aplicativo TemperatureSample*

<table summary="Esta tabela descreve na primeira linha o aplicativo de amostra WordCount Beam. A tabela inclui na segunda linha um link para um tutorial sobre como implementar o aplicativo de amostra WordCount.
 ">
  <tr>
    <th id="WordCountSample" colspan="3">Aplicativo de amostra WordCount<br></th>
  </tr>
  <tr>
    <td headers="WordCountSample" colspan="3">O aplicativo de amostra WordCount da Iniciação rápida do Apache Beam 2.0 Java SDK cria pipelines reutilizáveis e sustentáveis que podem ler em um arquivo de texto, aplicar transformações para converter em token e contar as palavras e gravar os dados em um arquivo de texto de saída.
</td>
  </tr>
  <tr>
    <td headers="WordCountSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/wordcount/" target="_blank">IMPLEMENTAR O APP ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a><br></td>
  </tr>
</table>

*Tabela 5. Aplicativo de amostra WordCount*

<table summary="Esta tabela descreve, na primeira linha, o aplicativo de amostra FileStreamSample. A tabela inclui na segunda linha um link para um tutorial sobre como implementar o aplicativo FileStreamSample.
 ">
  <tr>
    <th id="FilterStreamSample" colspan="3">Aplicativo FileStreamSample<br></th>
  </tr>
  <tr>
    <td headers="FilterStreamSample" colspan="3">É possível usar o aplicativo de amostra IBM® Streams Runner for Apache Beam FileStreamSample para aprender a usar o armazenamento de objeto do {{site.data.keyword.Bluemix_notm}} para entrada e saída de arquivo.
</td>
  </tr>
  <tr>
    <td headers="FilterStreamSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/objstor/" target="_blank">IMPLEMENTAR O APP ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")</a><br></td>
  </tr>
</table>

*Tabela 6. App FileStreamSample*
