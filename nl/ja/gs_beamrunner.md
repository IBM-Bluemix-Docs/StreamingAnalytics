---

copyright:
  years: 2015, 2019
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics での IBM Streams Runner for Apache Beam
{: #gs_beamrunner}

{{site.data.keyword.streamsshort}} 開発環境が用意されている場合、ご使用の環境で Beam アプリケーションをローカルに開発してから、{{site.data.keyword.Bluemix_notm}} でそのアプリケーションを {{site.data.keyword.streaminganalyticsshort}} サービスにサブミットできるようになりました。 {{site.data.keyword.streamsshort}} Runner for Apache Beam は、{{site.data.keyword.streamsshort}} 環境で Beam パイプラインを実行します。 Streams Runner を使用して起動される Beam アプリケーションは、後で {{site.data.keyword.streaminganalyticsshort}} でデプロイしてモニターできる Streams Application Bundle (SAB) ファイルに変換されます。


[ サンプル・アプリケーション](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps)を使用して開始して、{{site.data.keyword.streaminganalyticsshort}} サービスで Beam アプリケーションをサブミットしてモニターする方法を確認します。 サンプル・アプリケーションは {{site.data.keyword.streaminganalyticsshort}} コンソールからダウンロードできます。

[{{site.data.keyword.streamsshort}}Runner for Apache Beam の資料![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/){:new_window}をチェックし、Streams Runner の [Beam capability matrix](https://beam.apache.org/documentation/runners/capability-matrix/) への適合状況を示す表を確認してください。 ご使用の Streams 環境に `com.ibm.streams.beam` ツールキットをインストールして、{{site.data.keyword.streaminganalyticsshort}} でサブミットしてモニターできる Beam アプリケーションを作成する方法に関する手順を確認するには、[Installing IBM Streams Runner for Apache Beam ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://bit.ly/2zFDpPr){:new_window} を参照してください。

Beam プログラミングの知識がある程度あると役立ちますが、必須ではありません。[Apache Beam Web サイト ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://beam.apache.org/documentation/){:new_window} には、有益な [Apache Beam Java SDK Quickstart ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://beam.apache.org/get-started/quickstart-java/){:new_window} ページとその他の資料があります。
