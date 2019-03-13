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

# 샘플 애플리케이션
{: #starterapps}

스타터 애플리케이션을 배치 및 수정하고 {{site.data.keyword.streaminganalyticsshort}} 서비스를 사용하는 방법을 빠르게 배우십시오. v2 서비스 플랜의 경우 RHEL 7에서 Streams를 실행해야 합니다. {{site.data.keyword.streaminganalyticsshort}}에서는 신속하게 v2 서비스 플랜을 시작할 수 있도록 [ 스타터 및 샘플 애플리케이션 세트](https://developer.ibm.com/streamsdev/docs/starter-sample-apps-v2-plans/)를 제공합니다. EventDetection 및 NYCTraffic 샘플 애플리케이션은 v2 서비스 플랜에서는 작동하지 않습니다.
{:shortdesc}


<table summary="이 표의 첫 번째 행에는 Stock Trades 스타터 애플리케이션에 대한 설명이 있습니다. 표의 두 번째 행에는 다음이 포함되어 있습니다.
1. 첫 번째 열에는 Stock Trades 스타터 애플리케이션을 배치하는 방법에 대한 비디오 링크가 있습니다. 2. 두 번째 열에는 Stock Trades 스타터 애플리케이션을 직접 다운로드할 수 있는 링크가 있습니다.">
  <tr>
    <th id="stocktrades" colspan="3">Stock Trades 샘플 앱<br></th>
  </tr>
  <tr>
    <td headers="stocktrades" colspan="3">이 애플리케이션은 주식 시세의 흐름을 분석하고 <a href="https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$spl/op$spl.relational$Aggregate.html">집계 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a> 연산자를 사용하여 가격의 평균을 산출합니다.
수정하지 않고 스타터 애플리케이션을 실행할 수 있습니다. 서비스를 더 실험해 보고 싶으면 코드를 수정하여 변경을 {{site.data.keyword.Bluemix_short}} 환경에 다시 넣을 수도 있습니다. 스타터 애플리케이션에 대한 전체 소스는 <a href="https://github.com/IBMStreams/samples/tree/master/QuickStart/TradesApp">GitHub에서 사용 가능 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a>합니다.</p>
</td>
  </tr>
  <tr>
    <td headers="stocktrades"><a href="https://developer.ibm.com/streamsdev/videos/getting-started-streaming-analytics-service-using-trades-starter-application/" target="_blank">앱 배치 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a><br></td>
    <td headers="stocktrades"><a href="https://github.com/IBMStreams/samples/raw/master/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab" target="_blank">다운로드 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a></td>
  </tr>
</table>

*표 1. Stock Trades 샘플 앱*


<table summary="이 표의 첫 번째 행에는 Event Detection v2 샘플 애플리케이션에 대한 설명이 있습니다. 표의 두 번째 행에는 다음이 포함되어 있습니다.
1. 첫 번째 열에는 Event Detection v2 스타터 애플리케이션을 배치하는 방법에 대한 지시사항 링크가 있습니다. 2. 두 번째 열에는 Event Detection 스타터 애플리케이션 사용 방법에 대한 튜토리얼 링크가 있습니다. 3. 세 번째 열에는 Event Detection 스타터 애플리케이션을 직접 다운로드할 수 있는 링크가 있습니다.">
  <tr>
    <th id="EventDetection2" colspan="3">Event Detection v2 샘플 앱<br></th>
  </tr>
  <tr>
    <td colspan="3" headers="EventDetection2">Event Detection v2 앱은 <a href="https://{DomainName}/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">SDK for Node.js ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a> 런타임을 통해 구현됩니다. 이 스타터 앱은 [v2 서비스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)과만 호환됩니다.
앱은 분석의 상태와 결과를 표시하기 위한 간단한 웹 UI를 제공합니다.
Node.js 앱은 {{site.data.keyword.streaminganalyticsshort}} 서비스의 인스턴스에 바인드됩니다. 앱은 {{site.data.keyword.streaminganalyticsshort}} v2 REST API를 통해 서비스를 제어합니다.
<p>수정하지 않고 스타터 애플리케이션을 실행할 수 있습니다.
서비스를 더 실험해 보고 싶으면 코드를 수정하여 변경을 {{site.data.keyword.Bluemix_short}} 환경에 다시 넣을 수도 있습니다.</p>
</td>
  </tr>
  <tr>
    <td headers="EventDetection2"><a href="/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps_deploy#starterapps_deploy" target="_blank">앱 배치</a><br></td>
    <td headers="EventDetection2"><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">튜토리얼 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a></td>
    <td headers="EventDetection2"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetectionV2" target="_blank">다운로드 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a></td>
  </tr>
</table>

*표 2. Event Detection v2 샘플 앱*
<table summary="이 표의 첫 번째 행에는 Event Detection 샘플 애플리케이션에 대한 설명이 있습니다. 표의 두 번째 행에는 다음 내용이 있습니다.
1. 첫 번째 행에는 Event Detection 스타터 애플리케이션 배치 방법에 대한 지시사항 링크가 있습니다. 2. 두 번째 행에는 Event Detection 스타터 애플리케이션 사용 방법에 대한 튜토리얼 링크가 있습니다.">
  <tr>
    <th id="EventDetection1" colspan="3">Event Detection 샘플 앱<br></th>
  </tr>
  <tr>
    <td headers="EventDetection1" colspan="3">Event Detection 앱은 <a href="https://{DomainName}/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">SDK for Node.js ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a> 런타임을 통해 구현됩니다.
이 스타터 앱은 [v1 서비스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)과만 호환됩니다. 앱은 분석의 상태와 결과를 표시하기 위한 간단한 웹 UI를 제공합니다.
Node.js 앱은 {{site.data.keyword.streaminganalyticsshort}} 서비스의 인스턴스에 바인드됩니다. 앱은 {{site.data.keyword.streaminganalyticsshort}} REST API를 통해 서비스를 제어합니다.
<p>수정하지 않고 스타터 애플리케이션을 실행할 수 있습니다.
서비스를 더 실험해 보고 싶으면 코드를 수정하여 변경을 {{site.data.keyword.Bluemix_short}} 환경에 다시 넣을 수도 있습니다.</p>
</td>
  </tr>
  <tr>
    <td headers="EventDetection1"><a href="/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps_deploy" target="_blank">앱 배치</a><br></td>
    <td headers="EventDetection1"><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">튜토리얼 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a></td>
    <td headers="EventDetection1"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection" target="_blank">다운로드 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a></td>
  </tr>
</table>

*표 2. Event Detection 샘플 앱*

<table summary="이 표의 첫 번째 행에는 뉴욕 트래픽 샘플 애플리케이션에 대한 설명이 있습니다. 표의 두 번째 행에는 다음 내용이 있습니다.
1. 첫 번째 행에는 뉴욕 트래픽 샘플 애플리케이션 배치 방법에 대한 지시사항 링크가 있습니다. 2. 두 번째 행에는 뉴욕 트래픽 샘플 애플리케이션 사용 방법에 대한 튜토리얼 링크가 있습니다.">
  <tr>
    <th id="NYCTraffic" colspan="3">NYC Traffic 샘플 앱<br></th>
  </tr>
  <tr>
    <td headers="NYCTraffic" colspan="3">NYC Traffic 스타터 앱은 Liberty for Java로 작성된 {{site.data.keyword.Bluemix_short}}용 애플리케이션입니다. 여기에는 뉴욕시 트래픽 센서에서 얻은 공공 데이터를 검색하고 집계 통계를 계산하며 결과를 Liberty 애플리케이션으로 다시 전송하는 {{site.data.keyword.streamsshort}} 애플리케이션이 있습니다. 이 스타터 앱은 [v1 서비스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)과만 호환됩니다.
<p>수정하지 않고 스타터 애플리케이션을 실행할 수 있습니다. 서비스를 더 실험해 보고 싶으면 코드를 수정하여 변경을 {{site.data.keyword.Bluemix_short}} 환경에 다시 넣을 수도 있습니다.</p>
</td>
  </tr>
  <tr>
    <td headers="NYCTraffic" deploylink><a href="/docs/services/StreamingAnalytics/?topic=StreamingAnalytics-starterapps_deploy" target="_blank">앱 배치</a><br></td>
    <td headers="NYCTraffic"><a href="https://developer.ibm.com/streamsdev/docs/bluemix-streaming-analytics-starter-application/" target="_blank">튜토리얼 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a></td>
    <td headers="NYCTraffic"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic" target="_blank">다운로드 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a></td>
  </tr>
</table>

*표 3. NYC Traffic 샘플 앱*

## IBM Streams Runner for Apache Beam 샘플 앱

<table summary="이 표의 첫 번째 행에는 TemperatureSample Beam 애플리케이션이 설명되어 있습니다. 이 표의 두 번째 행에는 TemperatureSample Beam 애플리케이션을 배치하는 방법에 대한 튜토리얼의 링크가 포함되어 있습니다.">
  <tr>
    <th id="TemperatureSample" colspan="3">TemperatureSample Beam 앱<br></th>
  </tr>
  <tr>
    <td headers="TemperatureSample" colspan="3">이 애플리케이션은 여러 디바이스로부터 온도 수치를 읽습니다. 이 스타터 앱은 [v2 서비스 플랜](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)에만 사용할 수 있습니다. 이 애플리케이션은 특정 임계값에 따라 수치를 "바른"(올바름) 수치와 "잘못된"(올바르지 않음) 수치로 구분합니다. 그 다음 잘못된 수치를 계산하고 바른 수치에 대한 몇 가지 기본 통계를 생성한 후 마지막으로 결과를 로그합니다. TemperatureSample 앱은 Streaming Analytics 콘솔에서 다운로드할 수 있습니다.
</td>
  </tr>
  <tr>
    <td headers="TemperatureSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/sample/#running-the-temperaturesample-application" target="_blank">앱 배치 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a><br></td>
    <td headers="TemperatureSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/sample/#viewing-the-running-application" target="_blank">앱 보기 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a></td>
  </tr>
</table>

*표 4. TemperatureSample 앱*

<table summary="이 표의 첫 번째 행에는 WordCount Beam 샘플 애플리케이션이 설명되어 있습니다. 이 표의 두 번째 행에는 WordCount 샘플 애플리케이션을 배치하는 방법에 대한 튜토리얼의 링크가 포함되어 있습니다.">
  <tr>
    <th id="WordCountSample" colspan="3">WordCount 샘플 앱<br></th>
  </tr>
  <tr>
    <td headers="WordCountSample" colspan="3">Apache Beam 2.0 Java SDK Quickstart WordCount 샘플 애플리케이션은 텍스트 파일에서 읽고, 변환을 적용하여 토큰화하고 단어 수를 계산하며, 데이터를 출력 텍스트 파일에 쓸 수 있는 재사용이 가능하고 유지보수할 수 있는 파이프라인을 작성합니다.
</td>
  </tr>
  <tr>
    <td headers="WordCountSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/wordcount/" target="_blank">앱 배치 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a><br></td>
  </tr>
</table>

*표 5. WordCount 샘플 앱*

<table summary="이 표는 첫 번째 행에서 FileStreamSample 샘플 애플리케이션에 대해 설명합니다. 표에는 FileStreamSample 애플리케이션을 배치하는 방법에 대한 튜토리얼의 링크가 두 번째 행에 포함되어 있습니다.">
  <tr>
    <th id="FilterStreamSample" colspan="3">FileStreamSample 앱<br></th>
  </tr>
  <tr>
    <td headers="FilterStreamSample" colspan="3">IBM® Streams Runner for Apache Beam FileStreamSample 샘플 애플리케이션을 사용하여 파일 입력 및 출력을 위해 {{site.data.keyword.Bluemix_notm}} 오브젝트 스토리지를 사용하는 방법을 알아볼 수 있습니다.
</td>
  </tr>
  <tr>
    <td headers="FilterStreamSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/objstor/" target="_blank">앱 배치 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")</a><br></td>
  </tr>
</table>

*표 6. FileStreamSample 앱*
