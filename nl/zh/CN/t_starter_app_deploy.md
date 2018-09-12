---

copyright:
  years: 2015, 2018
lastupdated: "2018-07-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# 入门教程
{: #starterapps_deploy}

Streaming Analytics 是完全受管的服务，可使您免于进行耗时的安装和管理任务，让您有更多的时间来开发流式应用程序。在此入门教程中，将其中一个 {{site.data.keyword.streaminganalyticsshort}} 入门模板应用程序推送并部署到 {{site.data.keyword.Bluemix_notm}}。
{:shortdesc}


## 开始之前
{: #prereqs}

您必须遵循以下步骤以部署入门模板应用程序：

* 注册 [{{site.data.keyword.Bluemix_notm}} 帐户 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://console.{DomainName}/registration){:new_window}
* 在 {{site.data.keyword.Bluemix_notm}} 组织中创建 {{site.data.keyword.streaminganalyticsshort}} 服务的实例。您可以直接通过 [{{site.data.keyword.Bluemix_notm}} 服务目录中的 **{{site.data.keyword.streaminganalyticsshort}}** 页面 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://console.{DomainName}/catalog/services/streaming-analytics/){:new_window} 创建实例。  
* [安装 {{site.data.keyword.Bluemix_notm}} CLI ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://console.{DomainName}/docs/cli/reference/bluemix_cli/get_started.html#getting-started)。



## 步骤 1. 创建应用程序并将其连接到服务
{: #create_connect}

1. 在 {{site.data.keyword.Bluemix_notm}} 中创建应用程序：

    a. 在 **{{site.data.keyword.Bluemix_notm}}** 菜单中，选择 **Cloud Foundry 应用程序**并单击**创建资源**。

    b. 为“事件检测”或“事件检测”V2 入门模板应用程序选择 {{site.data.keyword.sdk4node}} 运行时。

    请记住为应用程序指定的名称，稍后需要此名称。
1. 将 {{site.data.keyword.streaminganalyticsshort}} 服务实例连接到应用程序并重新编译打包应用程序。

## 步骤 2. 设置入门模板应用程序
{: #setup_app}

1. 如果使用 [V1 服务套餐](/docs/services/StreamingAnalytics/service_plans.html)，请下载[“事件检测”![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection) 入门模板应用程序。如果使用 [V2 服务套餐](/docs/services/StreamingAnalytics/service_plans.html)，请下载[“事件检测”V2 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://streams-github-samples.mybluemix.net/?get=QuickStart%2FBeta201801%2FEventDetectionV2) 入门模板应用程序。

1. 重命名目录以匹配在 {{site.data.keyword.Bluemix_notm}} 中为应用程序指定的名称。

## 步骤 3. 部署入门模板应用程序
{: #deploy_app}

1. 转至入门模板应用程序目录：
  <pre><code>cd myapp</code></pre>
  {:pre}

1. 登录到 {{site.data.keyword.Bluemix_notm}} 并在提示时设置目标组织：

  <pre><code>bx login</code></pre>
  {:pre}

1. 将应用程序推送到 {{site.data.keyword.Bluemix_notm}}：
  <pre><code>bx app push myapp</code></pre>
  {:pre}

1. 转至应用程序概述页面（可从 {{site.data.keyword.Bluemix_notm}} 仪表板访问），以验证应用程序成功启动。

1. 启动应用程序，以在浏览器中进行查看。您可以在应用程序概述页面上，找到应用程序的 URL（或“路径”）。


## 后续步骤
{: #next_steps}

既然您的应用程序正在运行，那么您可以通过 {{site.data.keyword.streaminganalyticsshort}} 控制台来监视应用程序。转至服务仪表板，选择 {{site.data.keyword.streaminganalyticsshort}} 服务并单击**启动**。
