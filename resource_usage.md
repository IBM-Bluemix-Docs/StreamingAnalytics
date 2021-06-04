---

copyright:
  years: 2015, 2021
lastupdated: "2021-06-07"

subcollection: StreamingAnalytics

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
You can view and edit the number of resources entitled to the instance on the service details page or the [{{site.data.keyword.streaminganalyticsshort}} REST API ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://{DomainName}/apidocs/streaming-analytics-v2#get-a-streaming-analytics-instance).

## Resource allocation
- Resources are automatically allocated to the instance when you submit a job that runs successfully.
- Resources are removed from the instance if no jobs are running on the resource. For example, you have two jobs where job 1 is running on resource 1 and job 2 is running on resource 1 and resource 2. If job 2 is canceled, resource 1 remains in the instance while resource 2 is removed.
- When you submit a job, this job is placed on a new resource if the instance does not reach its allocation limit.
- Once an instance is uses all resources that are entitled, new jobs are scheduled on the existing resources.

## Resource constraints

Resource constraints can be used to control resource allocation and usage. For example, using resource constraints you can specify that two jobs use a single resource instead of being separated on two resources.
