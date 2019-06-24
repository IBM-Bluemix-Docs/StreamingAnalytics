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

# Alta disponibilidad y recuperación tras desastre
{: #c_ha}

{{site.data.keyword.streaminganalyticsshort}} es altamente disponible dentro de una ubicación de {{site.data.keyword.Bluemix_notm}} (por ejemplo, Dallas, Washington DC, Londres, Frankfurt). Sin embargo, la recuperación de posibles desastres que afecten a toda la región de {{site.data.keyword.Bluemix_notm}} requiere planificación y preparación.
{:shortdesc}


Usted es el responsable de comprender su configuración, personalización y uso del servicio. También es el responsable de estar preparado para volver a crear una instancia del servicio en una nueva ubicación de {{site.data.keyword.Bluemix_notm}} y de volver a desplegar sus aplicaciones en dicha ubicación. Consulte [¿Cómo puedo asegurar un tiempo de inactividad cero?](/docs/services/overview?topic=overview-zero-downtime#zero-downtime) para obtener más información sobre los estándares de alta disponibilidad y recuperación tras desastre en {{site.data.keyword.Bluemix_notm}}. También encontrará información sobre los [Acuerdos de nivel de servicio](/docs/services/overview?topic=overview-zero-downtime#zero-downtime#SLAs).

## Alta disponibilidad

{{site.data.keyword.streaminganalyticsshort}} permite una alta disponibilidad para las aplicaciones. Sus aplicaciones se despliegan en contenedores Docker que se ejecutan en clústeres de Kubernetes. Para escribir aplicaciones altamente disponibles, debe comprender cómo funcionan estos contenedores para asegurar una alta disponibilidad:

* Los recursos de aplicación son contenedores con la CPU y la memoria asignadas de acuerdo con su plan de servicio.
* Durante un fallo de hardware o software, los contenedores podrían moverse. Cuando los contenedores se mueven, los elementos de procesamiento se reinician.
* Durante un mantenimiento planificado, los contenedores podrían moverse (los elementos de procesamiento se reinician).

Por lo tanto, a la hora de escribir sus aplicaciones, debería considerar que los contenedores en ocasiones pueden moverse. Además, tenga en cuenta lo siguiente:
* Asegúrese de que los elementos de procesamiento (PE) sean reiniciables y reubicables.
* Asegúrese de que su aplicación puede tolerar el reinicio de algunos o todos los PE, en cualquier orden.
* Asegúrese de que el origen y los operadores sink de su aplicación Streams estén configurados para restablecer las conexiones cuando su PE se reinicia.

Consulte la [guía de desarrollo de {{site.data.keyword.streaminganalyticsshort}}](https://developer.ibm.com/streamsdev/docs/streaming-analytics-dev-guide/#troubleshooting) para obtener ejemplos sobre cómo resolver los problemas de su aplicación.

Para implementar una alta disponibilidad, se habilitan las aplicaciones para garantizar el procesamiento de todas las tuplas. Para alcanzar el procesamiento de tuplas garantizado, se establece un punto de comprobación periódicamente para todos los operadores en una región coherente. En caso de fallo de una aplicación, todos los operadores se retrotraerán al último estado de punto de comprobación satisfactorio.
{{site.data.keyword.streaminganalyticsshort}} le permite utilizar regiones coherentes.

### Procesamiento de tuplas garantizado
Debido a los requisitos empresariales, algunas aplicaciones requieren que todas las tuplas se procesen al menos una vez. Se ha reforzado {{site.data.keyword.streamsshort}} con operadores y anotaciones que permiten la definición de una región que no pierde tuplas durante el proceso de secuencias. Las tuplas de una región coherente se procesan por lo menos una vez.

Si se detecta un fallo de aplicación dentro de una región coherente, {{site.data.keyword.streaminganalyticsshort}} puede establecer la aplicación en el último estado coherente (también conocido como punto de comprobación), y dirigir los orígenes de datos de la aplicación para reproducir tuplas desde ese punto.

Puede ejecutar y supervisar aplicaciones Streams con las regiones coherentes definidas en {{site.data.keyword.streaminganalyticsshort}}. Cuando crea un servicio de {{site.data.keyword.streaminganalyticsshort}}, la instancia ya está configurada para permitir el uso de regiones coherentes.

Una región coherente es un subgrafo donde los estados de los operadores ganan coherencia procesando todas las tuplas y signos de puntuación dentro de puntos definidos en una secuencia. Esto permite procesar al menos una vez las tuplas del subgrafo. La región coherente se drena periódicamente de sus tuplas actuales. Todas las tuplas de una región coherente se procesan hasta el final de subgrafo. El estado en memoria de los operadores se serializa y almacena automáticamente en el punto de comprobación para cada uno de los operadores de la región.

Puede escribir aplicaciones Java, SPL y Phyton que tengan el proceso de tuplas garantizado, y desplegarlas en {{site.data.keyword.streaminganalyticsshort}}.

Puede definir el inicio de una región coherente con la anotación `@consistent` en un operador con capacidad. {{site.data.keyword.streamsshort}} determina automáticamente el ámbito de la región coherente, pero puede cambiar el operador final de la región con la anotación `@autonomous`. La región coherente definida establece periódicamente un estado coherente.

Consulte la [documentación de {{site.data.keyword.streamsshort}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.dev.doc/doc/consistentregions.html) para obtener información detallada sobre cómo utilizar regiones coherentes en aplicaciones Streams.

## Recuperación tras desastre
{{site.data.keyword.streaminganalyticsshort}} es un servicio de disponibilidad general que se ofrece en múltiples regiones de {{site.data.keyword.Bluemix_notm}}. {{site.data.keyword.streaminganalyticsshort}} no almacena datos de usuario en {{site.data.keyword.Bluemix_notm}}.

En función de sus requisitos empresariales, seleccione una de las siguientes estrategias de recuperación tras desastre:
* Si no necesita interrumpir su aplicación:
  1. Cree instancias de {{site.data.keyword.streaminganalyticsshort}} en múltiples regiones de {{site.data.keyword.Bluemix_notm}}.
  2. Envíe su aplicación a múltiples regiones.


* Si necesita interrumpir mínimamente su aplicación:
  1. Cree instancias de {{site.data.keyword.streaminganalyticsshort}} en múltiples regiones de {{site.data.keyword.Bluemix_notm}}.
  2. Supervise la aplicación utilizando la [API REST de servicio](https://ibm.co/2Gt9mB6) y cambie dinámicamente la carga de trabajo a una nueva región, según sea necesario.

**Nota**: Cada región coherente está vinculada a la región de {{site.data.keyword.Bluemix_notm}}. En un escenario de recuperación tras desastre, las regiones coherentes de una aplicación no realizan ninguna función.
