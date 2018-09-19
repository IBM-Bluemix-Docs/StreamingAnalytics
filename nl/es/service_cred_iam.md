---

copyright:
  years:  2017
lastupdated: "2018-07-24"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Autenticación de Identity and Access Management

El acceso a las instancias de servicio de {{site.data.keyword.streaminganalyticsshort}} para los usuarios de su cuenta está controlado por {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM). Para gestionar el servicio de {{site.data.keyword.streaminganalyticsshort}}, debe utilizar una señal de autenticación.

## Recuperación de las señales de acceso de IAM

### Requisitos previos

a. Debe tener un IBMid válido.

b. Descargue e instale la [CLI de {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/cli/reference/bluemix_cli/get_started.html#getting-started).

### Paso 1. Iniciar sesión en la CLI de {{site.data.keyword.Bluemix_notm}}.

```
bx api https://api.ng.bluemix.net
bx login
<especifique sus credenciales>

<Si forma parte de varias cuentas de {{site.data.keyword.Bluemix_notm}}, se le pedirá que elija una cuenta para la sesión actual. Además, necesitará elegir una organización y un espacio en {{site.data.keyword.Bluemix_notm}}.>
```

### Paso 2. Captar la señal de acceso de IAM.

```
bx iam oauth-tokens
```

Se crean dos señales: una denominada `Señal de IAM` y la otra denominada `Señal de UAA`. Utilice `Señal de IAM` para realizar llamadas de API REST.
