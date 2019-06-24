---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-16"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# サービス・エンドポイントの管理
{: #manage_endpoints}

プライベート・エンドポイントを使用することで、{{site.data.keyword.Bluemix_short}} Service Endpoint は、内部 {{site.data.keyword.Bluemix_notm}} ネットワークを経由して {{site.data.keyword.streaminganalyticsshort}} サービスへの接続を有効にします。
{:shortdesc}

サービス・インスタンスにアクセスして管理するため、プライベート・エンドポイントを追加できます。

## 前提条件
{: #prereqs notoc}

以下の要件を満たしていることを確認します。
- 非ライト [v2 コンテナー・プラン](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)を使用してサービス・インスタンスを作成します。
- {{site.data.keyword.Bluemix_notm}} アカウントの[仮想経路転送 (VRF)](/docs/infrastructure/direct-link?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud) を使用可能にします。


プライベート・エンドポイントを追加するには、次のようにします。

1. 「サービスの詳細」ページで、**エンドポイントの管理**をクリックします。 サービス・インスタンスに割り当てられたパブリック・エンドポイントが表示されます。
2. **「プライベート・エンドポイントの追加」**をクリックします。 プライベート・エンドポイントがサービス・インスタンスに割り当てられます。
3. **オプション。** エンドポイント・トグルを使用して、必要に応じてエンドポイントを使用可能にしたり使用不可にしたりします。


サービス・エンドポイントについて詳しくは、[{{site.data.keyword.Bluemix_notm}} Service Endpoint の資料](/docs/services/service-endpoint?topic=service-endpoint-about#about){:new_window}を確認してください。
