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

# Streaming Analytics の高可用性
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} では、アプリケーションの高可用性を実現します。 いずれかのアプリケーション・ノード ({{site.data.keyword.streamsshort}} リ
ソース) で問題が発生すると、そのノードは自動的に置き換えられ、そのノードで実行されていたジ
ョブはすべてマイグレーションされます。 インスタンスに複数のアプリケーション・ノードが含まれている場合、ジョブはマイグレーションされ、再開されるだけです。 インスタンスは、[サービス・ダッシュボード](/docs/services/StreamingAnalytics/r_service_dashboard.html)または [{{site.data.keyword.streaminganalyticsshort}} REST API ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.ng.bluemix.net/apidocs/220){:new_window} を使用してサイズ変更できます。
{:shortdesc}

このビデオは、サービス・ダッシュボードを使用してインスタンスをサイズ変更する方法を示しています。

<iframe width="560" height="315" src="https://www.youtube.com/embed/zbZ9am9UhPw?rel=0" frameborder="0" allowfullscreen>インスタンスのサイズ変更</iframe>
