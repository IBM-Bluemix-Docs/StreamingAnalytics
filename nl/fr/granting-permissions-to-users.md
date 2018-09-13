---

copyright:
  years: 2017, 2018
lastupdated: "2018-07-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Octroi de droits aux utilisateurs

Un compte {{site.data.keyword.Bluemix_notm}} vous accorde des privilèges d'administration dans l'organisation ou l'espace qui se trouve sous votre compte, de sorte que vous pouvez effectuer toutes les opérations possibles sur {{site.data.keyword.streaminganalyticsshort}}. Toutefois, lorsque vous intégrez d'autres utilisateurs à votre compte, vous devez gérer leurs droits afin qu'ils disposent des privilèges requis pour exécuter des instances de service sous votre compte.

Dans {{site.data.keyword.streaminganalyticsshort}}, l'accès aux opérations de gestion des services est régi par les niveaux de droits suivants :

| Opération | Droits {{site.data.keyword.Bluemix_notm}} requis | Droits IAM requis |
|-----------|------------------------------|--------------------------|
| Création ou suppression d'un service | Rôle de développeur sur l'espace {{site.data.keyword.Bluemix_notm}} | Aucun |
| Affichage du tableau de bord des services | Rôle de développeur sur l'espace {{site.data.keyword.Bluemix_notm}} | Afficheur au minimum |
| Redimensionnement du service   | Rôle de développeur sur l'espace {{site.data.keyword.Bluemix_notm}} | Editeur au minimum |
| Génération de clés de service à l'aide de l'interface de ligne de commande CF ou de l'interface utilisateur {{site.data.keyword.Bluemix_notm}} | Rôle de développeur sur l'espace {{site.data.keyword.Bluemix_notm}} | Aucun |

Pour intégrer de nouveaux utilisateurs à votre compte :

1.	Connectez-vous au tableau de bord [{{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net).

2.	Cliquez sur **Gérer -> Compte -> Utilisateurs**.

3.	Dans la page **Gestion des utilisateurs**, cliquez sur **Inviter des utilisateurs**.

4.	Entrez l'IBMid de l'utilisateur à inviter.

5.	Sous la section Accès, développez **Services avec l'offre Identity and Access activée** et sélectionnez les valeurs suivantes :

	a.	Services : Sélectionnez **Tous les services avec l'offre Identity and Access activée**.

	b.	Région : Sélectionnez **Sud des Etats-Unis**.

	c.	Instance de service : Sélectionnez **Toutes les instances de service en cours**.

	d.	Rôles : Choisissez un rôle pour l'utilisateur. Les membres dotés du rôle Afficheur disposent d'un accès en lecture seule à {{site.data.keyword.streaminganalyticsshort}}. Les membres dotés du rôle Editeur au minimum peuvent modifier le service {{site.data.keyword.streaminganalyticsshort}}.

6.	Développez **Accès Cloud Foundry** et sélectionnez l'organisation à laquelle vous souhaitez que l'utilisateur ait accès.

	a. Sélectionnez un rôle au niveau organisation pour votre utilisateur.

	b.	Choisissez la région Sud des Etats-Unis.

	c.	Sélectionnez l'espace auquel vous souhaitez que l'utilisateur ait accès.

	e.	Sélectionnez le rôle que vous souhaitez affecter à l'utilisateur. Pour afficher le tableau de bord des services et effectuer des tâches telles que la génération de clés de service, vous devez affecter le rôle Développeur.
