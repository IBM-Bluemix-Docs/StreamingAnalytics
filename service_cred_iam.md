---

copyright:
  years: 2015, 2021
lastupdated: "2021-06-07"

subcollection: StreamingAnalytics

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:deprecated: .deprecated}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Identity and Access Management authentication
{: #iam}

{{site.data.keyword.streaminganalyticsfull}} is deprecated. As of July 30, 2021, 
you can't create new instances, and access to free Lite instances will be removed. 
Existing paid plan instances are supported until May 1, 2022. Any instance that still exist on that date will be stopped and deleted. 
For more information, see [End of Market](/docs/StreamingAnalytics?topic=StreamingAnalytics-end_of_market).
{: deprecated}

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
