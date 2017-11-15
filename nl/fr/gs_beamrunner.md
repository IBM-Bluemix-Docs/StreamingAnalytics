---

copyright:
  years: 2015, 2017
lastupdated: "2017-10-27"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# IBM Streams Runner for Apache Beam dans Streaming Analytics
{: #gs_beamrunner}

Si vous disposez d'un environnement de développement {{site.data.keyword.streamsshort}}, vous pouvez maintenant développer des applications Beam en local dans votre environnement, puis les soumettre au service {{site.data.keyword.streaminganalyticsshort}} dans {{site.data.keyword.Bluemix_notm}}. {{site.data.keyword.streamsshort}} Runner for Apache Beam exécute des pipelines Beam dans un environnement {{site.data.keyword.streamsshort}}. Une application Beam lancée avec Streams Runner est convertie en un fichier SAB (Streams Application Bundle) que vous pouvez ensuite déployer et surveiller dans {{site.data.keyword.streaminganalyticsshort}}.


Commencez par utiliser les [exemples d'applications](/docs/services/StreamingAnalytics/c_starterapps.html) pour apprendre à soumettre et surveiller une application Beam dans le service {{site.data.keyword.streaminganalyticsshort}}. Vous pouvez télécharger les exemples d'applications à partir de la console {{site.data.keyword.streaminganalyticsshort}}.

Consultez la [documentation {{site.data.keyword.streamsshort}} Runner for Apache Beam](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/) pour prendre connaissances des tableaux qui indiquent comment Streams Runner s'adapte à la [matrice de fonctionnalités Beam]. Pour obtenir des instructions sur l'installation du kit d'outils `com.ibm.streams.beam` dans votre environnement Streams afin de créer des applications Beam que vous pouvez soumettre et surveiller dans {{site.data.keyword.streaminganalyticsshort}}, voir [Installing IBM Streams Runner for Apache Beam](http://bit.ly/2zFDpPr). 

Il est conseillé, mais pas nécessaire de posséder des connaissances en programmation Beam ; le [site Web Apache Beam](https://beam.apache.org/documentation/){:new_window} comprend une page de démarrage rapide [Apache Beam Java SDK Quickstart](https://beam.apache.org/get-started/quickstart-java/){:new_window} ainsi qu'une documentation.
