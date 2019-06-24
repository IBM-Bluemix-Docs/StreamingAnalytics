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

# Environnement et outils de développement
{: #c_beta_tooling}


Les considérations ci-dessous s'appliquent aux outils et à l'environnement que vous utilisez pour développer vos applications pour {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}} n'inclut pas d'environnement de développement {{site.data.keyword.streamsshort}} ni Streams Studio dans le cloud. Développez vos applications dans un environnement {{site.data.keyword.streamsshort}} installé localement et soumettez-les en tant que bundle d'applications. Si vous ne disposez pas d'un environnement de développement, vous pouvez télécharger gratuitement [{{site.data.keyword.streamsshort}} Quick Start Edition avec Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) pour les [plans de service version 2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) ou, si vous utilisez des [plans de service version 1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans), vous pouvez télécharger l'[image de machine virtuelle {{site.data.keyword.streamsshort}} Quick Start Edition ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}.
* Compilez vos applications sous Red Hat Enterprise Linux (RHEL) 7.x si vous utilisez les plans de service version 2 ou avec RHEL 6.5 si vous utilisez des plans de service version 1, à l'aide de processeurs Intel.
* Dans votre environnement de développement {{site.data.keyword.streamsshort}}, pour la variable d'environnement `JAVA_HOME`, définissez $STREAMS_INSTALL/java.
