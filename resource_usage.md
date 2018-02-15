---

copyright:
  years: 2015, 2018
lastupdated: "2018-02-14"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}


# Resource usage
{: #resourceusage}

{{site.data.keyword.streaminganalyticsshort}} has a series of behaviors and policies to ensure appropriate resource allocation and usage.

## Viewing and editing instance resources
You can view and edit the number of resources entitled to the instance on the service dashboard or using the [{{site.data.keyword.streaminganalyticsshort}} v2 REST API](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#get-a-streaming-analytics-instance).

## Resource allocation
- Resources are automatically allocated to the instance when you submit a job that runs successfully.
- Resources are removed from the instance if there are no jobs running on the resource. For example, you have two jobs where job 1 is running on resource 1 and job 2 is running on resource 1 and resource 2. If job 2 is canceled, resource 1 remains in the instance while resource 2 is removed.
- When you submit a job, this job is placed on a new resource if the instance has not reached its allocation limit.
- Once an instance is using all its entitled resources, new jobs are scheduled on the existing resources.

## Resource constraints

Resource constraints can be used to control resource allocation and usage. For example, using resource constraints you can specify that two jobs use a single resource instead of being separated on two resources.
