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

# Streaming Analytics での Python アプリケーションの開発
{: #t_develop_apps_python}

Python アプリケーションを {{site.data.keyword.DSX_full}} で、またはローカル側の Python 開発環境で開発し、それらのアプリケーションを {{site.data.keyword.streaminganalyticsshort}} にデプロイできるようになりました。
{:shortdesc}

以下のいずれかの方法によって、{{site.data.keyword.streaminganalyticsshort}} サービスを使用して Python アプリケーションを開発して {{site.data.keyword.Bluemix_short}} にデプロイします。


## Watson Studio での Streams Python アプリケーションの開発
{: #t_develop_python_dsx}

Python 開発環境がない場合は、{{site.data.keyword.DSX_short}} の {{site.data.keyword.streamsshort}} ノートブックを使用して、サンプル Python アプリケーションを作成するのが、最も簡単な開始方法です。 以下のノートブックには、{{site.data.keyword.DSX_short}} Python 環境で {{site.data.keyword.streaminganalyticsshort}} サービス用の単純な Python アプリケーションを作成およびデプロイするためのステップとコード・サンプルが用意されています。

* [Hello World! ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039ca9c6e8): 開始点としてシンプルな Hello World! アプリケーションを作成し、そのアプリケーションを {{site.data.keyword.streaminganalyticsshort}} サービスのインスタンスにデプロイします。

* [Healthcare Demo ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039cad29a6): フィードからのストリーミング・データを取り込んで分析してから、ノートブックでデータを視覚化するアプリケーションを作成します。 最終的に、このアプリケーションを {{site.data.keyword.streaminganalyticsshort}} サービス・インスタンスにサブミットします。

* [Neural Net Demo ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039ca60bb7): サンプル・データ・セットを作成し、データ・モデルを作成し、ストリーミング・アプリケーションでそのモデルを使用し、ストリーミング・データを視覚化し、そのストリーミング・アプリケーションをサービスにサブミットします。

## ローカル Python 環境でのアプリケーションの開発
 {: #t_develop_python_api}

streamsx パッケージに含まれている [{{site.data.keyword.streamsshort}} Python Application API ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features) を使用すると、Python 呼び出し可能クラスまたは関数を使用してストリーム処理アプリケーションを作成できます。その後、Python Application API を使用して、アプリケーションを定義してサービスにサブミットします。

[Developing for the {{site.data.keyword.streaminganalyticsshort}} service ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html)チュートリアルのステップに従って開始します。このチュートリアルでは、ローカル Python 環境でサンプル・アプリケーションを作成し、それを {{site.data.keyword.streaminganalyticsshort}} サービスにデプロイします。

{{site.data.keyword.streamsshort}} Python アプリケーション API についてより深く知るには、[このオンライン・コース ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/courses/all/streaming-analytics-basics-python-developers/){:new_window} を視聴して、Python 開発者のための {{site.data.keyword.streaminganalyticsshort}} の基本を学習してください。
