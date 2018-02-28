---

copyright:
  years: 2015, 2018
lastupdated: "2018-02-14"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# ベータ・エントリー・プランおよびベータ・エンハンスト・プラン
{: #beta_plans}

{{site.data.keyword.streaminganalyticsshort}} サービスの新しいベータ・エントリー・プランおよびベータ・エンハンスト・プランには、既存のサービス・プランからの拡張点と相違点がいくつか含まれます。
{:shortdesc}

**新しい [{{site.data.keyword.streamsshort}} QSE for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi):** {{site.data.keyword.streamsshort}} Quick Start Edition は、{{site.data.keyword.streamsshort}} の無償の非実稼働バージョンです。ベータ・エントリー・プランおよびベータ・エンハンスト・プランを使用してアプリケーションを {{site.data.keyword.streaminganalyticsshort}} にデプロイするには、 {{site.data.keyword.streamsshort}} QSE の Red Hat Enterprise Linux (RHEL) 7 バージョンを使用してアプリケーションをコンパイルする必要があります。
[Beta Development Guide ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/streamsdev/docs/cloud-beta-devguide/) を参照して、新しい {{site.data.keyword.streaminganalyticsshort}} ベータ・プランでアプリケーションをコンパイルしてデプロイするために、Docker 環境で実行されている RHEL 7 での新しい Streams QSE の使用方法を学習します。   

**{{site.data.keyword.streaminganalyticsshort}} v2 REST API:** [{{site.data.keyword.streaminganalyticsshort}} v2 REST API ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#introduction) を使用して、サービス・インスタンスと {{site.data.keyword.streamsshort}} ジョブを管理できます。{{site.data.keyword.streaminganalyticsshort}} v2 API は、新しいベータ・プランの 1 つで作成されたサービス・インスタンスでのみサポートされます。[v1 REST API ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.bluemix.net/apidocs/220-streaming-analytics?&language=node#introduction) は、既存の {{site.data.keyword.streaminganalyticsshort}} インスタンス、および既存のサービス・プランで作成した新しいインスタンスでのみサポートされます。

**新しいスターター・アプリケーションおよびサンプル・アプリケーション:** 新しいベータ・プランは RHEL 7 上で Streams を実行する必要があるため、既存のサンプル・アプリケーションの多くは、新しいベータ・プランでは動作しません。{{site.data.keyword.streaminganalyticsshort}} では、新しいベータ・プランを素早く開始するために、[スターター・アプリケーションとサンプル・アプリケーションの新しいセット]( https://developer.ibm.com/streamsdev/docs/cloud-beta-samples/)が提供されます。

**高可用性の強化:** 整合領域を定義することで、ストリーム処理アプリケーションでのデータ損失を回避します。{{site.data.keyword.streamsshort}} は、ストリーム処理中にタプルを失わない領域の定義を可能にするオペレーターとアノテーションによって拡張されています。整合領域内のタプルは、少なくとも一度処理されます。
ベータ・エントリーまたはベータ・エンハンストの価格プランを使用すると、{{site.data.keyword.streaminganalyticsshort}} に[定義された整合領域で Streams アプリケーションを実行およびモニターできるようになりました。

新しい問題判別機能: ベータ・エントリー・プランおよびベータ・エンハンスト・プランには、アプリケーションのエラーを素早く見つけて修正するためのいくつかの機能強化が含まれています。詳しくは、[{{site.data.keyword.streaminganalyticsshort}} Console により、エラーを見つけて修正する方法が提供される (ベータ・プラン) ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")を参照してください。](https://wp.me/p4IICn-4cx)(/docs/services/StreamingAnalytics/consistentregions.html)]

**クラウドにおけるオペレーターの動作方法のモニターとタプル処理の保証:** {{site.data.keyword.streamsshort}} には {{site.data.keyword.streamsshort}} サービスの正常性を評価するためのメトリックが用意されており、パフォーマンスの問題の診断や要求のスループットの分析に役立てることができます。{{site.data.keyword.streaminganalyticsshort}} の Streams Console を使用して、[オペレーターの動作方法をモニターし、リソースの最適化を確実にする![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")ことができます。](https://wp.me/p4IICn-4bH)
