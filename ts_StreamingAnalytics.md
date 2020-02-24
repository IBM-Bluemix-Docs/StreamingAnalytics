---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-16"

subcollection: StreamingAnalytics

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

You must compile your application in Red Hat Enterprise Linux (RHEL) 7.x with Intel processors. Submit your application to the service instance again. You can download the [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) if you don't have a compatible development environment.{: tsResolve}

## My application is unhealthy after it restarted
{: #app_restart}

Your application is unhealthy after it restarted due to system maintenance or failure recovery scenario.
{:shortdesc}

You have multiple applications in your service instance and one of the applications utilizes a tag for operator placement. After the application restarts, the resources for non-tagged operators are acquired first and consume all of your resource quota before the tagged operators can be placed.
{: tsSymptoms}

A large scale pod restart- which is most often triggered by service updates- can lead to applications being unable to restart if they require special tagging, and the resource quota was already met. In some cases, large scale pod restarts can be caused by failure recovery scenarios.
{: tsCauses}

You need to either increase your resource quota or free up some resources so the applications can acquired resources with the required tags. To increase your quota, go to the service details page and grow your instance size. To free up resources, cancel existing jobs until enough resources are freed to properly place the applications.
{: tsResolve}
