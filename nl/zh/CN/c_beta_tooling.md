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

# 开发工具和环境
{: #c_beta_tooling}


以下注意事项适用于您用来为 {{site.data.keyword.streaminganalyticsshort}} 开发应用程序的工具和环境。
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}} 未在云中包括 {{site.data.keyword.streamsshort}} 开发环境，也未在云中包括 Streams Studio。请在本地安装的 {{site.data.keyword.streamsshort}} 环境中开发应用程序，并作为应用程序捆绑软件提交它们。如果您没有开发环境，那么可以免费下载 [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) 以使用 [V2 服务套餐](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，如果您要使用 [V1 服务套餐](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans)，那么可以免费下载 [{{site.data.keyword.streamsshort}} Quick Start Edition VM 映像 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}。
* 使用 Intel 处理器编译应用程序，如果要使用 V2 服务套餐，请以 Red Hat Enterprise Linux (RHEL) 7.x 进行编译，如果要使用 V1 服务套餐，请以 RHEL 6.5 进行编译。
* 在 {{site.data.keyword.streamsshort}} 开发环境中，将环境变量 `JAVA_HOME` 设置为 $STREAMS_INSTALL/java。
