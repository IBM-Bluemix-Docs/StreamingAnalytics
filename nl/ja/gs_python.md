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

# Streaming Analytics 用の Streams Python アプリケーション
{: #gettingstarted_py}

{{site.data.keyword.DSX_full}} などの Python 環境で Streams アプリケーションを作成し、それらのアプリケーションを、{{site.data.keyword.Bluemix_notm}} にデプロイされる {{site.data.keyword.streaminganalyticsshort}} インスタンスにサブミットできるようになりました。 Streams Python アプリケーションをコンパイルおよびデプロイするために、{{site.data.keyword.streamsshort}} をローカルにインストールする必要がなくなりました。

始めに、{{site.data.keyword.DSX_short}} で Jupyter ノートブックを使用してサンプルの Streams Python アプリケーションを作成し、次に、それらのアプリケーションを {{site.data.keyword.DSX_short}} からサービス・インスタンスに直接サブミットします。 詳しくは、[
{{site.data.keyword.DSX_short}} での Streams Python アプリケーションの開発](/docs/services/StreamingAnalytics/t_develop_apps_python.html#t_develop_python_dsx)を参照してください。

{{site.data.keyword.streaminganalyticsshort}} では、ローカル Python 環境からの Streams アプリケーションのデプロイもサポートされます。 Streams Python アプリケーションをローカルで開発してサービス・インスタンスにサブミットするには、streamsx パッケージに含まれている [{{site.data.keyword.streamsshort}} Python Application API ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features) を使用する必要があります。 開始するには、『[Developing for the {{site.data.keyword.streaminganalyticsshort}} service ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html)』チュートリアルのステップに従います。
