---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-16"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Sample applications
{: #starterapps}

Deploy and modify the starter applications and quickly learn how to use the {{site.data.keyword.streaminganalyticsshort}} service. {{site.data.keyword.streaminganalyticsshort}} provides a [set of starter and sample applications](https://developer.ibm.com/streamsdev/docs/starter-sample-apps-v2-plans/) to quickly get you started. Note that the service plans require applications to run Streams on RHEL 7.
{:shortdesc}


## IBM Streams SPL application samples

### Stock Trades sample app

<table summary="This table describes, in the first row, the Stock Trades starter application. The table includes on the second row:
1. In the first column, a link to a video on how to deploy the Stock Trades starter application. 2. In the second column, a link to directly download the Stock Trades starter application.
 ">
  <tr>
    <td headers="stocktrades" colspan="3">This application analyzes a stream of stock quotes and produces a rolling average of the prices using the <a href="https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$spl/op$spl.relational$Aggregate.html">Aggregate ![External link icon](../../icons/launch-glyph.svg "External link icon")</a> operator.
You can run the starter application without modification. If you want to experiment further with the service, you can also modify the code and push your changes back to the {{site.data.keyword.Bluemix_short}} environment. The full source for the starter application is <a href="https://github.com/IBMStreams/samples/tree/master/QuickStart/TradesApp">available on GitHub ![External link icon](../../icons/launch-glyph.svg "External link icon")</a>.</p>
</td>
  </tr>
  <tr>
    <td headers="stocktrades"><a href="https://developer.ibm.com/streamsdev/videos/getting-started-streaming-analytics-service-using-trades-starter-application/" target="_blank">DEPLOY THE APP ![External link icon](../../icons/launch-glyph.svg "External link icon")</a><br></td>
    <td headers="stocktrades"><a href="https://github.com/IBMStreams/samples/raw/master/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab" target="_blank">DOWNLOAD ![External link icon](../../icons/launch-glyph.svg "External link icon")</a></td>
  </tr>
</table>

### Event Detection sample app

<table summary="This table describes, in the first row, the Event Detection sample application. The table includes on the second row:
1. In the first column, a link to instructions on how to deploy the Event Detection starter application. 2. In the second column, a link to tutorials on how to use the Event Detection starter application. 3. In the third column, a link to directly download the Event Detection starter application.
 ">
  <tr>
    <td colspan="3" headers="EventDetection2">The Event Detection app is implemented via the <a href="https://{DomainName}/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">SDK for Node.js ![External link icon](../../icons/launch-glyph.svg "External link icon")</a> runtime. The app provides a simple web UI to display status and results of the analysis.
The Node.js app is bound to an instance of the {{site.data.keyword.streaminganalyticsshort}} service. The app controls the service via the {{site.data.keyword.streaminganalyticsshort}} REST API.
<p>You can run the starter application without modification.
If you want to experiment further with the service, you can also modify the code and push your changes back to the {{site.data.keyword.Bluemix_short}} environment.</p>
</td>
  </tr>
  <tr>
    <td headers="EventDetection2"><a href="/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps_deploy#starterapps_deploy" target="_blank">DEPLOY THE APP</a><br></td>
    <td headers="EventDetection2"><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">TUTORIAL ![External link icon](../../icons/launch-glyph.svg "External link icon")</a></td>
    <td headers="EventDetection2"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetectionV2" target="_blank">DOWNLOAD ![External link icon](../../icons/launch-glyph.svg "External link icon")</a></td>
  </tr>
</table>


## IBM Streams Runner for Apache Beam samples

### TemperatureSample Beam app

<table summary="This table describes, in the first row, the TemperatureSample Beam application. The table includes on the second row a link to a tutorial how to deploy the TemperatureSample Beam application.
 ">
  <tr>
    <td headers="TemperatureSample" colspan="3">This application takes temperature readings from multiple devices. The application splits the readings into “good” (valid) and “bad” (invalid) readings based on a specific threshold. It counts the bad readings and generates some basic statistics for the good readings, and finally logs the results. You can download the TemperatureSample app from the Streaming Analytics console.
</td>
  </tr>
  <tr>
    <td headers="TemperatureSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/sample/#running-the-temperaturesample-application" target="_blank">DEPLOY THE APP ![External link icon](../../icons/launch-glyph.svg "External link icon")</a><br></td>
    <td headers="TemperatureSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/sample/#viewing-the-running-application" target="_blank">VIEW THE APP ![External link icon](../../icons/launch-glyph.svg "External link icon")</a></td>
  </tr>
</table>

### WordCount Beam app

<table summary="This table describes, in the first row, the WordCount Beam sample application. The table includes on the second row a link to a tutorial how to deploy the WordCount sample application.
 ">
  <tr>
    <td headers="WordCountSample" colspan="3">The Apache Beam 2.0 Java SDK Quickstart WordCount sample application creates reusable and mantainable pipelines that can read from a text file, apply transforms to tokenize and count the words, and write the data to an output text file.
</td>
  </tr>
  <tr>
    <td headers="WordCountSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/wordcount/" target="_blank">DEPLOY THE APP ![External link icon](../../icons/launch-glyph.svg "External link icon")</a><br></td>
  </tr>
</table>

### FileStreamSample Beam app

<table summary="This table describes, in the first row, the FileStreamSample sample application. The table includes on the second row a link to a tutorial how to deploy the FileStreamSample application.
 ">
  <tr>
    <td headers="FilterStreamSample" colspan="3">You can use the IBM® Streams Runner for Apache Beam FileStreamSample sample application to learn how to use {{site.data.keyword.Bluemix_notm}} object storage for file input and output.
</td>
  </tr>
  <tr>
    <td headers="FilterStreamSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/objstor/" target="_blank">DEPLOY THE APP ![External link icon](../../icons/launch-glyph.svg "External link icon")</a><br></td>
  </tr>
</table>
