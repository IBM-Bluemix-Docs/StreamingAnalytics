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

# FAQ
{: #faq}

## Streaming Analytics サービスに登録するにはどうすればいいですか?
{: #signup notoc}  

{{site.data.keyword.streaminganalyticsshort}} サービス・プランについては、[{{site.data.keyword.Bluemix_short}} カタログ・ページ](https://console.bluemix.net/catalog/services/streaming-analytics)を参照してください。

## 自分が使用している Streaming Analytics サービスのバージョンを知るにはどうすればいいですか?
{: #version notoc}   

すべての {{site.data.keyword.streaminganalyticsshort}} サービスに、定期的に機能改良がプッシュされています。 常に最新バージョンのマネージド・サービスが使用されているので、お客様が製品バージョンやレベルを追跡する必要はありません。

## IBM によってどのようなことが管理されるのですか?
{: #ibm_manage notoc}   

IBM は、インストール、ソフトウェア・アップグレード、ドメインの作成と管理、およびハードウェア保守の処理を行います。 サービスには、1 日 24 時間 x 週 7 日対応の正常性モニタリングが含まれます。


## 利用者側で行う作業には何がありますか?  
{: #responsible notoc}

お客様は、{{site.data.keyword.streaminganalyticsshort}} サービスおよびオンプレミスの Streams のインスタンスで実行されるアプリケーションを作成し、それらが正しく機能してパフォーマンス要件を満たすようにします。 また、アプリケーション固有のモニタリングもお客様の責任となります。

## 高可用性 (HA) はサポートされますか?
{: #ha notoc}

高可用性は、IBM によって管理されます。 {{site.data.keyword.streaminganalyticsshort}} は、HA をサポートするように構成されます。 フェイルオーバーの場合には、追加のサーバー・リソースが有効になります。

## Streaming Analytics サービスではセキュリティーはどのように管理されますか?
{: #security notoc}  

セキュリティーは、IBM によって完全に管理されます。 サービスごとに資格情報が生成され、お客様に提供されます。 IBM によってセキュリティー更新が管理され、利用可能になると速やかに適用されます。

## Streaming Analytics サービスを構成する必要がありますか?  
{: #configure notoc}

サービスは、IBM によって作成され、完全に管理されます。 各サービスは、専用の一連のアプリケーション・ノードで構成されています。

## Streams アプリケーションはどのようにして開発しますか?
{: #streamsapp notoc}

[v2 サービス・プラン](/docs/services/StreamingAnalytics/service_plans.html)であれば、無料の Streams である [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-install-docker/) を使用して、ローカル側で Streams アプリケーションを開発する必要があります。[v1 サービス・プラン](/docs/services/StreamingAnalytics/service_plans.html)を使用している場合は、[{{site.data.keyword.streamsshort}} Quick Start Edition VM イメージ ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window} をダウンロードできます。

また、オンプレミスの {{site.data.keyword.streamsshort}} インストール済み環境があれば、それを使用することも可能です。 ローカルで開発してコンパイルしたアプリケーションは、その後、クラウドの
Streams サービスにバンドルとしてシームレスにデプロイできます。

しかし、クラウド内の Python アプリケーションを実行する場合は、{{site.data.keyword.streamsshort}} をオンプレミスにインストールする必要はありません。 `STREAMING\_ANALYTICS\_SERVICE` コンテキストを使用して Python アプリケーションを {{site.data.keyword.streaminganalyticsshort}} サービスにサブミットするだけです。 アプリケーションは、標準の Python 開発環境または Jupyter インタラクティブ・ノートブックで開発できますが、Python 3.5 を使用する必要があります。

アプリケーション開発の手引きについては、[{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.streaminganalyticsshort}} Development Guide ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")]( https://developer.ibm.com/streamsdev/?p=16589&post_type=doc&preview=1&_ppp=7ad76a418b) を参照してください。

## Streaming Analytics サービス・ホストに直接サインインできますか?
{: #host notoc}  

いいえ。Telnet および Secure Shell (ssh) によるサーバーへの直接ログインはサポートされていません。 Streams ホストでは、追加のソフトウェアをインストールすることも、Streams 以外のソフトウェアを実行することもできません。

## Streaming Analytics サービス上のファイル・システムにアクセスできますか?
{: #filesystem notoc}  

Streams ホスト上のファイル・システムに直接アクセスできるのは、Streams アプリケーションだけです。

Streams が他のソリューション・コンポーネントと相互作用するための仕組みが必要なソリューションのために、クラウドに対応した代替策があります。 ファイルの代わりに、他の source と sink のプロトコルを使用できます。 例えば、クラウド・ベースのデータ・ストアなどです。

## Streaming Analytics サービス・アプリケーションは、組織のエンタープライズ・データにどのようにしてアクセスできますか?
{: #access notoc}  

[{{site.data.keyword.Bluemix_notm}} Secure Gateway Service](https://console.bluemix.net/catalog/services/secure-gateway) を使用して、Streams アプリケーションをエンタープライズにセキュアに接続することができます。

## オンプレミス用の IBM Streams のすべての機能は、クラウドの Streaming Analytics サービスによってサポートされますか?
{: #features notoc}

{{site.data.keyword.streaminganalyticsshort}} サービスでサポートされない機能として、以下のものがあります。

  - ドメイン権限を必要とする、インスタンスの管理タスク。 例えば、カスタム・ホスト・タグの追加やジョブ・グループの作成などです。
  - 整合領域のチェックポイント。
  - 一部のツールキットの演算子は、サポートされていません。 詳しくは、[サポートされるツールキットおよびアダプター](/docs/services/StreamingAnalytics/compatible_toolkits.html)を参照してください。
  - Streams JMX API。

## Streaming Analytics サービスについてもっとよく知るにはどこにアクセスすればいいですか?
{: #roadmap notoc}

IBM developerWorks® の記事「[Roadmap for {{site.data.keyword.streaminganalyticsshort}} Service on {{site.data.keyword.Bluemix_notm}} ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/streamsdev/docs/roadmap-for-streaming-analytics-service-on-bluemix/)」に、サービスの詳細を知るための手引きと、役に立つブログ、デモ、および記事へのリンクがあります。
