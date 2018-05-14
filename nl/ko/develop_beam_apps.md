---

copyright:
  years: 2015, 2018
lastupdated: "2018-04-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Streaming Analytics에 Beam 애플리케이션 배치
{: #develop_beam_apps}

이제 로컬 {{site.data.keyword.streamsshort}} 개발 환경에서 Beam 애플리케이션을 개발하고 이러한 애플리케이션을 {{site.data.keyword.streaminganalyticsshort}}에 배치할 수 있습니다.
{:shortdesc}

{{site.data.keyword.streamsshort}} Runner for Apache Beam은 {{site.data.keyword.streamsshort}} 환경에서 Beam 파이프라인을 실행합니다. Streams Runner를 사용하여 실행된 Beam 애플리케이션은 {{site.data.keyword.streaminganalyticsshort}}에서 배치하고 모니터할 수 있는 SAB(Streams Application Bundle) 파일로 변환됩니다.

Beam 애플리케이션을 {{site.data.keyword.Bluemix_notm}}의 {{site.data.keyword.streaminganalyticsshort}} 서비스에 제출하려면 이 서비스의 신임 정보 및 기타 정보를 포함하는 JSON 형식의 VCAP 파일을 작성해야 합니다.

1. Streams 로컬 환경에서 툴킷을 설치한 샘플 서브폴더($STREAMS_BEAM_RUNNER/samples)로 이동하여 template.vcap 파일을 새 파일에 복사하십시오. 이 파일에 의미가 있는 이름과 파일 확장자 .vcap을 지정하십시오.
1. [{{site.data.keyword.streaminganalyticsshort}} 서비스의 신임 정보를 복사](/docs/services/StreamingAnalytics/r_vcap_services.html)하여 작성한 VCAP 파일에 신임 정보를 붙여넣고 다음 행을 바꾸십시오.
```
 <REMOVE THIS LINE AND INSERT CREDENTIALS HERE>
 ```
1. 개발 환경에서 Beam 애플리케이션이 올바르게 실행되는지 확인하십시오. Streams Runner를 사용하여 Beam 애플리케이션을 실행하면 애플리케이션이 SAB(Streams Application Bundle) 파일로 변환됩니다.
1. Beam 애플리케이션과 연관된 SAB 파일을 {{site.data.keyword.streaminganalyticsshort}}에 제출하십시오.

애플리케이션이 이제 클라우드에 배치됩니다. {{site.data.keyword.streaminganalyticsshort}} 서비스를 사용하여 애플리케이션을 모니터할 수 있습니다.

{{site.data.keyword.streaminganalyticsshort}}에서 Beam 애플리케이션을 배치하고 모니터하는 데 대한 세부사항은 [Apache Beam을 위한 Streams Runner ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://ibmstreams.github.io/streamsx.documentation/docs/beamrunner/beamrunner-1-intro/)를 참조하십시오.
