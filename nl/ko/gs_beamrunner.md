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

# Streaming Analytics의 IBM Streams Runner for Apache Beam
{: #gs_beamrunner}

{{site.data.keyword.streamsshort}} 개발 환경을 보유한 경우에는 이제 이 환경에서 Beam 애플리케이션을 로컬 개발한 후 이러한 앱을 {{site.data.keyword.Bluemix_notm}}의 {{site.data.keyword.streaminganalyticsshort}} 서비스에 제출할 수 있습니다. {{site.data.keyword.streamsshort}} Runner for Apache Beam은 {{site.data.keyword.streamsshort}} 환경에서 Beam 파이프라인을 실행합니다. Streams Runner를 사용하여 실행된 Beam 애플리케이션은 {{site.data.keyword.streaminganalyticsshort}}에서 배치하고 모니터할 수 있는 SAB(Streams Application Bundle) 파일로 변환됩니다.


[샘플 애플리케이션](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-starterapps)을 사용하여 {{site.data.keyword.streaminganalyticsshort}} 서비스에서 Beam 애플리케이션을 제출하고 모니터하는 방법을 알아보십시오. 샘플 애플리케이션은 {{site.data.keyword.streaminganalyticsshort}} 콘솔에서 다운로드할 수 있습니다.

Streams Runner가 [Beam 기능 매트릭스](https://beam.apache.org/documentation/runners/capability-matrix/)에 적응하는 방법을 보여주는 표를 보려면 [{{site.data.keyword.streamsshort}} Runner for Apache Beam 문서 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/){:new_window}를 확인하십시오. {{site.data.keyword.streaminganalyticsshort}}에 제출하고 모니터할 수 있는 Beam 애플리케이션을 작성하기 위해 `com.ibm.streams.beam` 툴킷을 Streams 환경에 설치하는 방법에 대한 지시사항을 확인하려면 [IBM Streams Runner for Apache Beam 설치 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://bit.ly/2zFDpPr){:new_window}를 참조하십시오.

Beam 프로그래밍에 대한 일부 경험이 도움은 되지만 필수적인 것은 아닙니다. [Apache Beam 웹 사이트 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://beam.apache.org/documentation/){:new_window}에 유용한 [Apache Beam Java SDK Quickstart ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://beam.apache.org/get-started/quickstart-java/){:new_window} 페이지 및 기타 문서가 포함되어 있습니다.
