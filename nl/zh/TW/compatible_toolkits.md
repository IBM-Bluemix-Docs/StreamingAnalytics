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

# 支援的工具箱及配接器
{: #compatible_toolkits}

{{site.data.keyword.streaminganalyticsshort}} 支援這些分析工具箱和配接器。
{:shortdesc}

| 工具箱| 說明|
| --------------------------------| --------------------------|
| [Complex Event Processing (CEP)](https://ibm.co/2zOwODa)    |	提供 MatchRegex 運算子來執行複式事件處理。|
| [Datetime](https://ibmstreams.github.io/streamsx.datetime/)	|	處理日期、時間及時間戳記的公用程式集。|
| [HBase](http://ibmstreams.github.io/streamsx.hbase/)        | 讓 Streams 應用程式能連接至 Apache HBase。|
| [HDFS](http://ibmstreams.github.io/streamsx.hdfs/)          | 提供與 Hadoop Distributed File System 互動的操作子及函數。|
| [Internet (Inet)](http://ibmstreams.github.io/streamsx.inet)|  專注於與網路管理資料互動。|
| [IoT](http://ibmstreams.github.io/streamsx.iot/)            | 提供 Internet of Things (IoT) 整合，包括 IBM Watson IoT Platform，無論是在 {{site.data.keyword.Bluemix_notm}} 或內部部署 ({{site.data.keyword.streamsshort}})。|
| [JDBC](http://ibmstreams.github.io/streamsx.jdbc/)          | 讓 Streams 應用程式能透過 JDBC 使用資料庫。|
| [JSON](http://ibmstreams.github.io/streamsx.json/)          | 容許您將資料從 JSON 轉換成 Streams 值組格式，反之亦然。|
| [Kafka](https://ibmstreams.github.io/streamsx.kafka/)       | 讓 Streams 應用程式能輕鬆與 Apache Kafka 整合。|
| [MessageHub](https://ibmstreams.github.io/streamsx.messagehub/) | 讓 Streams 應用程式能使用 MessageHub。|
| [Messaging](https://ibmstreams.github.io/streamsx.messaging/)   |  	專注於與熱門傳訊系統互動，例如 Kafka、MQTT、JMS 及 XMS	<br>**附註**：若要搭配使用 JMSSource、JMSSink、XMSSource、XMSSink 與 WebSphere MQ，請在開發環境中完成下列必要步驟：<br>1. 移至 [GitHub 上的 IBMStreams](https://github.com/IBMStreams){:new_window}，並在開發環境中下載 Messaging Toolkit (com.ibm.streamsx.messaging) 3.0.0 版或更新版本。<br>2. 使用 5.1.0 版或更新版本的工具箱來建置您的應用程式。<br>3. 將必要的 .bindings 檔案放在您應用程式的 `/etc` 目錄中，以將它包括在 {{site.data.keyword.streamsshort}} 應用程式軟體組中。|
| [Mining](https://ibm.co/2y3i5au)              	   	            |  所包括的運算子可用來透過套用模型來發掘資料串流。|
| [RabbitMQ](https://ibmstreams.github.io/streamsx.rabbitmq/)     |  所提供的運算子可讓您的 Streams 應用程式從 Rabbit MQ 讀取及傳送訊息。|
| [R-project](https://ibm.co/2h7D9lu)          	   	              |   所包括的 RScript 運算子可用來執行 R 指令，並套用複式資料採礦演算法來偵測資料串流中感興趣的型樣。|
| [Topology](http://ibmstreams.github.io/streamsx.topology/)      |  提供在 {{site.data.keyword.Bluemix_notm}} 平台及 {{site.data.keyword.streamsshort}} 上為 {{site.data.keyword.streaminganalyticsshort}} 服務建置 Python 串流應用程式的功能。|
| [DPS](http://ibmstreams.github.io/streamsx.dps/) |	 讓在一台以上機器執行處理元素 (PE) 的多個應用程式，能共用應用程式特有的狀態資訊。<br>**限制：**只支援使用 REDIS 作為資料庫後端。| 	 	 	
| [Geospatial](https://ibm.co/2h9x0VR) 	     |	所包括的運算子和函數有助於位置資料的有效處理和編製索引作業。<br>**限制：**不支援使用共用對映的運算子（共用對映模式中的 `MapStore`、`PointMapMatcher`）。|
| [TEDA](https://ibm.co/2z9DS00)	   | 	提供一組用於電信應用程式的通用運算子，同時提供一個設定新的檔案對檔案應用程式的應用程式架構。請遵循 [TEDA 指導教學](http://ibmstreams.github.io/streamsx.tutorial.teda/)以便開始。支援工具箱的所有運算子及函數。<br>**限制：**不支援應用程式架構。|
| [TimeSeries](https://ibm.co/2zEPILZ)	 	  | TimeSeries 工具箱中的運算子和函數可設定時間序列資料的條件、對其進行分析並建立其模型。<br>**限制：**不支援已淘汰的運算子。|

*表 1. 支援的工具箱*

## 其他工具箱及運算子
{: #other_operators}

{{site.data.keyword.streaminganalyticsshort}} 支援其他運算子（包括為您自己的需求所開發的工具箱運算子）。
{:shortdesc}

工具箱必須符合下列準則，才能與 {{site.data.keyword.streaminganalyticsshort}} 相容：

1. 不需要在服務實例的應用程式節點上預先安裝額外的軟體。
2. 可以使用工具箱，在應用程式軟體組中包括工具箱所需的任何配置資訊。