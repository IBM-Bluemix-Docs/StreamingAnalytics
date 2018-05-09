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

# Streaming Analytics の高可用性
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} では、アプリケーションの高可用性を実現します。 いずれかのアプリケーション・ノード ({{site.data.keyword.streamsshort}} リ
ソース) で問題が発生すると、そのノードは自動的に置き換えられ、そのノードで実行されていたジ
ョブはすべてマイグレーションされます。 インスタンスに複数のアプリケーション・ノードが含まれている場合、ジョブはマイグレーションされ、再開されるだけです。 [v1 サービス・プランの場合、](/docs/services/StreamingAnalytics/service_plans.html)インスタンスは、[サービス・ダッシュボード](/docs/services/StreamingAnalytics/r_service_dashboard.html)または [{{site.data.keyword.streaminganalyticsshort}} v1 REST API ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.bluemix.net/apidocs/220){:new_window} を使用してサイズ変更できます。v2 サービス・プランの場合は、[v2 REST API ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.bluemix.net/apidocs/1939){:new_window} を使用します。
{:shortdesc}

このビデオは、サービス・ダッシュボードを使用してインスタンスをサイズ変更する方法を示しています。

<iframe width="560" height="315" src="https://www.youtube.com/embed/zbZ9am9UhPw?rel=0" frameborder="0" allowfullscreen>インスタンスのサイズ変更</iframe>

## 整合領域
一部のアプリケーションでは、ビジネス要件のため、すべてのタプルを少なくとも一度処理することが必要です。 {{site.data.keyword.streamsshort}} は、ストリーム処理中にタプルを失わない領域の定義を可能にするオペレーターとアノテーションによって拡張されています。 整合領域内のタプルは、少なくとも一度処理されます。

{{site.data.keyword.streaminganalyticsshort}} に定義されている整合領域を使用して、Streams アプリケーションを実行およびモニターすることができます。{{site.data.keyword.streaminganalyticsshort}} サービスを作成した場合、そのインスタンスは既に整合領域を使用するように構成されています。

整合領域とは、ストリーム中の定義されたポイント間にあるすべてのタプルおよび句読記号を処理することによって全オペレーターの状態が整合したものになるサブグラフです。 これによって、そのサブグラフ内ではタプルが少なくとも一度は処理されることになります。 整合領域では、現行タプルが定期的にドレーンされます。 整合領域内のすべてのタプルは、サブグラフの終わりまで順に処理されます。 領域内の各オペレーターについて、メモリー内のオペレーター状態は、チェックポイント処理が行われると自動的に直列化され、保管されます。

これで、タプル処理が保証された Java アプリケーションと SPL アプリケーションの両方を作成でき、これらのアプリケーションを {{site.data.keyword.streaminganalyticsshort}} にデプロイできるようになりました。

整合領域の始まりは、対応するオペレーターで `@consistent` アノテーションを使用して定義できます。 整合領域の範囲は {{site.data.keyword.streamsshort}} が自動的に決定しますが、領域の終了オペレーターは `@autonomous` アノテーションを使用して変更できます。 定義済みの整合領域は定期的に整合状態を確立します。

Streams アプリケーションでの整合領域の使用について詳しくは、![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン") [{{site.data.keyword.streamsshort}} の資料を参照してください。
