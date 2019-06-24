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

# Kits de ferramentas e adaptadores suportados
{: #compatible_toolkits}

Esses kits de ferramentas e adaptadores analíticos são suportados pelo {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

| Kit de ferramentas                        | Descrição							                  |
| --------------------------------| --------------------------|
| [Processamento de Evento Complexo (CEP) ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://ibm.co/2zOwODa)    |	Fornece o operador MatchRegex para executar processamento de evento complexo.  		 |
| [Data/hora ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://ibmstreams.github.io/streamsx.datetime/)	|	Conjunto de utilitários para manipular datas, horas e registros de data e hora.	 |
| [HBase![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.hbase/)        | Permite que aplicativos Streams se conectem ao Apache HBase.	 	   |
| [HDFS ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.hdfs/)          | Fornece operadores e funções que interagem com o Sistema de arquivos distribuído Hadoop.	|
| [Internet (Inet) ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.inet)|  Foca em interagir com dados hospedados de rede.				       |
| [IoT ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.iot/)            | Fornece a integração da Internet of Things (IoT) ao IBM Watson IoT Platform, no {{site.data.keyword.Bluemix_notm}} ou no local ({{site.data.keyword.streamsshort}}). |
| [JDBC ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.jdbc/)          | Permite que aplicativos Streams trabalhem com bancos de dados via JDBC.		   |
| [JSON ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.json/)          | Saiba como converter dados de JSON para o formato de tuplas do Streams e inversamente.   		|
| [Kafka ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://ibmstreams.github.io/streamsx.kafka/)       | Permite que aplicativos Streams se integrem facilmente ao Apache Kafka. 	 |
| [MessageHub ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://ibmstreams.github.io/streamsx.messagehub/) | Permite que aplicativos Streams trabalhem com o MessageHub.			     |
| [Sistema de mensagens ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://ibmstreams.github.io/streamsx.messaging/)   |  	Foca na interação com sistemas de mensagens populares, como Kafka, MQTT, JMS e XMS	<br>**Nota**: para usar JMSSource, JMSSink, XMSSource, XMSSink com o WebSphere MQ, conclua estas etapas em seu ambiente de desenvolvimento: <br>1. Acesse [IBMStreams no GitHub ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://github.com/IBMStreams){:new_window} e faça download do Messaging Toolkit (com.ibm.streamsx.messaging) versão 3.0.0 ou mais recente em seu ambiente de desenvolvimento.<br>2. Use a versão 5.1.0 ou mais recente do kit de ferramentas para construir seu aplicativo.<br>3. Coloque o arquivo `.bindings` necessário no diretório `/etc` do seu aplicativo para incluí-lo no pacote configurável do aplicativo do {{site.data.keyword.streamsshort}}.	    |
| [RabbitMQ ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://ibmstreams.github.io/streamsx.rabbitmq/)     |  Fornece operadores que permitem que o aplicativo Streams leia e envie mensagens de RabbitMQ.  |
| [R-project ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://ibm.co/2rj2lKw)          	   	              |   Inclui o operador RScript, que pode ser usado para executar comandos R e aplicar algoritmos de mineração de dados complexos para detectar padrões de interesse em fluxos de dados.			     |
| [Topologia ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.topology/)      |  Saiba como construir aplicativos de fluxo Python para o serviço do {{site.data.keyword.streaminganalyticsshort}} na plataforma do {{site.data.keyword.Bluemix_notm}} e no {{site.data.keyword.streamsshort}}.		     |
| [DPS ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.dps/) |	 Permite que múltiplos aplicativos que estão executando elementos de processamento (PEs) em uma ou mais máquinas compartilhem informações de estado específicas do aplicativo.<br>**Restrição:** apenas REDIS é suportado como backend do banco de dados.	| 	 	 	
| [Geoespacial ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$com.ibm.streams.geospatial/tk$com.ibm.streams.geospatial.html) 	     |	Inclui operadores e funções que facilitam o processamento e a indexação eficientes de dados da localização.<br>**Restrição:** os operadores que usam o modo de mapa compartilhado não são suportados (`MapStore`, `PointMapMatcher` no modo de mapa compartilhado).		 |
| [TEDA ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$com.ibm.streams.teda/tk$com.ibm.streams.teda.html)	   | 	Fornece um conjunto de operadores genéricos que é usado em aplicativos de telecomunicações e também fornece uma estrutura de aplicativo para configurar novos aplicativos de arquivo para arquivo. Comece seguindo os [Tutoriais do TEDA ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](http://ibmstreams.github.io/streamsx.tutorial.teda/). Todos os operadores e funções do kit de ferramentas são suportados. <br>**Restrição:** a estrutura de aplicativo não é suportada.	 	 |
| [TimeSeries ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/support/knowledgecenter/en/SSCRJU_4.3.0/com.ibm.streams.toolkits.doc/spldoc/dita/tk$com.ibm.streams.timeseries/tk$com.ibm.streams.timeseries.html)	 	  | Os operadores e as funções na condição do kit de ferramentas do TimeSeries analisam e modelam dados de séries temporais. <br>**Restrição:** os operadores descontinuados não são suportados.	   |
| [{{site.data.keyword.cos_short}}
![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://bit.ly/2Ggp03T)	 	  | Fornece operadores primitivos e funções nativas para ler e gravar dados do {{site.data.keyword.cos_short}} e para ele respectivamente. O kit de ferramentas suporta S3 compatível {{site.data.keyword.cos_short}}.	   |

*Tabela 1. Kits de ferramentas suportados*

## Outros kits de ferramentas e operadores
{: #other_operators}

Outros operadores, incluindo os operadores do kit de ferramentas, que você desenvolveu para suas próprias necessidades, podem ser suportados pelo {{site.data.keyword.streaminganalyticsshort}}.
{:shortdesc}

Os kits de ferramentas devem atender aos critérios a seguir para serem compatíveis com o {{site.data.keyword.streaminganalyticsshort}}:

1. Nenhum software adicional precisa ser pré-instalado nos recursos de aplicativo de sua instância de serviço.
2. Quaisquer informações de configuração que o kit de ferramentas requeira podem ser incluídas no pacote configurável do aplicativo usando o kit de ferramentas.
