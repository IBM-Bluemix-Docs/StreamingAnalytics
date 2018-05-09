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

# サンプル・アプリケーション
{: #starterapps}

スターター・アプリケーションをデプロイして変更すると、{{site.data.keyword.streaminganalyticsshort}} サービスの使用法がすぐに分かります。
v2 サービス・プランでは、RHEL 7 で Streams を実行する必要があることに注意してください。{{site.data.keyword.streaminganalyticsshort}} には、v2 サービス・プランを素早く開始するために、[スターター・アプリケーションとサンプルアプリケーションのセット](https://developer.ibm.com/streamsdev/docs/starter-sample-apps-v2-plans/)が用意されています。EventDetection および NYCTraffic のサンプル・アプリケーションは、v2 サービス・プランでは機能しません。
{:shortdesc}


<table summary="この表では、最初の行で Stock Trades スターター・アプリケーションについて説明しています。この表の 2 行目には、以下が含まれています。
1. 最初の列には、Stock Trades スターター・アプリケーションのデプロイ方法のビデオへのリンクが含まれています。 2. 2 列目には、Stock Trades スターター・アプリケーションを直接ダウンロードするためのリンクが含まれています。
 ">
  <tr>
    <th colspan="3">Stock Trades サンプル・アプリケーション<br></th>
  </tr>
  <tr>
    <td colspan="3">このアプリケーションは、株価の流れを分析し、<a href="https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.1/com.ibm.streams.toolkits.doc/spldoc/dita/tk$spl/op$spl.relational$Aggregate.html">集約 ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a> 演算子を使用して価格の移動平均を生成します。
スターター・アプリケーションは、変更せずに実行できます。 さらにサービスを試してみたい場合は、コードを変更し、変更内容をプッシュして {{site.data.keyword.Bluemix_short}} 環境に戻すこともできます。 スターター・アプリケーションの全ソースは、<a href="https://github.com/IBMStreams/samples/tree/master/QuickStart/TradesApp">GitHub から入手可能 ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a> です。</p>
</td>
  </tr>
  <tr>
    <td><a href="https://developer.ibm.com/streamsdev/videos/getting-started-streaming-analytics-service-using-trades-starter-application/" target="_blank">DEPLOY THE APP ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a><br></td>
    <td><a href="https://github.com/IBMStreams/samples/raw/master/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab" target="_blank">DOWNLOAD ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a></td>
  </tr>
</table>

*表 1. Stock Trades サンプル・アプリケーション*


<table summary="この表では、最初の行で Event Detection v2 サンプル・アプリケーションについて説明しています。この表の 2 行目には、以下が含まれています。
1. 最初の列には、Event Detection v2 スターター・アプリケーションをデプロイする方法に関する説明へのリンクが含まれています。 2. 2 列目には、Event Detection スターター・アプリケーションを使用する方法に関するチュートリアルへのリンクが含まれています。3. 3 列目には、Event Detection スターター・アプリケーションを直接ダウンロードするためのリンクが含まれています。
 ">
  <tr>
    <th colspan="3">Event Detection v2 サンプル・アプリケーション<br></th>
  </tr>
  <tr>
    <td colspan="3">Event Detection v2 アプリケーションは、<a href="https://console.ng.bluemix.net/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">{{site.data.keyword.sdk4node}} ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a> ランタイムを介して実装されます。このスターター・アプリケーションは、[v2 サービス・プラン](/docs/services/StreamingAnalytics/service_plans.html)とのみ互換性があります。
このアプリケーションは、分析の状況と結果を表示する単純な Web UI を提供します。
Node.js アプリケーションは、{{site.data.keyword.streaminganalyticsshort}} サービスのインスタンスにバインドされま
す。 このアプリケーションは、{{site.data.keyword.streaminganalyticsshort}} v2 REST API を介してサービスを制御します。
<p>スターター・アプリケーションは、変更せずに実行できます。
さらにサービスを試してみたい場合は、コードを変更し、変更内容をプッシュして {{site.data.keyword.Bluemix_short}} 環境に戻すこともできます。</p>
</td>
  </tr>
  <tr>
    <td><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">アプリケーションのデプロイ</a><br></td>
    <td><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">TUTORIAL ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a></td>
    <td><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetectionV2" target="_blank">DOWNLOAD ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a></td>
  </tr>
</table>

*表 2. Event Detection v2 サンプル・アプリケーション*
<table summary="この表では、最初の行で Event Detection サンプル・アプリケーションについて説明しています。この表の 2 行目には、以下が含まれています。
1. 最初の列には、Event Detection スターター・アプリケーションをデプロイする方法に関する説明へのリンクが含まれています。2. 2 列目には、Event Detection スターター・アプリケーションを使用する方法に関するチュートリアルへのリンクが含まれています。3. 3 列目には、Event Detection スターター・アプリケーションを直接ダウンロードするためのリンクが含まれています。
 ">
  <tr>
    <th colspan="3">Event Detection サンプル・アプリケーション<br></th>
  </tr>
  <tr>
    <td colspan="3">Event Detection アプリケーションは、<a href="https://console.ng.bluemix.net/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">{{site.data.keyword.sdk4node}} ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a> ランタイムによって実装されます。
このスターター・アプリケーションは、[v1 サービス・プラン](/docs/services/StreamingAnalytics/service_plans.html)とのみ互換性があります。このアプリケーションは、分析の状況と結果を表示する単純な Web UI を提供します。
Node.js アプリケーションは、{{site.data.keyword.streaminganalyticsshort}} サービスのインスタンスにバインドされま
す。 このアプリケーションは、{{site.data.keyword.streaminganalyticsshort}} REST API を介してサービスを制御します。
<p>スターター・アプリケーションは、変更せずに実行できます。
さらにサービスを試してみたい場合は、コードを変更し、変更内容をプッシュして {{site.data.keyword.Bluemix_short}} 環境に戻すこともできます。</p>
</td>
  </tr>
  <tr>
    <td><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">アプリケーションのデプロイ</a><br></td>
    <td><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">TUTORIAL ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a></td>
    <td><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection" target="_blank">DOWNLOAD ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a></td>
  </tr>
</table>

*表 2. Event Detection サンプル・アプリケーション*

<table summary="この表では、最初の行で New York traffic サンプル・アプリケーションについて説明しています。この表の 2 行目には、以下が含まれています。
1. 最初の列には、New York traffic サンプル・アプリケーションをデプロイする方法に関する説明へのリンクが含まれています。2. 2 列目には、New York traffic サンプル・アプリケーションを使用する方法に関するチュートリアルへのリンクが含まれています。3. 3 列目には、New York traffic サンプル・アプリケーションを直接ダウンロードするためのリンクが含まれています。">
  <tr>
    <th colspan="3">NYC Traffic サンプル・アプリケーション<br></th>
  </tr>
  <tr>
    <td colspan="3">NYC Traffic スターター・アプリケーションは、Liberty for Java で書かれた、{{site.data.keyword.Bluemix_short}} 用のアプリケーションです。 これには、ニューヨーク市の交通量センサーからパブリック・データを取得し、総統計を計算して、結果を Liberty アプリケーションに送り返す、{{site.data.keyword.streamsshort}} アプリケーションが含まれています。このスターター・アプリケーションは、[v1 サービス・プラン](/docs/services/StreamingAnalytics/service_plans.html)とのみ互換性があります。
<p>スターター・アプリケーションは、変更せずに実行できます。 さらにサービスを試してみたい場合は、コードを変更し、変更内容をプッシュして {{site.data.keyword.Bluemix_short}} 環境に戻すこともできます。</p>
</td>
  </tr>
  <tr>
    <td><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">アプリケーションのデプロイ</a><br></td>
    <td><a href="https://developer.ibm.com/streamsdev/docs/bluemix-streaming-analytics-starter-application/" target="_blank">TUTORIAL ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a></td>
    <td><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic" target="_blank">DOWNLOAD ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a></td>
  </tr>
</table>

*表 3. NYC Traffic サンプル・アプリケーション*

## IBM Streams Runner for Apache Beam サンプル・アプリケーション

<table summary="この表では、最初の行で TemperatureSample Beam アプリケーションについて説明しています。この表の 2 行目には、TemperatureSample Beam アプリケーションのデプロイ方法に関するチュートリアルへのリンクが含まれています。
 ">
  <tr>
    <th colspan="3">TemperatureSample Beam アプリケーション<br></th>
  </tr>
  <tr>
    <td colspan="3">このアプリケーションは、複数のデバイスから温度計測値を取得します。 このスターター・アプリケーションは、[v2 サービス・プラン](/docs/services/StreamingAnalytics/service_plans.html)でのみ使用できます。アプリケーションは、特定のしきい値に基づいて計測値を「良好」(有効) と「不良」(無効) の計測値に分けます。 これは、不良な計測値をカウントし、良好な計測値の基本的な統計をいくつか生成して、最後に結果をログに記録します。 TemperatureSample アプリケーションは Streaming Analytics コンソールからダウンロードすることができます。
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3-sample/#running-the-temperaturesample-application" target="_blank">DEPLOY THE APP ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a><br></td>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3-sample/#viewing-the-running-application" target="_blank">VIEW THE APP ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a></td>
  </tr>
</table>

*表4. TemperatureSample アプリケーション*

<table summary="この表では、最初の行で WordCount Beam サンプル・アプリケーションについて説明しています。この表の 2 行目には、WordCount サンプル・アプリケーションのデプロイ方法に関するチュートリアルへのリンクが含まれています。
 ">
  <tr>
    <th colspan="3">WordCount サンプル・アプリケーション<br></th>
  </tr>
  <tr>
    <td colspan="3">Apache Beam 2.0 Java SDK Quickstart WordCount サンプル・アプリケーションは、テキスト・ファイルから読み取り、変換を適用して単語をトークン化してカウントし、そのデータを出力テキスト・ファイルに書き込むことができる、再使用可能かつ保守可能なパイプラインを作成します。
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3b-wordcount/" target="_blank">DEPLOY THE APP ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a><br></td>
  </tr>
</table>

*表 5. WordCount サンプル・アプリケーション*

<table summary="この表の 1 行目には、FileStreamSample サンプル・アプリケーションについての説明があります。この表の 2 行目には、FileStreamSample アプリケーションのデプロイ方法のチュートリアルへのリンクが含まれています。">
  <tr>
    <th colspan="3">FileStreamSample アプリケーション<br></th>
  </tr>
  <tr>
    <td colspan="3">IBM® Streams Runner for Apache Beam FileStreamSample サンプル・アプリケーションを使用して、ファイルの入出力に {{site.data.keyword.Bluemix_notm}} オブジェクト・ストレージを使用する方法について説明します。
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-5b-objstor/" target="_blank">DEPLOY THE APP ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")</a><br></td>
  </tr>
</table>

*表 6.FileStreamSample アプリケーション*
