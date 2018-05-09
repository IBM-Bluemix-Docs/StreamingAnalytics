---

copyright:
  years: 2015, 2018
lastupdated: "2018-04-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}


# 资源使用情况
{: #resourceusage}

{{site.data.keyword.streaminganalyticsshort}} 使用一系列行为和策略来确保适当的资源分配和使用情况。

## 查看和编辑实例资源
您可以在服务仪表板上查看和编辑实例的授权资源数，也可以使用 V1 REST API（适用于 [V1 服务套餐](/docs/services/StreamingAnalytics/service_plans.html)）或者 [{{site.data.keyword.streaminganalyticsshort}} V2 REST API](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#get-a-streaming-analytics-instance)（适用于 [V2 服务套餐](/docs/services/StreamingAnalytics/service_plans.html)）进行查看和编辑。

## 资源分配
- 当您提交成功运行的作业时，会将资源自动分配给实例。
- 如果资源上未运行任何作业，会将资源从实例中除去。例如，您具有两个作业，其中作业 1 正在资源 1 上运行，而作业 2 正在资源 1 和资源 2 上运行。如果取消作业 2，实例中会保留资源 1，但会除去资源 2。
- 提交作业时，如果实例未达到其分配限制，那么此作业会置于新资源中。
- 如果实例使用了其所有授权资源，那么将在现有资源上安排新作业。

## 资源约束

资源约束可用于控制资源分配和使用情况。例如，使用资源约束可指定两个作业使用单个资源而非分别位于两个资源上。
