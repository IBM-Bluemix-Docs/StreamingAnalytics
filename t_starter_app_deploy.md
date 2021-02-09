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

# Getting started tutorial
{: #starterapps_deploy}

{{site.data.keyword.streaminganalyticsshort}} is a fully managed service that frees you from time-consuming installation, administration, and management tasks, giving you more time to develop streaming applications. In this getting started tutorial, you push and deploy one of the {{site.data.keyword.streaminganalyticsshort}} starter applications to {{site.data.keyword.cloud_notm}}.
{:shortdesc}


## Before you begin
{: #prereqs}

You must follow these steps to deploy the starter apps:

* Register for an [{{site.data.keyword.cloud_notm}} account ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/registration){:new_window}.
* Create an instance of the {{site.data.keyword.streaminganalyticsshort}} service in your {{site.data.keyword.cloud_notm}} organization. You can create the instance directly from the [**{{site.data.keyword.streaminganalyticsshort}}** offering details page in the {{site.data.keyword.cloud_notm}} catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/catalog/services/streaming-analytics/){:new_window}.  
* Download and install the [{{site.data.keyword.cloud_notm}} CLI ![External link icon](../../icons/launch-glyph.svg "External link icon")](/docs/cli?topic=cli-install-ibmcloud-cli#install-ibmcloud-cli){:new_window}.



## Step 1. Creating and connecting the app to your service
{: #create_connect}

1. Create an application in {{site.data.keyword.cloud_notm}}:

    a. Go to **Menu**>**Cloud Foundry Apps**>**Create resource** to create a resource.

    b. Select the SDK runtime for the Event Detection starter app.

    Remember the name that you give your application; you need it later on.
1. Connect the {{site.data.keyword.streaminganalyticsshort}} service instance to your application and restage the application.

## Step 2. Setting up the starter application
{: #setup_app}

1. Download the [Event Detection ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetectionV2) starter app.

1. Rename the directory to match the name you gave your application in {{site.data.keyword.cloud_notm}}.

## Step 3. Deploying starter application
{: #deploy_app}

1. Go to the starter application directory:
   ```
   cd myapp
   ```
   {:pre}

1. Log in to {{site.data.keyword.cloud_notm}} and set your target organization when prompted:
   ```
   bx login
   ```
   {:pre}

1. Push your application to {{site.data.keyword.cloud_notm}}:
   ```
   bx app push myapp
   ```
   {:pre}

1. Go to your application details page, accessible from the {{site.data.keyword.cloud_notm}} dashboard to verify that your application started successfully.
1. Launch your application to see it in your browser. You can find your application's URL (or "route") on the application details page.

## Next steps
{: #next_steps}

Now that your application is running, you can monitor the application from the {{site.data.keyword.streaminganalyticsshort}} console. Go to the service details page, select your {{site.data.keyword.streaminganalyticsshort}} service, and click **Launch**.
