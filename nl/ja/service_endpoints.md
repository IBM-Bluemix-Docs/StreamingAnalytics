---

copyright:
  years: 2015, 2018
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# サービス・エンドポイントの管理
{: #manage_endpoints}

内部エンドポイントを使用することで、{{site.data.keyword.Bluemix_short}} Service Endpoint は内部の IBM Cloud ネットワークを経由して {{site.data.keyword.streaminganalyticsshort}} サービスへの接続を有効にします。
{:shortdesc}

これで内部エンドポイントを追加し、サービス・インスタンスにアクセスして管理できるようになりました。

## 前提条件
{: #prereqs notoc}

以下の要件を満たしていることを確認します。
- 非ライト [v2 コンテナー・プラン](/docs/services/StreamingAnalytics/service_plans.html)を使用してサービス・インスタンスを作成します。
- {{site.data.keyword.Bluemix_short}}英国 (ロンドン) 地域またはドイツ (フランクフルト) 地域にサービス・インスタンスを作成します。
- {{site.data.keyword.Bluemix_short}} アカウントの[仮想経路転送 (VRF)](/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud) を使用可能にします。


内部エンドポイントを追加するには、次のようにします。

1. 「サービスの詳細」ページで、**エンドポイントの管理**をクリックします。サービス・インスタンスに割り当てられた外部エンドポイントを表示できます。
2. **内部エンドポイントの追加**をクリックします。内部エンドポイントがサービス・インスタンスに割り当てられます。
3. **オプション。** エンドポイント・トグルを使用して、必要に応じてエンドポイントを使用可能にしたり使用不可にしたりします。


サービス・エンドポイントについて詳しくは、[{{site.data.keyword.Bluemix_short}} Service Endpoint の資料](/docs/services/service-endpoint/getting-started.html#about){:new_window}を確認してください。
