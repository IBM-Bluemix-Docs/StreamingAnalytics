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

# Utilisation des applications de démarrage Streaming Analytics
{: #starterapps}

Déployez et modifiez les applications de démarrage et apprenez rapidement comment utiliser le service {{site.data.keyword.streaminganalyticsshort}} :
{:shortdesc}

<table summary="Ce tableau décrit, dans la première ligne, l'application de démarrage Stock Trades. Dans la seconde ligne, il inclut : 1. Dans la première colonne, un lien vers une vidéo illustrant comment déployer l'application de démarrage Stock Trades. 2. Dans la seconde colonne, un lien permettant de télécharger directement l'application de démarrage Stock Trades.">
  <tr>
    <th colspan="3">Application exemple Stock Trades<br></th>
  </tr>
  <tr>
    <td colspan="3">Cette application analyse un flux d'actions en bourse et génère la moyenne des prix à l'aide de l'opérateur <a href="https://www.ibm.com/support/knowledgecenter/SSCRJU_4.2.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$spl/op$spl.relational$Aggregate.html">Aggregate</a>.
Vous pouvez exécuter l'application de démarrage sans modification. Si vous souhaitez expérimenter le service plus en profondeur, vous pouvez modifier le code et renvoyer vos modifications dans l'environnement {{site.data.keyword.Bluemix_short}}. La source intégrale de l'application de démarrage est <a href="https://github.com/IBMStreams/samples/tree/master/QuickStart/TradesApp">disponible sur GitHub</a>.</p>
</td>
  </tr>
  <tr>
    <td><a href="https://developer.ibm.com/streamsdev/videos/getting-started-streaming-analytics-service-using-trades-starter-application/" target="_blank">DEPLOYER L'APPLICATION</a><br></td>
    <td><a href="https://github.com/IBMStreams/samples/raw/master/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab" target="_blank">TELECHARGER</a></td>
  </tr>
</table>

*Tableau 1. Application exemple Stock Trades*


<table summary="Ce tableau décrit, sur la première ligne, l'application exemple Event Detection. Il inclut, sur la deuxième ligne, les éléments suivants : 1. Dans la première colonne, un lien vers les instructions de déploiement de l'application de démarrage. 2. Dans la deuxième colonne, un lien vers les tutoriels sur l'utilisation de l'application de démarrage. 3. Dans la troisième colonne, un lien pour le téléchargement direct de l'application de démarrage Event Detection.">
  <tr>
    <th colspan="3">Application exemple Event Detection<br></th>
  </tr>
  <tr>
    <td colspan="3">L'application Event Detection est implémentée via la phase d'exécution <a href="https://console.ng.bluemix.net/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">{{site.data.keyword.sdk4node}}</a>.
Elle fournit une interface utilisateur Web simple pour afficher le statut et les résultats de l'analyse.
L'application Node.js est liée à une instance du service {{site.data.keyword.streaminganalyticsshort}}. L'application contrôle le service via l'interface API REST {{site.data.keyword.streaminganalyticsshort}}.
<p>Vous pouvez exécuter l'application de démarrage sans modification.
Si vous souhaitez expérimenter le service plus en profondeur, vous pouvez modifier le code et renvoyer vos modifications dans l'environnement {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">DEPLOYER_L'APPLICATION</a><br></td>
    <td><a href="http://www.ibm.com/developerworks/library/ba-bluemix-detect-complex-events-from-data-stream-trs/index.html" target="_blank">TUTORIEL</a></td>
    <td><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection" target="_blank">TELECHARGER</a></td>
  </tr>
</table>

*Tableau 2. Application exemple Event Detection*

<table summary="Ce tableau décrit, sur la première ligne, l'application exemple relative au trafic new-yorkais. Il inclut, sur la deuxième ligne, les éléments suivants : 1. Dans la première colonne, un lien vers les instructions de déploiement de l'application exemple. 2. Dans la deuxième colonne, un lien vers les tutoriels sur l'utilisation de l'application exemple. 3. Dans la troisième colonne, un lien pour le téléchargement direct de l'application exemple relative au trafic new-yorkais.">
  <tr>
    <th colspan="3">Application exemple NYC Traffic<br></th>
  </tr>
  <tr>
    <td colspan="3">L'application de démarrage NYC Traffic est une application pour {{site.data.keyword.Bluemix_short}} écrite en Liberty for Java. Elle contient une application {{site.data.keyword.streamsshort}} qui extrait des données publiques à partir des détecteurs de trafic de la ville de New York, calcule des statistiques d'agrégat et renvoie les résultats à l'application Liberty.
<p>Vous pouvez exécuter l'application de démarrage sans modification. Si vous souhaitez expérimenter le service plus en profondeur, vous pouvez modifier le code et renvoyer vos modifications dans l'environnement {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td><a href="/docs/services/StreamingAnalytics/t_starter_app_deploy.html" target="_blank">DEPLOYER_L'APPLICATION</a><br></td>
    <td><a href="https://developer.ibm.com/streamsdev/docs/bluemix-streaming-analytics-starter-application/" target="_blank">TUTORIEL</a></td>
    <td><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic" target="_blank">TELECHARGER</a></td>
  </tr>
</table>

*Tableau 3. Application exemple NYC Traffic*

## Exemples d'applications IBM Streams Runner for Apache Beam

<table summary="La première ligne de ce tableau décrit l'application Beam TemperatureSample. La seconde ligne du tableau inclut un lien menant vers un tutoriel indiquant comment déployer l'application Beam TemperatureSample.">
  <tr>
    <th colspan="3">Application Beam `TemperatureSample`<br></th>
  </tr>
  <tr>
    <td colspan="3">Cette application prend des lectures de température issues de plusieurs appareils. Elle répartit ces lectures en lectures "satisfaisantes" (valides) et "mauvaises" (non valides) en fonction d'un seuil établi. Elle compte les mauvaises lectures, génère des statistiques de base concernant les lectures satisfaisantes, puis consigne les résultats. Vous pouvez télécharger l'application TemperatureSample à partir de la console Streaming Analytics.
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3-sample/#running-the-temperaturesample-application" target="_blank">DEPLOYER_L'APPLICATION</a><br></td>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3-sample/#viewing-the-running-application" target="_blank">AFFICHER L'APPLICATION</a></td>
  </tr>
</table>

*Tableau 4. Application TemperatureSample*

<table summary="La première ligne de ce tableau décrit l'application exemple Beam WordCount. La seconde ligne du tableau inclut un lien menant à un tutoriel indiquant comment déployer l'application exemple WordCount. ">
  <tr>
    <th colspan="3">Application exemple WordCount<br></th>
  </tr>
  <tr>
    <td colspan="3">L'application exemple Apache Beam 2.0 Java SDK Quickstart WordCount crée des pipelines réutilisables et gérables qui peuvent lire un fichier texte, appliquer des transformations afin de segmenter et compter les mots, et écrire les données dans un fichier texte de sortie.
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-3b-wordcount/" target="_blank">DEPLOYER_L'APPLICATION</a><br></td>
  </tr>
</table>

*Tableau 5. Exemple d'application `WordCount`*

<table summary="La première ligne de ce tableau décrit l'exemple d'application `FileStreamSample`. La seconde ligne du tableau inclut un lien menant à un tutoriel indiquant comment déployer l'application `FileStreamSample`. ">
  <tr>
    <th colspan="3">Application FileStreamSample<br></th>
  </tr>
  <tr>
    <td colspan="3">Vous pouvez utiliser l'exemple d'application FileStreamSample d'IBM® Streams Runner for Apache Beam pour apprendre à utiliser le stockage d'objets {{site.data.keyword.Bluemix_notm}} pour l'entrée et la sortie de fichier.
</td>
  </tr>
  <tr>
    <td><a href="https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-5b-objstor/" target="_blank">DEPLOYER_L'APPLICATION</a><br></td>
  </tr>
</table>

*Tableau 6. Application `FileStreamSample`*
