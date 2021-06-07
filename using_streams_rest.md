---

copyright:
  years: 2015, 2021
lastupdated: "2021-06-07"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:deprecated: .deprecated}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:tip: .tip}
{:pre: .pre}

# Using the Streams REST API
{: #using_streams_rest_api}

{{site.data.keyword.streaminganalyticsfull}} is deprecated. As of July 30, 2021, 
you can't create new instances, and access to free Lite instances will be removed. 
Existing paid plan instances are supported until May 1, 2022. Any instance that still exist on that date will be stopped and deleted. 
For more information, see [End of Market](/docs/StreamingAnalytics?topic=StreamingAnalytics-end_of_market).
{: deprecated}

Do you want to gain a deeper understanding of your Streams apps running either on-premises or in the {{site.data.keyword.streaminganalyticsshort}} service on IBM Cloud? The Streams Console enables interactive monitoring of your IBM Streams installation. Moreover, the Streams REST API provides powerful programmatic access to detailed metrics for Streams instances, jobs, PEs, and more. The REST API is available wherever you can access the Streams Console. Note that the Streams REST API interacts with the underlying Streams infrastructure and is different than the {{site.data.keyword.streaminganalyticsshort}} REST API. To learn about {{site.data.keyword.streaminganalyticsshort}} REST API, see the [{{site.data.keyword.streaminganalyticsshort}} v2 - IBM Cloud API Docs](https://ibm.co/2Gt9mB6).

This article is an introduction to the Streams REST API for both IBM Streams on-premise and {{site.data.keyword.streaminganalyticsshort}} in the cloud.

## Prerequisites
{: #prerequisites}

To follow the steps described in this article, you must have an IBM Streams installation or a {{site.data.keyword.streaminganalyticsshort}} service on IBM Cloud:

- To get an IBM Streams on-premise installation, you can use the [IBM Streams Quick Start Edition (QSE)](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/).
- To get a {{site.data.keyword.streaminganalyticsshort}} service, go to [IBM Cloud catalog](https://cloud.ibm.com/catalog/services/streaming-analytics) and create an instance.

If you use the {{site.data.keyword.streaminganalyticsshort}} service, follow these steps:

1.  Add the {{site.data.keyword.streaminganalyticsshort}} service credentials:
    1.  In the {{site.data.keyword.streaminganalyticsshort}} service dashboard, navigate to the **Service credentials** section and click **New credential**.
    2.  Name your service credential and click **Add**. The service credential is generated:

        ```
        {
          "apikey": "[your_api_key]",
          "iam_apikey_description": "Auto generated apikey during resource-key operation for Instance - crn:v1:staging:public:streaming-analytics:us-south:a/[instanceId]",
          "iam_apikey_name": "auto-generated-apikey-",
          "iam_role_crn": "crn:v1:bluemix:public:iam::::serviceRole:Manager",
          "iam_serviceid_crn": "crn:v1:staging:public:iam-identity:[iam_identity]::serviceid:[serviceId]",
          "v2_rest_url": "https://[host]/v2/streaming_analytics/[instanceId]"
        }
        ```
        {:pre}

    3.  Copy the value of the `apikey` parameter.

- Generate an [IBM Cloud IAM access token](https://cloud.ibm.com/docs/account?topic=account-iamtoken_from_apikey) using the value of the `apikey` parameter in the service credentials. To work with the Streams REST API, authenticate your {{site.data.keyword.streaminganalyticsshort}} service by including the IAM access token in the Authorization header of your API requests.

## Getting the URI to access the Streams REST API
{: #getting_urI}

Let’s start by getting the URI to access the Streams URI, to then dig into other REST calls from there. You can get the REST API URI:

- If you use the IBM Streams Quick Start Edition:
    1.  Open the Streams Console located in the Desktop of the QSE host. The Streams Console opens in a URI with the following structure: `https://[host]/streams/domain/console[#anchor]`. The `[host]` variable might include a port number, and the [#anchor] variable might not be included.
    2.  Change this URI to `https://[host]/streams/rest/instances` and open it in a browser window to access the Streams REST API.
    3.  Enter your Streams username and password. The default for the Streams QSE is `streamsadmin / passw0rd`.
- If you are using the {{site.data.keyword.streaminganalyticsshort}} service:
    1.  Go to the service REST API URL by copying the value of the v2_rest_url parameter in a browser window. This parameter is part of the service credentials. The {{site.data.keyword.streaminganalyticsshort}} instance information is displays in a JavaScript Object Notation (JSON) payload.

        ```
        {
          "role": "Manager",
          "jobs": "https://[host]/v2/streaming_analytics/[instanceId]/jobs",
          "documentation": "https://[host]/docs/StreamingAnalytics",
          "enabled": true,
          "streams_self": "https://[streams_host]:[port]/streams/rest/instances/[instanceId]/",
          "job_count": 0,
          "size": 1,
          "auto_stop": true,
          "maximum": 1,
          "self": "https://[v2_rest_host]/v2/streaming_analytics/[instanceId]",
          "state": "STOPPED",
          "streams_console": "https://[streams_host]:[port]/streams/domain/console",
          "id": "[instanceId]",
          "plan": "[service_plan]",
          "minimum": 1,
          "crn": "crn:v1:staging:public:streaming-analytics:us-south:a/[iam_identity]:[instanceId]",
          "status": "stopped"
        }
        ```
        {:pre}

    2.  To access the Streams REST API, you must use the value of `streams_self` parameter corresponds to the URI that you can use to access the Streams REST API.

## Exploring the Streams REST API
{: #exploring_streams_rest}

Now that you have access to the Streams REST API, you can explore the Streams REST API by performing the following actions:

1.  Get instance information
2.  Get job information
3.  Get PE information

## Get instance information by using the Streams REST API
{: #get_instance_information}

You can use the following API call to get some general instance information that you can later use to dig further into the REST API:

```
curl --request GET \
     --url  'https://{streams_self_uri}' \ - |
     --header 'authorization: Bearer {access_token}'
```

Examples of API requests in this article use cURL commands. Note, however, that you can access the Streams REST API programmatically to proactively monitor your Streams instance, build your own custom dashboard, or store the instance state for later analysis.
{:tip .tip}

To better format the JSON payloads, find and install a JSON formatter browser extension.
{:tip .tip}

The previous API call returns the following response:

```
{
    "creationUser": "[",
    "creationTime": 1542275822213,
    "restrictedTags": [],
    "jobsSnapshot": "https://[host]:[port]/streams/rest/instances/[instanceId]/jobs/snapshot",
    "operators": "https://[host]:[port]/streams/rest/instances/[instanceId]/operators",
    "startTime": 1542275851929,
    "activeViews": "https://[host]:[port]/streams/rest/instances/[instanceId]/activeviews",
    "activeVersion": {
        "buildVersion": "20180802125400",
        "productVersion": "4.3.0.0",
        "hotFix": "20180802125400",
        "minimumOSVersion": "Red Hat Enterprise Linux Server release 7.0 (Maipo)",
        "editionName": "IBM Streams",
        "minimumOSPatchVersion": "0",
        "fullProductVersion": "4.3.0.0.20180802125400",
        "minimumOSBaseVersion": "7",
        "productName": "IBM Streams",
        "architecture": "x86_64"
    },
    "id": "[instanceId]",
    "views": "https://[host]:[port]/streams/rest/instances/[instanceId]/views",
    "pes": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes",
    "resourceAllocations": "https://[host]:[port]/streams/rest/instances/[instanceId]/resourceallocations",
    "owner": "[serviceId]",
    "restid": "[instanceId]",
    "exportedStreams": https://[host]:[port]/streams/rest/instances/[instanceId]/exportedstreams",
    "startedBy": "ServiceId-0e42969e-cba0-4c68-9d71-5f464ff4f953",
    "hosts": "https://[host]:[port]/streams/rest/instances/[instanceId]/hosts",
    "jobs": "https://[host]:[port]/streams/rest/instances/[instanceId]/jobs",
    "importedStreams": "https://[host]:[port]/streams/rest/instances/[instanceId]/importedstreams",
    "health": "healthy",
    "jobsMetricsSnapshot": "https://[host]:[port]/streams/rest/instances/[instanceId]/jobs/metricssnapshot",
    "activeServices": "https://[host]:[port]/streams/rest/instances/[instanceId]/activeservices",
    "configuredViews": "https://[host]:[port]/streams/rest/instances/[instanceId]/configuredviews",
    "domain": "https://[host]:[port]/streams/rest/domains/[domainName]",
    "self": "https://[host]:[port]/streams/rest/instances/[instanceId]",
    "peConnections": "https://[host]:[port]/streams/rest/instances/[instanceId]/peconnections",
    "operatorConnections": "https://[host]:[port]/streams/rest/instances/[instanceId]/operatorconnections",
    "resourceType": "instance",
    "status": "running"
}
```

### Get job information by using the Streams REST API
{: #get_job_information}

Now, let’s dig a little deeper and get information about all jobs in the instance. But first, make sure that you have jobs running in the instance:

1.  Go to the IBM Streams Samples Catalog and search for “{{site.data.keyword.streaminganalyticsshort}}”.
1.  Select and download a sample application.
1.  Submit the application by using the {{site.data.keyword.streaminganalyticsshort}} console or the {{site.data.keyword.streaminganalyticsshort}} REST API.

When you have jobs running in your instance, simply make the following API request:

```
curl --request GET \
     --url  'https://{streams_self_uri}/jobs ' \ - |
     --header 'authorization: Bearer {access_token}'
```

The previous API call returns the following response:

```
{
    "total": 2,
    "jobs": [
        {
            "proposedOperatorsPerResource": 8,
            "instance": "https://[host]:[port]/streams/rest/instances/[instanceId]",
            "submitParameters": [],
            "metricsSnapshot": "https://[host]:[port]/streams/rest/instances/[instanceId]/jobs/0/metricssnapshot",
            "dataPath": "/home/streamsadmin/samples/QuickStart/TradesApp/data",
            "productVersion": "4.3.0.0.20180802125400",
            "operators": "https://[host]:[port]/streams/rest/instances/[instanceId]/operators?job.restid=0",
            "topologyUpdating": false,
            "outputPath": "BuildConfig",
            "dynamicThreadingThreadCount": null,
            "activeViews": "https://[host]:[port]/streams/rest/instances/[instanceId]/activeviews?job.restid=0",
            "id": "0",
            "applicationName": "application::TradesAppCloud",
            "views": "https://[host]:[port]/streams/rest/instances/[instanceId]/views?job.restid=0",
            "pes": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes?job.restid=0",
            "resourceAllocations": "https://[host]:[port]/streams/rest/instances/[instanceId]/resourceallocations?job.restid=0",
            "applicationVersion": "1.0.0",
            "generationId": 0,
            "restid": "0",
            "startedBy": "ORZA@de.ibm.com",
            "hosts": "https://[host]:[port]/streams/rest/instances/[instanceId]/hosts?job.restid=0",
            "applicationLogTrace": "https://[host]:[port]/streams/rest/instances/[instanceId]/jobs/0/applicationlogtrace",
            "dynamicThreadingElastic": null,
            "health": "healthy",
            "productLog": https://[host]:[port]/streams/rest/instances/[instanceId]/jobs/0/productlog",
            "jobGroup": "default",
            "threadingModel": "notSpecified",
            "adlFile": "BuildConfig/application.TradesAppCloud.adl",
            "jobResourceSharing": "sameInstance",
            "submitTime": 1542288512000,
            "applicationPath": "toolkits/TradesApp",
            "checkpointPath": "/home/streamsadmin/samples/QuickStart/TradesApp/data/ckpt",
            "domain": "https://[host]:[port]/streams/rest/domains/[domainName]",
            "name": "application::TradesAppCloud_0",
            "self": "https://[host]:[port]/streams/rest/instances/[instanceId]/jobs/0",
            "fusionScheme": "automatic",
            "peConnections": "https://[host]:[port]/streams/rest/instances/[instanceId]/peconnections?job.restid=0",
            "operatorConnections": "https://[host]:[port]/streams/rest/instances/[instanceId]/operatorconnections?job.restid=0",
            "snapshot": "https://[host]:[port]/streams/rest/instances/[instanceId]/jobs/0/snapshot",
            "resourceType": "job",
            "status": "running",
            "applicationScope": "Default"
        },
        {
            "proposedOperatorsPerResource": 8,
            "instance": "https://[host]:[port]/streams/rest/instances/[instanceId]",
            "submitParameters": [
                {
                    "parameterKind": "named",
                    "composite": "com.ibm.streamsx.health.physionet::PhysionetIngestServiceMulti",
                    "defaultValue": "1",
                    "values": [
                        "1"
                    ],
                    "name": "num.patients",
                    "value": "1",
                    "required": false
                }
            ],
            "metricsSnapshot": "https://[host]:[port]/streams/rest/instances/[instanceId]/jobs/1/metricssnapshot",
            "dataPath": null,
            "productVersion": "4.3.0.0.20180802125400",
            "operators": "https://[host]:[port]/streams/rest/instances/[instanceId]/operators?job.restid=1",
            "topologyUpdating": false,
            "outputPath": "output",
            "dynamicThreadingThreadCount": null,
            "activeViews": "https://[host]:[port]/streams/rest/instances/[instanceId]/activeviews?job.restid=1",
            "id": "1",
            "applicationName": "com.ibm.streamsx.health.physionet::PhysionetIngestServiceMulti",
            "views": "https://[host]:[port]/streams/rest/instances/[instanceId]/views?job.restid=1",
            "pes": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes?job.restid=1",
            "resourceAllocations": "https://[host]:[port]/streams/rest/instances/[instanceId]/resourceallocations?job.restid=1",
            "applicationVersion": "1.0.0",
            "generationId": 0,
            "restid": "1",
            "startedBy": "ORZA@de.ibm.com",
            "hosts": "https://[host]:[port]/streams/rest/instances/[instanceId]/hosts?job.restid=1",
            "applicationLogTrace": "https://[host]:[port]/streams/rest/instances/[instanceId]/jobs/1/applicationlogtrace",
            "dynamicThreadingElastic": null,
            "health": "healthy",
            "productLog": "https://[host]:[port]/streams/rest/instances/[instanceId]/jobs/1/productlog",
            "jobGroup": "default",
            "threadingModel": "notSpecified",
            "adlFile": "output/com.ibm.streamsx.health.physionet.PhysionetIngestServiceMulti.adl",
            "jobResourceSharing": "sameInstance",
            "submitTime": 1542288896000,
            "applicationPath": "toolkits/com.ibm.streamsx.health.physionet",
            "checkpointPath": "/home/streamsadmin/health/git/streamsx.health/samples/HealthcareJupyterDemo/spl/com.ibm.streamsx.health.physionet/data/ckpt",
            "domain": "https://[host]:[port]/streams/rest/domains/[domainName]",
            "name": "com.ibm.streamsx.health.physionet::PhysionetIngestServiceMulti_1",
            "self": "https://[host]:[port]/streams/rest/instances/[instanceId]/jobs/1",
            "fusionScheme": "automatic",
            "peConnections": "https://[host]:[port]/streams/rest/instances/[instanceId]/peconnections?job.restid=1",
            "operatorConnections": "https://[host]:[port]/streams/rest/instances/[instanceId]/operatorconnections?job.restid=1",
            "snapshot": "https://[host]:[port]/streams/rest/instances/[instanceId]/jobs/1/snapshot",
            "resourceType": "job",
            "status": "constructed",
            "applicationScope": "Default"
        }
    ],
    "resourceType": "jobList"
}
```

This JSON payload provides details about the job, such as name, status, health, and more. It also provides URIs that you can use to dig in even further. Let’s follow one of these URIs to see the PE information from one of the jobs in the instance.

### Get PE information by using the Streams REST API
{: #get_pe_information}

Pick one of the jobs from the GET/jobs JSON array and navigate to the PE URI. You are now ready to make the following API call:

```
curl --request GET \
     --url  'https://{streams_self_uri}//pes?job.restid=1' \ - |
     --header 'authorization: Bearer {access_token}'
```

The previous API call returns the following response, which provides details about the PEs in a particular job:

```
{
    "total": 2,
    "pes": [
        {
            "instance": "https://[host]:[port]/streams/rest/instances/[instanceId]",
            "restartable": true,
            "metricsSnapshot": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/2/metricssnapshot",
            "relocatable": true,
            "resourceTags": [],
            "resourceAllocation": "https://[host]:[port]/streams/rest/instances/[instanceId]/resourceallocations/[resourceId]",
            "indexWithinJob": 0,
            "statusReason": "none",
            "processId": "1856",
            "operators": "https://[host]:[port]/streams/rest/instances/[instanceId]/operators?pe.restid=2",
            "requiredConnections": "connected",
            "outputPorts": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/2/outputports",
            "host": null,
            "id": "2",
            "osCapabilities": [],
            "connections": "https://[host]:[port]/streams/rest/instances/[instanceId]/peconnections?pe.restid=2",
            "launchCount": 1,
            "restid": "2",
            "currentWorkingPath": "/home/streamsuser/.streams/var/Streams.sab_DLZ-production-lite-1-720983a7-0d81-4fd8-8389-3dcffb073f20/ff94523b-1b71-49e1-9ba9-4ea50bce6027/currentWorkingDir/1",
            "consoleLog": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/2/consolelog",
            "health": "healthy",
            "productLog": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/2/productlog",
            "tracingLevel": "error",
            "optionalConnections": "connected",
            "pendingTracingLevel": null,
            "domain": "https://[host]:[port]/streams/rest/domains/[domainName]",
            "self": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/2",
            "inputPorts": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/2/inputports",
            "applicationTrace": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/2/applicationtrace",
            "metrics": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/2/metrics",
            "job": "https://[host]:[port]/streams/rest/instances/[instanceId]/jobs/1",
            "snapshot": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/2/snapshot",
            "resourceType": "pe",
            "status": "running"
        },
        {
            "instance": "https://[host]:[port]/streams/rest/instances/[instanceId]",
            "restartable": true,
            "metricsSnapshot": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/3/metricssnapshot",
            "relocatable": true,
            "resourceTags": [],
            "resourceAllocation": "https://[host]:[port]/streams/rest/instances/[instanceId]/resourceallocations/[resourceId]",
            "indexWithinJob": 1,
            "statusReason": "none",
            "processId": "1855",
            "operators": "https://[host]:[port]/streams/rest/instances/[instanceId]/operators?pe.restid=3",
            "requiredConnections": "connected",
            "outputPorts": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/3/outputports",
            "host": null,
            "id": "3",
            "osCapabilities": [],
            "connections": "https://[host]:[port]/streams/rest/instances/[instanceId]/peconnections?pe.restid=3",
            "launchCount": 1,
            "restid": "3",
            "currentWorkingPath": "",
            "consoleLog": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/3/consolelog",
            "health": "healthy",
            "productLog": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/3/productlog",
            "tracingLevel": "error",
            "optionalConnections": "connected",
            "pendingTracingLevel": null,
            "domain": "https://[host]:[port]/streams/rest/domains/[domainName]",
            "self": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/3",
            "inputPorts": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/3/inputports",
            "applicationTrace": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/3/applicationtrace",
            "metrics": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/3/metrics",
            "job": "https://[host]:[port]/streams/rest/instances/[instanceId]/jobs/1",
            "snapshot": "https://[host]:[port]/streams/rest/instances/[instanceId]/pes/3/snapshot",
            "resourceType": "pe",
            "status": "running"
        }
    ],
    "resourceType": "peList"
}
```

## Conclusion
{: #conclusion}

You have just scratched the surface of the information you can get by using the Streams REST API. Dig into the other URIs inside the JSON payloads to get even more details. It is also easy to access REST APIs programmatically, even from Streams itself. With programmatic access, you can proactively monitor your Streams instance, build your own custom dashboard, or store the instance state for later analysis.

- Programmatically monitoring the REST API allows you to quickly diagnose and resolve Streams state anomalies. It also provides reassurance when everything is working correctly.
- To easily access metrics not provided by the Streams console, you can make a custom dashboard view from the Streams REST API metrics.
- Persisting snapshots of the Streams REST API over time provides historical insight that you can use to pinpoint unexpected Streams state changes.
- Using the REST API, you can now monitor your Streams instances both on-premise and in the cloud using the same REST interface.

