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

# Planes Beta-Entry y Beta-Enhanced
{: #beta_plans}

Los nuevos planes Beta-Entry y Beta-Enhanced del servicio de {{site.data.keyword.streaminganalyticsshort}} incluye varias mejoras y diferencias, en comparación con los planes de servicio actuales:
{:shortdesc}

**Nueva edición [{{site.data.keyword.streamsshort}} QSE for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi):** {{site.data.keyword.streamsshort}} Quick Start Edition es una versión gratuita de no producción de {{site.data.keyword.streamsshort}}. Para utilizar los planes Beta-Entry y Beta-Enhanced para desplegar aplicaciones en {{site.data.keyword.streaminganalyticsshort}}, debe compilar sus aplicaciones con Red Hat Enterprise Linux (RHEL) versión 7 de {{site.data.keyword.streamsshort}} QSE.
Consulte la [Guía de desarrollo Beta ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/streamsdev/docs/cloud-beta-devguide/) para aprender a utilizar el nuevo Streams QSE con RHEL 7, en ejecución en un entorno Docker para compilar y desplegar sus aplicaciones con los nuevos planes beta {{site.data.keyword.streaminganalyticsshort}}.   

**API REST {{site.data.keyword.streaminganalyticsshort}} v2:** puede utilizar la API REST [{{site.data.keyword.streaminganalyticsshort}} v2 ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#introduction) para gestionar las instancias de servicio y los trabajos de {{site.data.keyword.streamsshort}}. La API {{site.data.keyword.streaminganalyticsshort}} v2 solo se admite en instancias de servicio creadas con uno de los nuevos planes beta. La API REST [v1 ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://console.bluemix.net/apidocs/220-streaming-analytics?&language=node#introduction) solo se admite en instancias de {{site.data.keyword.streaminganalyticsshort}} existentes y cualquier instancia nueva que cree con los planes de servicio existentes.

**Nuevo iniciador y aplicaciones de muestra:** como los nuevos planes beta requieren ejecutar Streams en RHEL 7, muchas de las aplicaciones de muestra existentes no funcionan con los nuevos planes beta. {{site.data.keyword.streaminganalyticsshort}} proporciona un [nuevo conjunto de iniciador y aplicaciones de muestra]( https://developer.ibm.com/streamsdev/docs/cloud-beta-samples/) para que pueda empezar rápidamente con los nuevos planes beta.

**Mejoras de alta disponibilidad:** evite la pérdida de datos en aplicaciones de proceso de secuencias definiendo regiones coherentes. Se ha reforzado {{site.data.keyword.streamsshort}} con operadores y anotaciones que permiten la definición de una región que no pierde tuplas durante el proceso de secuencias. Las tuplas de una región coherente se procesan por lo menos una vez. Si utiliza los planes de precios Beta-Entry o Beta-Enhanced, puede ejecutar y supervisar aplicaciones Streams con las [regiones coherentes definidas en {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/consistentregions.html).

**Nuevas características de determinación de problemas:** los planes Beta-Entry y Beta-Enhanced incluyen varias mejoras que le ayudarán a acelerar la detección y corrección de errores en sus aplicaciones. Para obtener información detallada, consulte [La Consola de {{site.data.keyword.streaminganalyticsshort}} le ofrece más formas de detectar y corregir errores ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo").](https://wp.me/p4IICn-4cx)

**Supervisar cómo se comportan los operadores y el proceso de tupla garantizado en la nube:** {{site.data.keyword.streamsshort}} proporciona métricas para evaluar el estado de los servicios de {{site.data.keyword.streamsshort}}, facilitar el diagnóstico de problemas de rendimiento y analizar el rendimiento de solicitudes. Puede utilizar la Consola de Streams en {{site.data.keyword.streaminganalyticsshort}} para [supervisar cómo se comportan los operadores y garantizar la optimización de recursos ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo").](https://wp.me/p4IICn-4bH)
