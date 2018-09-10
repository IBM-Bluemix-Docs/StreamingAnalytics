---

copyright:
  years: 2015, 2018
lastupdated: "2018-09-04"

---

<!-- Attribute definitions -->
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics のトラブルシューティング
{: #ts_StreamingAnalytics}

{{site.data.keyword.Bluemix_short}} 上の {{site.data.keyword.streaminganalyticsshort}} の使用法について、よくある質問の解答を記載します。
{:shortdesc}

## サービスを起動すると、コンソールにログインするための資格情報を求めるプロンプトが出される
{: #log_in_console}

{{site.data.keyword.streaminganalyticsshort}} を起動すると、サービス・コンソールにログインするための資格情報を求めるプロンプトが出されます。
{:shortdesc}

作成した {{site.data.keyword.streaminganalyticsshort}} サービスを起動すると、サービス・コンソールに直接アクセスせずに、ログイン・ページが表示され、そこで資格情報を求めるプロンプトが出されます。
{: tsSymptoms}

サービス・インフラストラクチャーに更新がありますが、ブラウザー・キャッシュが原因でサービスが更新を取り出せません。
{: tsCauses}

ブラウザー・キャッシュをクリアして、サービス・コンソールの最新バージョンを取得できるようにしてください。
{: tsResolve}

## アプリケーションが正常でない
{: #app_unhealthy}

アプリケーションを正常に実行できず、正常性状況が `unhealthy` です。
{:shortdesc}

アプリケーションをサービス・インスタンスにサブミットし、アプリケーションが開始しましたが、即時に失敗し、正常性状況が `unhealthy` です。 ログ・ファイルに「`/lib64/libc.so.6: version GLIBC_2.14 not found`」というエラーが表示されます。
{: tsSymptoms}

RHEL 7.x オペレーティング・システムまたは同等の CentOS バージョンを使用してアプリケーションをコンパイルしませんでした。
{: tsCauses}

[v2 サービス・プラン](/docs/services/StreamingAnalytics/service_plans.html)を使用している場合は、Red Hat Enterprise Linux (RHEL) 7.x でアプリケーションをコンパイルする必要があります。[v1 サービス・プラン](/docs/services/StreamingAnalytics/service_plans.html)を使用している場合は、Intel プロセッサーで RHEL 6.5 を使用してアプリケーションをコンパイルする必要があります。アプリケーションをサービス・インスタンスに再度サブミットしてください。 互換性のある開発環境がなく、v2 サービス・プランを使用している場合は、[{{site.data.keyword.streamsshort}}Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) をダウンロードできます。 v1 サービス・プランを使用している場合は、[{{site.data.keyword.streamsshort}} QSE ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window} をダウンロードします。
{: tsResolve}

## 再始動後、アプリケーションが正常でない
{: #app_restart}

システム保守または障害回復のシナリオのために、アプリケーションが再始動した後に問題が発生します。
{:shortdesc}

サービス・インスタンスに複数のアプリケーションがあり、アプリケーションの 1 つで演算子の配置にタグを使用しています。アプリケーションを再始動した後、タグの付いていない演算子のリソースが最初に取得され、タグ付きの演算子を配置する前にすべてのリソース割り当て量を消費します。
{: tsSymptoms}

大規模なポッドの再始動 (ほとんどの場合、サービスの更新によってトリガーされます) は、特殊なタグ付けを必要とするアプリケーションを再始動できず、リソース割り当て量が既にいっぱいになっている可能性があります。場合によっては、大規模なポッドの再始動が障害回復シナリオによって発生することがあります。
{: tsCauses}

リソース割り当て量を増やすか、リソースを解放して、アプリケーションが必要なタグを使用してリソースを取得できるようにする必要があります。割り当て量を増やすには、サービス・ダッシュボードに移動し、インスタンス・サイズを大きくします。リソースを解放するには、十分なリソースが解放されるまで既存のジョブをキャンセルし、アプリケーションを適切に配置します。
{: tsResolve}
