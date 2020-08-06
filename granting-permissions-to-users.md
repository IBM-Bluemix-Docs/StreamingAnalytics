---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-16"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Granting permissions to users

With an {{site.data.keyword.cloud_notm}} account, you have administrative privileges in the organization or space under your account to perform all operations on {{site.data.keyword.streaminganalyticsshort}}. However, when you add other users to your account, you need to manage their permissions so that they have the required privileges to operate service instances under your account.

In {{site.data.keyword.streaminganalyticsshort}}, access to service management operations is governed by the following permission levels:

| Operation | Required {{site.data.keyword.cloud_notm}} permissions | Required IAM permissions |
|-----------|------------------------------|--------------------------|
| Create or delete a service | Developer role to the {{site.data.keyword.cloud_notm}} space | None |
| View the service details page | Developer role to the {{site.data.keyword.cloud_notm}} space | Viewer and above |
| Resize the service   | Developer role to the {{site.data.keyword.cloud_notm}} space | Editor and above |
| Generate service keys by using the CF CLI or the {{site.data.keyword.cloud_notm}} UI | Developer role to the {{site.data.keyword.cloud_notm}} space | None |

To add new users to your account:

1.	Log on to the [{{site.data.keyword.cloud_notm}} dashboard](https://{DomainName}).

2.	Click **Manage -> Access (IAM) -> Users**.

3.	In the **Users** page, click **Invite users**.

4.	Enter the IBMid of the user you want to invite.

5.	Under the Access section, expand **Identity and Access Enabled services** and select the following values:

	a.	Services: Select **All Identity and Access enabled services**.

	b.	Region: Select **US South**.

	c.	Service instance: Select **All current service instances**.

	d.	Roles: Choose a role for the user. Members with Viewer role have read-only access to {{site.data.keyword.streaminganalyticsshort}}. Members assigned Editor and above privileges can modify the {{site.data.keyword.streaminganalyticsshort}} service.

6.	Expand **Cloud Foundry access** and select the organization that you want to give the user access to.

	a. Select a role at the organization level for your user.

	b.	Choose US south for region.

	c.	Select the space that you want to grant the user access to.

	e.	Select the role that you want to assign to the user. To view the service details page and perform tasks such as generating service keys you must, assign Developer role.
