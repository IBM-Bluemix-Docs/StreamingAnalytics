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


# リソース使用量
{: #resourceusage}

{{site.data.keyword.streaminganalyticsshort}} には、適切にリソースが割り振られ、適切な使用量であることを確実にするための一連の動作とポリシーがあります。

## インスタンス・リソースの表示および編集
サービス・ダッシュボードで、または v1 REST API ([v1 サービス・プランの場合](/docs/services/StreamingAnalytics/service_plans.html)) や [{{site.data.keyword.streaminganalyticsshort}} v2 REST API](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#get-a-streaming-analytics-instance) ([v2 サービス・プランの場合](/docs/services/StreamingAnalytics/service_plans.html)) を使用して、インスタンスに対して有効なリソースの数を表示および編集することができます。

## リソース割り振り
- 正常に実行されるジョブをサブミットすると、リソースは自動的にインスタンスに割り振られます。
- リソースに対して実行中のジョブがない場合、リソースはインスタンスから削除されます。 例えば、ジョブ 1 がリソース 1 で実行され、ジョブ 2 がリソース 1 とリソース 2 で実行されている 2 つのジョブがあるとします。ジョブ 2 が取り消された場合、リソース 2 が削除されても、リソース 1 はインスタンスに残ります。
- ジョブをサブミットすると、インスタンスが割り振り制限に達していなければ、このジョブは新しいリソースに配置されます。
- インスタンスが使用可能なすべてのリソースを使用している場合は、新しいジョブは既存のリソースに対してスケジュールされます。

## リソース制約

リソース割り振りと使用量を制御するために、リソース制約を使用できます。 例えば、リソース制約を使用して、2 つのジョブが 2 つの個別のリソースではなく、単一のリソースを使用するように指定できます。
