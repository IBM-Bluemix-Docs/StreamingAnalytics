---

copyright:
  years: 2015, 2019
lastupdated: "2018-12-06"

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


Commencez par utiliser les [modèles d'application](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps) pour apprendre à soumettre et surveiller une application Beam dans le service {{site.data.keyword.streaminganalyticsshort}}. Vous pouvez télécharger les modèles d'applications à partir de la console {{site.data.keyword.streaminganalyticsshort}}.

Reportez-vous à la [documentation {{site.data.keyword.streamsshort}} Runner for Apache Beam ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/){:new_window} pour consulter des tables qui montrent comment Streams Runner s'intègre à la [matrice de capacité Beam](https://beam.apache.org/documentation/runners/capability-matrix/). Voir [Installing IBM Streams Runner for Apache Beam ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://bit.ly/2zFDpPr){:new_window} pour des instructions d'installation du kit d'outils `com.ibm.streams.beam` dans votre environnement Streams pour créer des applications Beam que vous pouvez soumettre et surveiller dans {{site.data.keyword.streaminganalyticsshort}}.

Il est recommandé de posséder des connaissances en programmation Beam, mais pas nécessaire ; le [site Web Apache Beam ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://beam.apache.org/documentation/){:new_window} présente une page [Apache Beam Java SDK Quickstart ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://beam.apache.org/get-started/quickstart-java/){:new_window} utile ainsi que d'autres documents.
