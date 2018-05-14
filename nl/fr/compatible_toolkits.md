---

copyright:
  years: 2015, 2018
lastupdated: "2018-04-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Kits d'outils et adaptateurs pris en charge
{: #compatible_toolkits}

Ces kits d'outils d'analyse et adaptateurs sont pris en charge par {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

| Kits d'outils                        | Description							                  |
| --------------------------------| --------------------------|
| [Complex Event Processing (CEP) ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://ibm.co/2zOwODa)    |	Fournit l'opérateur MatchRegex pour traiter les événements complexes.  		 |
| [Datetime ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://ibmstreams.github.io/streamsx.datetime/)	|	Ensemble d'utilitaires permettant de traiter les dates, les heures et les horodatages.	 |
| [HBase![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.hbase/)        | Permet aux applications Streams de se connecter à Apache HBase.	 	   |
| [HDFS ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.hdfs/)          | Fournit des opérateurs et des fonctions qui interagissent avec Hadoop Distributed File System.	|
| [Internet (Inet) ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.inet)|  Met l'accent sur l'interaction avec des données hébergées sur le réseau.				       |
| [IoT ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.iot/)            | Fournit l'intégration IoT (Internet of Things) comprenant IBM Watson IoT Platform, dans {{site.data.keyword.Bluemix_notm}} ou sur site ({{site.data.keyword.streamsshort}}). |
| [JDBC ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.jdbc/)          | Permet aux applications Streams de fonctionner avec des bases de données via JDBC.		   |
| [JSON ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.json/)          | Permet de convertir des données du format JSON au format de tuple Streams, et inversement.   		|
| [Kafka ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://ibmstreams.github.io/streamsx.kafka/)       | Permet aux applications Streams de s'intégrer facilement avec Apache Kafka. 	 |
| [MessageHub ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://ibmstreams.github.io/streamsx.messagehub/) | Permet aux applications Streams de fonctionner avec MessageHub.			     |
| [Messaging ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://ibmstreams.github.io/streamsx.messaging/)   |  	Met l'accent sur l'interaction avec des systèmes de messagerie populaires, tels que Kafka, MQTT, JMS et XMS	<br>**Remarque** : pour utiliser JMSSource, JMSSink, XMSSource, XMSSink avec WebSphere MQ, effectuez la procédure ci-dessous dans votre environnement de développement : <br>1. Accédez à [IBMStreams on GitHub ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://github.com/IBMStreams){:new_window} et téléchargez Messaging Toolkit (com.ibm.streamsx.messaging) version 3.0.0 ou ultérieure dans votre environnement de développement.<br>2. Utilisez la version 5.1.0 du kit d'outils ou une version ultérieure pour générer votre application.<br>3. Placez le fichier .bindings requis dans le répertoire `/etc` de votre application pour l'inclure dans le bundle d'applications {{site.data.keyword.streamsshort}}.	    |
| [Mining ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://ibm.co/2y3i5au)              	   	            |  Inclut des opérateurs que vous pouvez utiliser pour explorer des flux de données en appliquant des modèles. <br> **Restriction :** ce kit d'outils n'est pas pris en charge si vous utilisez les [plans Beta-Entry et Beta-Enhanced](/docs/services/StreamingAnalytics/beta_plans.html) car vous devez compiler votre bundle d'applications dans un environnement RHEL 7 ou une version CentOS équivalente. 	     |
| [RabbitMQ ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://ibmstreams.github.io/streamsx.rabbitmq/)     |  Fournit des opérateurs qui permettant à votre application Streams de lire et d'envoyer des messages à partir de Rabbit MQ.  |
| [R-project ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://ibm.co/2h7D9lu)          	   	              |   Inclut l'opérateur RScript, que vous pouvez utiliser pour exécuter des commandes R et appliquer des algorithmes d'exploration de données complexes pour détecter des zones d'intérêt dans les flux de données.			     |
| [Topology ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.topology/)      |  Permet de créer des applications Python de diffusion en flux pour le service {{site.data.keyword.streaminganalyticsshort}} sur la plateforme {{site.data.keyword.Bluemix_notm}} et {{site.data.keyword.streamsshort}}.		     |
| [DPS ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.dps/) |	 Permet à plusieurs applications exécutant des éléments de traitement sur une ou plusieurs machines de partager des informations d'état spécifiques aux applications.<br>**Restriction :** Seul REDIS est pris en charge comme système de back end de base de données.	| 	 	 	
| [Geospatial ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://ibm.co/2h9x0VR) 	     |	Inclut des opérateurs et des fonctions qui facilitent le traitement efficace et l'indexation des données de localisation.<br>**Restriction :** Les opérateurs utilisant le mode de carte partagée ne sont pas pris en charge (`MapStore`, `PointMapMatcher` en mode carte partagée).		 |
| [TEDA ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://ibm.co/2z9DS00)	   | 	Fournit un ensemble d'opérateurs génériques utilisés dans les applications de télécommunication, ainsi qu'une structure d'application qui vous permet de configurer de nouvelles applications fichier à fichier. Initiez-vous en suivant les [tutoriels TEDA ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.tutorial.teda/). Tous les opérateurs et toutes les fonctions du kit d'outils sont pris en charge. <br>**Restriction :** La structure d'application n'est pas prise en charge.	 	 |
| [TimeSeries ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://ibm.co/2zEPILZ)	 	  | Les opérateurs et fonctions du kit d'outils TimeSeries Toolkit conditionnent, analysent et modèlent les données de séries temporelles. <br>**Restriction :** Les opérateurs obsolètes ne sont pas pris en charge.	   |
| [{{site.data.keyword.cos_short}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://bit.ly/2Ggp03T)	 	  | Fournit des opérateurs primitifs et des fonctions natives pour lire et écrire des données dans {{site.data.keyword.cos_short}} respectivement. Le kit d'outils prend en charge {{site.data.keyword.cos_short}} compatible avec S3.	   |

*Tableau 1. Kits d'outils pris en charge*

## Autres kits d'outils et opérateurs
{: #other_operators}

D'autres opérateurs, notamment les opérateurs des kits d'outils que vous avez développés pour vos propres besoins, peuvent être pris en charge par {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

Les kits d'outils doivent répondre aux critères suivants pour être compatibles avec {{site.data.keyword.streaminganalyticsshort}} :

1. Aucune préinstallation de logiciel supplémentaire n'est requise sur les noeuds d'application de votre instance de service.
2. Toutes les informations de configuration requises par le kit d'outils peuvent être incluses dans le bundle d'applications à l'aide du kit d'outils.
