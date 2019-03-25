---

copyright:
  years: 2017, 2019
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Benutzern Berechtigungen erteilen

Mit einem {{site.data.keyword.Bluemix_notm}}-Konto verfügen Sie über Administratorberechtigungen für die Organisation bzw. den Bereich unter Ihrem Konto. Damit können Sie alle Operationen für {{site.data.keyword.streaminganalyticsshort}} ausführen. Wenn Sie jedoch andere Benutzer zu Ihrem Konto hinzufügen, müssen Sie deren Berechtigungen so verwalten, dass sie über die erforderlichen Zugriffsrechte für die Ausführung von Serviceinstanzen unter Ihrem Konto verfügen.

In {{site.data.keyword.streaminganalyticsshort}} wird der Zugriff auf Service-Management-Operationen mithilfe der folgenden Berechtigungsstufen gesteuert:

| Operation | Erforderliche {{site.data.keyword.Bluemix_notm}}-Berechtigungen | Erforderliche IAM-Berechtigungen |
|-----------|------------------------------|--------------------------|
| Service erstellen oder löschen | Entwicklerrolle für den {{site.data.keyword.Bluemix_notm}}-Bereich | Keine |
| Servicedetailseite anzeigen | Entwicklerrolle für den {{site.data.keyword.Bluemix_notm}}-Bereich | Anzeigeberechtigter und höher |
| Größe des Service ändern   | Entwicklerrolle für den {{site.data.keyword.Bluemix_notm}}-Bereich | Bearbeiter und höher |
| Serviceschlüssel mithilfe der CF-Befehlszeilenschnittstelle oder der {{site.data.keyword.Bluemix_notm}}-Benutzerschnittstelle generieren | Entwicklerrolle für den {{site.data.keyword.Bluemix_notm}}-Bereich | Keine |

Gehen Sie wie folgt vor, um neue Benutzer zu Ihrem Konto hinzuzufügen:

1.	Melden Sie sich beim [{{site.data.keyword.Bluemix_notm}}-Dashboard](https://{DomainName}) an.

2.	Klicken Sie auf **Verwalten -> Zugriff (IAM) -> Benutzer**.

3.	Klicken Sie auf der Seite **Benutzer** auf **Benutzer einladen**.

4.	Geben Sie die IBMid des Benutzers ein, der eingeladen werden soll.

5.	Erweitern Sie unter dem Abschnitt 'Zugriff' die Option **Services mit aktiviertem Identity and Access Management** und wählen Sie die folgenden Werte aus:

	a.	Services: Wählen Sie **Alle Services mit aktiviertem Identity and Access Management** aus.

	b.	Region: Wählen Sie **Vereinigte Staaten (Süden)** aus.

	c.	Serviceinstanz: Wählen Sie **Alle aktuellen Serviceinstanzen** aus.

	d.	Rollen: Wählen Sie eine Rolle für den Benutzer aus. Mitglieder mit der Rolle eines Anzeigeberechtigten verfügen über Lesezugriff auf {{site.data.keyword.streaminganalyticsshort}}. Mitglieder, denen die Berechtigungen eines Bearbeiters oder höherer Berechtigungsstufen zugewiesen sind, können den {{site.data.keyword.streaminganalyticsshort}}-Service ändern.

6.	Erweitern Sie **Cloud Foundry-Zugriff** und wählen Sie die Organisation aus, für die Sie dem Benutzer Zugriffsberechtigungen zuweisen möchten.

	a. Wählen Sie eine Rolle auf Organisationsebene für den Benutzer aus.

	b.	Wählen Sie 'Vereinigte Staaten (Süden) als Region aus.

	c.	Wählen Sie den Bereich aus, für den Sie dem Benutzer Zugriffsberechtigungen erteilen möchten.

	e.	Wählen Sie die Rolle aus, die Sie dem Benutzer zuweisen möchten. Zum Anzeigen der Servicedetailseite und zum Durchführen von Tasks wie z. B. der Generierung von Serviceschlüsseln müssen Sie die Entwicklerrolle zuweisen.
