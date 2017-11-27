---

copyright:
  years: 2015, 2017
lastupdated: "2017-10-27"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# IBM Streams Runner for Apache Beam de Streaming Analytics
{: #gs_beamrunner}

Si tiene un entorno de desarrollo {{site.data.keyword.streamsshort}}, ahora puede desarrollar las aplicaciones Beam localmente en su entorno y enviar esas apps al servicio {{site.data.keyword.streaminganalyticsshort}} en {{site.data.keyword.Bluemix_notm}}. {{site.data.keyword.streamsshort}} Runner for Apache Beam realiza ejecuciones secuenciales de Beam en un entorno de {{site.data.keyword.streamsshort}}. Una aplicación Beam que se inicia con Streams Runner se traduce a un archivo Streams Application Bundle (SAB) que puede desplegar y supervisar desde {{site.data.keyword.streaminganalyticsshort}}.


Empiece utilizando las aplicaciones de muestra [](/docs/services/StreamingAnalytics/c_starterapps.html) para saber cómo enviar y supervisar una aplicación Beam en el servicio {{site.data.keyword.streaminganalyticsshort}}. Puede descargar las aplicaciones de muestra desde la consola de {{site.data.keyword.streaminganalyticsshort}}.

Consulte la documentación de [{{site.data.keyword.streamsshort}} Runner for Apache Beam ](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/) para ver las tablas que muestran cómo se ajusta Streams Runner en la [matrix de capacidad de Beam]. Consulte [Installing IBM Streams Runner for Apache Beam](http://bit.ly/2zFDpPr) para obtener las instrucciones para instalar
el kit de herramientas de `com.ibm.streams.beam` en su entorno de Streams para crear aplicaciones de Beam que puede enviar y supervisar desde {{site.data.keyword.streaminganalyticsshort}}.

Es útil tener algunos conocimientos de programación con Beam, pero no es un requisito; el sitio web de  [Apache Beam](https://beam.apache.org/documentation/){:new_window} tiene una página de [
Inicio rápido de Apache Beam Java SDK](https://beam.apache.org/get-started/quickstart-java/){:new_window} y otra documentación.
