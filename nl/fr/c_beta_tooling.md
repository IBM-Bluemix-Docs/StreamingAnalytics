---

copyright:
  years: 2015, 2018
lastupdated: "2017-12-15"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Environnement et outils de développement
{: #c_beta_tooling}


Les considérations ci-dessous s'appliquent aux outils et à l'environnement que vous utilisez pour développer vos applications pour {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}


* {{site.data.keyword.streaminganalyticsshort}} n'inclut pas d'environnement de développement {{site.data.keyword.streamsshort}} ni Streams Studio dans le cloud. Développez vos applications dans un environnement {{site.data.keyword.streamsshort}} installé localement et soumettez-les en tant que bundle d'applications. Si vous ne disposez pas d'un environnement de développement, vous pouvez télécharger gratuitement le produit [{{site.data.keyword.streamsshort}} Quick Start Edition ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://ibmstreams.github.io/streamsx.documentation/docs/4.2/qse-intro/).
* Compilez le bundle d'applications dans un environnement Red Hat Enterprise Linux 6.5 ou une version CentOS équivalente afin de garantir la compatibilité.

  **Remarque :** si vous utilisez les plans Beta-Entry et Beta-Enhanced, vous devez compiler votre bundle d'applications dans un environnement RHEL 7 ou une version CentOS équivalente. Vous pouvez utiliser [{{site.data.keyword.streamsshort}} QSE for Docker](https://www-01.ibm.com/marketing/iwm/iwm/web/preLogin.do?source=swg-ibmistvi) si vous ne disposez pas d'un environnement de développement compatible. Consultez la [documentation relative aux plans bêta](/docs/services/StreamingAnalytics/beta_plans.html) pour des détails. 
* Dans votre environnement de développement {{site.data.keyword.streamsshort}}, pour la variable d'environnement `JAVA_HOME`, définissez $STREAMS_INSTALL/java.
