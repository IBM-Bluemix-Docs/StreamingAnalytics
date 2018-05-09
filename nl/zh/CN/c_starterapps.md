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

# 样本应用程序
{: #starterapps}

部署并修改入门模板应用程序，并快速了解如何使用 {{site.data.keyword.streaminganalyticsshort}} 服务。
请注意，V2 服务套餐需要在 RHEL 7 上运行 Streams。{{site.data.keyword.streaminganalyticsshort}} 提供[一组入门模板和样本应用程序](https://developer.ibm.com/streamsdev/docs/starter-sample-apps-v2-plans/)，让您可以快速开始使用 V2 服务套餐。EventDetection 和 NYCTraffic 样本应用程序不适用于 V2 服务套餐。
{:shortdesc}


<table summary="此表在第一行描述“股票交易”入门模板应用程序。该表在第二行包含：
1. 在第一列中，如何部署“股票交易”入门模板应用程序的视频链接。2. 在第二列中，直接下载“股票交易”入门模板应用程序的链接。
 ">
  <tr>
    <th colspan="3">股票交易样本应用程序<br></th>
  </tr>
  <tr>
    <td colspan="3">此应用程序对股票报价流进行分析，并使用<a href="https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.1/com.ibm.streams.toolkits.doc/spldoc/dita/tk$spl/op$spl.relational$Aggregate.html">聚合 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a> 运算符生成价格的滚动平均值。
您可以运行入门模板应用程序，而不进行修改。如果您想要进一步尝试该服务，那么您可以修改代码并将更改推送回 {{site.data.keyword.Bluemix_short}} 环境。入门模板应用程序的完整来源<a href="https://github.com/IBMStreams/samples/tree/master/QuickStart/TradesApp">在 GitHub 上提供 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a>。</p>
</td>
  </tr>
  <tr>
    <td><a href="https://developer.ibm.com/streamsdev/videos/getting-started-streaming-analytics-service-using-trades-starter-application/" target="_blank">部署应用程序 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a><br></td>
    <td><a href="https://github.com/IBMStreams/samples/raw/master/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab" target="_blank">下载 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a></td>
  </tr>
</table>

*表 1. 股票交易样本应用程序*


<table summary="此表的第一行描述了“事件检测”V2 样本应用程序，表格的第二行中包含以下内容：1. 第一列是有关如何部署“事件检测”V2 入门模板应用程序的指示信息的链接。2、第二列是有关如何使用“事件检测”入门模板应用程序的教程的链接。3、第三列是直接下载“事件检测”入门模板应用程序的链接。">
  <tr>
    <th colspan="3">“事件检测”V2 样本应用程序<br></th>
  </tr>
  <tr>
    <td colspan="3">“事件检测”V2 应用程序通过 <a href="https://console.ng.bluemix.net/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">{{site.data.keyword.sdk4node}} ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a> 运行时实现。
此入门模板应用程序仅适用于 [V2 服务套餐。](/docs/services/StreamingAnalytics/service_plans.html)。
该应用程序提供一个简单的 Web UI，以显示分析的状态和结果。
Node.js 应用程序绑定到 {{site.data.keyword.streaminganalyticsshort}} 服务的实例。该应用程序通过 {{site.data.keyword.streaminganalyticsshort}} V2 REST API 控制该服务。
<p>您可以运行入门模板应用程序，而不进行修改。
如果您想要进一步尝试该服务，那么您可以修改代码并将更改推送回 {{site.data.keyword.Bluemix_short}} 环境。</p>
</td>
  </tr>
  <tr>
    <td><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">部署应用程序</a><br></td>
    <td><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">教程 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a></td>
    <td><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetectionV2" target="_blank">下载 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a></td>
  </tr>
</table>

*表 2. 事件检测 V2 样本应用程序*
<table summary="此表的第一行描述了“事件检测”样本应用程序。表格的第二行中包含以下内容：
1. 第一列是有关如何部署“事件检测”入门模板应用程序的指示信息的链接。2. 第二列是有关如何使用“事件检测”入门模板应用程序的教程的链接。3. 第三列是用于直接下载“事件检测”入门模板应用程序的链接。">
  <tr>
    <th colspan="3">事件检测样本应用程序<br></th>
  </tr>
  <tr>
    <td colspan="3">“事件检测”应用程序通过 <a href="https://console.ng.bluemix.net/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">{{site.data.keyword.sdk4node}} ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a> 运行时实现。
此入门模板应用程序仅适用于 [V1 服务套餐。](/docs/services/StreamingAnalytics/service_plans.html)。
该应用程序提供一个简单的 Web UI，以显示分析的状态和结果。
Node.js 应用程序绑定到 {{site.data.keyword.streaminganalyticsshort}} 服务的实例。该应用程序通过 {{site.data.keyword.streaminganalyticsshort}} REST API 控制该服务。
<p>您可以运行入门模板应用程序，而不进行修改。
如果您想要进一步尝试该服务，那么您可以修改代码并将更改推送回 {{site.data.keyword.Bluemix_short}} 环境。</p>
</td>
  </tr>
  <tr>
    <td><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">部署应用程序</a><br></td>
    <td><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">教程 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a></td>
    <td><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection" target="_blank">下载 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a></td>
  </tr>
</table>

*表 2. 事件检测样本应用程序*

<table summary="此表在第一行描述“纽约交通”样本应用程序。该表的第二行包括：
1. 在第一列上，是指向如何部署“纽约交通”样本应用程序指示信息的链接。2. 在第二列中，是指向如何使用“纽约交通”样本应用程序教程的链接。3. 在第三列中，是用于直接下载“纽约交通”样本应用程序的链接。">
  <tr>
    <th colspan="3">NYC 交通样本应用程序<br></th>
  </tr>
  <tr>
    <td colspan="3">“NYC 交通”入门模板应用程序是用 Liberty for Java 针对 {{site.data.keyword.Bluemix_short}} 编写的应用程序。它包含 {{site.data.keyword.streamsshort}} 应用程序，可从纽约城交通传感器检索公共数据、计算聚集统计信息，并将结果发送回 Liberty 应用程序。
此入门模板应用程序仅适用于 [V1 服务套餐。](/docs/services/StreamingAnalytics/service_plans.html)。
<p>您可以运行入门模板应用程序，而不进行修改。如果您想要进一步尝试该服务，那么您可以修改代码并将更改推送回 {{site.data.keyword.Bluemix_short}} 环境。</p>
</td>
  </tr>
  <tr>
    <td><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">部署应用程序</a><br></td>
    <td><a href="https://developer.ibm.com/streamsdev/docs/bluemix-streaming-analytics-starter-application/" target="_blank">教程 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a></td>
    <td><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic" target="_blank">下载 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a></td>
  </tr>
</table>

*表 3. NYC 交通样本应用程序*

## IBM Streams Runner for Apache Beam 样本应用程序

<table summary="此表第一行描述 TemperatureSample Beam 应用程序，第二行包含指向如何部署 TemperatureSample Beam 应用程序的教程的链接。
 ">
  <tr>
    <th colspan="3">TemperatureSample Beam 应用程序<br></th>
  </tr>
  <tr>
    <td colspan="3">此应用程序用于从多个设备获取温度读数。此入门模板应用程序仅适用于 [V2 服务套餐。](/docs/services/StreamingAnalytics/service_plans.html)。
此应用程序基于特定的阈值，将读数划分为“良好”（有效）和“不良”（无效）读数。它会统计不良读数的计数，并为良好读数生成一些基本的统计信息，最后记录结果。可以从 Streaming Analytics 控制台下载 TemperatureSample 应用程序。
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3-sample/#running-the-temperaturesample-application" target="_blank">部署应用程序 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a><br></td>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3-sample/#viewing-the-running-application" target="_blank">查看应用程序 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a></td>
  </tr>
</table>

*表 4. TemperatureSample 应用程序*

<table summary="此表第一行描述 WordCount Beam 示例应用程序，第二行包含指向如何部署 WordCount 示例应用程序的教程的链接。
 ">
  <tr>
    <th colspan="3">WordCount 样本应用程序<br></th>
  </tr>
  <tr>
    <td colspan="3">Apache Beam 2.0 Java SDK 快速入门 WordCount 样本应用程序用于创建可复用且可维护的管道，管道可以从文本文件中读取数据，应用转换以对字进行标记化和计数，然后将数据写入输出文本文件。
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3b-wordcount/" target="_blank">部署应用程序 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a><br></td>
  </tr>
</table>

*表 5. WordCount 样本应用程序*

<table summary="此表在第一行中描述 FileStreamSample 样本应用程序。此表在第二行上包含一个链接，该链接指向如何部署 FileStreamSample 应用程序的教程。
 ">
  <tr>
    <th colspan="3">FileStreamSample 应用程序<br></th>
  </tr>
  <tr>
    <td colspan="3">可以使用 IBM® Streams Runner for Apache Beam FileStreamSample 样本应用程序来了解如何将 {{site.data.keyword.Bluemix_notm}} 对象存储器用于文件输入和输出。
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-5b-objstor/" target="_blank">部署应用程序 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")</a><br></td>
  </tr>
</table>

*表 6. FileStreamSample 应用程序*
