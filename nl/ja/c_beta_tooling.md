---

copyright:
  years: 2015, 2018
lastupdated: "2018-07-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# 開発ツールおよび環境
{: #c_beta_tooling}


{{site.data.keyword.streaminganalyticsshort}} 用のアプリケーションの開発に使用されるツールおよび環境には、以下の考慮事項が適用されます。
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}} には、クラウド内の {{site.data.keyword.streamsshort}} 開発環境およびクラウド内の Streams Studio は含まれません。 ローカル側にインストールされた {{site.data.keyword.streamsshort}} 環境でアプリケーションを開発し、それらをアプリケーション・バンドルとしてサブミットしてください。 開発環境がない場合、[v2 サービス・プラン](/docs/services/StreamingAnalytics/service_plans.html)であれば [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) を、[v1 サービス・プラン](/docs/services/StreamingAnalytics/service_plans.html)を使用しているのであれば [{{site.data.keyword.streamsshort}} Quick Start Edition VM イメージ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window} を無料でダウンロードできます。
* Intel プロセッサーを使用して、アプリケーションを Red Hat Enterprise Linux (RHEL) 7.x (v2 サービス・プランを使用している場合) または RHEL 6.5 (v1 サービス・プランを使用している場合) でコンパイルします。
* {{site.data.keyword.streamsshort}} 開発環境で、環境変数 `JAVA_HOME` を $STREAMS_INSTALL/java に設定してください。
