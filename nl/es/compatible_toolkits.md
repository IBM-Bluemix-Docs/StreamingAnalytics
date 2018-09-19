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

# Adaptadores y kits de herramientas admitidos
{: #compatible_toolkits}

Los siguientes kits de herramientas y kits de herramientas y adaptadores de análisis son compatibles con {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

| Kits de herramientas                        | Descripción							                  |
| --------------------------------| --------------------------|
| [Proceso de sucesos complejos (CEP) ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://ibm.co/2zOwODa)    |	Proporciona el operador MatchRegex para llevar a cabo procesos de sucesos complejos.  		 |
| [Datetime ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://ibmstreams.github.io/streamsx.datetime/)	|	Conjunto de utilidades para gestionar fechas, horas e indicaciones de fecha y hora.	 |
| [HBase![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.hbase/)        | Permite a las aplicaciones de Streams conectar con Apache HBase.	 	   |
| [HDFS ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.hdfs/)          | Proporciona a los operadores y funciones que interactúan con el Sistema de archivos distribuido de Hadoop.	|
| [Internet (Inet) ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.inet)|  Se centra en interactuar con los datos alojados en la red.				       |
| [IoT ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.iot/)            | Proporciona la integración de Internet of Things (IoT) con la plataforma de IBM Watson IoT, ya sea en {{site.data.keyword.Bluemix_notm}} o en local ({{site.data.keyword.streamsshort}}). |
| [JDBC ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.jdbc/)          | Permite a las aplicaciones de Streams trabajar con bases de datos a través de JDBC.		   |
| [JSON ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.json/)          | Aprenda a convertir los datos desde JSON al formato de tupas de Streams, y a la inversa.   		|
| [Kafka ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://ibmstreams.github.io/streamsx.kafka/)       | Permite a las aplicaciones de Streams integrarse fácilmente con Apache Kafka. 	 |
| [MessageHub ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://ibmstreams.github.io/streamsx.messagehub/) | Permite a las aplicaciones de Streams trabajar con MessageHub.			     |
| [Messaging ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://ibmstreams.github.io/streamsx.messaging/)   |  	Se centra en interactuar con sistema de mensajería populares como Kafka, MQTT, JMS y XMS	<br>**Nota**: Para utilizar JMSSource, JMSSink, XMSSource, XMSSink con WebSphere MQ, complete estos pasos en el entorno de desarrollo: <br>1. Vaya a [IBMStreams on GitHub ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://github.com/IBMStreams){:new_window} y descargue Messaging Toolkit (com.ibm.streamsx.messaging) versión 3.0.0 o posterior en su entorno de desarrollo.<br>2. Utilice la versión 5.1.0 o superior del kit de herramientas para crear su aplicación.<br>3. Coloque el archivo `.bindings` necesario en el directorio `/etc` de su aplicación para incluirlo en paquete de aplicación {{site.data.keyword.streamsshort}}.	    |
| [Mining ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://ibm.co/2y3i5au)              	   	            |  Incluye operadores que puede utilizar aplicando modelos. <br> **Restricción:** no se admite este kit de herramientas si utiliza los [planes de servicio de v2](/docs/services/StreamingAnalytics/service_plans.html), ya que debe compilar el paquete de aplicaciones en un entorno RHEL 7 o una versión de CentOS equivalente. 	     |
| [RabbitMQ ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://ibmstreams.github.io/streamsx.rabbitmq/)     |  Proporciona a los operadores que permiten su aplicación Streams leer y enviar mensajes desde Rabbit MQ.  |
| [R-project ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://ibm.co/2h7D9lu)          	   	              |   Incluye el operador RScript, que se puede utilizar para ejecutar mandatos R y aplicar algoritmos de minería de datos complejos para detectar patrones de interés en secuencias de datos.			     |
| [Topology ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.topology/)      |  Aprenda a construir aplicaciones de modalidad continua para el servicio de {{site.data.keyword.streaminganalyticsshort}} en la plataforma {{site.data.keyword.Bluemix_notm}} y {{site.data.keyword.streamsshort}}.		     |
| [DPS ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.dps/) |	 Permite que varias aplicaciones que están ejecutando elementos de procesamiento (PE) en una o dos máquinas para compartir la información del estado específica de la aplicación.<br>**Restricción:** Solo es compatible REDIS como base de datos de fondo.	| 	 	 	
| [Geospatial ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://ibm.co/2h9x0VR) 	     |	Incluye operadores y funciones que facilitan el procesamiento y la indexación eficientes de datos de ubicación.<br>**Restricción:** Los operadores que utilizan el modo de correlación compartida no son compatibles(`MapStore`, `PointMapMatcher` en modo correlación compartida).		 |
| [TEDA ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://ibm.co/2z9DS00)	   | 	Proporciona un conjunto de operadores genéricos que se utiliza en aplicaciones de telecomunicaciones, y también ofrece un marco de aplicaciones que para configurar nuevas aplicaciones de archivo a archivo. Comience siguiendo las [guías de aprendizaje de TEDA ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.tutorial.teda/). Se admiten todos los operadores y funciones del kit de herramientas. <br>**Restricción:** No se admite el marco de aplicaciones.	 	 |
| [TimeSeries ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://ibm.co/2zEPILZ)	 	  | Los operadores y funciones en la condición de TimeSeries Toolkit, analizan y modelan datos de series temporales. <br>**Restricción:** No se admiten operadores en desuso.	   |
| [{{site.data.keyword.cos_short}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://bit.ly/2Ggp03T)	 	  | Proporciona operadores primitivos y funciones nativas para leer y escribir datos desde y a {{site.data.keyword.cos_short}}, respectivamente. El kit de herramientas admite {{site.data.keyword.cos_short}} compatible con S3.	   |

*Tabla 1. Kits de herramientas admitidos*

## Otros kits de herramientas y operadores
{: #other_operators}

Otros operadores, incluidos aquellos operadores del kit de herramientas que ha desarrollado para sus propias necesidades, pueden ser compatibles con {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

Los kits de herramientas deben cumplir los siguientes criterios para ser compatibles con {{site.data.keyword.streaminganalyticsshort}}:

1. No es necesario instalar previamente software adicional en el nodo de aplicación de la instancia de servicio.
2. Cualquier información de configuración que requiera el kit de herramientas se puede incluir en el paquete de aplicación mediante el kit de herramientas.
