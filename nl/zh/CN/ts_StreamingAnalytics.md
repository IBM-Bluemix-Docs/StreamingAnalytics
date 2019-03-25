---

copyright:
  years: 2015, 2019
lastupdated: "2018-09-04"

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

启动已创建的 {{site.data.keyword.streaminganalyticsshort}} 服务，而不是直接访问服务控制台，这样您将看到登录页面，其中系统将提示您输入凭证。
{: tsSymptoms}

服务基础架构中有更新，但是您的浏览器高速缓存阻止服务获取该更新。
{: tsCauses}

请清除浏览器高速缓存，以确保获取最新的服务控制台版本。
{: tsResolve}

## 我的应用程序运行状况异常
{: #app_unhealthy}

无法正确运行应用程序，运行状况状态为 `unhealthy`。
{:shortdesc}

将应用程序提交给服务实例，应用程序启动，但马上出现故障，运行状况状态为 `unhealthy`。日志文件中出现以下错误：`/lib64/libc.so.6: version GLIBC_2.14 not found`。
{: tsSymptoms}

您未使用 RHEL 7.x 操作系统或等同的 CentOS 版本来编译应用程序。
{: tsCauses}

如果使用 [V2 服务套餐](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，那么必须以 Red Hat Enterprise Linux (RHEL) 7.x 编译应用程序。如果使用 [V1 服务套餐](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，那么必须以使用 Intel 处理器的 RHEL 6.5 编译应用程序。重新向服务实例提交应用程序。
如果没有兼容的开发环境，又要使用 V2 服务套餐，那么可以下载 [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi)。如果要使用 V1 服务套餐，请下载 [{{site.data.keyword.streamsshort}} QSE ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}。
{: tsResolve}

## 我的应用程序在重新启动后运行状况异常
{: #app_restart}

在由于系统维护或故障恢复场景而重新启动应用程序后，应用程序运行状况异常。
{:shortdesc}

您在服务实例中有多个应用程序，并且其中一个应用程序将标记用于操作程序布置。在应用程序重新启动后，首先获取未标记的操作程序的资源，并且在尚未放置标记的操作程序之前，这些资源就消耗了全部资源配额。
{: tsSymptoms}

如果应用程序需要特殊标记，并且已达到资源配额，那么大规模 pod 重新启动（通常由服务更新触发）可能导致应用程序无法重新启动。在某些情况下，故障恢复场景可能导致大规模 pod 重新启动。
{: tsCauses}

您需要增加资源配额或者释放一些资源，从而使应用程序可获取具有所需标记的资源。要增加配额，请转至服务详细信息页面并增加实例大小。要释放资源，请取消现有作业，直至释放足够的资源来正确放置应用程序。
{: tsResolve}
