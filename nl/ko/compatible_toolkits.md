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

# 지원되는 툴킷 및 어댑터
{: #compatible_toolkits}

{{site.data.keyword.streaminganalyticsshort}}에서는 다음 분석 툴킷 및 어댑터를 지원합니다.
{:shortdesc}

| 툴킷                            | 설명        						                  |
| --------------------------------| --------------------------|
| [Complex Event Processing(CEP)](https://ibm.co/2zOwODa)     |	복합 이벤트 처리를 수행하기 위한 MatchRegex 연산자를 제공합니다. |
| [Datetime](https://ibmstreams.github.io/streamsx.datetime/)	|	날짜, 시간 및 시간소인을 처리하기 위한 유틸리티 세트입니다. |
| [HBase](http://ibmstreams.github.io/streamsx.hbase/)        | Streams 애플리케이션이 Apache HBase에 연결할 수 있게 해 줍니다. |
| [HDFS](http://ibmstreams.github.io/streamsx.hdfs/)          | 하둡 분산 파일 시스템과 상호작용하는 연산자 및 함수를 제공합니다. |
| [Internet(Inet)](http://ibmstreams.github.io/streamsx.inet) |  네트워크 호스팅되는 데이터와의 상호작용을 주로 수행합니다. |
| [IoT](http://ibmstreams.github.io/streamsx.iot/)            | {{site.data.keyword.Bluemix_notm}} 또는 사내 구축 환경({{site.data.keyword.streamsshort}})에서 IBM Watson IoT Platform을 비롯한 IoT(Internet of Things) 통합을 제공합니다. |
| [JDBC](http://ibmstreams.github.io/streamsx.jdbc/)          | Streams 애플리케이션이 JDBC를 통해 데이터베이스 관련 작업을 수행할 수 있도록 합니다. |
| [JSON](http://ibmstreams.github.io/streamsx.json/)          | 사용자가 데이터를 JSON에서 Streams 튜플 형식으로, 또는 그 반대로 변환할 수 있게 해 줍니다. |
| [Kafka](https://ibmstreams.github.io/streamsx.kafka/)       | Streams 애플리케이션이 Apache Kafka와 손쉽게 통합할 수 있게 해 줍니다. |
| [MessageHub](https://ibmstreams.github.io/streamsx.messagehub/) | Streams 애플리케이션이 MessageHub 관련 작업을 수행할 수 있도록 해 줍니다. |
| [Messaging](https://ibmstreams.github.io/streamsx.messaging/)   |  	Kafka, MQTT, JMS 및 XMS와 같은 인기 메시징 시스템과의 상호작용을 주로 수행합니다. <br>**참고**: WebSphere MQ와 함께 JMSSource, JMSSink, XMSSource, XMSSink를 사용하려면 사용자의 개발 환경에 필요한 해당 단계를 완료하십시오.<br>1. [GitHub의 IBM Streams](https://github.com/IBMStreams){:new_window}로 이동하여 메시징 툴킷(com.ibm.streamsx.messaging) 버전 3.0.0 이상을 개발 환경에 다운로드하십시오. <br>2. 버전 5.1.0 이상의 툴킷을 사용하여 애플리케이션을 빌드하십시오. <br>3. 필요한 .bindings 파일을 애플리케이션의 `/etc` 디렉토리에 삽입하여 {{site.data.keyword.streamsshort}} 애플리케이션 번들에 포함시키십시오. |
| [Mining](https://ibm.co/2y3i5au)               	   	            |  모델을 적용하여 데이터 스트림을 마이닝하는 데 사용할 수 있는 연산자를 포함합니다. |
| [RabbitMQ](https://ibmstreams.github.io/streamsx.rabbitmq/)     |  사용자의 Streams 애플리케이션이 Rabbit MQ에서 메시지를 읽고 전송할 수 있게 해 주는 연산자를 제공합니다. |
| [R-project](https://ibm.co/2h7D9lu)          	   	              |   R 명령을 실행하고 데이터 스트림에서 관심 있는 패턴을 발견하기 위해 복합 데이터 마이닝 알고리즘을 적용하는 데 사용할 수 있는 RScript 연산자를 포함합니다. |
| [Topology](http://ibmstreams.github.io/streamsx.topology/)      |  {{site.data.keyword.Bluemix_notm}} 플랫폼 및 {{site.data.keyword.streamsshort}}의 {{site.data.keyword.streaminganalyticsshort}} 서비스를 위한 Python 스트리밍 애플리케이션을 빌드하는 기능을 제공합니다.	|
| [DPS](http://ibmstreams.github.io/streamsx.dps/) |	 하나 이상의 시스템에서 처리 요소(PE)를 실행 중인 여러 애플리케이션이 애플리케이션 고유 상태 정보를 공유할 수 있게 해 줍니다. <br>**제한사항:** 데이터베이스 백엔드로서 지원되는 것은 REDIS뿐입니다. | 	 	 	
| [Geospatial](https://ibm.co/2h9x0VR) 	     |	위치 데이터의 효율적 처리와 색인 작성을 용이하게 하는 연산자 및 함수가 포함되어 있습니다. <br>**제한사항:** 공유 지도 모드를 사용하는 연산자는 지원되지 않습니다(공유 지도 모드의 `MapStore`, `PointMapMatcher`). |
| [TEDA](https://ibm.co/2z9DS00)	   | 	원격 통신 애플리케이션에서 사용되는 일반 연산자 세트를 제공하며, 새로운 파일 대 파일 애플리케이션을 설정할 수 있게 해 주는 애플리케이션 프레임워크 또한 제공합니다. [TEDA 튜토리얼](http://ibmstreams.github.io/streamsx.tutorial.teda/)에 따라 사용을 시작해 보십시오. 이 툴킷의 모든 연산자 및 함수는 지원됩니다. <br>**제한사항:** 애플리케이션 프레임워크는 지원되지 않습니다. |
| [TimeSeries](https://ibm.co/2zEPILZ)	 	  | TimeSeries 툴킷의 연산자 및 함수는 시계열 데이터를 조건 지정하고, 분석하고 모델링합니다. <br>**제한사항:** 더 이상 사용되지 않는 연산자는 지원되지 않습니다. |

*표 1. 지원되는 툴킷*

## 기타 툴킷 및 연산자
{: #other_operators}

{{site.data.keyword.streaminganalyticsshort}}는 사용자가 자신의 필요에 따라 개발한 툴킷 연산자를 비롯한 기타 연산자를 지원할 수 있습니다.
{:shortdesc}

툴킷은 다음 기준에 부합해야 {{site.data.keyword.streaminganalyticsshort}}와 호환될 수 있습니다. 

1. 추가 소프트웨어는 서비스 인스턴스의 애플리케이션 노드에 사전 설치될 필요가 없습니다.
2. 툴킷이 요구하는 구성 정보는 툴킷을 사용하는 애플리케이션 번들에 포함될 수 있습니다.
