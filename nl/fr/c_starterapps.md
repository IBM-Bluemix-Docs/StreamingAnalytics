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

# Modèles d'application
{: #starterapps}

Déployez et modifiez les applications de démarrage et apprenez rapidement à utiliser le service {{site.data.keyword.streaminganalyticsshort}}. Notez que les plans de service version 2 requièrent l'exécution de Streams sous RHEL 7. {{site.data.keyword.streaminganalyticsshort}} fournit un [ensemble d'applications de démarrage et de modèles d'application](https://developer.ibm.com/streamsdev/docs/starter-sample-apps-v2-plans/) pour que vous puissiez commencer à utiliser rapidement les plans de service version 2. Les modèles d'application EventDetection et NYCTraffic ne fonctionnent pas avec les plans de service version 2.
{:shortdesc}


<table summary="La première ligne de ce tableau décrit l'application de démarrage Stock Trades. La deuxième ligne inclut :
1. Dans la première colonne, un lien vers une vidéo expliquant comment déployer l'application de démarrage Stock Trades. 2. Dans la deuxième colonne, un lien permettant de télécharger directement l'application de démarrage Stock Trades.
">
  <tr>
    <th id="stocktrades" colspan="3">Modèle d'application Stock Trades<br></th>
  </tr>
  <tr>
    <td headers="stocktrades" colspan="3">Cette application analyse un flux d'actions en bourse et génère la moyenne des prix à l'aide de l'opérateur <a href="https://www.ibm.com/support/knowledgecenter/SSCRJU_4.3.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$spl/op$spl.relational$Aggregate.html">Aggregate ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a>.
Vous pouvez exécuter l'application de démarrage sans modification. Si vous souhaitez expérimenter le service plus en profondeur, vous pouvez modifier le code et renvoyer vos modifications dans l'environnement {{site.data.keyword.Bluemix_short}}. La source intégrale de l'application de démarrage est <a href="https://github.com/IBMStreams/samples/tree/master/QuickStart/TradesApp">disponible sur GitHub ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a>.</p>
</td>
  </tr>
  <tr>
    <td headers="stocktrades"><a href="https://developer.ibm.com/streamsdev/videos/getting-started-streaming-analytics-service-using-trades-starter-application/" target="_blank">DEPLOYER L'APPLICATION ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a><br></td>
    <td headers="stocktrades"><a href="https://github.com/IBMStreams/samples/raw/master/QuickStart/TradesApp/starterApp/StockTradesStarterApp.sab" target="_blank">TELECHARGEMENT ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a></td>
  </tr>
</table>

*Tableau 1. Modèle d'application Stock Trades*


<table summary="Ce tableau décrit, sur la première ligne, le modèle d'application Event Detection version 2. Il inclut les éléments suivants sur la deuxième ligne :
1. Dans la première colonne, un lien vers les instructions de déploiement de l'application de démarrage Event Detection version 2. 2. Dans la deuxième colonne, un lien vers des tutoriels expliquant comment utiliser l'application de démarrage Event Detection. 3. Dans la troisième colonne, un lien permettant de télécharger directement l'application de démarrage Event Detection.
 ">
  <tr>
    <th id="EventDetection2" colspan="3">Modèle d'application Event Detection version 2<br></th>
  </tr>
  <tr>
    <td colspan="3" headers="EventDetection2">L'application Event Detection v2 est implémentée via l'exécution de <a href="https://{DomainName}/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">SDK for Node.js ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a>. Cette application de démarrage est uniquement compatible avec des [plans de service version 2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans).
Elle fournit une interface utilisateur Web simple pour afficher le statut et les résultats de l'analyse.
L'application Node.js est liée à une instance du service {{site.data.keyword.streaminganalyticsshort}}. L'application contrôle le service via l'interface API REST {{site.data.keyword.streaminganalyticsshort}} version 2.
<p>Vous pouvez exécuter l'application de démarrage sans modification.
Si vous souhaitez expérimenter le service plus en profondeur, vous pouvez modifier le code et renvoyer vos modifications dans l'environnement {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td headers="EventDetection2"><a href="/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps_deploy#starterapps_deploy" target="_blank">DEPLOYER L'APPLICATION</a><br></td>
    <td headers="EventDetection2"><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">TUTORIEL ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a></td>
    <td headers="EventDetection2"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetectionV2" target="_blank">TELECHARGEMENT ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a></td>
  </tr>
</table>

*Tableau 2. Modèle d'application Event Detection version 2*
<table summary="La première ligne de ce tableau décrit le modèle d'application Event Detection. La deuxième ligne inclut les éléments suivants :
1. Dans la première colonne, un lien vers les instructions de déploiement de l'application de démarrage. 2. Dans la deuxième colonne, un lien vers les tutoriels sur l'utilisation de l'application de démarrage. 3. Dans la troisième colonne, un lien pour le téléchargement direct de l'application de démarrage Event Detection.
">
  <tr>
    <th id="EventDetection1" colspan="3">Modèle d'application Event Detection<br></th>
  </tr>
  <tr>
    <td headers="EventDetection1" colspan="3">L'application Event Detection est implémentée via l'exécution de <a href="https://{DomainName}/catalog/starters/sdk-for-nodejs/?cm_mmc=dw-_-bluemix-_-ba-bluemix-detect-complex-events-from-data-stream-trs-_-article">SDK for Node.js ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a>.
Cette application de démarrage est uniquement compatible avec des [plans de service version 1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans). Elle fournit une interface utilisateur Web simple pour afficher le statut et les résultats de l'analyse.
L'application Node.js est liée à une instance du service {{site.data.keyword.streaminganalyticsshort}}. L'application contrôle le service via l'interface API REST {{site.data.keyword.streaminganalyticsshort}}.
<p>Vous pouvez exécuter l'application de démarrage sans modification.
Si vous souhaitez expérimenter le service plus en profondeur, vous pouvez modifier le code et renvoyer vos modifications dans l'environnement {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td headers="EventDetection1"><a href="/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps_deploy" target="_blank">DEPLOYER L'APPLICATION</a><br></td>
    <td headers="EventDetection1"><a href="https://developer.ibm.com/streamsdev/docs/detect-events-with-streams/" target="_blank">TUTORIEL ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a></td>
    <td headers="EventDetection1"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/EventDetection" target="_blank">TELECHARGEMENT ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a></td>
  </tr>
</table>

*Tableau 2. Modèle d'application Event Detection*

<table summary="La première ligne de ce tableau décrit le modèle d'application relatif au trafic new-yorkais. La deuxième ligne inclut les éléments suivants :
1. Dans la première colonne, un lien vers les instructions de déploiement du modèle d'application. 2. Dans la deuxième colonne, un lien vers les tutoriels sur l'utilisation du modèle d'application. 3. Dans la troisième colonne, un lien pour le téléchargement direct du modèle d'application relatif au trafic new-yorkais. ">
  <tr>
    <th id="NYCTraffic" colspan="3">Modèle d'application NYC Traffic<br></th>
  </tr>
  <tr>
    <td headers="NYCTraffic" colspan="3">L'application de démarrage NYC Traffic est une application pour {{site.data.keyword.Bluemix_short}} écrite en Liberty for Java. Elle contient une application {{site.data.keyword.streamsshort}} qui extrait des données publiques à partir des détecteurs de trafic de la ville de New York, calcule des statistiques d'agrégat et renvoie les résultats à l'application Liberty. Cette application de démarrage est uniquement compatible avec des [plans de service version 1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans).
<p>Vous pouvez exécuter l'application de démarrage sans modification. Si vous souhaitez expérimenter le service plus en profondeur, vous pouvez modifier le code et renvoyer vos modifications dans l'environnement {{site.data.keyword.Bluemix_short}}.</p>
</td>
  </tr>
  <tr>
    <td headers="NYCTraffic" deploylink><a href="/docs/services/StreamingAnalytics/?topic=StreamingAnalytics-starterapps_deploy" target="_blank">DEPLOYER L'APPLICATION</a><br></td>
    <td headers="NYCTraffic"><a href="https://developer.ibm.com/streamsdev/docs/bluemix-streaming-analytics-starter-application/" target="_blank">TUTORIEL ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a></td>
    <td headers="NYCTraffic"><a href="https://streams-github-samples.mybluemix.net/?get=QuickStart/NYCTraffic" target="_blank">TELECHARGEMENT ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a></td>
  </tr>
</table>

*Tableau 3. Modèle d'application NYC Traffic*

## Modèles d'Application IBM Streams Runner for Apache Beam

<table summary="La première ligne de ce tableau décrit l'application Beam TemperatureSample. La seconde ligne du tableau inclut un lien menant vers un tutoriel expliquant comment déployer l'application Beam TemperatureSample.
">
  <tr>
    <th id="TemperatureSample" colspan="3">Application Beam TemperatureSample<br></th>
  </tr>
  <tr>
    <td headers="TemperatureSample" colspan="3">Cette application prend des lectures de température issues de plusieurs appareils. Cette application de démarrage est uniquement disponible pour des [plans de service version 2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans). Elle répartit ces lectures en lectures "satisfaisantes" (valides) et "mauvaises" (non valides) en fonction d'un seuil établi. Elle compte les mauvaises lectures, génère des statistiques de base concernant les lectures satisfaisantes, puis consigne les résultats. Vous pouvez télécharger l'application TemperatureSample à partir de la console Streaming Analytics.
</td>
  </tr>
  <tr>
    <td headers="TemperatureSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/sample/#running-the-temperaturesample-application" target="_blank">DEPLOYER L'APPLICATION ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a><br></td>
    <td headers="TemperatureSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/sample/#viewing-the-running-application" target="_blank">AFFICHER L'APPLICATION ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a></td>
  </tr>
</table>

*Tableau 4. Application TemperatureSample*

<table summary="La première ligne de ce tableau décrit le modèle d'application Beam WordCount. La seconde ligne du tableau inclut un lien menant à un tutoriel indiquant comment déployer le modèle d'application WordCount.
">
  <tr>
    <th id="WordCountSample" colspan="3">Modèle d'application WordCount<br></th>
  </tr>
  <tr>
    <td headers="WordCountSample" colspan="3">Le modèle d'application Apache Beam 2.0 Java SDK Quickstart WordCount crée des pipelines réutilisables et gérables qui peuvent lire un fichier texte, appliquer des transformations afin de segmenter et compter les mots, et écrire les données dans un fichier texte de sortie.
</td>
  </tr>
  <tr>
    <td headers="WordCountSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/wordcount/" target="_blank">DEPLOYER L'APPLICATION ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a><br></td>
  </tr>
</table>

*Tableau 5. Modèle d'application WordCount*

<table summary="La première ligne de ce tableau décrit le modèle d'application FileStreamSample. La deuxième ligne inclut un lien vers un tutoriel expliquant comment déployer l'application FileStreamSample.
">
  <tr>
    <th id="FilterStreamSample" colspan="3">Application FileStreamSample<br></th>
  </tr>
  <tr>
    <td headers="FilterStreamSample" colspan="3">Vous pouvez utiliser le modèle d'application FileStreamSample d'IBM® Streams Runner for Apache Beam pour apprendre à utiliser le stockage d'objets {{site.data.keyword.Bluemix_notm}} pour l'entrée et la sortie de fichier.
</td>
  </tr>
  <tr>
    <td headers="FilterStreamSample"><a href="http://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/objstor/" target="_blank">DEPLOYER L'APPLICATION ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")</a><br></td>
  </tr>
</table>

*Tableau 6. Application FileStreamSample*
