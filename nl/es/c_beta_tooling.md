---

copyright:
  years: 2015, 2018
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Herramientas de desarrollo y entorno
{: #c_beta_tooling}


Estas consideraciones se aplican a las herramientas y al entorno que se utiliza para desarrollar aplicaciones para {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}} no incluye ningún entorno de desarrollo de {{site.data.keyword.streamsshort}} en la nube o en Streams Studio en la nube. Desarrolle las aplicaciones en un entorno {{site.data.keyword.streamsshort}} localmente y envíelas como paquetes de aplicaciones. Si no dispone de un entorno de desarrollo, puede descargar la [{{site.data.keyword.streamsshort}} Quick Start Edition con Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) para [planes de servicio de v2](/docs/services/StreamingAnalytics/service_plans.html) o si está utilizando los [planes de servicio de v1](/docs/services/StreamingAnalytics/service_plans.html), puede descargar la [{{site.data.keyword.streamsshort}} imagen de Quick Start Edition VM ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}, de forma gratuita.
* Compile sus aplicaciones en un sistema operativo Red Hat Enterprise Linux (RHEL) 7.x si está utilizando los planes de servicio de v2 o con RHEL 6.5 si está utilizando planes de servicio de v1, utilizando procesadores Intel.
* En el entorno de desarrollo de {{site.data.keyword.streamsshort}}, defina la variable de entorno `JAVA_HOME` en $STREAMS_INSTALL/java.
