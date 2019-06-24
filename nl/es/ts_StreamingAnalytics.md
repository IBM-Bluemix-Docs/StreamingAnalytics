---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-16"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Resolución de problemas de Streaming Analytics
{: #ts_StreamingAnalytics}

Puede encontrar respuestas a preguntas comunes sobre cómo utilizar {{site.data.keyword.streaminganalyticsshort}} en {{site.data.keyword.Bluemix_short}}.
{:shortdesc}

## Cuando inicio el servicio, me solicitan credenciales para iniciar sesión en la consola
{: #log_in_console}

Al iniciar {{site.data.keyword.streaminganalyticsshort}}, se le solicitarán las credenciales para iniciar sesión en la consola de servicio.
{:shortdesc}

Inicia un servicio {{site.data.keyword.streaminganalyticsshort}} que ha creado y, en lugar de acceder directamente a la consola de servicio, ve una página de inicio de sesión donde se le solicitan las credenciales.
{: tsSymptoms}

Se ha producido una actualización de la infraestructura de servicio y la memoria caché del navegador está impidiendo que el servicio seleccione la actualización.
{: tsCauses}

Borre la memoria caché del navegador para asegurarse de obtener la versión más reciente de la consola de servicio.
{: tsResolve}

## Mi aplicación no funciona correctamente
{: #app_unhealthy}

No puede ejecutar la aplicación correctamente y su estado es `unhealthy`.
{:shortdesc}

Envía una aplicación a la instancia del servicio, la aplicación se inicia pero falla de inmediato y su estado es `unhealthy`. Aparece el siguiente error en el archivo de registro: `/lib64/libc.so.6: no se ha encontrado la versión GLIBC_2.14`.
{: tsSymptoms}

No ha compilado la aplicación con un sistema operativo RHEL 7.x o una versión de CentOS equivalente.
{: tsCauses}

Debe compilar la aplicación en Red Hat Enterprise Linux (RHEL) 7.x si está utilizando los [planes de servicio de v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans). Si está utilizando [planes de servicio de v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans), debe compilar su aplicación con RHEL 6.5 con procesadores Intel. Vuelva a enviar la aplicación a la instancia del servicio. Puede descargar [{{site.data.keyword.streamsshort}} Quick Start Edition con Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) si no tiene un entorno de desarrollo compatible y si está utilizando los planes de servicio de v2. Si está utilizando planes de servicio de v1, descargue [{{site.data.keyword.streamsshort}} QSE ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}.
{: tsResolve}

## Mi aplicación no funciona correctamente una vez reiniciada
{: #app_restart}

Su aplicación no funciona correctamente una vez reiniciada por mantenimiento del sistema o en un escenario de recuperación de error.
{:shortdesc}

Tiene varias aplicaciones en la instancia de servicio y una de las aplicaciones utiliza una etiqueta para la colocación de operadores. Una vez que la aplicación se reinicia, los recursos para los operadores no etiquetados se adquieren en primer lugar y se consume toda la cuota de recursos antes de que se puedan colocar los operadores etiquetados.
{: tsSymptoms}

Un reinicio del pod a gran escala, desencadenado la mayoría de las veces por actualizaciones de servicio, puede provocar que las aplicaciones no se puedan reiniciar si necesitan etiquetas especiales y la cuota de recursos ya se ha alcanzado. En algunos casos, los reinicios del pod a gran escala pueden estar causados por escenarios de recuperación de errores.
{: tsCauses}

Se debe aumentar la cuota de recursos o liberar recursos, de modo que las aplicaciones puedan adquirir recursos con las etiquetas necesarias. Para aumentar la cuota, vaya a la página de detalles del servicio y aumente el tamaño de la instancia. Para liberar recursos, cancele trabajos existentes hasta que se hayan liberado suficientes recursos para colocar correctamente las aplicaciones.
{: tsResolve}
