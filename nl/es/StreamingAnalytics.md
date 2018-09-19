---

copyright:
  years: 2015, 2018
lastupdated: "2018-07-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Acerca de Streaming Analytics
{: #about}

Puede realizar análisis en tiempo real sobre los datos en movimiento como parte de las aplicaciones de {{site.data.keyword.Bluemix_short}} con {{site.data.keyword.streaminganalyticsfull}}.
{:shortdesc}

¿Es nuevo en {{site.data.keyword.streaminganalyticsshort}}? Obtenga una [presentación rápida del servicio ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/streamsdev/docs/streaming-analytics-now-available-bluemix-2/){:new_window}.

El servicio de {{site.data.keyword.streaminganalyticsshort}} proporciona las siguientes capacidades para desplegar, analizar y supervisar datos en la nube:

**Uso interactivo y programático del servicio:**

Puede utilizar el servicio de forma interactiva a través de la [consola de {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/c_streams_console.html) o mediante programación a través de la [API REST de {{site.data.keyword.streaminganalyticsshort}} v1 ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://console.bluemix.net/apidocs/streaming-analytics-v1){:new_window} si está utilizando los [planes de servicio de v1](/docs/services/StreamingAnalytics/service_plans.html). Para los [planes de servicio de v2](/docs/services/StreamingAnalytics/service_plans.html), utilice la API REST de {{site.data.keyword.streaminganalyticsshort}} v2 ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")https://console.bluemix.net/apidocs/streaming-analytics-v2.

**Desarrollo y supervisión de aplicaciones SPL, Java, Scala y Python:**

Puede escribir aplicaciones de {{site.data.keyword.streamsshort}} en SPL, Java, Scala y Python. [Despliegue y supervise estas aplicaciones](/docs/services/StreamingAnalytics/t_deploytocloud.html) con la consola de {{site.data.keyword.streaminganalyticsshort}}.

Si desea escribir sus aplicaciones en SPL, {{site.data.keyword.streamsfull}} Processing Language (SPL) es un lenguaje de programación que se utiliza para crear aplicaciones de proceso de secuencias. Si desea profundizar en el uso de sus propias aplicaciones SPL, puede obtener un entorno de desarrollo de {{site.data.keyword.streamsshort}} y debe preparar sus apps SPL para la nube.

Para crear y desplegar aplicaciones Python sin un entorno de desarrollo de {{site.data.keyword.streamsshort}}, utilice los cuadernos de servicio de {{site.data.keyword.DSX_short}} o la API de {{site.data.keyword.streamsshort}} Python. Para obtener más información, consulte el tema sobre [Desarrollo de aplicaciones Python para {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/t_develop_apps_python.html).

Puede desarrollar aplicaciones Beam con el ejecutor de Streams en su entorno de desarrollo, que después puede desplegar y supervisar en el servicio de {{site.data.keyword.streaminganalyticsshort}}. Para obtener más información sobre las aplicaciones de Beam con el ejecutor de Streams, consulte las [apps de Monitor Beam con Streams Runner en {{site.data.keyword.streaminganalyticsshort}}](docs/services/StreamingAnalytics/gs_beamrunner.html).


**Compatibilidad con los operadores de {{site.data.keyword.streamsshort}}:**

Los operadores de {{site.data.keyword.streamsshort}} del kit de herramientas estándar de [{{site.data.keyword.streamsshort}} Processing Language (SPL) son compatibles](/docs/services/StreamingAnalytics/compatible_toolkits.html) con {{site.data.keyword.streaminganalyticsshort}}.

## Responsabilidades de Streaming Analytics
{: #responsibilities notoc}

### Responsabilidades del cliente
{: #clientresponsibilities notoc}

El cliente es responsable de:

* Seguir la configuración inicial de IBM de {{site.data.keyword.streamsshort}} y de supervisar, configurar y gestionar los trabajos de {{site.data.keyword.streamsshort}} que se ejecutan en la instancia. El cliente puede iniciar y detener la instancia e iniciar y detener los trabajos que se ejecutan en la instancia.
* Desarrollar, según sea necesario, programas y aplicaciones en el servicio para analizar datos y obtener detalles de los mismos. El cliente también es responsable de la calidad y el rendimiento de dichos programas o aplicaciones desarrollados. Los programas se pueden desarrollar en SPL, Java o en otros lenguajes soportados mediante la característica Topology de {{site.data.keyword.streamsshort}}. Se deben compilar con {{site.data.keyword.streamsshort}} Developer Edition o {{site.data.keyword.streamsshort}} Quick Start Edition con el mismo sistema operativo que se ha utilizado para {{site.data.keyword.streaminganalyticsshort}}.
* Comprobar periódicamente el siguiente enlace para estar informado sobre tiempos de inactividad disruptivos o no disruptivos planificados - [https://developer.ibm.com/bluemix/support/#status ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/bluemix/support/#status){:new_window}  
* Hacer copia de seguridad de todos los datos, metadatos, archivos de configuración y parámetros de entorno según los requisitos de la empresa para garantizar la continuidad.
* Restaurar los datos, metadatos, archivos de configuración y parámetros de entorno de una copia de seguridad para garantizar la continuidad, en el caso de que se produzca un error de cualquier tipo. Se incluyen, a título enunciativo y no limitativo, errores en el centro de datos o de pod, errores del servidor, errores del disco duro o errores de software.

### Responsabilidades de IBM
{: #ibmresponsibilities notoc}

Como parte de {{site.data.keyword.streaminganalyticsfull}}, IBM:

* Proporcionará y gestionará servidores, almacenamiento e infraestructura de red para la instancia del cliente.
* Proporcionará una configuración inicial de {{site.data.keyword.streamsshort}} en los nodos seleccionados.
* Proporcionará y gestionará la infraestructura para disponer de Internet y de un cortafuegos interno para garantizar la protección y aislamiento.
* Supervisará y gestionará los siguientes componentes en {{site.data.keyword.streaminganalyticsshort}}:
	* Componentes de red
	* Servidores y su almacenamiento local
	* Sistemas operativos de la infraestructura
	* Servicios de gestión de {{site.data.keyword.streamsshort}}
	* Instancias de {{site.data.keyword.streamsshort}}
* Proporcionará partes de mantenimiento, incluidos los parches de seguridad necesarios para los sistemas operativos de la infraestructura y para {{site.data.keyword.streamsshort}}.
* Realizará tareas de mantenimiento que no deberían derivar en inactividad del sistema (mantenimiento “no disruptivo”) y mantenimiento que requiera cierto tiempo de inactividad y reinicio (mantenimiento “disruptivo””), que se llevarán a cabo en momentos planificados que se publicarán en [https://developer.ibm.com/bluemix/support/#status ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/bluemix/support/#status){:new_window}
* Cualquier cambio en los tiempos planificados de mantenimiento se publicará con el aviso adecuado.
