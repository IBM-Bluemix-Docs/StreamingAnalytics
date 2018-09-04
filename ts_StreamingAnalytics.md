---

copyright:
  years: 2015, 2018
lastupdated: "2018-07-24"

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

# Streaming Analytics troubleshooting
{: #ts_StreamingAnalytics}

You can find the answers to common questions about how to use {{site.data.keyword.streaminganalyticsshort}} on {{site.data.keyword.Bluemix_short}}.
{:shortdesc}

## When I launch the service, I am prompted for credentials to log into the console
{: #log_in_console}

When you launch {{site.data.keyword.streaminganalyticsshort}}, you are prompted for credentials to log into the service console.
{:shortdesc}

You launch a {{site.data.keyword.streaminganalyticsshort}} service you created and instead of directly accessing the service console, you see a login page where you are prompted for credentials.
{: tsSymptoms}

There was an update in the service infrastructure and your browser cache is preventing the service from picking up the update.
{: tsCauses}

Clear your browser cache to make sure that you get the latest version of the service console.
{: tsResolve}

## My application is unhealthy
{: #app_unhealthy}

You can't run your application correctly and the health status is `unhealthy`.
{:shortdesc}

You submit an application to the service instance, the application starts but fails immediately, and the health status is `unhealthy`. The following error appears in the log file: `/lib64/libc.so.6: version GLIBC_2.14 not found`.
{: tsSymptoms}

You did not compile the application with an RHEL 7.x operating system or an equivalent CentOS version.
{: tsCauses}

You must compile your application in Red Hat Enterprise Linux (RHEL) 7.x if you are using the [v2 service plans](/docs/services/StreamingAnalytics/service_plans.html). If you're using [v1 service plans](/docs/services/StreamingAnalytics/service_plans.html), you must compile your application with RHEL 6.5 with Intel processors. Submit your application to the service instance again. You can download the [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) if you don't have a compatible development environment and you're using the v2 service plans. If you're using v1 service plans, download the  [{{site.data.keyword.streamsshort}} QSE ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window}.
{: tsResolve}

## I can't restart my application
{: #app_restart}

You can't restart your application after a service upgrade.
{:shortdesc}

You have multiple applications in your service instance and one of the applications requires a tag for one of its operators. After a service upgrade, you cannot restart your application and you reached your resource quota.
{: tsSymptoms}

A large scale pod restart- which is most often triggered by service updates- can lead to applications being unable to restart if they require special tagging, and the resource quota was already met. In some cases, large scale pod restarts can be caused by failure recovery scenarios.
{: tsCauses}

Contact IBM Support. To contact IBM Support, create a case on the [{{site.data.keyword.Bluemix_short}} Service Portal ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://watson.service-now.com/wcp){:new_window}.
{: tsResolve}
