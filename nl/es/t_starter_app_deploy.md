---

copyright:
  years: 2015, 2018
lastupdated: "2018-12-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Guía de aprendizaje de iniciación
{: #starterapps_deploy}

Streaming Analytics es un servicio totalmente gestionado que le libera de la instalación, de la administración y de las tareas de gestión que consumen mucho tiempo, dándole más tiempo para desarrollar aplicaciones de streaming. En esta guía de aprendizaje de iniciación, se envía y despliega una de las aplicaciones de inicio de {{site.data.keyword.streaminganalyticsshort}} en {{site.data.keyword.Bluemix_notm}}.
{:shortdesc}


## Antes de empezar
{: #prereqs}

Debe seguir estos pasos para desplegar las apps de inicio:

* Regístrese para una cuenta de [{{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/registration){:new_window}
* Cree una instancia del servicio de {{site.data.keyword.streaminganalyticsshort}} en la organización de {{site.data.keyword.Bluemix_notm}}. Puede crear la instancia directamente desde la [página de detalles de la oferta de **{{site.data.keyword.streaminganalyticsshort}}** en el catálogo de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/catalog/services/streaming-analytics/){:new_window}.  
* [Instale la CLI de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/docs/cli/reference/bluemix_cli/get_started.html#getting-started).



## Paso 1. Creación y conexión de la app al servicio
{: #create_connect}

1. Cree una aplicación en {{site.data.keyword.Bluemix_notm}}:

    a. Vaya a **Menú**>**Apps de Cloud Foundry**>**Crear recurso** para crear un recurso.

    b. Seleccione el tiempo de ejecución de {{site.data.keyword.sdk4node}} para las apps de inicio Event Detection o Event Detection v2.

    Recuerde el nombre que asigna a la aplicación; lo necesitará más adelante.
1. Conecte la instancia de servicio de {{site.data.keyword.streaminganalyticsshort}} a la aplicación y vuelva a transferir la aplicación.

## Paso 2. Configuración de la aplicación de inicio
{: #setup_app}

1. Si está utilizando los [planes de servicio de v1](/docs/services/StreamingAnalytics/service_plans.html), descargue la app de inicio [Event Detection ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection). Descargue la app de inicio [Event Detection v2 ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://streams-github-samples.mybluemix.net/?get=QuickStart%2FBeta201801%2FEventDetectionV2) para los [planes de servicio de v2](/docs/services/StreamingAnalytics/service_plans.html).

1. Cambie el nombre del directorio para que coincida con el nombre asignado a la aplicación en {{site.data.keyword.Bluemix_notm}}.

## Paso 3. Despliegue la aplicación de inicio
{: #deploy_app}

1. Vaya al directorio de la aplicación de inicio:
  <pre><code>cd myapp</code></pre>
  {:pre}

1. Inicie sesión en {{site.data.keyword.Bluemix_notm}} y defina la organización de destino cuando se solicite:
  <pre><code>bx login</code></pre>
  {:pre}

1. Envíe por push la aplicación a {{site.data.keyword.Bluemix_notm}}:
  <pre><code>bx app push myapp</code></pre>
  {:pre}

1. Vaya a la página de detalles de la aplicación, a la que puede acceder desde el panel de control de {{site.data.keyword.Bluemix_notm}}, para comprobar que la aplicación se ha iniciado correctamente.
1. Inicie la aplicación para verla en el navegador. Encontrará el URL de la aplicación (o "ruta") en la página de detalles de la aplicación.

## Pasos siguientes
{: #next_steps}

Ahora que se está ejecutando su aplicación, puede supervisarla desde la consola de {{site.data.keyword.streaminganalyticsshort}}. Vaya a la página de detalles del servicio, seleccione el servicio de {{site.data.keyword.streaminganalyticsshort}} y pulse **Iniciar**.
