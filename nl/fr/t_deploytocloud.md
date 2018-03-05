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

# Déploiement d'applications Streams dans le cloud
{: #t_deploytocloud}

Vous pouvez déployer vos applications {{site.data.keyword.streamsshort}} dans une instance {{site.data.keyword.streaminganalyticsshort}} s'exécutant dans {{site.data.keyword.Bluemix_short}}.
{:shortdesc}

Les applications {{site.data.keyword.streamsshort}} sont écrites en {{site.data.keyword.streamsshort}} Processing Language (SPL), SPL, Java, Scala ou Python dans un environnement {{site.data.keyword.streamsshort}}. Vous pouvez désormais développer des applications Streams Python sans passer par un environnement {{site.data.keyword.streamsshort}}. Voir la rubrique relative au [déploiement des applications {{site.data.keyword.streamsshort}} dans le cloud](docs/services/StreamingAnalytics/t_deploytocloud.html#t_deploypython)


{{site.data.keyword.streaminganalyticsshort}} n'inclut pas de développement d'environnement {{site.data.keyword.streamsshort}} dans le cloud mais vous pouvez déployer les applications que vous développez localement dans le cloud.

Avant de commencer, désactivez le logiciel de blocage d'incrustation de votre navigateur pour afficher la console {{site.data.keyword.streaminganalyticsshort}}.

Pour déployer vos applications {{site.data.keyword.streamsshort}} dans le cloud :

1. Configurez votre environnement de développement pour développer et tester votre application.

	Si vous voulez utiliser un environnement {{site.data.keyword.streamsshort}}, vous pouvez télécharger gratuitement le produit [{{site.data.keyword.streamsshort}} Quick Start Edition ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/){:new_window}.

2. Développez votre application de diffusion en flux continu dans votre environnement de développement. Dans un environnement de développement {{site.data.keyword.streamsshort}}, vous pouvez utiliser Streams Studio ou les outils de ligne de commande pour développer votre application.

3. Vérifiez que votre application de diffusion en flux continu s'exécute correctement dans votre environnement de développement.
**Remarque :** vous devez compiler votre application sous le système d'exploitation Red Hat Enterprise Linux (RHEL) 6.5 ou une version CentOS équivalente, utilisant des processeurs Intel.

4. Soumettez le bundle d'applications (fichier .sab) associé à votre application SPL, Java, Scala ou Python dans votre instance de service du cloud en utilisant l'une des méthodes suivantes :
	* Utilisez la console {{site.data.keyword.streaminganalyticsshort}} pour soumettre le bundle d'applications.

  * Créez une application dans {{site.data.keyword.Bluemix_notm}} et ajoutez-y l'application {{site.data.keyword.streamsshort}}. Contrôlez-la en utilisant l'API REST {{site.data.keyword.streaminganalyticsshort}}.

Votre application est maintenant déployée dans le cloud. Vous pouvez la surveiller à l'aide du service {{site.data.keyword.streaminganalyticsshort}}. Il vous est aussi possible de soumettre plus d'une application (fichiers .sab) dans votre instance de service, sans limite de nombre.

{{site.data.keyword.streamsshort}} prend également en charge plusieurs kits de développement Java™ que vous pouvez utiliser pour développer vos applications. Pour plus d'informations sur la prise en charge de Java dans {{site.data.keyword.streamsshort}}, voir [Kits de développement Java pris en charge pour le développement d'application ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.2.1/com.ibm.streams.install.doc/doc/ibminfospherestreams-install-prerequisites-java-supported-sdks.html){:new_window}.

## Déploiement d'applications Python Streams dans le cloud
{: #t_deploypython}

Déployez vos applications Python {{site.data.keyword.streamsshort}} dans un service {{site.data.keyword.streaminganalyticsshort}} s'exécutant dans {{site.data.keyword.Bluemix_short}}. Vous n'avez pas besoin de disposer d'une installation {{site.data.keyword.streamsshort}}.
{:shortdesc}

L'[API d'application Python {{site.data.keyword.streamsshort}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features){:new_window} incluse dans le package streamsx vous permet de déployer des applications Python dans le service {{site.data.keyword.streaminganalyticsshort}}. Consultez le tutoriel [Developing for the {{site.data.keyword.streaminganalyticsshort}} service ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html){:new_window} pour un exemple de création et de déploiement d'une application Python simple pour le service {{site.data.keyword.streaminganalyticsshort}}.

IBM Data Science Experience (DSX) prend également en charge la soumission des applications Python dans les fichiers notebook interactifs Jupyter. Pour plus d'informations, voir [Développement d'applications Python pour {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics/t_develop_apps_python.html).
