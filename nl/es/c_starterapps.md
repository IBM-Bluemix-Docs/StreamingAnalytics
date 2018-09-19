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

# Aplicaciones de ejemplo
{: #starterapps}

Despliegue y modifique las aplicaciones de inicio y aprenda rápidamente a utilizar el servicio de {{site.data.keyword.streaminganalyticsshort}}. Tenga en cuenta que los planes de servicio de v2 necesitan ejecutar Streams en RHEL 7. {{site.data.keyword.streaminganalyticsshort}} proporciona un [conjunto de iniciador y aplicaciones de muestra](https://developer.ibm.com/streamsdev/docs/starter-sample-apps-v2-plans/) para que pueda empezar rápidamente con los planes de servicio de v2. Las aplicaciones de muestra EventDetection y NYCTraffic no funcionan con los planes de servicio de v2.
{:shortdesc}


<table summary="En la primera fila de esta tabla se describe la aplicación de inicio Stock Trades. En la segunda fila, la tabla incluye:
1. En la primera columna, un enlace a un vídeo sobre cómo desplegar la aplicación de inicio Stock Trades. 2. En la segunda columna, un enlace a la descarga directa de la aplicación de inicio Stock Trades.
 ">
  <tr>
    <th id="stocktrades" colspan="3">App de muestra Stock Trades<br></th>
  </tr>
  <tr>
    <td headers="stocktrades" colspan="3">Esta aplicación analiza una secuencia de cotizaciones bursátiles y genera una media móvil de los precios utilizando el operador <a href="https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.1/com.ibm.streams.toolkits.doc/spldoc/dita/tk$spl/op$spl.relational$Aggregate.html">Agregar ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a>.
Puede ejecutar la aplicación de inicio sin ninguna modificación. Si desea experimentar más con el servicio, también puede modificar el código y devolver los cambios al entorno de {{site.data.keyword.Bluemix_short}}. El código fuente completo de la aplicación de inicio <a href="https://github.com/IBMStreams/samples/tree/master/QuickStart/TradesApp">está disponible en GitHub ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a>.</p>
</td>
  </tr>
  <tr>
    <td headers="stocktrades"><a href="https://developer.ibm.com/streamsdev/videos/getting-started-streaming-analytics-service-using-trades-starter-application/" target="_blank">DESPLEGAR LA APP ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a><br></td>
    <td headers="stocktrades"><a href="https://github.com/IBMStreams/samples/raw/master/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab" target="_blank">DESCARGAR ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a></td>
  </tr>
</table>

*Tabla 1. App de muestra de Stock Trades*


<table summary="Esta tabla describe, en la primera columna, la aplicación de muestra Event Detection v2. La tabla incluye en la segunda fila:
1. En la primera columna, un enlace a las instrucciones sobre cómo desplegar la aplicación de muestra Event Detection v2. 2. En la segunda columna, un enlace a las guías de aprendizaje sobre cómo utilizar la aplicación de muestra Event Detection. 3. En la tercera columna, un enlace para descargar directamente la aplicación de muestra Event Detection.
 ">
  <tr>
    <th id="EventDetection2" colspan="3">App de muestra Event Detection v2<br></th>
  </tr>
  <tr>
    <td colspan="3" headers="EventDetection2">La app Event Detection v2 se implementa a través del tiempo de ejecución de <a href="https://console.ng.bluemix.net/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">{{site.data.keyword.sdk4node}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a>. Esta app de inicio solo es compatible con los [planes de servicio de v2](/docs/services/StreamingAnalytics/service_plans.html).
La app proporciona una sencilla IU web para mostrar el estado y los resultados del análisis.
La app Node.js está enlazada con una instancia del servicio de {{site.data.keyword.streaminganalyticsshort}}. La app controla el servicio mediante la API REST de {{site.data.keyword.streaminganalyticsshort}} v2.
<p>Puede ejecutar la aplicación de inicio sin ninguna modificación.
Si desea experimentar más con el servicio, también puede modificar el código y devolver los cambios al entorno de {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td headers="EventDetection2"><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">DESPLEGAR LA APP</a><br></td>
    <td headers="EventDetection2"><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">TUTORIAL ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a></td>
    <td headers="EventDetection2"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetectionV2" target="_blank">DESCARGAR ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a></td>
  </tr>
</table>

*Tabla 2. App de muestra Event Detection v2*
<table summary="En la primera fila de esta tabla se describe la aplicación de ejemplo Event Detection. En la segunda fila, la tabla incluye:
1. En la primera columna, un enlace a las instrucciones sobre cómo desplegar la aplicación de inicio Event Detection. 2. En la segunda columna, un enlace a guías de aprendizaje sobre cómo utilizar la aplicación de inicio Event Detection. 3. En la tercera columna, un enlace a la descarga directa de la aplicación de inicio Event Detection.
 ">
  <tr>
    <th id="EventDetection1" colspan="3">App de muestra Event Detection<br></th>
  </tr>
  <tr>
    <td headers="EventDetection1" colspan="3">La app Event Detection se implementa a través del tiempo de ejecución <a href="https://console.ng.bluemix.net/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">{{site.data.keyword.sdk4node}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a>.
Esta app de inicio solo es compatible con los [planes de servicio de v1](/docs/services/StreamingAnalytics/service_plans.html). La app proporciona una sencilla IU web para mostrar el estado y los resultados del análisis.
La app Node.js está enlazada con una instancia del servicio de {{site.data.keyword.streaminganalyticsshort}}. La app controla el servicio mediante la API REST de {{site.data.keyword.streaminganalyticsshort}}.
<p>Puede ejecutar la aplicación de inicio sin ninguna modificación.
Si desea experimentar más con el servicio, también puede modificar el código y devolver los cambios al entorno de {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td headers="EventDetection1"><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">DESPLEGAR LA APP</a><br></td>
    <td headers="EventDetection1"><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">TUTORIAL ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a></td>
    <td headers="EventDetection1"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection" target="_blank">DESCARGAR ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a></td>
  </tr>
</table>

*Tabla 2. App de muestra Event Detection*

<table summary="En la primera fila de esta tabla se describe la aplicación de ejemplo Tráfico en Nueva York. En la segunda fila, la tabla incluye:
1. En la primera columna, un enlace a las instrucciones sobre cómo desplegar la aplicación de ejemplo Tráfico en Nueva York. 2. En la segunda columna, un enlace a guías de aprendizaje sobre cómo utilizar la aplicación de ejemplo Tráfico en Nueva York. 3. En la tercera columna, un enlace a la descarga directa de la aplicación de ejemplo Tráfico en Nueva York.">
  <tr>
    <th id="NYCTraffic" colspan="3">App de muestra NYC Traffic<br></th>
  </tr>
  <tr>
    <td headers="NYCTraffic" colspan="3">La app de inicio The NYC Traffic es una aplicación para {{site.data.keyword.Bluemix_short}} que está escrita en Liberty for Java. Contiene una aplicación de {{site.data.keyword.streamsshort}} que recupera datos públicos de los sensores de tráfico de la ciudad de Nueva York, calcula estadísticas globales y devuelve los resultados a la aplicación Liberty. Esta app de inicio solo es compatible con los [planes de servicio de v1](/docs/services/StreamingAnalytics/service_plans.html).
<p>Puede ejecutar la aplicación de inicio sin ninguna modificación. Si desea experimentar más con el servicio, también puede modificar el código y devolver los cambios al entorno de {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td headers="NYCTraffic" deploylink><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">DESPLEGAR LA APP</a><br></td>
    <td headers="NYCTraffic"><a href="https://developer.ibm.com/streamsdev/docs/bluemix-streaming-analytics-starter-application/" target="_blank">TUTORIAL ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a></td>
    <td headers="NYCTraffic"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic" target="_blank">DESCARGAR ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a></td>
  </tr>
</table>

*Tabla 3. App de muestra NYC Traffic*

## Apps de muestra IBM Streams Runner for Apache Beam

<table summary="Esta tabla describe, en la primera fila, la aplicación de TemperatureSample Beam. La tabla incluye en la segunda fila un enlace a un tutorial de cómo desplegar la aplicación de TemperatureSample Beam. ">
  <tr>
    <th id="TemperatureSample" colspan="3">App Beam TemperatureSample<br></th>
  </tr>
  <tr>
    <td headers="TemperatureSample" colspan="3">Esta aplicación realiza lecturas de temperatura desde varios dispositivos. Esta app de inicio solo está disponible para los [planes de servicio de v2](/docs/services/StreamingAnalytics/service_plans.html). La aplicación divide las lecturas entre lecturas “buenas” (válidas) y “malas” (inválidas) basándose en un umbral determinado. Cuenta las lecturas malas y genera algunas estadísticas básicas para las lecturas buenas, y finalmente registra los resultados. Puede descargar la app TemperatureSample desde la consola Streaming Analytics.
</td>
  </tr>
  <tr>
    <td headers="TemperatureSample"><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3-sample/#running-the-temperaturesample-application" target="_blank">DESPLEGAR LA APP ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a><br></td>
    <td headers="TemperatureSample"><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3-sample/#viewing-the-running-application" target="_blank">VER LA APP ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a></td>
  </tr>
</table>

*Tabla 4. App TemperatureSample*

<table summary="Esta tabla describe, en la primera fila, la aplicación de ejemplo de WordCount Beam. La tabla incluye en la segunda fila un enlace a una guía de aprendizaje acerca de cómo desplegar la aplicación de ejemplo de WordCount.
 ">
  <tr>
    <th id="WordCountSample" colspan="3">App de ejemplo WordCount<br></th>
  </tr>
  <tr>
    <td headers="WordCountSample" colspan="3">La aplicación de ejemplo Apache Beam 2.0 Java SDK Quickstart WordCount crea ejecuciones secuenciales reutilizables, que se pueden mantener y leer desde el archivo de texto, aplicar transformaciones para tokenizar y contar las palabras, y escribir los datos a un archivo de texto resultante.
</td>
  </tr>
  <tr>
    <td headers="WordCountSample"><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3b-wordcount/" target="_blank">DESPLEGAR LA APP ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a><br></td>
  </tr>
</table>

*Tabla 5. App de ejemplo WordCount*

<table summary="Esta tabla describe, en la primera fila, la aplicación de ejemplo FileStreamSample. La tabla incluye en la segunda fila un enlace a una guía de aprendizaje sobre cómo desplegar la aplicación FileStreamSample.
 ">
  <tr>
    <th id="FilterStreamSample" colspan="3">App FileStreamSample<br></th>
  </tr>
  <tr>
    <td headers="FilterStreamSample" colspan="3">Puede utilizar la aplicación de ejemplo de IBM® Streams Runner for Apache Beam FileStreamSample para aprender cómo utilizar el almacenamiento de objetos {{site.data.keyword.Bluemix_notm}} para la entrada y salida de archivos.
</td>
  </tr>
  <tr>
    <td headers="FilterStreamSample"><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-5b-objstor/" target="_blank">DESPLEGAR LA APP ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")</a><br></td>
  </tr>
</table>

*Tabla 6. App FileStreamSample*
