---
title: Preis- und Nachkalkulationsdimensions-Homepage
description: Dieses Thema enthält einen Überblick über Preisdimensionen.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3721965"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Preis- und Nachkalkulationsdimensions-Homepage

Die Dimensionen, die in der Personalverwaltung zum Einrichten von Preisen und Kosten verwendet werden, lassen sich in zwei Kategorien einteilen:

- Personen
- Geplante Arbeit

Daher gibt es zwei Arten von Preisdimensionswerten, die in Project Service Automation (PSA) verfügbar sind: 

- **Optionssätze** – Dimensionen, bei denen es sich um feste Enumerationen für einen Satz von Werten handelt.
- **Entität-basierte Werte** – Dimensionen, bei denen es sich um unterschiedliche Sätze von Werten handeln kann.

## <a name="pricing-dimensions"></a>Preisdimensionen

PSA wird mit einem Standardsatz an Preisdimensionen bereitgestellt. Sie können diese anzeigen, indem Sie zu **Project Service** > **Parameter** navigieren. Prüfen Sie im Parameterdatensatz auf der Registerkarte **Betragsbasierte Preisdimensionen**, dass bei der Rolle **msdyn_resourcecategory** und der Organisationseinheit der Ressource **msdyn_organizationalunit** die Felder **Gilt für Vertrieb** und **Gilt für Kosten** auf **Ja** festgelegt sind. Dadurch können Sie den Preis und die Kosten für jede Kombination aus Rolle und Organisationseinheit einrichten.

![Screenshot der Project Service-Parameter mit Markierung von „Gilt für Vertrieb”](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Falls Sie die vorgegebenen Felder von Rolle und Organisationseinheit als Preisdimensionen vor Version 3 von PSA verwenden, gibt es keine wahrnehmbare Änderung. Sie können Project Service wie gehabt verwenden. 

Wenn Sie einen Preis oder Kosten für Ihre Ressourcen mit zusätzlichen Attributen festlegen müssen, können Sie benutzerdefinierte Felder, Entitäten und Dimensionen einrichten. Weitere Informationen finden Sie in den folgenden Themen. Beachten Sie jedoch, dass Sie die Vorgehensweisen in der unten angegebenen Reihenfolge abschließen müssen:

- [Erstellen benutzerdefinierter Felder und Entitäten](create-custom-fields-entities.md)
- [Hinzufügen von benutzerdefinierten Feldern zum Preissetup und zu Transaktionsentitäten](field-references.md)
- [Einrichten von benutzerdefinierten Feldern als Preisdimensionen](set-up-pricing-dimensions.md)
- [Aktualisieren von Plug-In-Attributen zum Einbinden neuer Preisdimensionen](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Preise für die Personalzeit
Die Preisgestaltung der Personalzeit in einer Organisation ist häufig eine wichtige strategische Überlegung, die sich direkt auf die Rentabilität der Organisation auswirkt. Arbeiten Sie mit den Finanzteams und Übungsleitern zusammen, wenn Ihre Organisation bereit ist, zu ermitteln, wie Rechnungs- und Kostensätze für die Personalzeit eingerichtet werden sollen.

Zu den weiteren Überlegungen für Preise gehört, ob Felder oder Entitäten wiederverwendet werden sollen, die derzeit keine Preisdimensionen sind, jedoch für Ihre Organisation als Preisdimension gelten. Felder wie **Transaktionskategorie** (**msdyn_transactioncategory**) und **Buchbare Ressource** (**bookableresource**) sind Beispiele für Kandidatendimensionen. 

Sie sollten auch berücksichtigen, ob Ihre Preisdimension eine Tabelle oder ein Optionssatz sein soll. Wenn Sie von mehr als 10 oder 12 Änderungen an den Werten einer Dimension ausgehen und Sie zusätzliche Attribute für diese Werte benötigen, können Sie anstelle eines Optionssatzes eine Entität erstellen. Das Verwalten eines Optionssatzes, z. B. das Hinzufügen oder Entfernen von Werten, erfordert einen Administrator oder Entwickler, während das Hinzufügen neuer Zeilen zu einer Tabelle von den meisten Benutzern durchgeführt werden kann.

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
