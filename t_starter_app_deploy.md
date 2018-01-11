---

copyright:
  years: 2015, 2018
lastupdated: "2017-12-15"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Getting started tutorial
{: #starterapps_deploy}

Streaming Analytics is a fully managed service that frees you from time-consuming installation, administration, and management tasks, giving you more time to develop streaming applications. In this getting started tutorial you will push and deploy one of the {{site.data.keyword.streaminganalyticsshort}} starter applications to {{site.data.keyword.Bluemix_notm}}.
{:shortdesc}


## Before you begin
{: #prereqs}

Before deploying the starter apps, you must follow these steps:

* Register for an [{{site.data.keyword.Bluemix_notm}} account ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.{DomainName}/registration){:new_window}
* Create an instance of the {{site.data.keyword.streaminganalyticsshort}} service in your {{site.data.keyword.Bluemix_notm}} organization. You can create the instance directly from the [{{site.data.keyword.streaminganalyticsshort}} page in the {{site.data.keyword.Bluemix_notm}} Services Catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.{DomainName}/catalog/services/streaming-analytics/){:new_window}.  
* [Install the {{site.data.keyword.Bluemix_notm}} CLI ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.stage1.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).



## Step 1: Create app and connect app to your service
{: #create_connect}

1. Create an application in {{site.data.keyword.Bluemix_notm}}:

    a. In the {{site.data.keyword.Bluemix_notm}} menu, select **Cloud Foundry Apps** and click **Create resource**.

    b. Select your application runtime:
  	* To deploy the Event Detection starter app, create an application with {{site.data.keyword.sdk4node}} runtime.
  	* To deploy the NYC Traffic starter app, create an application with Liberty for Java™ runtime.

  Remember the name that you give your application; you will need it later on.
1. Connect the {{site.data.keyword.streaminganalyticsshort}} service instance to your application and restage the application.

## Step 2: Set up the starter application
{: #setup_app}

1. Download the [Event Detection ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection) or the [NYC Traffic ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic) starter application.

1. Rename the directory to match the name you gave your application in {{site.data.keyword.Bluemix_notm}}.

## Step 3: Deploy starter application
{: #deploy_app}

1. Go to the starter application directory:
  <pre><code>cd myapp</code></pre>
  {:pre}

1. Log in to {{site.data.keyword.Bluemix_notm}} and set your target organization when prompted:
  <pre><code>bx login</code></pre>
  {:pre}

1. Push your application to {{site.data.keyword.Bluemix_notm}}:
  <pre><code>bx app push myapp</code></pre>
  {:pre}

1. Go to your application overview page, accessible from the {{site.data.keyword.Bluemix_notm}} dashboard, to verify that your application started successfully.
1. Launch your application to see it in your browser. You can find your application's URL (or "route") on the application overview page.

## Next steps
{: #next_steps}

Now that your application is running, you can monitor the application from the {{site.data.keyword.streaminganalyticsshort}} console. Go to the service dashboard, select your {{site.data.keyword.streaminganalyticsshort}} service, and click **Launch**.
