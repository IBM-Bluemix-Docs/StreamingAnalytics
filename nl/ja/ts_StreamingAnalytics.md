---

copyright:
  years: 2015, 2018
lastupdated: "2018-04-24"

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

以前に作成した {{site.data.keyword.streaminganalyticsshort}} サービスを起動すると、サービス・コンソールに直接アクセスせずに、ログイン・ページが表示され、そこで資格情報を求めるプロンプトが出されます。
{: tsSymptoms}

サービス・インフラストラクチャーが更新されていますが、ブラウザー・キャッシュが原因でサービスが更新を取得できません。
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

Intel プロセッサーを使用して、Red Hat Enterprise Linux (RHEL) 7.x ([v2 サービス・プランを使用している場合](/docs/services/StreamingAnalytics/service_plans.html)) または RHEL 6.5 ([v1 サービス・プランを使用している場合](/docs/services/StreamingAnalytics/service_plans.html)) でアプリケーションを再コンパイルする必要があります。アプリケーションをサービス・インスタンスに再度サブミットしてください。互換性のある開発環境がなく、v2 サービス・プランを使用している場合は、[{{site.data.keyword.streamsshort}} Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) をダウンロードできます。v1 サービス・プランを使用している場合は、[{{site.data.keyword.streamsshort}} QSE ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window} をダウンロードします。
{: tsResolve}
