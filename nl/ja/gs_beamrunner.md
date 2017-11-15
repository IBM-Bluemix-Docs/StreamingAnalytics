---

copyright:
  years: 2015, 2017
lastupdated: "2017-10-27"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics での IBM Streams Runner for Apache Beam 
{: #gs_beamrunner}

{{site.data.keyword.streamsshort}} 開発環境が用意されている場合、ご使用の環境で Beam アプリケーションをローカルに開発してから、{{site.data.keyword.Bluemix_notm}} でそのアプリケーションを {{site.data.keyword.streaminganalyticsshort}} サービスにサブミットできるようになりました。{{site.data.keyword.streamsshort}} Runner for Apache Beam は、{{site.data.keyword.streamsshort}} 環境で Beam パイプラインを実行します。Streams Runner を使用して起動される Beam アプリケーションは、後で {{site.data.keyword.streaminganalyticsshort}} でデプロイしてモニターできる Streams Application Bundle (SAB) ファイルに変換されます。


[ サンプル・アプリケーション](/docs/services/StreamingAnalytics/c_starterapps.html)を使用して開始して、{{site.data.keyword.streaminganalyticsshort}} サービスで Beam アプリケーションをサブミットしてモニターする方法を確認します。サンプル・アプリケーションは {{site.data.keyword.streaminganalyticsshort}} コンソールからダウンロードできます。

Streams Runner が [Beam 機能マトリックス] にどのように適合するかを示す表を確認するには、[{{site.data.keyword.streamsshort}} Runner for Apache Beam の資料](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/)を参照してください。ご使用の Streams 環境に `com.ibm.streams.beam` ツールキットをインストールして、{{site.data.keyword.streaminganalyticsshort}} でサブミットしてモニターできる Beam アプリケーションを作成する方法に関する手順を確認するには、[Installing IBM Streams Runner for Apache Beam](http://bit.ly/2zFDpPr) を参照してください。

Beam プログラミングの知識がある程度あると役立ちますが、必須ではありません。[Apache Beam Web サイト](https://beam.apache.org/documentation/){:new_window}には、有益な [Apache Beam Java SDK Quickstart](https://beam.apache.org/get-started/quickstart-java/){:new_window} ページとその他の資料があります。
