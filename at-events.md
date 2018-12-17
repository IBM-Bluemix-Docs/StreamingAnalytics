---

copyright:
  years: 2016, 2018
lastupdated: "2018-11-14"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:table: .aria-labeledby="caption"}



# {{site.data.keyword.cloudaccesstrailshort}} events
{: #at_events}

Use the {{site.data.keyword.cloudaccesstrailfull}} service to track how users and applications interact with the {{site.data.keyword.streaminganalyticsshort}} service in {{site.data.keyword.Bluemix}}.
{: shortdesc}

The {{site.data.keyword.cloudaccesstrailfull_notm}} service records user-initiated activities that change the state of a service in {{site.data.keyword.Bluemix_notm}}. For more information, see the [{{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla).

<!-- You can create different sections to group events by area. -->

## List of events
{: #events}

The following table lists the actions that generate Activity Tracker events when you use the {{site.data.keyword.streaminganalyticsshort}} service:

| Action | Description |
|:-----------------|:-----------------|
| `streams.instance.start` | The `{instance_name}` instance started successfully for the following domain: `{domain_name}`. If the operation fails, the following message is displayed: The `{instance_name}` instance failed to start for the following domain: `{domain_name}`. The instance could not be started. |
| `streams.instance.stop` | The `{instance_name}` instance stopped successfully for the following domain: `{domain_name}`. If the operation fails, the following message is displayed: The `{instance_name}` instance failed to stop for the following domain: `{domain_name}`. The instance could not be stopped. |
| `streams.instance.submit_job` |  The Streams Application Manager submitted application `{application_name}` of version `{application_version}` with submission parameters: `{submission_parameters}`. |
| `streams.instance.cancel_job` | The Streams Application Manager canceled job ID `{job_id}` with parameters: `{cancel_parameters}`. |
| `streams.instance.remove_instance` | The `{instance_name}` instance was removed successfully from the following domain: `{domain_name}`. If the operation fails, the following message is returned: An error occurred removing the `{instance_name}` instance from the following domain: `{domain_name}`.  |

{: caption="Table 1. Actions that generate events" caption-side="top"}
