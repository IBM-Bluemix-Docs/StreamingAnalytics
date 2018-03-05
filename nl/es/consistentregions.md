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


# Mejoras de alta disponibilidad
{: #consistentregions}

Debido a los requisitos empresariales, algunas aplicaciones requieren que todas las tuplas se procesen al menos una vez. Se ha reforzado {{site.data.keyword.streamsshort}} con operadores y anotaciones que permiten la definición de una región que no pierde tuplas durante el proceso de secuencias. Las tuplas de una región coherente se procesan por lo menos una vez. 


Si utiliza los planes de precios Beta-Entry o Beta-Enhanced, puede ejecutar y supervisar aplicaciones Streams con las regiones coherentes definidas en {{site.data.keyword.streaminganalyticsshort}}. Cuando crea un servicio de {{site.data.keyword.streaminganalyticsshort}} con los planes Beta-Entry o Beta-Enhanced, la instancia ya está configurada para utilizar regiones coherentes.

Una región coherente es un subgrafo donde los estados de los operadores ganan coherencia procesando todas las tuplas y signos de puntuación dentro de puntos definidos en una secuencia. Esto permite procesar al menos una vez las tuplas del subgrafo. La región coherente se drena periódicamente de sus tuplas actuales. Todas las tuplas de una región coherente se procesan hasta el final de subgrafo. El estado en memoria de los operadores se serializa y almacena automáticamente en el punto de comprobación para cada uno de los operadores de la región.

Puede escribir aplicaciones Java y SPL, que tengan el proceso de tuplas garantizado, y desplegarlas en {{site.data.keyword.streaminganalyticsshort}}.

Puede definir el inicio de una región coherente con la anotación `@consistent` en un operador con capacidad. {{site.data.keyword.streamsshort}} determina automáticamente el ámbito de la región coherente, pero puede cambiar el operador final de la región con la anotación `@autonomous`. La región coherente definida establece periódicamente un estado coherente.

Consulte la [documentación de {{site.data.keyword.streamsshort}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.1/com.ibm.streams.dev.doc/doc/consistentregions.html) para obtener información detallada sobre cómo utilizar regiones coherentes en aplicaciones Streams.
