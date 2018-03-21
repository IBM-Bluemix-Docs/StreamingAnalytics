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

# Adattatori e toolkit supportati
{: #compatible_toolkits}

Questi adattatori e toolkit di analisi sono supportati da {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

| Toolkit                        | Descrizione							                  |
| --------------------------------| --------------------------|
| [Complex Event Processing (CEP) ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://ibm.co/2zOwODa)    |	Fornisce l'operatore MatchRegex per eseguire l'elaborazione di eventi complessi.  		 |
| [Datetime ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://ibmstreams.github.io/streamsx.datetime/)	|	Configura i programmi di utilità per gestire le date, le ore e le date/ore.	 |
| [HBase![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.hbase/)        | Abilita le applicazioni Streams a collegarsi a Apache HBase.	 	   |
| [HDFS ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.hdfs/)          | Fornisce gli operatori e le funzioni che interagiscono con Hadoop Distributed File System.	|
| [Internet (Inet) ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.inet)|  Si concentra sull'interazione con i dati ospitati nella rete.				       |
| [IoT ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.iot/)            | Fornisce l'integrazione Internet of Things (IoT) incluso IBM Watson IoT Platform, entrambi in {{site.data.keyword.Bluemix_notm}} o in loco ({{site.data.keyword.streamsshort}}). |
| [JDBC ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.jdbc/)          | Abilita le applicazioni Streams ad utilizzare il database tramite JDBC.		   |
| [JSON ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.json/)          | Ti consente di convertire i dati da JSON nel formato tuple Streams e viceversa.   		|
| [Kafka ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://ibmstreams.github.io/streamsx.kafka/)       | Abilita le applicazioni Streams ad integrarsi facilmente con Apache Kafka. 	 |
| [MessageHub ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://ibmstreams.github.io/streamsx.messagehub/) | Abilita le applicazioni Streams ad utilizzare MessageHub.			     |
| [Messaging ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://ibmstreams.github.io/streamsx.messaging/)   |  	Si concentra sull'interazione con i sistemi di messaggistica popolari come Kafka, MQTT, JMS e XMS	<br>**Nota**: per utilizzare JMSSource, JMSSink, XMSSource, XMSSink con WebSphere MQ, completa la seguente procedura nel tuo ambiente di sviluppo: <br>1. Vai a [IBMStreams su GitHub ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://github.com/IBMStreams){:new_window} e scarica Messaging Toolkit (com.ibm.streamsx.messaging) versione 3.0.0 o successiva nel tuo ambiente di sviluppo.<br>2. Utilizza la versione 5.1.0 o successiva del toolkit per creare la tua applicazione.<br>3. Inserisci il file .bindings necessario nella directory `/etc` della tua applicazione per includerlo nel bundle dell'applicazione {{site.data.keyword.streamsshort}}.	    |
| [Mining ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://ibm.co/2y3i5au)              	   	            |  Include operatori che puoi utilizzare per esaminare i flussi di dati applicando dei modelli. <br> **Limitazione:** questo toolkit non è supportato se stai utilizzando i [piani Beta-Entry e Beta-Enhanced](/docs/services/StreamingAnalytics/beta_plans.html), poiché devi compilare il tuo bundle dell'applicazione in un ambiente RHEL 7 o in una versione CentOS equivalente. 	     |
| [RabbitMQ ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://ibmstreams.github.io/streamsx.rabbitmq/)     |  Fornisce gli operatori che consentono alle tue applicazioni Streams di leggere e inviare messaggi da Rabbit MQ.  |
| [R-project ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://ibm.co/2h7D9lu)          	   	              |   Include l'operatore RScript, che puoi utilizzare per eseguire i comandi R e applicare algoritmi di data mining complessi per individuare pattern di interesse nei flussi di dati.			     |
| [Topology ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.topology/)      |  Fornisce la capacità di creare le applicazioni di gestione flussi Python per il servizio {{site.data.keyword.streaminganalyticsshort}} nella piattaforma {{site.data.keyword.Bluemix_notm}} e {{site.data.keyword.streamsshort}}.		     |
| [DPS ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.dps/) |	 Abilita più applicazioni che stanno eseguendo gli elementi elaborati (PEs) su una o più macchine a condividere le informazioni di stato specifiche per l'applicazione.<br>**Limitazione:** è supportato solo REDIS come database di backend.	| 	 	 	
| [Geospatial ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://ibm.co/2h9x0VR) 	     |	Include operatori e funzioni che facilitano l'indicizzazione e l'elaborazione efficiente dei dati locali.<br>**Limitazione:** gli operatori che utilizzano la modalità di associazione non sono supportati `MapStore`, `PointMapMatcher` nella modalità di associazione condivisa).		 |
| [TEDA ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://ibm.co/2z9DS00)	   | 	Fornisce una serie di operatori generici utilizzati nelle applicazioni di telecomunicazioni e fornisce inoltre un framework dell'applicazione che ti consente di configurare nuove applicazioni file-to-file. Inizia seguendo [TEDA tutorials ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://ibmstreams.github.io/streamsx.tutorial.teda/). Tutti gli operatori e le funzioni del toolkit sono supportati. <br>**Limitazione:** il framework dell'applicazione non è supportato.	 	 |
| [TimeSeries ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://ibm.co/2zEPILZ)	 	  | Le funzioni e gli operatori in TimeSeries Toolkit condizionano, analizzano e modellano i dati delle serie temporali. <br>**Limitazione:** gli operatori obsoleti non sono supportati.	   |

*Tabella 1. Toolkit supportati*

## Altri toolkit e operatori
{: #other_operators}

Gli altri operatori, inclusi gli operatori toolkit che hai sviluppato per i tuoi bisogni, possono essere supportati da {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

I toolkit devono rispettare i seguenti criteri per essere compatibili con {{site.data.keyword.streaminganalyticsshort}}:

1. Nessun software aggiuntivo deve essere preinstallato sui nodi dell'applicazione della tua istanza del servizio.
2. Tutte le informazioni di configurazione che richiede il toolkit possono essere incluse nel bundle dell'applicazione utilizzando il toolkit.
