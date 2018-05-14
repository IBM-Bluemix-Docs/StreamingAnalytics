---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# 사용자에게 권한 부여

{{site.data.keyword.Bluemix_notm}} 계정으로 계정의 조직 또는 영역에 대한 관리 권한을 갖게 되며, 이를 통해 {{site.data.keyword.streaminganalyticsshort}}에서 모든 오퍼레이션을 수행할 수 있습니다. 그러나 기타 사용자를 사용자의 계정에 온보딩하는 경우 계정의 서비스 인스턴스를 작동할 수 있는 필수 권한을 보유하도록 이들의 권한을 관리해야 합니다. 

{{site.data.keyword.streaminganalyticsshort}}에서 다음 권한 레벨로 제어되는 서비스 관리 오퍼레이션에 액세스하십시오. 

| 오퍼레이션 | 필수 {{site.data.keyword.Bluemix_notm}} 권한 | 필수 IAM 권한 |
|-----------|------------------------------|--------------------------|
| 서비스 작성 또는 삭제 | {{site.data.keyword.Bluemix_notm}} 영역에 대한 개발자 역할 | 없음 |
| 서비스 대시보드 보기 | {{site.data.keyword.Bluemix_notm}} 영역에 대한 개발자 역할 | 뷰어 이상 |
| 서비스 크기 조정   | {{site.data.keyword.Bluemix_notm}} 영역에 대한 개발자 역할 | 편집자 이상 |
| CF CLI 또는 {{site.data.keyword.Bluemix_notm}} UI를 사용하여 서비스 키 생성 | {{site.data.keyword.Bluemix_notm}} 영역에 대한 개발자 역할 | 없음 |

새 사용자를 사용자의 계정에 온보딩하려면 다음을 수행하십시오.

1.	[{{site.data.keyword.Bluemix_notm}} 대시보드](https://console.bluemix.net)에 로그온하십시오.

2.	**관리 -> 계정 -> 사용자**를 클릭하십시오.

3.	사용자 관리 페이지에서 **사용자 초대**를 클릭하십시오.

4.	초대할 사용자의 IBM ID를 입력하십시오.

5.	액세스 섹션에서 **ID 및 액세스 사용 서비스**를 펼치고 다음 값을 선택하십시오.

	a.	서비스: **모든 ID 및 액세스 사용 서비스**를 선택하십시오.

	b.	지역: **미국 남부**를 선택하십시오.

	c.	서비스 인스턴스: **모든 현재 서비스 인스턴스**를 선택하십시오.

	d.	역할: 사용자의 역할을 선택하십시오. 뷰어 역할이 있는 구성원은 {{site.data.keyword.streaminganalyticsshort}}에 대한 읽기 전용 액세스 권한이 있습니다. 편집자 이상의 권한이 지정된 구성원은 {{site.data.keyword.streaminganalyticsshort}} 서비스를 수정할 수 있습니다. 

6.	**Cloud Foundry 액세스**를 펼치고 사용자에게 액세스 권한을 제공할 조직을 선택하십시오. 

	a. 사용자의 조직 레벨에서 역할을 선택하십시오. 

	b.	지역으로 미국 남부를 선택하십시오. 

	c.	사용자에게 액세스 권한을 부여할 영역을 선택하십시오. 

	e.	사용자에게 지정할 역할을 선택하십시오. 서비스 대시보드를 보고 서비스 키 생성과 같은 태스크를 수행하려면 개발자 역할을 지정해야 합니다. 
