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

# Sobre o Streaming Analytics
{: #about}

É possível executar a análise em tempo real em dados em movimento como parte de seus aplicativos {{site.data.keyword.Bluemix_short}} com o {{site.data.keyword.streaminganalyticsfull}}.
{:shortdesc}

Novo no {{site.data.keyword.streaminganalyticsshort}}? Obtenha uma [rápida introdução ao serviço ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/streamsdev/docs/streaming-analytics-now-available-bluemix-2/){:new_window}.

O {{site.data.keyword.streaminganalyticsshort}}
fornece os recursos a seguir para implementar, analisar e monitorar os seus dados na nuvem:

**Uso interativo e programático do serviço:**

É possível usar o serviço interativamente por meio do [console do {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-console#console) ou programaticamente por meio da [API de REST do {{site.data.keyword.streaminganalyticsshort}} v1 ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/apidocs/streaming-analytics-v1){:new_window} se você está usando os [planos de serviço da v1](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans). Para planos de serviços do [v2](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans), use a API de REST do [{{site.data.keyword.streaminganalyticsshort}} v2 ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/apidocs/streaming-analytics-v2).

**Implementação e monitoramento de aplicativos SPL, Java, Scala e Python:**

É possível gravar aplicativos {{site.data.keyword.streamsshort}} em SPL, Java, Scala e Python. [Implemente e monitore esses aplicativos](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_deploytocloud) com o console do {{site.data.keyword.streaminganalyticsshort}}.

Se desejar gravar seus aplicativos em SPL, {{site.data.keyword.streamsfull}} Processing Language (SPL) é uma linguagem de programação que é usada para criar aplicativos de processamento de fluxos. Se você deseja ir além com seus próprios aplicativos SPL, é possível obter um ambiente de desenvolvimento do {{site.data.keyword.streamsshort}} e deve-se deixar seus apps SPL prontos para a nuvem.

Para criar e implementar aplicativos Python sem um ambiente de desenvolvimento do {{site.data.keyword.streamsshort}}, use os blocos de notas de serviço no {{site.data.keyword.DSX_short}} ou na API {{site.data.keyword.streamsshort}} Python. Para obter mais informações, consulte [Desenvolvendo aplicativos Python para o {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-t_develop_apps_python).

É possível desenvolver aplicativos Beam com o executor Streams em seu ambiente de desenvolvimento local, que pode ser implementado e monitorado no serviço do {{site.data.keyword.streaminganalyticsshort}}. Para obter mais informações sobre os aplicativos Beam com o Streams Runner, consulte [IBM Streams Runner for Apache Beam no {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-gs_beamrunner).


**Compatibilidade com operadores do {{site.data.keyword.streamsshort}}:**

Os operadores do {{site.data.keyword.streamsshort}} no kit de ferramentas padrão do [{{site.data.keyword.streamsshort}} Processing Language (SPL) são compatíveis](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-compatible_toolkits) com o {{site.data.keyword.streaminganalyticsshort}}.

## Responsabilidades do Streaming Analytics
{: #responsibilities notoc}

### Responsabilidades do cliente
{: #clientresponsibilities notoc}

O cliente é responsável por:

* Seguir a configuração inicial pela IBM do {{site.data.keyword.streamsshort}}, monitorar, configurar e gerenciar as tarefas do {{site.data.keyword.streamsshort}} que estão em execução em sua instância. O cliente tem flexibilidade de iniciar e parar a instância e iniciar e parar tarefas que estão em execução na instância.
* Desenvolver, conforme necessário, programas e aplicativos no serviço para analisar dados e obter insights dele. O cliente também é responsável pela qualidade e o desempenho de tais programas ou aplicativos desenvolvidos. Os programas podem ser desenvolvidos em SPL, Java ou outras linguagens suportadas usando o recurso Topologia do {{site.data.keyword.streamsshort}}. Eles devem ser compilados com o {{site.data.keyword.streamsshort}} Developer Edition ou o {{site.data.keyword.streamsshort}} Quick Start Edition com o mesmo sistema operacional que o usado para o {{site.data.keyword.streaminganalyticsshort}}.
* Verificar o link a seguir periodicamente para ser informado sobre um tempo de inatividade planejado com ou sem interrupção - [https://developer.ibm.com/bluemix/support/#status ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/bluemix/support/#status){:new_window}  
* Fazer backup de todos os dados, metadados, arquivos de configuração e parâmetros de ambiente de acordo com os requisitos de negócios para assegurar a continuidade.
* Restaurar dados, metadados, arquivos de configuração e parâmetros de ambiente de qualquer backup para assegurar a continuidade, em uma eventualidade de falha de qualquer tipo. Isso inclui, mas não se limita a falha de data center ou pod, falha de servidor, falha de disco rígido ou falhas de software.

### Responsabilidades da IBM
{: #ibmresponsibilities notoc}

Como parte do {{site.data.keyword.streaminganalyticsfull}}, a IBM irá:

* Fornecer e gerenciar servidores, armazenamento e infraestrutura de rede para a instância do Cliente.
* Forneça uma configuração inicial do {{site.data.keyword.streamsshort}} no número de recursos selecionados.
* Fornecer e gerenciar a infraestrutura da exposição dos produtos da Internet e do firewall interno quanto à proteção e ao isolamento.
* Monitorar e gerenciar os componentes a seguir no {{site.data.keyword.streaminganalyticsshort}}:
	* Componentes de Rede
	* Servidores e seu armazenamento local
	* Sistemas operacionais de infraestrutura
	* Serviços de gerenciamento do {{site.data.keyword.streamsshort}}
	* Instâncias do {{site.data.keyword.streamsshort}}
* Fornecer correções de manutenção, incluindo correções de segurança apropriadas para os sistemas operacionais de infraestrutura e o {{site.data.keyword.streamsshort}}.
* Execute a manutenção regular que não deve requerer nenhum tempo de inatividade do sistema (manutenção “sem interrupção”) e a manutenção que pode requerer algum tempo de inatividade do sistema e reinicialização (manutenção “com interrupção”), que são executadas nos tempos planejados publicados em [https://developer.ibm.com/bluemix/support/#status ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/bluemix/support/#status){:new_window}
* Quaisquer mudanças nos horários de manutenção planejados serão postadas com aviso apropriado.
