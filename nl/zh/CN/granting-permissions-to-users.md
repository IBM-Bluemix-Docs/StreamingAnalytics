---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# 授予用户权限

只要有 {{site.data.keyword.Bluemix_notm}} 帐户，那么您对帐户下的组织或空间就具有管理权限，就可以对 {{site.data.keyword.streaminganalyticsshort}} 执行所有操作。但是，当您将其他用户载入您的账户时，您需要管理他们的权限，使其获得在您帐户下操作服务实例所需的权限。

在 {{site.data.keyword.streaminganalyticsshort}} 中，服务管理操作的访问权由以下权限级别管理：

| 操作 | 需要 {{site.data.keyword.Bluemix_notm}} 权限| 需要 IAM 权限|
|-----------|------------------------------|--------------------------|
| 创建或删除服务| {{site.data.keyword.Bluemix_notm}} 空间的开发者角色| 无|
| 查看服务仪表板| {{site.data.keyword.Bluemix_notm}} 空间的开发者角色| 查看者和以上权限|
| 调整服务大小| {{site.data.keyword.Bluemix_notm}} 空间的开发者角色| 编辑者和以上权限|
| 使用 CF CLI 或 {{site.data.keyword.Bluemix_notm}} UI 生成服务密钥| {{site.data.keyword.Bluemix_notm}} 空间的开发者角色| 无|

要将新用户载入您的帐户：

1.	登录 [{{site.data.keyword.Bluemix_notm}} 仪表板](https://console.bluemix.net)。

2.	单击**管理 -> 帐户 -> 用户**。

3.	在“用户”管理页面中，单击**邀请用户**。

4.	输入要邀请的用户的 IBM 标识。

5.	在“访问权”部分，展开**启用“身份和访问权”的服务**并选择以下值：

	a.	服务：选择**所有启用“身份和访问权”的服务**。

	b.	区域：选择**美国南部**。

	c.	服务实例：选择**所有当前服务实例**。

	d.	角色：选择用户角色。具有“查看者”角色的成员对 {{site.data.keyword.streaminganalyticsshort}} 有只读访问权。授予“编辑者”和以上权限的成员可以修改
{{site.data.keyword.streaminganalyticsshort}} 服务。

6.	展开 **Cloud Foundry 访问权**，选择要授予用户访问权的组织。

	a. 在组织级别，选择用户角色。

	b.	地区选择美国南部。

	c.	选择要授予用户访问权的空间。

	e.	选择要分配给用户的角色。如果要查看服务仪表板，要执行如生成服务密钥等任务，那么必须分配“开发者”角色。
