---
title: Preis- und Nachkalkulationsdimensions-Homepage
description: Dieses Thema enthält einen Überblick über Preisdimensionen.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 515a2e2e518614884b414ca43702e8bfea2c6919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076565"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Preis- und Nachkalkulationsdimensions-Homepage

Die Dimensionen, die zum Festlegen der Lohnkosten in projektbasierten Organisationen verwendet werden, werden von den folgenden Attributen beeinflusst:

- Menschen, die entsprechend ihrer Erfahrung, Rolle oder Geografie arbeiten
- Arbeiten, die entsprechend der Komplexität oder Tageszeit ausgeführt werden sollen

Angesichts der typischen Art dieser Arbeitsattribute und der für die Ausführung der Arbeit erforderlichen Personen stehen in Project Service Automation zwei Arten von Preisdimensionswerten zur Verfügung: 

- **Optionssätze** – Attribute, bei denen es sich um feste Enumerationen für einen Satz von Werten handelt.
- **Entitätsbasierte Werte** – Attribute, die unterschiedliche Werte haben können, die endlich sind, sich aber im Laufe der Zeit ändern können.

## <a name="pricing-dimensions"></a>Preisdimensionen

PSA wird mit einem Standardsatz an Preisdimensionen bereitgestellt. Sie können diese anzeigen, indem Sie zu **Project Service** > **Parameter** navigieren. Prüfen Sie im Parameterdatensatz auf der Registerkarte **Betragsbasierte Preisdimensionen** , dass bei der Rolle **msdyn_resourcecategory** und der Organisationseinheit der Ressource **msdyn_organizationalunit** die Felder **Gilt für Vertrieb** und **Gilt für Kosten** auf **Ja** festgelegt sind. Dadurch können Sie den Preis und die Kosten für jede Kombination aus Rolle und Organisationseinheit einrichten.

![Screenshot der Project Service-Parameter mit Markierung von „Gilt für Vertrieb”](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Falls Sie die vorgegebenen Felder von Rolle und Organisationseinheit als Preisdimensionen vor Version 3 von PSA verwenden, gibt es keine wahrnehmbare Änderung. Sie können Project Service wie gehabt verwenden. 

Wenn Sie einen Preis oder Kosten für Ihre Ressourcen mit zusätzlichen Attributen festlegen müssen, können Sie benutzerdefinierte Felder, Entitäten und Dimensionen einrichten. Weitere Informationen finden Sie in den folgenden Themen. Beachten Sie jedoch, dass Sie die Vorgehensweisen in der unten angegebenen Reihenfolge abschließen müssen:

- [Erstellen benutzerdefinierter Felder und Entitäten](create-custom-fields-entities.md)
- [Hinzufügen von benutzerdefinierten Feldern zum Preissetup und zu Transaktionsentitäten](field-references.md)
- [Einrichten von benutzerdefinierten Feldern als Preisdimensionen ](set-up-pricing-dimensions.md)
- [Aktualisieren von Plug-In-Attributen zum Einbinden neuer Preisdimensionen](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Preise für die Personalzeit
Die Preisgestaltung der Personalzeit in einer Organisation ist häufig eine wichtige strategische Überlegung, die sich direkt auf die Rentabilität der Organisation auswirkt. Arbeiten Sie mit den Finanzteams und Übungsleitern zusammen, wenn Ihre Organisation bereit ist, zu ermitteln, wie Rechnungs- und Kostensätze für die Personalzeit eingerichtet werden sollen.

Zu den weiteren Überlegungen für Preise gehört, ob Felder oder Entitäten wiederverwendet werden sollen, die derzeit keine Preisdimensionen sind, jedoch für Ihre Organisation als Preisdimension gelten. Felder wie **Transaktionskategorie** ( **msdyn_transactioncategory** ) und **Buchbare Ressource** ( **bookableresource** ) sind Beispiele für Kandidatendimensionen. 

Sie sollten ebenfalls berücksichtigen, ob Ihre Preisdimension eine Tabelle oder ein Optionssatz sein soll. Wenn Sie von mehr als 10 oder 12 Änderungen an den Werten einer Dimension ausgehen und Sie zusätzliche Attribute für diese Werte benötigen, erstellen Sie anstelle eines Optionssatzes eine Entität. Das Verwalten eines Optionssatzes, z. B. das Hinzufügen oder Entfernen von Werten, erfordert einen Administrator oder Entwickler, während das Hinzufügen neuer Zeilen zu einer Tabelle von den meisten Geschäftsbenutzern durchgeführt werden kann.

Das folgende Beispiel zeigt Rechnungssätze, die basierend auf der Rolle und der Organisationseinheit der Ressource, zu der die Ressource gehört, eingerichtet werden. Kostensätze basieren in der Regel auf der Gehaltsspanne des Mitarbeiters und der Organisationseinheit, die er zugeordnet wurde. In diesem Beispiel sehen die Abrechnungs- und Kostensatztabellen wie folgt aus.

**Beispielrechnungssätze**

| Rolle        | Organisationseinheit    |Einheit      |Preis      |Währung  |
| ------------|-------------|----------|----------:|----------|
| Entwickler   | Contoso US  |Hour | 200|USD     |
| Entwickler   | Koch Indien |Hour|   112|USD     |


**Beispielkostensätze**

| Gehaltsspanne     | Organisationseinheit    |Einheit      |Preis      |Währung  |
| ----------------|-------------|----------|----------:|----------|
| Mein Unternehmen_Band1 | Contoso US  |Hour | 145|USD     |
| Mein Unternehmen_Band2 | Koch Indien |Hour|   67|USD     |
