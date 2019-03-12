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

# v1 および v2 のサービス・プラン
{: #service_plans}

{{site.data.keyword.streaminganalyticsshort}} は、サービスのセキュリティーと可用性の点で有利な Kubernetes コンテナー・ベース・インフラストラクチャーで稼働するようになりました。
{:shortdesc}

v2 のサービス・プランを使用して、この新しいコンテナー・ベース・インフラストラクチャーにアクセスできます。 お客様は、必要な作業に最適な {{site.data.keyword.streaminganalyticsshort}} プランを選択できます。


<table summary="この表は、{{site.data.keyword.streaminganalyticsshort}} サービスを作成するために使用できるサービス・プランのリストです。この表には、v1 および v2 のプラン・セットのすべてのサービス・プランがリストされており、各セットの機能のリストを示しています。">
  <tr>
    <th>サービス・プラン・セット<br></th>
    <th>プラン名<br></th>
    <th>使用可能な機能<br></th>
  </tr>
  <tr>
    <td width="15%">
    v1 サービス・プラン (非推奨)    
    </td>
    <td width="35%">
    <ul>
      <li>ライト VM</li>
      <li>エントリー VM 時間単位</li>
      <li>エントリー VM 月単位</li>
      <li>拡張 VM 時間単位</li>
      <li>拡張 VM 月単位</li>
      <li>拡張 VM サブスクリプション</li>
      <li>プレミアム VM 月単位</li>
      <li>プレミアム VM サブスクリプション</li>
    </ul>
    </td>
    <td>
      <ul>
        <li>Red Hat Enterprise Linux (RHEL) 6.5 オペレーティング・システムまたは同等の CentOS バージョンで Streams アプリケーションをコンパイルする必要があります。</li>
        <li>VM ベース・インフラストラクチャーで稼働します。</li>
        <li>v1 および v2 の REST API をサポートします。<br></li>
        <li>IAM 認証とユーザー資格情報認証の両方をサポートします。</li>
        <li>[{{site.data.keyword.streamsshort}} Quick Start Edition VM イメージ ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-linux/) をサポートします。
      </ul>    
    </td>
  </tr>
  <tr>
    <td>
    v2 サービス・プラン
    </td>
    <td>
      <ul>
        <li>ライト</li>
        <li>エントリー・コンテナー時間単位</li>
        <li>エントリー・コンテナー月単位</li>
        <li>エントリー・コンテナー・サブスクリプション</li>
        <li>拡張コンテナー時間単位</li>
        <li>拡張コンテナー月単位</li>
        <li>拡張コンテナー・サブスクリプション</li>
        <li>プレミアム・コンテナー時間単位</li>
        <li>プレミアム・コンテナー月単位</li>
        <li>プレミアム・コンテナー・サブスクリプション</li>
      </ul>
    </td>
    <td>
    <ul>
      <li>RHEL 7.x オペレーティング・システムまたは同等の CentOS バージョンで Streams アプリケーションをコンパイルする必要があります。</li>
      <li>コンテナー・ベース・インフラストラクチャーで稼働します。</li>
      <li>v2 REST API をサポートします。<br></li>
      <li>IAM 認証をサポートします。</li>
      <li>非ライト・サービス・プランのサービス・エンドポイントをサポートします。</li>
      <li>[{{site.data.keyword.streamsshort}} Quick Start Edition with Docker ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-docker/) をサポートします。</li>
    </ul>
    </td>
  </tr>
</table>

*表 1. {{site.data.keyword.streaminganalyticsshort}} v1 および v2 のサービス・プラン*

## v1 と v2 のサービス・プランの相違点

以下の機能は、v1 サービス・プランでのみサポートされています。

* [v1 REST API](https://{DomainName}/apidocs/streaming-analytics-v1)。 v2 インフラストラクチャーでは、[{{site.data.keyword.streaminganalyticsshort}} v2 REST API](https://{DomainName}/apidocs/streaming-analytics-v2) を使用する必要があります。
* NYC Traffic and Event Detection v1 サンプル・アプリケーション。 v2 コンテナー・ベース・インフラストラクチャーで {{site.data.keyword.streaminganalyticsshort}} を開始するために使用できるアプリケーションのリストについては、[サンプル・アプリケーション](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps)を参照してください。
* 一部のツールキットとの互換性。 新規のコンテナー・ベース・インフラストラクチャーと互換性があるツールキットのリストについては、[互換性があるツールキット](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-compatible_toolkits)を参照してください。

## v1 サービス・プランの VCAP_SERVICES 環境変数
{: #vcap_services}

v1 サービス・プランの {{site.data.keyword.streaminganalyticsshort}} サービス資格情報と VCAP_SERVICES 環境変数には、{{site.data.keyword.streaminganalyticsshort}} v1 REST API を使用するために必要な VCAP 情報が含まれています。 この VCAP 情報は、REST URL、サービス・インスタンス ID、バインディング ID 、および資格情報を各 {{site.data.keyword.streaminganalyticsshort}} v1 REST API に提供します。  
{:shortdesc}

 {{site.data.keyword.streaminganalyticsshort}} サービス・インスタンスをプロビジョンして {{site.data.keyword.Bluemix_notm}} でアプリケーションにバインドすると、このサービス・インスタンスの VCAP 情報は、{{site.data.keyword.Bluemix_notm}} アプリケーション環境で使用可能になります。 この情報は、VCAP_SERVICES 環境変数にあります。 バインド先の {{site.data.keyword.Bluemix_notm}} のアプリケーションを指定せずに {{site.data.keyword.streaminganalyticsshort}} サービス・インスタンスをプロビジョンした場合は、サービス資格情報が自動的に作成されます。 {{site.data.keyword.streaminganalyticsshort}} サービス資格情報は、「サービス詳細」ページからアクセスできます。


{{site.data.keyword.streaminganalyticsshort}} サービス資格情報および VCAP_SERVICES 環境変数には、以下の例に示されているような情報が含まれています。

<pre><code>
{
  "streaming-analytics": [
    {
      "name": "NYCTrafficStreaming Analytics-t6",
      "label": "streaming-analytics",
      "plan": "Standard",
      "credentials": {
        "status_path": "/jax-rs/streams/status/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "size_path": "/jax-rs/streams/size/service_instances/0fb17393-90eb-4066-96b6-df1ac9860743/service_bindings/b37b89df-b0d7-464e-b7d9-3db607a26550",
        "start_path": "/jax-rs/streams/start/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "stop_path": "/jax-rs/streams/stop/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "resources_path": "/jax-rs/resources/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "jobs_path": "/jax-rs/jobs/service_instances/9e86b8e6-f606-4a1a-9800-26b96d2bc923/service_bindings/83c9d52e-3069-46bf-a1e3-655cf95fb627",
        "rest_host": "{rest_url}",
        "rest_port": "443",
        "rest_url": "{rest_url}",
        "userid": "xxx",
        "password": "yyy"
      }
    }
  ]
}	  
</code></pre>

v1 REST API について詳しくは、[v1 REST API 資料 ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} を参照してください。

## v2 サービス・プランの VCAP_SERVICES 環境変数
{: #v2_vcap_services}

v2 サービス・プランの {{site.data.keyword.streaminganalyticsshort}} サービス資格情報と VCAP_SERVICES 環境変数には、{{site.data.keyword.streaminganalyticsshort}} v2 REST API を使用する必要がある VCAP 情報が含まれています。 この VCAP 情報は、{{site.data.keyword.streaminganalyticsshort}} v2 REST API にアクセスするための v2 REST URL、サービス ID、および資格情報を提供します。  
{:shortdesc}

v2 サービス・プランの {{site.data.keyword.streaminganalyticsshort}} サービス資格情報および VCAP_SERVICES 環境変数には、次の例にあるような情報が含まれています。

<pre><code>
    {
      "apikey": "aaaabbbbb1111222ABCDEFgh567appjurHKyY",
      "iam_apikey_description": "Auto generated apikey during resource-key operation for Instance - crn:v1:bluemix:public:streaming-analytics:us-south:a/aaabbbb120110ab123d456e78a0b78910:12e3456e-102f-47e0-9600-4313d496e07a::",
      "iam_apikey_name": "auto-generated-apikey-ab12c34d-e5d6-7890-123f-45dcece304df",
      "iam_role_crn": "crn:v1:bluemix:public:iam::::serviceRole:Manager",
      "iam_serviceid_crn": "crn:v1:bluemix:public:iam-identity::a/b123bb45670ab123d123e12d0a12345::serviceid:ServiceId-a1234b5c-678d-9f6f-bdb4-16c23935efb5",
      "v2_rest_url": "{rest_url}/v2/streaming_analytics/a1234b5c-678d-9f6f-bdb4-16c23935efb5"
    }
</code></pre>

v2 REST API について詳しくは、[v2 REST API 資料 ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window} を参照してください。
