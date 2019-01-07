---

copyright:
  years: 2017, 2018
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Cómo otorgar permisos a los usuarios

Con una cuenta de {{site.data.keyword.Bluemix_notm}}, tiene privilegios administrativos en la organización o en el espacio en su cuenta para realizar todas las operaciones en {{site.data.keyword.streaminganalyticsshort}}. Sin embargo, cuando añada otros usuarios a su cuenta, debe gestionar sus permisos para que tengan los privilegios necesarios para operar instancias de servicio en su cuenta.

En {{site.data.keyword.streaminganalyticsshort}}, el acceso a las operaciones de gestión de servicios se controla mediante los siguientes niveles de permiso:

| Operación | Permisos necesarios de {{site.data.keyword.Bluemix_notm}} | Permisos necesarios de IAM |
|-----------|------------------------------|--------------------------|
| Crear o suprimir un servicio | Rol de desarrollador en el espacio de {{site.data.keyword.Bluemix_notm}} | Ninguno |
| Ver la página de detalles del servicio | Rol de desarrollador en el espacio de {{site.data.keyword.Bluemix_notm}} | Visor y superior |
| Redimensionar el servicio   | Rol de desarrollador en el espacio de {{site.data.keyword.Bluemix_notm}} | Editor y superior |
| Generar claves de servicio utilizando la CLI CF o la IU de {{site.data.keyword.Bluemix_notm}} | Rol de desarrollador en el espacio de {{site.data.keyword.Bluemix_notm}} | Ninguno |

Para añadir usuarios nuevos a la cuenta:

1.	Inicie una sesión en el [panel de control de {{site.data.keyword.Bluemix_notm}}](https://{DomainName}).

2.	Pulse **Gestionar -> Acceso (IAM) -> Usuarios**.

3.	En la página **Usuarios**, pulse **Invitar a usuarios**.

4.	Escriba el IBMid del usuario que desee invitar.

5.	En la sección Acceso, expanda **Servicios habilitados para identificación y acceso** y seleccione los valores siguientes:

	a.	Servicios: Seleccione **Todos los servicios habilitados para identidad y acceso**.

	b.	Región: Seleccione **EE.UU. sur**.

	c.	Instancia de servicio: Seleccione **Todas las instancias de servicio actuales**.

	d.	Roles: Elija un rol para el usuario. Los miembros con el rol Visor tienen acceso de solo lectura a {{site.data.keyword.streaminganalyticsshort}}. Los miembros que tengan asignados los privilegios Editor y superior pueden modificar el servicio de {{site.data.keyword.streaminganalyticsshort}}.

6.	Expanda **Acceso a Cloud Foundry** y seleccione la organización a la que desea dar acceso al usuario.

	a. Seleccione un rol en el nivel de organización para el usuario.

	b.	Elija EE.UU. sur para región.

	c.	Seleccione el espacio al que desee otorgar acceso al usuario.

	e.	Seleccione el rol que desee asignar al usuario. Para ver la página de detalles del servicio y realizar tareas como la generación de claves de servicio, debe asignar el rol Desarrollador.
