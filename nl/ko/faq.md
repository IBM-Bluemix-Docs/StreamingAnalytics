---

copyright:
  years: 2015, 2018
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}
{:faq: data-hd-content-type='faq'}

# 자주 묻는 질문(FAQ)
{: #faq}

## Streaming Analytics 서비스에는 어떻게 가입합니까?
{: #signup notoc}
{: faq}  

{{site.data.keyword.streaminganalyticsshort}} 서비스 플랜에 대한 자세한 정보는 [{{site.data.keyword.Bluemix_short}} 카탈로그](https://{DomainName}/catalog/services/streaming-analytics)를 참조하십시오.

## 어떤 버전의 Streaming Analytics 서비스를 사용 중입니까?
{: #version notoc}
{: faq}   

모든 {{site.data.keyword.streaminganalyticsshort}} 서비스에 정기적으로 개선사항이 푸시됩니다. 사용자는 항상 최신 버전의 관리 서비스를 사용하며 제품 버전이나 레벨을 추적하지 않아도 됩니다.

## IBM에서 관리해 주는 것은 무엇입니까?
{: #ibm_manage notoc}
{: faq}   

IBM에서는 설치, 소프트웨어 업그레이드, 도메인 작성 및 관리, 하드웨어 유지보수를 처리해 드립니다. 이 서비스에는 연중무휴의 시스템 상태 모니터링이 포함됩니다.


## 사용자가 담당하는 작업은 무엇입니까?  
{: #responsible notoc}
{: faq}

{{site.data.keyword.streaminganalyticsshort}} 서비스 및 Streams 인스턴스 온프레미스에서 실행되는 애플리케이션을 작성하고 해당 애플리케이션이 제대로 작동하며 성능 요구사항을 충족하는지 확인합니다. 애플리케이션별 모니터링도 사용자가 담당합니다.

## 고가용성(HA)이 지원됩니까?
{: #ha notoc}
{: faq}

IBM에서 고가용성(HA)을 관리합니다. {{site.data.keyword.streaminganalyticsshort}}는 HA를 지원하도록 구성됩니다. 추가 서버 리소스가 장애 복구 이벤트를 위해 준비되어 있습니다.

## Streaming Analytics 서비스에 대해 보안은 어떻게 관리됩니까?
{: #security notoc}
{: faq}   

보안은 IBM에서 전체 관리합니다. 각 서비스에 대한 인증 정보가 생성되고 사용자에게 해당 정보가 제공됩니다. 보안 업데이트는 사용 가능하게 되는 즉시 IBM에서 관리하고 적용합니다.

## Streaming Analytics 서비스를 구성해야 합니까?  
{: #configure notoc}
{: faq}

IBM에서 서비스를 작성하고 전체 관리합니다. 각 서비스는 애플리케이션 노드의 전용 세트로 구성되어 있습니다.

## Streams 애플리케이션은 어떻게 개발합니까?
{: #streamsapp notoc}
{: faq}

[v2 서비스 플랜](/docs/services/StreamingAnalytics/service_plans.html)용 무료 Streams [{{site.data.keyword.streamsshort}} Quick Start Edition with Docker ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-install-docker/)를 사용하여 로컬로 Streams 애플리케이션을 개발해야 합니다. 또는 [v1 서비스 플랜](/docs/services/StreamingAnalytics/service_plans.html)을 사용하는 경우에는 [{{site.data.keyword.streamsshort}} Quick Start Edition VM 이미지 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibmstreams.github.io/streamsx.documentation/docs/4.3/qse-intro/){:new_window}를 다운로드할 수 있습니다.

이미 있다면 온프레미스 {{site.data.keyword.streamsshort}} 설치를 사용할 수도 있습니다. 로컬로 개발하고 컴파일한 애플리케이션은 클라우드 내의 Streams 서비스에 번들로 원활하게 배치될 수 있습니다.

그러나 클라우드에서 Python 애플리케이션을 실행하려는 경우에는 {{site.data.keyword.streamsshort}} 온프레미스를 설치할 필요가 없습니다. 간단히 `STREAMING\_ANALYTICS\_SERVICE` 컨텍스트를 사용하여 Python 애플리케이션을 {{site.data.keyword.streaminganalyticsshort}} 서비스에 제출하십시오. 표준 Python 개발 환경 또는 Jupyter 대화식 노트북에서 애플리케이션을 개발할 수 있지만 Python 3.5를 사용해야 합니다.

애플리케이션 개발에 대한 자세한 정보는 [{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.streaminganalyticsshort}} 개발 안내서 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/streamsdev/?p=16589&post_type=doc&preview=1&_ppp=7ad76a418b)를 참조하십시오.

## Streaming Analytics 서비스 호스트에 직접 로그인할 수 있습니까?
{: #host notoc}  
{: faq}

아니오. Telnet 또는 SSH(Secure Shell)로 서버에 직접 로그인하는 것은 지원되지 않습니다. 추가 소프트웨어를 설치하거나 Streams 호스트에서 Streams가 아닌 소프트웨어를 실행할 수 없습니다.

## Streaming Analytics 서비스의 파일 시스템에 액세스할 수 있습니까?
{: #filesystem notoc}
{: faq}   

Streams 애플리케이션만 Streams 호스트의 파일 시스템에 직접 액세스할 수 있습니다.

다른 솔루션 컴포넌트와 상호작용하기 위해 Streams용 메커니즘이 필요한 솔루션을 위해 클라우드 준비 대체 항목이 있습니다. 파일 대신 다른 소스 및 싱크 프로토콜을 사용할 수 있습니다 (예: 클라우드 기반 데이터 스토어).

## Streaming Analytics 서비스 애플리케이션에서 내 조직의 엔터프라이즈 데이터에 어떻게 액세스할 수 있습니까?
{: #access notoc}  

[{{site.data.keyword.Bluemix_notm}} Secure Gateway 서비스](https://{DomainName}/catalog/services/secure-gateway)를 사용하여 Streams 애플리케이션을 엔터프라이즈에 안전하게 연결할 수 있습니다.

## Streaming Analytics 서비스가 지원하는 온프레미스용 IBM Streams의 모든 기능이 클라우드에 있습니까?
{: #features notoc}

{{site.data.keyword.streaminganalyticsshort}} 서비스에 대해 지원되지 않는 일부 기능에는 다음이 포함됩니다.

  - 도메인 권한이 필요한 인스턴스의 관리 태스크 (예: 사용자 정의 호스트 태그 추가 또는 작업 그룹 작성)
  - 일관성 있는 지역 체크포인트
  - 일부 툴킷 연산자는 지원되지 않습니다. 자세한 정보는 [지원되는 툴킷 및 어댑터](/docs/services/StreamingAnalytics/compatible_toolkits.html)를 참조하십시오.
  - Streams JMX API

## Streaming Analytics 서비스에 대한 자세한 사항은 어디에서 살펴볼 수 있습니까?
{: #roadmap notoc}

IBM developerWorks® 기사, [Roadmap for {{site.data.keyword.streaminganalyticsshort}} Service on {{site.data.keyword.Bluemix_notm}} ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/streamsdev/docs/roadmap-for-streaming-analytics-service-on-bluemix/)에 유용한 블로그, 데모 및 기사에 대한 링크뿐만 아니라 서비스를 학습하기 위한 안내가 포함되어 있습니다.
