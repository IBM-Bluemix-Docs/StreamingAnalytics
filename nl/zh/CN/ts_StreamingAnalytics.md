---

copyright:
  years: 2015, 2018
lastupdated: "2018-02-14"

---

<!-- Attribute definitions -->
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics 故障诊断
{: #ts_StreamingAnalytics}

您可以找到有关如何在 {{site.data.keyword.Bluemix_short}} 上使用 {{site.data.keyword.streaminganalyticsshort}} 的常见问题的答案。
{:shortdesc}

## 启动服务时，系统提示需要凭证才能登录控制台
{: #log_in_console}

启动 {{site.data.keyword.streaminganalyticsshort}} 时，系统提示需要凭证才能登录服务控制台。
{:shortdesc}

如果启动之前创建的 {{site.data.keyword.streaminganalyticsshort}} 服务，而不是直接访问服务控制台，那么您将看到登录页面，提示您输入凭证。
{: tsSymptoms}

服务基础架构已经更新，但是您的浏览器高速缓存阻止服务选择该更新。
{: tsCauses}

请清除浏览器高速缓存，以确保获取最新的服务控制台版本。
{: tsResolve}

## 我的应用程序运行状况异常
{: #app_unhealthy}

无法正确运行应用程序，运行状况状态为 `unhealthy`。
{:shortdesc}

将应用程序提交给服务实例，应用程序启动，但马上出现故障，运行状况状态为 `unhealthy`。日志文件中出现以下错误：`/lib64/libc.so.6: version GLIBC_2.14 not found`。
{: tsSymptoms}

编译应用程序所使用的不是 RHEL 6.5 操作系统或等同的 CentOS 版本。
{: tsCauses}

必须使用 Red Hat Enterprise Linux (RHEL) 6.5 操作系统或等同的 CentOS 版本，使用 Intel 处理器，重新编译应用程序。重新向服务实例提交应用程序。


**注：**如果使用 Beta-Entry 和 Beta-Enhanced 套餐，那么必须在 RHEL 7 环境或同等 CentOS 版本中编译应用程序捆绑软件。如果不具有可编译的开发环境，您可以使用 [{{site.data.keyword.streamsshort}} Quick Start Edition for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi)。请查看 [Beta 套餐文档](/docs/services/StreamingAnalytics/beta_plans.html)以了解详细信息。
{: tsResolve}
