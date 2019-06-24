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


# Visión general de Streaming Analytics
{: #gettingstarted}

{{site.data.keyword.streaminganalyticsfull}} está basado en {{site.data.keyword.streamsshort}}, una plataforma analítica avanzada que se puede utilizar para introducir, analizar y correlacionar información a medida que llega desde distintos tipos de orígenes de datos en tiempo real. Cuando se crea una instancia del servicio {{site.data.keyword.streaminganalyticsshort}}, obtienen una instancia propia de
{{site.data.keyword.streamsshort}} que se ejecuta en {{site.data.keyword.Bluemix_short}}, lista para ejecutarse en las aplicaciones de {{site.data.keyword.streamsshort}}.
{:shortdesc}

Puede empezar a utilizar {{site.data.keyword.streaminganalyticsshort}} directamente ejecutando las [aplicaciones de inicio](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps_deploy){:new_window}.

Para empezar a utilizar {{site.data.keyword.streaminganalyticsshort}}, siga uno de estos métodos para enviar el paquete de aplicaciones (archivo .sab) asociado con la aplicación SPL, Java™, Python o Scala Streams:
* Utilice el botón **Enviar trabajo** de la consola de {{site.data.keyword.streaminganalyticsshort}}.
* Desarrolle una aplicación en {{site.data.keyword.Bluemix_notm}} y añádale la aplicación {{site.data.keyword.streamsshort}}. Contrólela mediante la [API REST de {{site.data.keyword.streaminganalyticsshort}} v1 ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} para [planes de servicio de v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) o la [API REST de {{site.data.keyword.streaminganalyticsshort}} v2 ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/apidocs/streaming-analytics-v2){:new_window} para los planes de servicio de v2.

Utilice {{site.data.keyword.streaminganalyticsshort}} con otros servicios, incluido {{site.data.keyword.cloudant}}. Consulte las [Guías de aprendizaje para la integración con otros servicios de {{site.data.keyword.Bluemix_short}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-tutorials){:new_window} para ver ejemplos que le ayuden a empezar.

Si desea profundizar en el uso de sus propias aplicaciones, puede obtener un entorno de desarrollo de {{site.data.keyword.streamsshort}} y debe preparar su aplicación para la nube. Si no dispone de un entorno de {{site.data.keyword.streamsshort}}, puede descargar [{{site.data.keyword.streamsshort}} Quick Start Edition con Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) para [planes de servicio de v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) o si está utilizando [planes de servicio de v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans), puede descargar la [imagen de VM de {{site.data.keyword.streamsshort}} Quick Start Edition ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}.

Si no está familiarizado con el desarrollo de aplicaciones {{site.data.keyword.streamsshort}}, hay recursos que le pueden ayudar. Para obtener más información, consulte [{{site.data.keyword.streamsshort}} Knowledge Center ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.welcome.doc/doc/kc-homepage.html){:new_window}

Si ya tiene una aplicación SPL que se ejecuta localmente, [prepare la aplicación para la nube.![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/streamsdev/docs/getting-spl-application-ready-cloud/){:new_window}

**Nota:** debe compilar sus aplicaciones en Red Hat Enterprise Linux (RHEL) 7.x si está utilizando los planes de servicio de v2 o con RHEL 6.5 si está utilizando planes de servicio de v1.
