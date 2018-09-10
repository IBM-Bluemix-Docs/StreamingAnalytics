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


# Streaming Analytics の概要
{: #gettingstarted}

{{site.data.keyword.streaminganalyticsfull}} では {{site.data.keyword.streamsshort}} を採用しています。これは、タイプが異なるデータ・ソースから到着する情報をリアルタイムで取り込み、分析し、相互に関連付けるために使用できる、高機能の分析プラットフォームです。 {{site.data.keyword.streaminganalyticsshort}} サービスのインスタンスを作成すると、{{site.data.keyword.Bluemix_short}} 内で稼働する {{site.data.keyword.streamsshort}} のユーザー独自のインスタンスが得られ、{{site.data.keyword.streamsshort}} アプリケーションを実行する準備が整います。
{:shortdesc}

[スターター・アプリケーション](/docs/services/StreamingAnalytics/t_starter_app_deploy.html){:new_window}を実行することで、すぐに {{site.data.keyword.streaminganalyticsshort}} を開始できます。

{{site.data.keyword.streaminganalyticsshort}} の使用を開始するには、以下のいずれかの方法を使用して、 SPL、Java™、Python、または Scala Streams アプリケーションに関連付けられているアプリケーション・バンドル (.sab ファイル) をサブミットします。
* {{site.data.keyword.streaminganalyticsshort}} コンソールで**「ジョブのサブミット (Submit Job)」**ボタンを使用します。
* {{site.data.keyword.Bluemix_notm}} でアプリケーションを開発し、この {{site.data.keyword.streamsshort}} アプリケーションをそれに追加します。 アプリケーションの制御には、[{{site.data.keyword.streaminganalyticsshort}} v1 REST API ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.bluemix.net/apidocs/streaming-analytics-v1){:new_window} ([v1 サービス・プランの場合](/docs/services/StreamingAnalytics/service_plans.html))、または [{{site.data.keyword.streaminganalyticsshort}} v2 REST API ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.bluemix.net/apidocs/streaming-analytics-v2){:new_window} (v2 サービス・プランの場合) を使用します。

{{site.data.keyword.streaminganalyticsshort}} を {{site.data.keyword.cloudant}} など、他のサービスと一緒に使用します。 稼働させる方法についての例は、[他の {{site.data.keyword.Bluemix_short}} サービスと統合するためのチュートリアル](/docs/services/StreamingAnalytics/r_integrating_cloudant_rest.html){:new_window}を参照してください。

ユーザー独自のアプリケーションでさらに活用する場合は、{{site.data.keyword.streamsshort}} 開発環境を取得でき、アプリケーションをクラウド対応にする必要があります。 {{site.data.keyword.streamsshort}} 環境がない場合、[v2 サービス・プラン](/docs/services/StreamingAnalytics/service_plans.html)であれば [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) を、[v1サービス・プラン](/docs/services/StreamingAnalytics/service_plans.html)を使用しているのであれば [{{site.data.keyword.streamsshort}} Quick Start Edition VM イメージ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window} をダウンロードできます。

{{site.data.keyword.streamsshort}} アプリケーション開発について熟知していない場合は、学習を支援するリソースがあります。 詳しくは、[{{site.data.keyword.streamsshort}} Knowledge Center ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.2.1/com.ibm.streams.welcome.doc/doc/kc-homepage.html){:new_window} を参照してください。

オンプレミスで実行される SPL アプリケーションが既にある場合は、[アプリケーションをクラウド対応にする![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/streamsdev/docs/getting-spl-application-ready-cloud/){:new_window} 必要があります。

**注:** アプリケーションを Red Hat Enterprise Linux (RHEL) 7.x (v2 サービス・プランを使用している場合) または RHEL 6.5 (v1 サービス・プランを使用している場合) でコンパイルする必要があります。
