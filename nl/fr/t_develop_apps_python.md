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

# Développement d'applications Python dans Streaming Analytics
{: #t_develop_apps_python}

Vous pouvez désormais développer des applications Python dans {{site.data.keyword.DSX_full}} ou dans votre environnement de développement Python local et déployer ces applications dans {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

Développez et déployez vos applications Python dans {{site.data.keyword.Bluemix_short}} avec le service {{site.data.keyword.streaminganalyticsshort}} via l'une des méthodes suivantes :


## Développement d'applications Python Streams dans Watson Studio
{: #t_develop_python_dsx}

Si vous ne disposez pas d'un environnement de développement Python, la façon la plus rapide de démarrer est d'utiliser les fichiers notebook {{site.data.keyword.streamsshort}} {{site.data.keyword.DSX_short}} et de créer des modèles d'application Python. Ces fichiers notebook fournissent les procédures et les codes exemple pour créer et déployer des modèles d'application Python simples pour le service {{site.data.keyword.streaminganalyticsshort}} au sein de l'environnement {{site.data.keyword.DSX_short}} Python :

* [Hello World! ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039ca9c6e8) : créez une application Hello World! simple pour démarrer puis déployez l'application dans une instance du service {{site.data.keyword.streaminganalyticsshort}}.

* [Healthcare Demo ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039cad29a6) : créez une application qui ingère et analyse des données de diffusion en flux depuis un flux, puis les visualise dans le bloc-notes. Ensuite, soumettez cette application à l'instance de service {{site.data.keyword.streaminganalyticsshort}}.

* [Neural Net Demo![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039ca60bb7) : créez un exemple d'ensemble de données, créez un modèle de données, utilisez ce modèle dans une application de diffusion en flux continu, visualisez le flux de données en continu et soumettez l'application de diffusion en flux continu au service.

## Développement d'applications dans votre environnement Python local
 {: #t_develop_python_api}

L'[API d'application Python {{site.data.keyword.streamsshort}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features), incluse dans le package streamsx, vous permet de créer des applications de traitement de flux avec des fonctions ou des classes appelables Python. Vous pouvez utiliser l'API d'application Python pour ensuite définir et soumettre l'application au service.

Commencez par suivre les étapes décrites dans le tutoriel [Developing for the {{site.data.keyword.streaminganalyticsshort}} service ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html). Dans ce tutoriel, vous créez un modèle d'application dans votre environnement Python local et vous le déployez dans le service {{site.data.keyword.streaminganalyticsshort}}.

Pour maîtriser l'API d'application Python {{site.data.keyword.streamsshort}} de façon plus approfondie, suivez [ce cours en ligne ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/courses/all/streaming-analytics-basics-python-developers/){:new_window} et apprenez les concepts de base de {{site.data.keyword.streaminganalyticsshort}} pour les développeurs Python.
