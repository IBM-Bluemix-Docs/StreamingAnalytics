---

copyright:
  years: 2015, 2018
lastupdated: "2018-04-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Despliegue de aplicaciones Beam en Streaming Analytics
{: #develop_beam_apps}

Ahora puede desarrollar aplicaciones Beam en su entorno de desarrollo local {{site.data.keyword.streamsshort}} y desplegar estas aplicaciones en {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

{{site.data.keyword.streamsshort}} Runner for Apache Beam realiza ejecuciones secuenciales de Beam en un entorno de {{site.data.keyword.streamsshort}}. Una aplicación Beam que se inicia con Streams Runner se traduce a un archivo Streams Application Bundle (SAB) que puede desplegar y supervisar desde {{site.data.keyword.streaminganalyticsshort}}.

Para enviar una aplicación de Beam a su servicio de {{site.data.keyword.streaminganalyticsshort}} en {{site.data.keyword.Bluemix_notm}}, debe crear un archivo VCAP formateadas por JSON que contiene credenciales y otra información del servicio.

1. En el entorno local de Streams, navegue a la subcarpeta de ejemplo donde ha instalado el kit de
herramientas ($STREAMS_BEAM_RUNNER/samples) y copie el archivo template.vcap a un nuevo archivo. Proporcione al nombre un nombre significativo y la extensión de archivo .vcap.
1. [Copie las credenciales de su servicio {{site.data.keyword.streaminganalyticsshort}} ](/docs/services/StreamingAnalytics/r_vcap_services.html) y pegue las credenciales en el archivo de VCAP que ha creado, sustituyendo la siguiente línea:
```
 <ELIMINE ESTA LÍNEA E INSERTE LAS CREDENCIALES AQUÍ>
 ```
1. Compruebe si la aplicación Beam se ejecuta correctamente en su entorno de desarrollo. Cuando inicia la aplicación Beam con
Streams Runner, la aplicación se traduce a un archivo de Streams Application Bundle (SAB).
1. Envíe el archivo SAB que está asociado con su aplicación Beam a {{site.data.keyword.streaminganalyticsshort}}

Ahora su aplicación está desplegada en la nube. Puede supervisar su aplicación utilizando el servicio de {{site.data.keyword.streaminganalyticsshort}}.

Para obtener más detalles acerca del despliegue y supervisión de sus aplicaciones Beam en {{site.data.keyword.streaminganalyticsshort}}, consulte [Streams Runner for Apache Beam ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/).
