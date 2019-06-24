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

# 管理服務端點
{: #manage_endpoints}

藉由使用專用端點，{{site.data.keyword.Bluemix_short}} 服務端點能夠促成透過內部 {{site.data.keyword.Bluemix_notm}} 網路而連接 {{site.data.keyword.streaminganalyticsshort}} 服務。
{:shortdesc}

您現在可以新增專用端點來存取及管理您的服務實例。

## 必要條件
{: #prereqs notoc}

確定您滿足下列需求：
- 使用非精簡的 [v2 容器方案](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)建立服務實例。
- 為 {{site.data.keyword.Bluemix_notm}} 帳戶啟用[虛擬路由轉遞 (VRF)](/docs/infrastructure/direct-link?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud)。


若要新增專用端點，請執行下列動作：

1. 在服務詳細資料頁面上，按一下**管理端點**。您可以看到指派給您服務實例的公用端點。
2. 按一下**新增專用端點**。專用端點已指派給您的服務實例。
3. **選用。**視需要使用端點切換以啟用或停用端點。


如需服務端點的相關資訊，請參閱 [{{site.data.keyword.Bluemix_notm}} 服務端點文件](/docs/services/service-endpoint?topic=service-endpoint-about#about){:new_window}。
