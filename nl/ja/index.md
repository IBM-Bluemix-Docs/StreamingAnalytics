---

copyright:
  years: 2015, 2017
lastupdated: "2017-12-15"

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
* {{site.data.keyword.Bluemix_notm}} でアプリケーションを開発し、この {{site.data.keyword.streamsshort}} アプリケーションをそれに追加します。 [{{site.data.keyword.streaminganalyticsshort}} REST API ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.ng.bluemix.net/apidocs/220){:new_window} を使用してアプリケーションを制御します。

{{site.data.keyword.cloudant}} や {{site.data.keyword.messagehub}} など、他の {{site.data.keyword.Bluemix_short}} サービスとともに {{site.data.keyword.streaminganalyticsshort}} を使用します。 稼働させる方法についての例は、[他の {{site.data.keyword.Bluemix_short}} サービスと統合するためのチュートリアル](/docs/services/StreamingAnalytics/r_integrating_cloudant_rest.html){:new_window}を参照してください。

ユーザー独自のアプリケーションでさらに活用する場合は、{{site.data.keyword.streamsshort}} 開発環境を取得でき、アプリケーションをクラウド対応にする必要があります。 {{site.data.keyword.streamsshort}} 環境がない場合は、{{site.data.keyword.streamsshort}} Quick Start Edition を無料で [{{site.data.keyword.streamsshort}} 製品ページ ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/analytics/us/en/technology/stream-computing/#products) からダウンロードできます。

{{site.data.keyword.streamsshort}} アプリケーション開発について熟知していない場合は、学習を支援するリソースがあります。 詳しくは、[{{site.data.keyword.streamsshort}} Knowledge Center ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.2.0/com.ibm.streams.welcome.doc/doc/kc-homepage.html){:new_window} を参照してください。

オンプレミスで実行される SPL アプリケーションが既にある場合は、[アプリケーションをクラウド対応にする![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/streamsdev/docs/getting-spl-application-ready-cloud/){:new_window} 必要があります。

**注:** Intel プロセッサーを使用し、Red Hat Enterprise Linux (RHEL) 6.5 または同等の CentOS バージョンでアプリケーションをコンパイルする必要があります。
