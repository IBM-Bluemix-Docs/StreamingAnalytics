---

copyright:
  years: 2015, 2019
lastupdated: "2018-12-06"

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


Empiece utilizando las aplicaciones de muestra [](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps) para saber cómo enviar y supervisar una aplicación Beam en el servicio {{site.data.keyword.streaminganalyticsshort}}. Puede descargar las aplicaciones de muestra desde la consola de {{site.data.keyword.streaminganalyticsshort}}.

Consulte la documentación de [{{site.data.keyword.streamsshort}} Runner for Apache Beam ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/){:new_window} para ver las tablas que muestran cómo se ajusta Streams Runner en la [matriz de capacidad de Beam](https://beam.apache.org/documentation/runners/capability-matrix/). Consulte [Installing IBM Streams Runner for Apache Beam ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://bit.ly/2zFDpPr){:new_window} para obtener las instrucciones para instalar el kit de herramientas de `com.ibm.streams.beam` en su entorno de Streams para crear aplicaciones de Beam que puede enviar y supervisar desde {{site.data.keyword.streaminganalyticsshort}}.

Es útil tener algunos conocimientos de programación con Beam, pero no es un requisito; el sitio web de [Apache Beam ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://beam.apache.org/documentation/){:new_window} tiene una página de [Inicio rápido de Apache Beam Java SDK ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://beam.apache.org/get-started/quickstart-java/){:new_window} y otra documentación.
