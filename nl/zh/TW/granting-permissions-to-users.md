---

copyright:
  years: 2017, 2018
lastupdated: "2018-07-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# 授與許可權給使用者

使用 {{site.data.keyword.Bluemix_notm}} 帳戶，您在您帳戶下的組織或空間會具有管理專用權，以在 {{site.data.keyword.streaminganalyticsshort}} 上執行所有作業。不過，當您將其他使用者加入到您的帳戶時，您需要管理他們的許可權，以便他們具有在您的帳戶下操作服務實例所需的專用權。

在 {{site.data.keyword.streaminganalyticsshort}} 中，對服務管理作業的存取是由下列許可權層次所控管：

|作業|必要的 {{site.data.keyword.Bluemix_notm}} 許可權|必要的 IAM 許可權|
|-----------|------------------------------|--------------------------|
|建立或刪除服務|對 {{site.data.keyword.Bluemix_notm}} 空間的開發人員角色|無|
|檢視服務儀表板|對 {{site.data.keyword.Bluemix_notm}} 空間的開發人員角色|檢視者以上|
|調整服務大小|對 {{site.data.keyword.Bluemix_notm}} 空間的開發人員角色|編輯者以上|
|使用 CF CLI 或 {{site.data.keyword.Bluemix_notm}} 使用者介面產生服務金鑰|對 {{site.data.keyword.Bluemix_notm}} 空間的開發人員角色|無|

若要將新的使用者加入您的帳戶中，請執行下列動作：

1.	登入 [{{site.data.keyword.Bluemix_notm}} 儀表板](https://console.bluemix.net)。

2.	按一下**管理 -> 帳戶 -> 使用者**。

3.	在**使用者管理**頁面中，按一下**邀請使用者**。

4.	輸入您要邀請之使用者的 IBM ID。

5.	在「存取」區段下，展開**已啟用身分及存取的服務**，然後選取下列值：

	a.	服務：選取**所有已啟用身分及存取的服務**。

	b.	地區：選取**美國南部**。

	c.	服務實例：選取**所有現行服務實例**。

	d.	角色：選擇使用者的角色。具有「檢視者」角色的成員對 {{site.data.keyword.streaminganalyticsshort}} 具有唯讀存取權。獲得指派「編輯者」以上專用權的成員可以修改 {{site.data.keyword.streaminganalyticsshort}} 服務。

6.	展開 **Cloud Foundry 存取**，然後選取您要提供使用者存取權的組織。

	a. 為您的使用者在組織層次選取一個角色。

	b.	針對地區選擇美國南部。

	c.	選取您要授與使用者存取權的空間。

	e.	選取您要指派給使用者的角色。若要檢視服務儀表板及執行例如產生服務金鑰的作業，您必須指派「開發人員」角色。
