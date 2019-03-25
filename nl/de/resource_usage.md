---

copyright:
  years: 2015, 2019
lastupdated: "2018-12-06"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}


# Ressourcennutzung
{: #resourceusage}

{{site.data.keyword.streaminganalyticsshort}} umfasst eine Reihe von Verhaltensweisen und Richtlinien, die eine korrekte Ressourcenzuordnung und -nutzung sicherstellen.

## Instanzressourcen anzeigen und bearbeiten
Sie können die Anzahl der Ressourcen, die für die Instanz berechtigt sind, über die Servicedetailseite oder mithilfe der v1-REST-API für [v1-Servicepläne](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) anzeigen und bearbeiten. Sie müssen die [{{site.data.keyword.streaminganalyticsshort}}-v2-REST-API](https://{DomainName}/apidocs/streaming-analytics-v2#get-a-streaming-analytics-instance) für [v2-Servicepläne](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-service_plans#service_plans) verwenden.

## Ressourcenzuordnung
- Ressourcen werden automatisch der Instanz zugeordnet, wenn ein Job übergeben wird, der erfolgreich ausgeführt wird.
- Ressourcen werden von der Instanz entfernt, wenn für die betreffende Ressource keine Jobs ausgeführt werden. Beispiel: Job 1 wird mit Ressource 1 ausgeführt, Job 2 mit Ressource 1 und Ressource 2. Wenn Job 2 abgebrochen wird, bleibt Ressource 1 der Instanz zugeordnet, Ressource 2 wird dagegen entfernt.
- Wird ein Job übergeben, wird dieser Job mit einer neuen Ressource ausgeführt, falls die Instanz den Zuordnungsgrenzwert nicht erreicht.
- Sobald eine Instanz alle Ressourcen nutzt, für die sie berechtigt ist, wird die Ausführung neuer Jobs mit den vorhandenen Ressourcen geplant.

## Einschränkungen für Ressourcen

Einschränkungen für Ressourcen können dazu verwendet werden, die Ressourcenzuordnung und -nutzung zu steuern. So kann beispielsweise mithilfe von Einschränkungen angegeben werden, dass zwei Jobs eine einzelne Ressource verwenden sollen, anstatt die Jobs auf zwei Ressourcen aufzuteilen.
