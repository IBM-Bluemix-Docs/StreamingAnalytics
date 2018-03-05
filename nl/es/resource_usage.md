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


# Uso de recursos
{: #resourceusage}

{{site.data.keyword.streaminganalyticsshort}} cuenta con una serie de comportamientos y políticas para garantizar la asignación y el uso adecuado de los recursos.

## Visualización y edición de recursos de instancia
Puede visualizar y editar el número de recursos autorizados a la instancia en el panel de control del servicio o utilizando la [API REST {{site.data.keyword.streaminganalyticsshort}} v2](https://console.bluemix.net/apidocs/1939-streaming-analytics-v2#get-a-streaming-analytics-instance).

## Asignación de recursos 
- Los recursos se asignan a la instancia automáticamente cuando envía un trabajo que se ejecuta correctamente.
- Los recursos se eliminan de la instancia si no hay trabajos en ejecución en el recurso. Por ejemplo, tiene dos trabajos donde el trabajo 1 se ejecuta en el recurso 1 y el trabajo 2 se ejecuta en el recurso 1 y el recurso 2. Si se cancela el trabajo 2, el recurso 1 permanece en la instancia, mientras que el recurso 2 se elimina.
- Al enviar un trabajo, este se coloca en un nuevo recurso si la instancia no ha alcanzado su límite de asignación. 
- Cuando una instancia está utilizando todos sus recursos autorizados, se planifican nuevos trabajos en los recursos existentes.

## Restricciones de recursos

Las restricciones de recursos se pueden utilizar para controlar la asignación y el uso de recursos. Por ejemplo, utilizando las restricciones de recursos puede especificar que dos trabajos utilizan un único recurso, en lugar de estar separados en dos recursos.
