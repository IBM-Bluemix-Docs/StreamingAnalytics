---

copyright:
  years: 2015, 2018
lastupdated: "2018-07-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# サポートされるツールキットおよびアダプター
{: #compatible_toolkits}

以下の分析ツールキットおよびアダプターが {{site.data.keyword.streaminganalyticsshort}} によってサポートされます。
{:shortdesc}

| ツールキット                        | 説明							                  |
| --------------------------------| --------------------------|
| [Complex Event Processing (CEP) ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://ibm.co/2zOwODa)    |	複合イベント処理を実行する MatchRegex 演算子を提供します。  		 |
| [Datetime ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://ibmstreams.github.io/streamsx.datetime/)	|	日付、時刻、およびタイム・スタンプを処理する一連のユーティリティー。	 |
| [HBase![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.hbase/)        | Streams アプリケーションが Apache HBase に接続できるようにします。	 	   |
| [HDFS ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.hdfs/)          | Hadoop 分散ファイル・システムと対話する演算子と関数を提供します。	|
| [Internet (Inet) ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.inet)|  ネットワークにホストされたデータとの対話に焦点を当てます。				       |
| [IoT ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.iot/)            |{{site.data.keyword.Bluemix_notm}} またはオンプレミス ({{site.data.keyword.streamsshort}}) のいずれかで、IBM Watson IoT プラットフォームとの Internet of Things (IoT) 統合を提供します。 |
| [JDBC ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.jdbc/)          | Streams アプリケーションが JDBC を介してデータベースで作業できるようにします。		   |
| [JSON ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.json/)          | データを JSON から Streams タプル形式 (およびその逆) に変換する方法を説明します。   		|
| [Kafka ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://ibmstreams.github.io/streamsx.kafka/)       | Streams アプリケーションが簡単に Apache Kafka と統合できるようにします。 	 |
| [MessageHub ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://ibmstreams.github.io/streamsx.messagehub/) | Streams アプリケーションが MessageHub で作業できるようにします。			     |
| [Messaging ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://ibmstreams.github.io/streamsx.messaging/)   |  	よく使用されるメッセージング・システム (Kafka、MQTT、JMS、XMS など) との対話に焦点を当てます。	<br>**注**: WebSphere MQ で JMSSource、JMSSink、XMSSource、XMSSink を使用するには、開発環境で以下の手順を実行します。 <br>1. [GitHub 上の IBMStreams ![外部リンク・アイコン ](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://github.com/IBMStreams){:new_window} にアクセスし、開発環境に Messaging Toolkit (com.ibm.streamsx.messaging) バージョン 3.0.0 以降をダウンロードします。<br>2. バージョン 5.1.0 以降のツールキットを使用して、アプリケーションをビルドします。<br>3. 必要な `.bindings` ファイルをアプリケーションの `/etc` ディレクトリーに入れて、それを {{site.data.keyword.streamsshort}} アプリケーション・バンドルに組み込みます。	    |
| [Mining ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://ibm.co/2y3i5au)              	   	            |  モデルを適用してデータ・ストリームのマイニングを行うために使用できる演算子が含まれています。 <br> **制約事項:** このツールキットは、RHEL 7 環境または同等の CentOS バージョンでアプリケーション・バンドルをコンパイルする必要があるため、[v2 サービス・プラン](/docs/services/StreamingAnalytics/service_plans.html)を使用している場合はサポートされません。 	     |
| [RabbitMQ ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://ibmstreams.github.io/streamsx.rabbitmq/)     |  Streams アプリケーションが Rabbit MQ からメッセージを読み取って送信できるようにする演算子を提供します。  |
| [R-project ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://ibm.co/2h7D9lu)          	   	              |   RScript 演算子が含まれています。これを使用して R コマンドを実行し、複雑なデータ・マイニング・アルゴリズムを適用して、データ・ストリーム内の対象パターンを検出できます。			     |
| [Topology ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.topology/)      | {{site.data.keyword.Bluemix_notm}} プラットフォームおよび {{site.data.keyword.streamsshort}} で {{site.data.keyword.streaminganalyticsshort}} サービス用の Python ストリーミング・アプリケーションをビルドする方法を説明します。|
| [DPS ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.dps/) |	 1 つ以上のマシン上で処理エレメント (PE) を実行している複数のアプリケーションが、アプリケーション固有の状態情報を共有できるようにします。<br>**制約事項:** REDIS のみがデータベース・バックエンドとしてサポートされます。	| 	 	 	
| [Geospatial ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://ibm.co/2h9x0VR) 	     |	位置データの処理および索引付けを効率的に行えるようにする演算子と関数が含まれています。<br>**制約事項:** 共有マップ・モードを使用する演算子はサポートされません (共有マップ・モードの `MapStore`、`PointMapMatcher`)。		 |
| [TEDA ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://ibm.co/2z9DS00)	   | 	遠隔通信アプリケーションに使用される一連の汎用演算子を提供します。また、新しいファイル間 (file-to-file) アプリケーションをセットアップするためのアプリケーション・フレームワークも提供します。 [TEDA チュートリアル ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.tutorial.teda/) に従って開始します。 ツールキットのすべての演算子と関数がサポートされます。 <br>**制約事項:** アプリケーション・フレームワークはサポートされません。	 	 |
| [TimeSeries ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://ibm.co/2zEPILZ)	 	  | TimeSeries Toolkit の演算子および関数は、時系列データの条件付け、分析、およびモデル化を行います。 <br>**制約事項:** 非推奨の演算子はサポートされません。	   |
| [{{site.data.keyword.cos_short}} ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://bit.ly/2Ggp03T)	 	  | {{site.data.keyword.cos_short}} との間でのデータの読み書きに関するプリミティブ演算子とネイティブ関数を提供します。 このツールキットは、S3 互換 {{site.data.keyword.cos_short}} をサポートします。	   |

*表 1. サポートされるツールキット*

## その他のツールキットおよび演算子
{: #other_operators}

その他の演算子 (ユーザー独自のニーズのために開発されたツールキットの演算子を含む) も {{site.data.keyword.streaminganalyticsshort}} によってサポートされる場合があります。
{:shortdesc}

{{site.data.keyword.streaminganalyticsshort}} と互換性があるためには、ツールキットは以下の基準を満たしている必要があります。

1. サービス・インスタンスのアプリケーション・ノードに追加のソフトウェアをプリインストールする必要がない。
2. ツールキットに必要な構成情報を、ツールキットを使用してアプリケーション・バンドルに組み込むことができる。
