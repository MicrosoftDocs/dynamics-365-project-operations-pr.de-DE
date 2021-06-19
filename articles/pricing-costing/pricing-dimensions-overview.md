---
title: Preisdimensionen – Übersicht
description: Dieses Thema enthält Informationen zum Einrichten der Preisdimensionen in Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 01ba11e34e7d8a59716fa9d8c8be3389ab380048
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004980"
---
# <a name="pricing-dimensions-overview"></a>Preisdimensionen – Übersicht

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Die Dimensionen, die in der Personalverwaltung zum Einrichten von Preisen und Kosten verwendet werden, lassen sich in zwei Kategorien einteilen:

- Personen
- Geplante Arbeit

Aus diesem Grund stehen zwei Arten von Preisdimensionswerten zur Verfügung:

- **Optionssätze**: Dimensionen, bei denen es sich um feste Enumerationen für einen Satz von Werten handelt.
- **Entität-basierte Werte**: Dimensionen, bei denen es sich um unterschiedliche Sätze von Werten handeln kann.

## <a name="pricing-dimensions"></a>Preisdimensionen

Dynamics 365 Project Operations wird mit einem Standardsatz an Preisdimensionen bereitgestellt. Sie können diese Preisdimensionen anzeigen, indem Sie zu **Project Operations** > **Parameter** navigieren. Prüfen Sie im Parameterdatensatz auf der Registerkarte **Betragsbasierte Preisdimensionen**, dass bei der Rolle **msdyn_resourcecategory** und der Organisationseinheit der Ressource **msdyn_organizationalunit** die Felder **Gilt für Vertrieb** und **Gilt für Kosten** auf **Ja** festgelegt sind. Wenn diese Felder aktiviert sind, können Sie den Preis und die Kosten für jede Kombination aus Rolle und Organisationseinheit einrichten.

![Screenshot der Project Service-Parameter mit Markierung von „Gilt für Vertrieb”](media/PS-OOB-parameters.png)

Wenn Sie einen Preis oder Kosten für Ihre Ressourcen mit zusätzlichen Attributen festlegen müssen, können Sie benutzerdefinierte Felder, Entitäten und Dimensionen einrichten. Weitere Informationen finden Sie in den folgenden Themen. 
  
  > [!NOTE]
  > Die Verfahren müssen in der angegebenen Reihenfolge ausgeführt werden.

1. [Erstellen einer Lösung für benutzerdefinierte Preisdimensionen](../sales/create-solution-custompd.md)
2. [Erstellen von benutzerdefinierten Feldern und Entitäten](create-custom-fields-entities-pricing-dimensions.md)
3. [Hinzufügen von benutzerdefinierten Feldern zur Preisgestaltung und zu Transaktionsentitäten ](add-custom-fields-price-setup-transactional-entities.md)
4. [Einrichten von benutzerdefinierten Feldern als Preisdimensionen ](set-up-custom-fields-pricing-dimensions.md)
5. [Aktualisieren von Plug-In-Attributen zum Einbinden neuer Preisdimensionen](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Preise für die Personalzeit
Die Preisgestaltung der Personalzeit in einer Organisation ist häufig eine wichtige strategische Überlegung, die sich direkt auf die Rentabilität der Organisation auswirkt. Arbeiten Sie mit den Finanzteams und Übungsleitern zusammen, wenn Ihre Organisation bereit ist, zu ermitteln, wie Rechnungs- und Kostensätze für die Personalzeit eingerichtet werden sollen.

Zu den weiteren Überlegungen für Preise gehört, ob Felder oder Entitäten wiederverwendet werden sollen, die derzeit keine Preisdimensionen sind, jedoch für Ihre Organisation als Preisdimension gelten. Felder wie **Transaktionskategorie** (**msdyn_transactioncategory**) und **Buchbare Ressource** (**bookableresource**) sind Beispiele für Kandidatendimensionen. 

Sie sollten ebenfalls berücksichtigen, ob Ihre Preisdimension eine Tabelle oder ein Optionssatz sein soll. Wenn Sie von mehr als 10 oder 12 Änderungen an den Werten einer Dimension ausgehen und Sie zusätzliche Attribute für diese Werte benötigen, können Sie anstelle eines Optionssatzes eine Entität erstellen. Das Verwalten eines Optionssatzes, z. B. das Hinzufügen oder Entfernen von Werten, erfordert einen Administrator oder Entwickler, während das Hinzufügen neuer Zeilen zu einer Tabelle von den meisten Benutzern durchgeführt werden kann.

Das folgende Beispiel zeigt Rechnungssätze, die basierend auf der Rolle und der Organisationseinheit der Ressource, zu der die Ressource gehört, eingerichtet werden. Kostensätze basieren in der Regel auf der Gehaltsspanne des Mitarbeiters und der Organisationseinheit, die er zugeordnet wurde. In diesem Beispiel sehen die Abrechnungs- und Kostensatztabellen wie folgt aus.

**Beispielrechnungssätze**

| Rolle        | Organisationseinheit    |Einheit      |Preis      |Währung  |
| ------------|-------------|----------|----------:|----------|
| Developer   | Contoso (USA)  |Stunde | 200|US-Dollar     |
| Developer   | Contoso Indien |Stunde|   112|US-Dollar     |


**Beispielkostensätze**

| Gehaltsspanne     | Organisationseinheit    |Einheit      |Preis      |Währung  |
| ----------------|-------------|----------|----------:|----------|
| Mein Unternehmen_Band1 | Contoso (USA)  |Stunde | 145|US-Dollar     |
| Mein Unternehmen_Band2 | Contoso Indien |Stunde|   67|US-Dollar     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]