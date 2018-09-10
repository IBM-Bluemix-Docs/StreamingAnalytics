---

copyright:
  years: 2017, 2018
lastupdated: "2018-07-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# ユーザーに対する許可の認可

{{site.data.keyword.Bluemix_notm}} アカウントがあると、自分のアカウントの組織やスペースでの管理特権があるため、{{site.data.keyword.streaminganalyticsshort}} のすべての操作を実行できます。ただし、自分のアカウントへ他のユーザーを入れる場合は、それらのユーザーがそのアカウント下でサービス・インスタンスを操作するために必要な特権を持てるよう、それらのユーザーの許可を管理する必要があります。

{{site.data.keyword.streaminganalyticsshort}} では、サービス管理操作へのアクセスは以下の許可レベルによって制御されます。

| 操作 | 必要な {{site.data.keyword.Bluemix_notm}} 許可 | 必要な IAM 許可 |
|-----------|------------------------------|--------------------------|
| サービスの作成または削除 | {{site.data.keyword.Bluemix_notm}} スペースに対する開発者役割 | なし |
| サービス・ダッシュボードの表示 | {{site.data.keyword.Bluemix_notm}} スペースに対する開発者役割 | ビューアー以上 |
| サービスのサイズ変更   | {{site.data.keyword.Bluemix_notm}} スペースに対する開発者役割 | エディター以上 |
| CF CLI または {{site.data.keyword.Bluemix_notm}} UI を使用したサービス・キーの生成 | {{site.data.keyword.Bluemix_notm}} スペースに対する開発者役割 | なし |

新規ユーザーを自分のアカウントへ入れるには、以下のようにします。

1.	[{{site.data.keyword.Bluemix_notm}} ダッシュボード](https://console.bluemix.net)にログオンします。

2.	**「管理」->「アカウント」->「ユーザー」**をクリックします。

3.	**「ユーザー管理」**ページで、**「ユーザーの招待」**をクリックします。

4.	招待するユーザーの IBM ID を入力します。

5.	「アクセス」セクションで、**「ID およびアクセス対応サービス」**を展開して、以下の値を選択します。

	a.	サービス: **「すべての ID およびアクセス対応サービス」**を選択します。

	b.	地域: **「米国南部」**を選択します。

	c.	サービス・インスタンス: **「すべての現行サービス・インスタンス」**を選択します。

	d.	役割: ユーザーの役割を選択します。 ビューアー役割のメンバーには、{{site.data.keyword.streaminganalyticsshort}} に対する読み取り専用アクセス権限があります。 エディター以上の特権を割り当てられたメンバーは、{{site.data.keyword.streaminganalyticsshort}} サービスを変更できます。

6.	**「Cloud Foundry アクセス権限」**を展開して、ユーザーにアクセス権限を与える組織を選択します。

	a. 組織レベルでのユーザーの役割を選択します。

	b.	地域には米国南部を選択します。

	c.	ユーザーにアクセス権限を付与するスペースを選択します。

	e.	ユーザーに割り当てる役割を選択します。 サービス・ダッシュボードを表示してサービス・キーの生成などのタスクを実行するには、開発者役割を割り当てる必要があります。
