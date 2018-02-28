---

copyright:
  years: 2015, 2018
lastupdated: "2017-12-15"

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


* {{site.data.keyword.streaminganalyticsshort}} には、クラウド内の {{site.data.keyword.streamsshort}} 開発環境およびクラウド内の Streams Studio は含まれません。 ローカル側にインストールされた {{site.data.keyword.streamsshort}} 環境でアプリケーションを開発し、それらをアプリケーション・バンドルとしてサブミットしてください。 開発環境が用意されていない場合は、[{{site.data.keyword.streamsshort}} Quick Start Edition ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/) を無料でダウンロードできます。
* 互換性を確保するために、アプリケーション・バンドルは Red Hat Enterprise Linux 6.5 環境、または同等の CentOS バージョンでコンパイルしてください。

  **注:** ベータ・エントリー・プランおよびベータ・エンハンスト・プランを使用している場合は、アプリケーション・バンドルを RHEL 7 環境または同等の CentOS バージョンでコンパイルする必要があります。互換性のある開発環境がない場合は、[{{site.data.keyword.streamsshort}} QSE for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) を使用できます。詳しくは、[ベータ・プランの資料](/docs/services/StreamingAnalytics/beta_plans.html)を参照してください。
* {{site.data.keyword.streamsshort}} 開発環境で、環境変数 `JAVA_HOME` を $STREAMS_INSTALL/java に設定してください。
