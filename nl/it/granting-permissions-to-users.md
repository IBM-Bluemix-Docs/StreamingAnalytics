---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-16"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Concessione delle autorizzazioni agli utenti

Con un account {{site.data.keyword.Bluemix_notm}}, disponi di privilegi amministrativi nell'organizzazione o nello spazio nel tuo account per eseguire tutte le operazioni su {{site.data.keyword.streaminganalyticsshort}}. Tuttavia, quando aggiungi altri utenti nel tuo account, hai bisogno di gestire le loro autorizzazioni in modo che dispongano dei privilegi richiesti per gestire le istanze di servizio nel tuo account.

In {{site.data.keyword.streaminganalyticsshort}}, l'accesso alle operazioni di gestione dei servizi è controllato dai seguenti livelli di autorizzazione:

| Operazione | Autorizzazioni {{site.data.keyword.Bluemix_notm}} richieste | Autorizzazioni IAM richieste |
|-----------|------------------------------|--------------------------|
| Creare o eliminare un servizio | Ruolo sviluppatore per lo spazio {{site.data.keyword.Bluemix_notm}} | Nessuna |
| Visualizzare la pagina dei dettagli del servizio | Ruolo sviluppatore per lo spazio {{site.data.keyword.Bluemix_notm}} | Visualizzatore e superiore |
| Ridimensionare il servizio   | Ruolo sviluppatore per lo spazio {{site.data.keyword.Bluemix_notm}} | Editor e superiore |
| Generare chiavi di servizio utilizzando la CLI CF oppure l'IU {{site.data.keyword.Bluemix_notm}} | Ruolo sviluppatore per lo spazio {{site.data.keyword.Bluemix_notm}} | Nessuna |

Per aggiungere nuovi utenti nel tuo account:

1.	Esegui l'accesso al [dashboard {{site.data.keyword.Bluemix_notm}}](https://{DomainName}).

2.	Fai clic su **Gestisci -> Accesso (IAM) -> Utenti**.

3.	Nella pagina **Utenti**, fai clic su **Invita utenti**.

4.	Immetti l'ID IBM dell'utente che vuoi invitare.

5.	nella sezione Accesso, espandi **Servizi abilitati per l'accesso e l'identità** e seleziona i seguenti valori:

	a.	Servizi: seleziona **Tutti i servizi abilitati per l'accesso e l'identità**.

	b.	Regione: seleziona **Stati Uniti Sud**.

	c.	Istanza del servizio: seleziona **Tutte le istanze del servizio correnti**.

	d.	Ruoli: scegli un ruolo per l'utente. I membri con il ruolo Visualizzatore hanno un accesso di sola lettura a {{site.data.keyword.streaminganalyticsshort}}. I membri a cui sono assegnati privilegi di Editor o superiori possono modificare il servizio {{site.data.keyword.streaminganalyticsshort}}.

6.	Espandi **Accesso Cloud Foundry** e seleziona l'organizzazione a cui desideri che l'utente possa accedere.

	a. Seleziona un ruolo a livello dell'organizzazione per il tuo utente.

	b.	Scegli Stati Uniti Sud per la regione.

	c.	Seleziona lo spazio a cui desideri che l'utente possa accedere.

	e.	Seleziona il ruolo che desideri assegnare all'utente. Per visualizzare la pagina dei dettagli del servizio ed eseguire attività quali la generazione di chiavi del servizio, devi assegnare il ruolo Sviluppatore.
