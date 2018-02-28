---

copyright:
  years: 2015, 2018
lastupdated: "2018-02-14"

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

RHEL 6.5 オペレーティング・システムまたは同等の CentOS バージョンを使用してアプリケーションをコンパイルしませんでした。
{: tsCauses}

Intel プロセッサーを使用し、Red Hat Enterprise Linux (RHEL) 6.5 オペレーティング・システムまたは同等の CentOS バージョンでアプリケーションを再コンパイルする必要があります。 アプリケーションをサービス・インスタンスに再度サブミットしてください。

**注:** ベータ・エントリー・プランおよびベータ・エンハンスト・プランを使用している場合は、アプリケーション・バンドルを RHEL 7 環境または同等の CentOS バージョンでコンパイルする必要があります。互換性のある開発環境がない場合は、[{{site.data.keyword.streamsshort}} Quick Start Edition for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) を使用できます。詳しくは、[ベータ・プランの資料](/docs/services/StreamingAnalytics/beta_plans.html)を参照してください。
{: tsResolve}
