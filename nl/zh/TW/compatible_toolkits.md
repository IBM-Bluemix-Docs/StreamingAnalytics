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

# 支援的工具箱及配接器
{: #compatible_toolkits}

{{site.data.keyword.streaminganalyticsshort}} 支援這些分析工具箱和配接器。
{:shortdesc}

|工具箱|說明|
| --------------------------------| --------------------------|
|[Complex Event Processing (CEP) ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://ibm.co/2zOwODa)    |	提供 MatchRegex 運算子來執行複式事件處理。|
|[Datetime ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://ibmstreams.github.io/streamsx.datetime/)	|	處理日期、時間及時間戳記的公用程式集。|
|[HBase![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.hbase/)        |讓 Streams 應用程式能連接至 Apache HBase。|
|[HDFS ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.hdfs/)          |提供與 Hadoop Distributed File System 互動的操作子及函數。|
|[Internet (Inet) ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.inet)|專注於與網路管理資料互動。|
|[IoT ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.iot/)            |在 {{site.data.keyword.Bluemix_notm}} 或內部部署 ({{site.data.keyword.streamsshort}}) 中提供 Internet of Things (IoT) 與「IBM Watson IoT 平台」的整合。|
|[JDBC ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.jdbc/)          |讓 Streams 應用程式能透過 JDBC 使用資料庫。|
|[JSON ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.json/)          |瞭解如何將資料從 JSON 轉換成 Streams 值組格式，反之亦然。|
|[Kafka ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://ibmstreams.github.io/streamsx.kafka/)       |讓 Streams 應用程式能輕鬆與 Apache Kafka 整合。|
|[MessageHub ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://ibmstreams.github.io/streamsx.messagehub/) |讓 Streams 應用程式能使用 MessageHub。|
|[Messaging ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://ibmstreams.github.io/streamsx.messaging/)   |  	專注於與熱門傳訊系統互動，例如 Kafka、MQTT、JMS 及 XMS	<br>**附註**：若要搭配使用 JMSSource、JMSSink、XMSSource、XMSSink 與 WebSphere MQ，請在開發環境中完成下列步驟：<br>1. 移至 [IBMStreams on GitHub ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://github.com/IBMStreams){:new_window}，並在開發環境中下載 Messaging Toolkit (com.ibm.streamsx.messaging) 3.0.0 版或更新版本。<br>2. 使用 5.1.0 版或更新版本的工具箱來建置您的應用程式。<br>3. 將必要的 `.bindings` 檔案放在您應用程式的 `/etc` 目錄中，以將它包含在 {{site.data.keyword.streamsshort}} 應用程式軟體組裡。|
|[Mining ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://ibm.co/2rj2lKw)              	   	            |所包括的運算子可用來透過套用模型來發掘資料串流。<br> **限制：**如果您要使用 [v2 服務方案](/docs/services/StreamingAnalytics/service_plans.html)，由於您必須在 RHEL 7 環境或相等的 CentOS 版本中編譯應用程式軟體組，因此不支援此工具箱。|
|[RabbitMQ ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://ibmstreams.github.io/streamsx.rabbitmq/)     |所提供的運算子可讓您的 Streams 應用程式從 Rabbit MQ 讀取及傳送訊息。|
|[R-project ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://ibm.co/2rj2lKw)          	   	              |所包括的 RScript 運算子可用來執行 R 指令，並套用複式資料採礦演算法來偵測資料串流中感興趣的型樣。|
|[Topology ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.topology/)      |瞭解如何在 {{site.data.keyword.Bluemix_notm}} 平台及 {{site.data.keyword.streamsshort}} 上為 {{site.data.keyword.streaminganalyticsshort}} 服務建置 Python 串流應用程式。|
|[DPS ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.dps/) |	 讓在一台以上機器執行處理元素 (PE) 的多個應用程式，能共用應用程式特有的狀態資訊。<br>**限制：**只支援使用 REDIS 作為資料庫後端。| 	 	 	
|[Geospatial ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://ibm.co/2KWf6nd) 	     |	所包括的運算子和函數有助於位置資料的有效處理和編製索引作業。<br>**限制：**不支援使用共用對映的運算子（共用對映模式中的 `MapStore`、`PointMapMatcher`）。|
|[TEDA ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://ibm.co/2FYeTRL)	   | 	提供一組用於電信應用程式的通用運算子，同時提供一個應用程式架構，來設定新的檔案對檔案應用程式。請遵循 [TEDA 指導教學 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://ibmstreams.github.io/streamsx.tutorial.teda/) 以開始使用。支援工具箱的所有運算子及函數。<br>**限制：**不支援應用程式架構。|
|[TimeSeries ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://ibm.co/2FXzsgX)	 	  |TimeSeries 工具箱中的運算子和函數可設定時間序列資料的條件、對其進行分析並建立其模型。<br>**限制：**不支援已淘汰的運算子。|
| [{{site.data.keyword.cos_short}} ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://bit.ly/2Ggp03T)	 	  |提供基本運算子及原生函數，以便讀寫 {{site.data.keyword.cos_short}} 的資料。工具箱支援 S3 相容的 {{site.data.keyword.cos_short}}。|

*表 1. 支援的工具箱*

## 其他工具箱及運算子
{: #other_operators}

{{site.data.keyword.streaminganalyticsshort}} 支援其他運算子（包括為您自己的需求所開發的工具箱運算子）。
{:shortdesc}

工具箱必須符合下列準則，才能與 {{site.data.keyword.streaminganalyticsshort}} 相容：

1. 不需要在服務實例的應用程式節點上預先安裝額外的軟體。
2. 可以使用工具箱，在應用程式軟體組裡包含工具箱所需的任何配置資訊。
