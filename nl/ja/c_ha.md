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

# 高可用性および災害復旧
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} は、1 つの {{site.data.keyword.Bluemix_notm}} ロケーション (例えば、ダラス、ワシントン DC、ロンドン、フランクフルト) 内で高い可用性を持ちます。ただし、1 つの {{site.data.keyword.Bluemix_notm}} 地域の全体に影響するような潜在的な災害からの復旧には、計画と準備が必要です。
{:shortdesc}


当サービスの構成、カスタマイズ、および使用法をよく理解することが必要です。また、新しい {{site.data.keyword.Bluemix_notm}} ロケーションにおいて当サービスのインスタンスを再作成すること、および、そのロケーションにアプリケーションを再デプロイすることの準備ができている必要もあります。高可用性および災害復旧に関する {{site.data.keyword.Bluemix_notm}} での標準について詳しくは、[ダウン時間をゼロにする方法](/docs/services/overview?topic=overview-zero-downtime#zero-downtime)を参照してください。[サービス・レベル・アグリーメント](/docs/services/overview?topic=overview-zero-downtime#zero-downtime#SLAs)についての説明もご覧ください。

## 高可用性

{{site.data.keyword.streaminganalyticsshort}} では、アプリケーションの高可用性を実現します。 ユーザーのアプリケーションは Kubernetes クラスターで実行されている Docker コンテナーにデプロイされます。可用性の高いアプリケーションを作成するには、これらのコンテナーがどのようにして高可用性を確保するのかを理解する必要があります。

* アプリケーション・リソースは、サービス・プランに従って割り振られる CPU およびメモリーがあるコンテナーです。
* ハードウェアまたはソフトウェアの障害が起こっているときにコンテナーが移動することがあります。コンテナーが移動すると、処理エレメントは再始動されます。
* 計画保守中にコンテナーが移動することがあります (処理エレメントは再始動されます)。

したがって、アプリケーションを作成するときには、コンテナーがときには移動することを考慮する必要があります。さらに、以下の事項も考慮する必要があります。
* PE が再始動可能かつ再配置可能であることを確認してください。
* アプリケーションが、一部またはすべての処理エレメント (PE) がどのような順序で再始動されても問題ないようになっていることを確認してください。
* Streams アプリケーション内のソース演算子およびシンク演算子が、PE 再始動時に接続を再確立するように構成されていることを確認してください。

[{{site.data.keyword.streaminganalyticsshort}} 開発ガイド](https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/#troubleshooting)で、アプリケーションのトラブルシューティング方法を示す例を確認してください。

高可用性を実装するため、Streams アプリケーションはすべてのタプルの処理を保証できるようになっています。保証されたタプル処理を実現するために、整合領域内のすべての演算子に対して定期的にチェックポイントが設定されます。アプリケーションで障害が発生すると、すべての演算子が、最後に成功したチェックポイント状態にロールバックされます。
{{site.data.keyword.streaminganalyticsshort}} では整合領域の使用が許可されています。

### 保証されたタプル処理
一部のアプリケーションでは、ビジネス要件のため、すべてのタプルを少なくとも一度処理することが必要です。 {{site.data.keyword.streamsshort}} の拡張機能の演算子およびアノテーションを使用すると、ストリーム処理中にタプルを失うことのない領域を定義できます。整合領域内のタプルは、少なくとも一度処理されます。

整合領域内でアプリケーションの障害が検出された場合、{{site.data.keyword.streaminganalyticsshort}} は、アプリケーションを最後の整合状態 (チェックポイントとも呼ばれます) に戻して、そのポイントからタプルを再生するようにアプリケーション・データ・ソースに指示することができます。

{{site.data.keyword.streaminganalyticsshort}} では、整合領域が定義された Streams アプリケーションを実行およびモニターすることができます。{{site.data.keyword.streaminganalyticsshort}} サービスを作成すると、そのインスタンスはすでに整合領域を使用できるように構成されています。

整合領域とは、ストリーム中の定義されたポイント間にあるすべてのタプルおよび句読記号を処理することによってすべての演算子の状態が整合したものになるサブグラフです。 これによって、そのサブグラフ内ではタプルが少なくとも一度は処理されることになります。 整合領域では、現行タプルが定期的にドレーンされます。 整合領域内のすべてのタプルは、サブグラフの終わりまで順に処理されます。 領域内の各演算子について、演算子のメモリー内状態は、チェックポイント処理が行われると自動的に直列化され、保管されます。

タプル処理が保証されたアプリケーションを、Java、SPL、および Python で作成でき、これらのアプリケーションを {{site.data.keyword.streaminganalyticsshort}} にデプロイできます。

整合領域の始まりは、`@consistent` アノテーションを、それが可能な演算子に付けることで定義できます。 整合領域の範囲は {{site.data.keyword.streamsshort}} が自動的に決定しますが、領域の終了演算子は `@autonomous` アノテーションを使用して変更できます。 定義済みの整合領域は、定期的に整合状態を確立します。

Streams アプリケーションでの整合領域の使用について詳しくは、[{{site.data.keyword.streamsshort}} の資料 ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html) を参照してください。

## 災害復旧
{{site.data.keyword.streaminganalyticsshort}} は、複数の {{site.data.keyword.Bluemix_notm}} 地域で提供される GA サービスです。{{site.data.keyword.streaminganalyticsshort}} は、{{site.data.keyword.Bluemix_notm}} にはユーザー・データを保管しません。

以下の災害復旧戦略のいずれかを業務要件に基づいて選択します。
* アプリケーションへの割り込みが必要ない場合:
  1. 複数の {{site.data.keyword.Bluemix_notm}} 地域に {{site.data.keyword.streaminganalyticsshort}} のインスタンスを作成します。
  2. アプリケーションを複数の地域に送信します。


* アプリケーションへの最小限の割り込みが必要な場合:
  1. 複数の {{site.data.keyword.Bluemix_notm}} 地域に {{site.data.keyword.streaminganalyticsshort}} のインスタンスを作成します。
  2. [サービス REST API](https://ibm.co/2Gt9mB6) を使用してアプリケーションをモニターし、必要に応じて新しい地域にワークロードを動的に移します。

**注:** 各整合領域は {{site.data.keyword.Bluemix_notm}} 地域に結合されています。災害復旧シナリオでは、アプリケーション内の整合領域には何の役割もありません。
