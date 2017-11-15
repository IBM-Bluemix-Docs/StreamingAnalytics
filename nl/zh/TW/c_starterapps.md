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

# 使用 Streaming Analytics 入門範本應用程式
{: #starterapps}

部署並修改入門範本應用程式，以及快速瞭解如何使用 {{site.data.keyword.streaminganalyticsshort}} 服務：
{:shortdesc}

<table summary="此表格的第一列說明 Stock Trades 入門範本應用程式。表格包含第二列：1. 在第一欄，有鏈結連往如何部署 Stock Trades 入門範本應用程式的視訊。2. 在第二欄，有鏈結可直接下載 Stock Trades 入門範本應用程式。">
  <tr>
    <th colspan="3">Stock Trades 範例應用程式<br></th>
  </tr>
  <tr>
    <td colspan="3">此應用程式會分析股票報價的串流，並使用 <a href="https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$spl/op$spl.relational$Aggregate.html">Aggregate</a> 運算子產生價格的滾動平均值。您可以執行入門範本應用程式，而不需要進行修改。如果您要進一步實驗服務，也可以修改程式碼，並將變更推送回 {{site.data.keyword.Bluemix_short}} 環境。入門範本應用程式的完整原始檔<a href="https://github.com/IBMStreams/samples/tree/master/QuickStart/TradesApp">提供於 GitHub</a>。</p></td>
  </tr>
  <tr>
    <td><a href="https://developer.ibm.com/streamsdev/videos/getting-started-streaming-analytics-service-using-trades-starter-application/" target="_blank">部署應用程式</a><br></td>
    <td><a href="https://github.com/IBMStreams/samples/raw/master/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab" target="_blank">下載</a></td>
  </tr>
</table>

*表 1. Stock Trades 範例應用程式*


<table summary="此表格的第一列說明 Event Detection 範例應用程式。表格第二列包含：1. 在第一欄中，如何部署 Event Detection 入門範本應用程式的指示鏈結。2. 在第二欄中，如何使用 Event Detection 入門範本應用程式的指導教學鏈結。3. 在第三欄中，直接下載 Event Detection 入門範本應用程式的鏈結。">
  <tr>
    <th colspan="3">Event Detection 範例應用程式<br></th>
  </tr>
  <tr>
    <td colspan="3">Event Detection 應用程式是透過 <a href="https://console.ng.bluemix.net/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">{{site.data.keyword.sdk4node}}</a> 運行環境實作。此應用程式提供簡單的 Web 使用者介面，來顯示分析的狀態和結果。Node.js 應用程式已連結至 {{site.data.keyword.streaminganalyticsshort}} 服務實例。此應用程式透過 {{site.data.keyword.streaminganalyticsshort}} REST API 來控制服務。<p>您可以執行入門範本應用程式，而不需要進行修改。如果您要進一步實驗服務，也可以修改程式碼，並將變更推送回 {{site.data.keyword.Bluemix_short}} 環境。</p></td>
  </tr>
  <tr>
    <td><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">部署應用程式</a><br></td>
    <td><a href="http://www.ibm.com/developerworks/library/ba-bluemix-detect-complex-events-from-data-stream-trs/index.html" target="_blank">指導教學</a></td>
    <td><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection" target="_blank">下載</a></td>
  </tr>
</table>

*表 2. Event Detection 範例應用程式*

<table summary="此表格的第一列說明 New York Traffic 範例應用程式。表格第二列包含：1. 在第一欄中，如何部署 New York Traffic 範例應用程式的指示鏈結。2. 在第二欄中，如何使用 New York Traffic 範例應用程式的指導教學鏈結。3. 在第三欄中，直接下載 New York Traffic 範例應用程式的鏈結。">
  <tr>
    <th colspan="3">NYC Traffic 範例應用程式<br></th>
  </tr>
  <tr>
    <td colspan="3">NYC Traffic 入門範本應用程式是以 Liberty for Java 撰寫的 {{site.data.keyword.Bluemix_short}} 應用程式。它所包含的 {{site.data.keyword.streamsshort}} 應用程式可以擷取紐約市交通感應器中的公用資料，並計算聚集統計資料，然後將結果傳回給 Liberty 應用程式。<p>您可以執行入門範本應用程式，而不需要進行修改。如果您要進一步實驗服務，也可以修改程式碼，並將變更推送回 {{site.data.keyword.Bluemix_short}} 環境。</p></td>
  </tr>
  <tr>
    <td><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">部署應用程式</a><br></td>
    <td><a href="https://developer.ibm.com/streamsdev/docs/bluemix-streaming-analytics-starter-application/" target="_blank">指導教學</a></td>
    <td><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic" target="_blank">下載</a></td>
  </tr>
</table>

*表 3. NYC Traffic 範例應用程式*

## IBM Streams Runner for Apache Beam 範例應用程式

<table summary="此表格的第一列說明 TemperatureSample Beam 應用程式。表格第二列包含如何部署 TemperatureSample Beam 應用程式的指導教學鏈結。">
  <tr>
    <th colspan="3">`TemperatureSample` Beam 應用程式<br></th>
  </tr>
  <tr>
    <td colspan="3">這個應用程式會從多台裝置取得溫度的讀數。應用程式根據特定的臨界值將讀數分成好（有效）和壞（無效）的讀數。它會計算壞的讀數、針對好的讀數產生一些基本統計資料，最後記錄結果。您可以從 Streaming Analytics 主控台下載 TemperatureSample 應用程式。</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3-sample/#running-the-temperaturesample-application" target="_blank">部署應用程式</a><br></td>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3-sample/#viewing-the-running-application" target="_blank">檢視應用程式</a></td>
  </tr>
</table>

*表 4. TemperatureSample 應用程式*

<table summary="此表格的第一列說明 WordCount Beam 範例應用程式。表格第二列包含如何部署 WordCount 範例應用程式的指導教學鏈結。">
  <tr>
    <th colspan="3">WordCount 範例應用程式<br></th>
  </tr>
  <tr>
    <td colspan="3">Apache Beam 2.0 Java SDK Quickstart WordCount 範例應用程式會建立可重複使用且可維護的管線，可以從文字檔讀取、套用轉換以便記號化並計算文字，然後將資料寫入到輸出文字檔。</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3b-wordcount/" target="_blank">部署應用程式</a><br></td>
  </tr>
</table>

*表 5. `WordCount` 範例應用程式*

<table summary="此表格的第一列說明 `FileStreamSample` 範例應用程式。表格第二列包含如何部署 `FileStreamSample` 應用程式的指導教學鏈結。">
  <tr>
    <th colspan="3">FileStreamSample 應用程式<br></th>
  </tr>
  <tr>
    <td colspan="3">您可以使用 IBM® Streams Runner for Apache Beam FileStreamSample 範例應用程式，以了解如何使用 {{site.data.keyword.Bluemix_notm}} Object Storage 進行檔案輸入及輸出。</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-5b-objstor/" target="_blank">部署應用程式</a><br></td>
  </tr>
</table>

*表 6.`FileStreamSample` 應用程式*
