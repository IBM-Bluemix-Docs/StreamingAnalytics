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
{:faq: data-hd-content-type='faq'}

# Preguntas más frecuentes
{: #faq}

## ¿Cómo me registro para el servicio de Streaming Analytics?
{: #signup notoc}
{: faq}  

Para obtener más información sobre los planes de servicio de {{site.data.keyword.streaminganalyticsshort}}, consulte el [catálogo de {{site.data.keyword.Bluemix_short}}](https://{DomainName}/catalog/services/streaming-analytics).

## ¿Qué versión del servicio de Streaming Analytics estoy utilizando?
{: #version notoc}
{: faq}   

Se envían mejoras regularmente a todos los servicios de {{site.data.keyword.streaminganalyticsshort}}. Utilice siempre la última versión del servicio gestionado, no debe realizar el seguimiento de ninguna versión o nivel de producto.

## ¿Qué gestiona IBM por mí?
{: #ibm_manage notoc}
{: faq}   

Manejamos la instalación, las actualizaciones de software, la creación y la gestión de dominios, y el mantenimiento de hardware. El servicio incluye supervisión de estado 24 horas al día, 7 días a la semana.


## ¿De qué tareas soy responsable?  
{: #responsible notoc}
{: faq}

Escribirá las aplicaciones que se ejecutan en un servicio de {{site.data.keyword.streaminganalyticsshort}} y la instancia de Streams local y se asegurará de que funcionan correctamente y de que cumplen los requisitos de rendimiento. También es responsable de cualquier supervisión específica de la aplicación.

## ¿Está soportada la alta disponibilidad (HA)?
{: #ha notoc}
{: faq}

La alta disponibilidad está gestionada por IBM. {{site.data.keyword.streaminganalyticsshort}} se ha configurado para dar soporte a HA. Hay más recursos de servidor colocados en caso de una migración tras error.

## ¿Cómo está gestionada la seguridad para el servicio de Streaming Analytics?
{: #security notoc}
{: faq}   

La seguridad está completamente gestionada por IBM. Las credenciales están generadas para cada servicio y se le proporcionan. Las actualizaciones de seguridad las gestiona y aplica IBM inmediatamente después de que estén disponibles.

## ¿Tengo que configurar un servicio de Streaming Analytics?  
{: #configure notoc}
{: faq}

El servicio está creado y completamente gestionado por IBM. Cada servicio consta de un conjunto dedicado de recursos de aplicación.

## ¿Cómo desarrollo las aplicaciones de Streams?
{: #streamsapp notoc}
{: faq}

Debe desarrollar las aplicaciones de Streams localmente utilizando los Streams gratuitos [{{site.data.keyword.streamsshort}} Quick Start Edition con Docker ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-docker/) para los [planes de servicio de v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) o si está utilizando los [planes de servicio de v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans), puede descargar la [imagen de VM de {{site.data.keyword.streamsshort}} Quick Start Edition ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}.

También puede utilizar la instalación local de {{site.data.keyword.streamsshort}} si la tiene. Las aplicaciones que desarrolle y compile localmente se podrán desplegar entonces sin problemas como un paquete en un servicio de Streams en la nube.

Pero si desea ejecutar las aplicaciones de Python en la nube, no tiene que instalar {{site.data.keyword.streamsshort}} de forma local. Simplemente utilice el contexto de `STREAMING\_ANALYTICS\_SERVICE` para enviar las aplicaciones de Python al servicio de {{site.data.keyword.streaminganalyticsshort}}. Puede desarrollar las aplicaciones en un entorno de desarrollo Python estándar o en un cuaderno interactivo de Jupyter, pero debe utilizar Python 3.5.

Para obtener más información sobre cómo desarrollar aplicaciones, consulte la [Guía de desarrollo de {{site.data.keyword.Bluemix_notm}} {{site.data.keyword.streaminganalyticsshort}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/streamsdev/?p=16589&post_type=doc&preview=1&_ppp=7ad76a418b).

## ¿Puedo iniciar sesión en un host de servicio de Streaming Analytics directamente?
{: #host notoc}  
{: faq}

No. No se da soporte a un inicio de sesión directo en el servidor con Telnet o Secure Shell (ssh). No puede instalar software adicional ni ejecutar software no Streams en un host de Streams.

## ¿Puedo acceder al sistema de archivos en el servicio de Streaming Analytics?
{: #filesystem notoc}
{: faq}   

Solo las aplicaciones de Streams pueden acceder directamente al sistema de archivos en un host de Streams.

Existen alternativas listas para la nube para soluciones que necesitan un mecanismo para que Streams interactúe con otros componentes de soluciones. Puede utilizar otros protocolos de origen y de receptor en lugar de archivos. Por ejemplo, almacenes de datos basados en la nube.

## ¿Cómo pueden acceder las aplicaciones de servicio de Streaming Analytics a los datos empresariales de mi organización?
{: #access notoc}  

Puede utilizar el [Servicio de Secure Gateway de {{site.data.keyword.Bluemix_notm}}](https://{DomainName}/catalog/services/secure-gateway) para conectarse de forma segura a las aplicaciones de secuencias de su empresa.

## ¿Están admitidas todas las características para IBM Streams local por el servicio de Streaming Analytics en la nube?
{: #features notoc}

Algunas de las características que no están admitidas para el servicio de {{site.data.keyword.streaminganalyticsshort}} incluyen:

  - Tareas administrativas para una instancia que requiere autoridad de dominio. Por ejemplo, la adición de etiquetas de host personalizadas o la creación de un grupo de trabajo.
  - Puntos de comprobación de regiones coherentes.
  - Algunos de los operadores de kit de herramientas no están admitidos. Para obtener más información, consulte [Adaptadores y kits de herramientas admitidos](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-compatible_toolkits).
  - La API de JMX de Streams.

## ¿Dónde puedo obtener más información sobre el servicio de Streaming Analytics?
{: #roadmap notoc}

El artículo de IBM developerWorks®, [Hoja de ruta para {{site.data.keyword.streaminganalyticsshort}} Service en {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/streamsdev/docs/roadmap-for-streaming-analytics-service-on-bluemix/), tiene orientación para obtener más información sobre el servicio, más enlaces a blogs, demostraciones y artículos informativos.
