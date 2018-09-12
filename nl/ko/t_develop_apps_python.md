---

copyright:
  years: 2015, 2018
lastupdated: "2018-07-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics에서 Python 애플리케이션 개발
{: #t_develop_apps_python}

이제 {{site.data.keyword.DSX_full}} 또는 로컬 Python 개발 환경에서 Python 애플리케이션을 개발하고 이러한 애플리케이션을 {{site.data.keyword.streaminganalyticsshort}}에 배치할 수 있습니다.
{:shortdesc}

다음 방법 중 하나를 사용하여 {{site.data.keyword.streaminganalyticsshort}} 서비스에서 Python 애플리케이션을 개발하고 이를 {{site.data.keyword.Bluemix_short}}에 배치하십시오. 


## Watson Studio에서 Streams Python 애플리케이션 개발
{: #t_develop_python_dsx}

Python 개발 환경이 없는 경우, 가장 손쉬운 시작 방법은 {{site.data.keyword.DSX_short}}에서 {{site.data.keyword.streamsshort}} 노트북을 사용하여 샘플 Python 애플리케이션을 작성하는 것입니다. 이러한 노트북은 {{site.data.keyword.DSX_short}} Python 환경 내에서 {{site.data.keyword.streaminganalyticsshort}} 서비스의 단순 Python 애플리케이션을 작성하고 배치하기 위한 단계와 코드 샘플을 제공합니다.

* [Hello World! ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039ca9c6e8): 간단한 Hello World! 애플리케이션을 작성하여 시작한 후에 이 애플리케이션을 {{site.data.keyword.streaminganalyticsshort}} 서비스의 인스턴스에 배치하십시오.

* [의료 서비스 데모 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039cad29a6): 피드에서 스트리밍 데이터를 수집하고 분석하는 애플리케이션을 작성한 후 노트북에서 데이터를 시각화하십시오. 최종적으로는 이 애플리케이션을 {{site.data.keyword.streaminganalyticsshort}} 서비스 인스턴스에 제출하십시오.

* [Neural Net 데모 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://apsportal.ibm.com/exchange/public/entry/view/9fc33ce7301f10e21a9f92039ca60bb7): 샘플 데이터 세트를 작성하고 데이터 모델을 작성하며 스트리밍 애플리케이션에서 해당 모델을 사용하고 스트리밍 데이터를 시각화한 후에 스트리밍 애플리케이션을 서비스에 제출하십시오. 

## 로컬 Python 환경에서 애플리케이션 개발
 {: #t_develop_python_api}

streamsx 패키지에 포함되어 있는 [{{site.data.keyword.streamsshort}}Python 애플리케이션 API ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibmstreams.github.io/streamsx.documentation/docs/python/python-appapi-devguide/#50-api-features)를 사용하면 Python 호출 가능 클래스 또는 함수로 스트림 처리 애플리케이션을 작성할 수 있습니다. Python 애플리케이션 API를 사용하여 애플리케이션을 정의하고 이를 서비스에 제출할 수 있습니다.

[{{site.data.keyword.streaminganalyticsshort}} 서비스 개발 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibmstreams.github.io/streamsx.documentation/docs/python/1.6/python-appapi-devguide-2a/index.html) 튜토리얼의 단계에 따라 시작하십시오. 이 튜토리얼에서 사용자는 로컬 Python 환경에서 샘플 애플리케이션을 작성하고 이를 {{site.data.keyword.streaminganalyticsshort}} 서비스에 배치합니다. 

{{site.data.keyword.streamsshort}} Python 애플리케이션 API에 대해 자세히 살펴보려면 [이 온라인 과정 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/courses/all/streaming-analytics-basics-python-developers/){:new_window}을 완료하고 Python 개발자용 {{site.data.keyword.streaminganalyticsshort}} 기초를 학습하십시오.
