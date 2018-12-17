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

# 管理服務端點
{: #manage_endpoints}

藉由使用內部端點，{{site.data.keyword.Bluemix_short}} 服務端點能夠促成透過內部 IBM Cloud 網路而連接 {{site.data.keyword.streaminganalyticsshort}} 服務。
{:shortdesc}

您現在可以新增內部端點來存取及管理您的服務實例。

## 必要條件
{: #prereqs notoc}

確定您滿足下列需求：
- 使用非精簡的 [v2 容器方案](/docs/services/StreamingAnalytics/service_plans.html)建立服務實例。
- 在 {{site.data.keyword.Bluemix_short}} 英國（倫敦）或德國（法蘭克福）地區建立服務實例。
- 為 {{site.data.keyword.Bluemix_short}} 帳戶啟用[虛擬路由轉遞 (VRF)](/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html#overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud)。


若要新增內部端點，請執行下列動作：

1. 在服務詳細資料頁面上，按一下**管理端點**。您可以看到指派給您服務實例的外部端點。
2. 按一下**新增內部端點**。內部端點已指派給您的服務實例。
3. **選用。**視需要使用端點切換以啟用或停用端點。


如需服務端點的相關資訊，請參閱 [{{site.data.keyword.Bluemix_short}} 服務端點文件](/docs/services/service-endpoint/getting-started.html#about){:new_window}。
