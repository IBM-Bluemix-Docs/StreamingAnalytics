---

copyright:
  years: 2015, 2018
lastupdated: "2017-12-15"

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


* {{site.data.keyword.streaminganalyticsshort}} no incluye ningún entorno de desarrollo de {{site.data.keyword.streamsshort}} en la nube o en Streams Studio en la nube. Desarrolle las aplicaciones en un entorno {{site.data.keyword.streamsshort}} localmente y envíelas como paquetes de aplicaciones. Si no dispone de un entorno de desarrollo, puede descargar la [{{site.data.keyword.streamsshort}} Quick Start Edition ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/), de forma gratuita.
* Compile el paquete de aplicación en un entorno Red Hat Enterprise Linux 6.5, o una versión de CentOS equivalente, para garantizar la compatibilidad.

  **Nota:** si utiliza los planes Beta-Entry y Beta-Enhanced, debe compilar su paquete de aplicaciones en un entorno RHEL 7 o una versión de CentOS equivalente. Puede utilizar [{{site.data.keyword.streamsshort}} QSE for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) si no tiene un entorno de desarrollo compatible. Consulte la [documentación de planes Beta](/docs/services/StreamingAnalytics/beta_plans.html) para obtener más información.
* En el entorno de desarrollo de {{site.data.keyword.streamsshort}}, defina la variable de entorno `JAVA_HOME` en $STREAMS_INSTALL/java.
