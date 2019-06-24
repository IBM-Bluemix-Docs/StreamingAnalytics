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

# Streaming Analytics の詳細
{: #about}

{{site.data.keyword.streaminganalyticsfull}} を使用して、Data in Motion (流れているデータ) に関するリアルタイム分析を、{{site.data.keyword.Bluemix_short}} アプリケーションの一部として実行することができます。
{:shortdesc}

{{site.data.keyword.streaminganalyticsshort}} を初めて使用する場合は、 [このサービスの簡単な概要 ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/streamsdev/docs/streaming-analytics-now-available-bluemix-2/){:new_window} を参照してください。

{{site.data.keyword.streaminganalyticsshort}} サービスは、クラウド内でデータをデプロイ、分析、およびモニターをするための以下の機能を提供します。

**サービスの対話式での使用およびプログラマチックな使用:**

[v1 サービス・プラン](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)を使用している場合は、[{{site.data.keyword.streaminganalyticsshort}} コンソールを使用して](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-console#console)対話式に使用することも、[{{site.data.keyword.streaminganalyticsshort}} v1 REST API ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} を使用してプログラマチックに使用することもできます。 [v2 サービス・プラン](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)の場合は、[{{site.data.keyword.streaminganalyticsshort}} v2 REST API ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/apidocs/streaming-analytics-v2)を使用します。

**SPL、Java、Scala、および Python アプリケーションのデプロイおよびモニター**

{{site.data.keyword.streamsshort}} アプリケーションは、SPL、Java、Scala、および Python で作成できます。 [これらのアプリケーションをデプロイおよびモニター](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_deploytocloud)するには、{{site.data.keyword.streaminganalyticsshort}} コンソールを使用します。

アプリケーションを SPL で作成する場合、{{site.data.keyword.streamsfull}} Processing Language (SPL) はストリーム処理アプリケーションの作成に使用されるプログラミング言語です。 ユーザー独自の SPL アプリケーションでさらに活用する場合は、{{site.data.keyword.streamsshort}} 開発環境を取得でき、SPL アプリケーションをクラウド対応にする必要があります。

{{site.data.keyword.streamsshort}} 開発環境なしで Python アプリケーションを作成およびデプロイする場合は、{{site.data.keyword.DSX_short}} のサービス・ノートブックまたは {{site.data.keyword.streamsshort}} Python API を使用します。 詳しくは、[{{site.data.keyword.streaminganalyticsshort}} 用の Python アプリケーションの開発](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_develop_apps_python)を参照してください。

後で {{site.data.keyword.streaminganalyticsshort}} サービス内のデプロイしてモニターできる Beam アプリケーションを、ご使用のローカル開発環境で Streams Runner を使用して開発することができます。 Streams Runner を使用する Beam アプリケーションについて詳しくは、{{site.data.keyword.streaminganalyticsshort}} の [IBM Streams Runner for Apache Beam ](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-gs_beamrunner) を参照してください。


**{{site.data.keyword.streamsshort}} 演算子との互換性:**

[{{site.data.keyword.streamsshort}} Processing Language (SPL) 標準ツールキット](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-compatible_toolkits)に含まれる {{site.data.keyword.streamsshort}} 演算子は、{{site.data.keyword.streaminganalyticsshort}} と互換性があります。

## Streaming Analytics の責任
{: #responsibilities notoc}

### お客様の責任
{: #clientresponsibilities notoc}

以下は、お客様の責任となります。

* {{site.data.keyword.streamsshort}} の IBM の初期構成の後での、インスタンスで実行される {{site.data.keyword.streamsshort}} ジョブのモニタリング、構成、および管理。 お客様は、インスタンスの開始および停止、ならびにインスタンスで実行されるジョブの開始および停止を柔軟に行うことができます。
* データを分析し、そこから洞察を得るための、サービスのプログラムおよびアプリケーションの必要に応じた開発。 お客様は、かかる開発されたプログラムや開発されたアプリケーションの品質およびパフォーマンスについても責任を負うものとします。 プログラムは、{{site.data.keyword.streamsshort}} トポロジー・フィーチャーを使用して、SPL、Java、または他のサート対象言語で開発することができます。 {{site.data.keyword.streaminganalyticsshort}} で使用されるのと同じオペレーティング・システムで、{{site.data.keyword.streamsshort}} Developer Edition または {{site.data.keyword.streamsshort}}Quick Start Edition のいずれかを使用してコンパイルする必要があります。
* 予定されている非中断型または中断型のダウン時間について情報を得るための以下のリンクの定期的な確認 - [https://developer.ibm.com/bluemix/support/#status ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/bluemix/support/#status){:new_window}  
* 継続性を確保するための、すべてのデータ、メタデータ、構成ファイル、および環境パラメーターのビジネス要件に従ったバックアップ。
* あらゆるタイプの不測の障害が発生した場合に継続性を確保するための、データ、メタデータ、構成ファイル、および環境パラメーターのバックアップからの復元。 障害には、データセンターや POD の障害、サーバー障害またはハード・ディスク障害、ソフトウェア障害などが含まれますが、これに限定されません。

### IBM の責任
{: #ibmresponsibilities notoc}

{{site.data.keyword.streaminganalyticsfull}} の一部として、IBM は以下を行います。

* お客様のインスタンスのサーバー、ストレージおよびネットワーキング・インフラストラクチャーの提供および管理。
* 選択されたリソース数での {{site.data.keyword.streamsshort}} の初期構成の提供。
* 保護および分離のための、インターネットに面している、内部ファイアウォールのインフラストラクチャーの提供および管理。
* {{site.data.keyword.streaminganalyticsshort}} 上の以下のコンポーネントのモニターおよび管理。
	* ネットワーク・コンポーネント
	* サーバーおよびそれぞれのローカル・ストレージ
	* インフラストラクチャー・オペレーティング・システム
	* {{site.data.keyword.streamsshort}} の管理サービス
	* {{site.data.keyword.streamsshort}} インスタンス
* インフラストラクチャー・オペレーティング・システムおよび {{site.data.keyword.streamsshort}} 用の適切なセキュリティー・パッチを含む、保守パッチの提供。
* システムのダウン時間を必要としない定期保守 (「非中断型」保守) および多少のシステムのダウン時間やリスタートが必要になる可能性のある保守 (「中断型」保守) の実行。[https://developer.ibm.com/bluemix/support/#status ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/bluemix/support/#status){:new_window} で公開されている予定時刻に実行されます。
* 定期保守時間に変更がある場合の、適宜通知のポスト。
