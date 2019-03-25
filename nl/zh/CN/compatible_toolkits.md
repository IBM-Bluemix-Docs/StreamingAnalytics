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

# 支持的工具箱和适配器
{: #compatible_toolkits}

{{site.data.keyword.streaminganalyticsshort}} 支持以下分析工具箱和适配器。
{:shortdesc}

|工具箱|描述|
| --------------------------------| --------------------------|
|[Complex Event Processing (CEP) ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://ibm.co/2zOwODa)    |	提供 MatchRegex 操作程序，以执行复杂事件处理。|
|[Datetime ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://ibmstreams.github.io/streamsx.datetime/)	|	用于处理日期、时间和时间戳记的一组实用程序。|
|[HBase ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.hbase/)        |支持 Streams 应用程序连接到 Apache HBase。|
|[HDFS ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.hdfs/)          |提供与 Hadoop 分布式文件系统进行交互的操作程序和功能。|
|[Internet (Inet) ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.inet)|专注于与网络托管的数据进行交互。|
|[IoT ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.iot/)            |在 {{site.data.keyword.Bluemix_notm}} 或内部部署 ({{site.data.keyword.streamsshort}}) 中提供物联网 (IoT) 与 IBM Watson IoT Platform 的集成。|
|[JDBC ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.jdbc/)          |支持 Streams 应用程序通过 JDBC 使用数据库。|
|[JSON ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.json/)          |了解如何将数据从 JSON 转换为 Streams 元组格式，或从 Streams 元组格式转换为 JSON。|
|[Kafka ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://ibmstreams.github.io/streamsx.kafka/)       |支持 Streams 应用程序与 Apache Kafka 轻松集成。|
|[MessageHub ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://ibmstreams.github.io/streamsx.messagehub/) |支持 Streams 应用程序使用 MessageHub。|
|[Messaging ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://ibmstreams.github.io/streamsx.messaging/)   |  	专注于与常用消息传递系统（如 Kafka、MQTT、JMS 和 XMS）进行交互。<br>**注**：要使用 JMSSource、JMSSink、XMSSource、XMSSink 与 WebSphere MQ，请在您的开发环境中完成以下步骤：
<br>1. 转至 [IBMStreams on GitHub ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://github.com/IBMStreams){:new_window} 并在您的开发环境中下载 Messaging Toolkit (com.ibm.streamsx.messaging) V3.0.0 或更高版本。<br>2. 使用 V5.1.0 或更高版本的工具箱来构建应用程序。<br>3. 在应用程序的 `/etc` 目录中放置必要的 `.bindings` 文件，以将其包含在 {{site.data.keyword.streamsshort}} 应用程序捆绑软件中。|
|[RabbitMQ ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://ibmstreams.github.io/streamsx.rabbitmq/) |提供允许 Streams 应用程序从 Rabbit MQ 读取和发送消息的操作程序。|
|[R-project ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://ibm.co/2rj2lKw)          	   	              |包含 RScript 操作程序，可以使用该操作程序来运行 R 命令，并应用复杂的数据挖掘算法，以检测数据流中的相关模式。
|
|[Topology ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.topology/) |了解如何为 {{site.data.keyword.Bluemix_notm}} 平台和 {{site.data.keyword.streamsshort}} 上的 {{site.data.keyword.streaminganalyticsshort}} 服务构建 Python 流式应用程序。|
|[DPS ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.dps/) |	 支持在一个或多个计算机上运行处理元素 (PE) 的多个应用程序共享特定于应用程序的状态信息。<br>**限制：**仅支持 REDIS 作为数据库后端。| 	 	 	
|[Geospatial ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$com.ibm.streams.geospatial/tk$com.ibm.streams.geospatial.html) 	     |	包含可促进对位置数据进行有效处理并建立索引的操作程序和功能。<br>**限制：**不支持使用共享映射方式的操作程序（共享映射方式下的 `MapStore` 和 `PointMapMatcher`）。|
|[TEDA ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$com.ibm.streams.teda/tk$com.ibm.streams.teda.html)	   | 	提供一组在电信应用程序中使用的通用操作程序，它还提供一种应用程序框架，可设置新的文件到文件应用程序。
首先请遵循 [TEDA教程 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.tutorial.teda/)。支持此工具箱的所有操作程序和功能。<br>**限制：**不支持应用程序框架。|
|[TimeSeries ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$com.ibm.streams.timeseries/tk$com.ibm.streams.timeseries.html)	 	  |TimeSeries Toolkit 中的操作程序和功能可限定和分析时间序列数据，并对这些数据进行建模。<br>**限制：**不支持已弃用的操作程序。|
| [{{site.data.keyword.cos_short}} ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://bit.ly/2Ggp03T)	 	  |提供原始运算符和本机函数，分别用于从
{{site.data.keyword.cos_short}} 读取数据或向其写入数据。该工具箱支持兼容 S3 的 {{site.data.keyword.cos_short}}。|

*表 1. 支持的工具箱*

## 其他工具箱和操作程序
{: #other_operators}

{{site.data.keyword.streaminganalyticsshort}} 可以支持其他操作程序，包括您针对自己的需求而开发的那些工具箱操作程序。
{:shortdesc}

工具箱必须满足以下条件，才能与 {{site.data.keyword.streaminganalyticsshort}} 兼容：

1. 在服务实例的应用程序节点上，无需预安装任何其他软件。
2. 工具箱所需的任何配置信息都可使用该工具箱包括在应用程序捆绑软件中。

