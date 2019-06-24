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

# Déploiement d'applications Beam dans Streaming Analytics
{: #develop_beam_apps}

Vous pouvez désormais développer des applications Beam dans votre environnement de développement local {{site.data.keyword.streamsshort}} et déployer ces applications dans {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

{{site.data.keyword.streamsshort}} Runner for Apache Beam exécute des pipelines Beam dans un environnement {{site.data.keyword.streamsshort}}. Une application Beam lancée avec Streams Runner est convertie en un fichier SAB (Streams Application Bundle) que vous pouvez ensuite déployer et surveiller dans {{site.data.keyword.streaminganalyticsshort}}.

Pour soumettre une application Beam auprès de votre service {{site.data.keyword.streaminganalyticsshort}} sur {{site.data.keyword.Bluemix_notm}}, vous devez créer un fichier VCAP au format JSON contenant les données d'identification et d'autres informations liées au service.

1. Dans votre environnement local Streams, accédez au sous-dossier samples dans lequel vous avez installé le kit d'outils (`$STREAMS_BEAM_RUNNER/samples`) et copiez le fichier template.vcap dans un nouveau fichier. Attribuez à ce fichier un nom significatif, ainsi qu'une extension de fichier `.vcap.`
1. [Copiez les données d'identification de votre service {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans#vcap_services) et collez-les dans le fichier VCAP que vous avez créé en remplaçant la ligne suivante :
```
 <REMOVE THIS LINE AND INSERT CREDENTIALS HERE>
 ```
1. Vérifiez que votre application Beam s'exécute correctement dans votre environnement de développement. Lorsque vous lancez votre application Beam avec Streams Runner, elle est convertie en un fichier SAB (Streams Application Bundle).
1. Soumettez le fichier SAB associé à votre application Beam auprès de {{site.data.keyword.streaminganalyticsshort}}

Votre application est maintenant déployée dans le cloud. Vous pouvez la surveiller avec le service {{site.data.keyword.streaminganalyticsshort}}.

Pour plus d'informations sur le déploiement et la surveillance de vos applications Beam dans {{site.data.keyword.streaminganalyticsshort}}, voir [Streams Runner for Apache Beam ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/).
