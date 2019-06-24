---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-16"

subcollection: StreamingAnalytics

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Esercitazione introduttiva
{: #starterapps_deploy}

Streaming Analytics è un servizio completamente gestito che ti libera da attività di gestione, amministrazione e installazione che richiedono molto tempo, dandoti maggior tempo per sviluppare le applicazioni di gestione dei flussi. In questa esercitazione introduttiva, esegui il push e la distribuzione di una delle applicazioni starter di {{site.data.keyword.streaminganalyticsshort}} a {{site.data.keyword.Bluemix_notm}}.
{:shortdesc}


## Prima di cominciare
{: #prereqs}

Devi attenerti alla seguente procedura per distribuire le applicazioni starter:

* Esegui la registrazione a un account [{{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/registration){:new_window}
* Crea un'istanza del servizio {{site.data.keyword.streaminganalyticsshort}} nella tua organizzazione {{site.data.keyword.Bluemix_notm}}. Puoi creare l'istanza direttamente dalla [pagina dei dettagli dell'offerta **{{site.data.keyword.streaminganalyticsshort}}** nel catalogo {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/catalog/services/streaming-analytics/){:new_window}.  
* [Installa la CLI {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](/docs/cli?topic=cloud-cli-install-ibmcloud-cli#install-ibmcloud-cli).



## Passo 1. Creazione e connessione dell'applicazione al tuo servizio
{: #create_connect}

1. Crea un'applicazione in {{site.data.keyword.Bluemix_notm}}:

    a. Vai a **Menu**>**Applicazioni Cloud Foundry**>**Crea risorsa** per creare una risorsa.

    b. Seleziona il runtime SDK per le applicazioni starter Event Detection o Event Detection v2.

    Ricorda il nome che fornisci per l'applicazione, ti servirà in seguito.
1. Collega l'istanza del servizio {{site.data.keyword.streaminganalyticsshort}} alla tua applicazione e ripreparala.

## Passo 2. Configurazione dell'applicazione starter
{: #setup_app}

1. Se stai utilizzando i [piani di servizio v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans), scarica l'applicazione starter [Event Detection ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection). Scarica l'applicazione starter [Event Detection v2 ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://streams-github-samples.mybluemix.net/?get=QuickStart%2FBeta201801%2FEventDetectionV2) per i piani di servizio [v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans).

1. Rinomina la directory in modo che corrisponda al nome fornito alla tua applicazione in {{site.data.keyword.Bluemix_notm}}.

## Passo 3. Distribuzione dell'applicazione starter
{: #deploy_app}

1. Passa alla directory dell'applicazione starter:
  <pre><code>cd myapp</code></pre>
  {:pre}

1. Accedi a {{site.data.keyword.Bluemix_notm}} e configura
la tua organizzazione di destinazione quando richiesto:
  <pre><code>bx login</code></pre>
  {:pre}

1. Trasmetti la tua applicazione a {{site.data.keyword.Bluemix_notm}}:
  <pre><code>bx app push myapp</code></pre>
  {:pre}

1. Vai alla pagina dei dettagli della tua applicazione, accessibile dal dashboard {{site.data.keyword.Bluemix_notm}}, per verificare che la tua applicazione sia stata avviata correttamente.
1. Avvia l'applicazione per visualizzarla nel browser. Puoi trovare l'URL della tua applicazione (o "rotta") nella pagina dei dettagli dell'applicazione.

## Fasi successive
{: #next_steps}

Ora che la tua applicazione è in esecuzione, puoi monitorarla dalla console {{site.data.keyword.streaminganalyticsshort}}. Passa alla pagina dei dettagli del servizio, seleziona il tuo servizio {{site.data.keyword.streaminganalyticsshort}} e fai clic su **Avvia**.
