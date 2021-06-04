---

copyright:
  years: 2015, 2021
lastupdated: "2021-06-07"

subcollection: StreamingAnalytics

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Identity and Access Management authentication
{: #iam}

Access to {{site.data.keyword.streaminganalyticsshort}} service instances for users in your account is controlled by {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM). To manage your {{site.data.keyword.streaminganalyticsshort}} service, you must use an authentication token.

## Retrieving IAM access tokens

### Prerequisites

a. You must have a valid IBMid.

b. Download and install the [{{site.data.keyword.cloud_notm}} CLI ![External link icon](../../icons/launch-glyph.svg "External link icon")](/docs/cli?topic=cli-install-ibmcloud-cli#install-ibmcloud-cli){:new_window}.

### Step 1. Log into the {{site.data.keyword.cloud_notm}} CLI.

```
ibmcloud login
<enter your credentials>

<If you are part of multiple {{site.data.keyword.cloud_notm}} accounts, you'll be asked to choose an account for the current session. Also, you'll need to choose an organization and space in {{site.data.keyword.cloud_notm}}.>
```

### Step 2. Fetch the IAM access token.

```
ibmcloud iam oauth-tokens
```

Use `IAM token` for making REST API calls.
