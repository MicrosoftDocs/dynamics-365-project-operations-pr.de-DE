---
title: Preisdimensionen – Übersicht
description: Dieser Artikel enthält Informationen über die Dimensionen der Preisgestaltung in Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 294dcff8e9717aaa3a0459daf87cb7d608c96106
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918035"
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

![Screenshot der Project Service-Parameter mit Markierung von „Gilt für Vertrieb“.](media/PS-OOB-parameters.png)

Wenn Sie einen Preis oder Kosten für Ihre Ressourcen mit zusätzlichen Attributen festlegen müssen, können Sie benutzerdefinierte Felder, Entitäten und Dimensionen einrichten. Weitere Informationen finden Sie in den folgenden Artikeln. 
  
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
| Entwickler   | Contoso US  |Hour | 200|USD     |
| Entwickler   | Koch Indien |Hour|   112|USD     |


**Beispielkostensätze**

| Gehaltsspanne     | Organisationseinheit    |Einheit      |Preis      |Währung  |
| ----------------|-------------|----------|----------:|----------|
| Mein Unternehmen_Band1 | Contoso US  |Hour | 145|USD     |
| Mein Unternehmen_Band2 | Koch Indien |Hour|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]