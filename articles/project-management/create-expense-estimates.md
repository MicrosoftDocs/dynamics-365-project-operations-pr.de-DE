---
title: Finanzielle Vorkalkulationen für die Ausgaben von Projekten
description: Dieses Thema enthält Informationen zum Definieren oder Kalkulieren projektbasierter Ausgaben.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c14dc31d666d0e0d026cf9cddfa1e78dee40f717
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589471"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Finanzielle Vorkalkulationen für die Ausgaben von Projekten
_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations ermöglicht es Projektmanagern, projektbasierte Ausgaben für jedes Projekt oder jede Aufgabe zu definieren. Jeder Ausgabenartikel kann einer bestimmten Projektaufgabe zugeordnet werden. Ausgaben werden in verschiedene Ausgabenkategorien eingeteilt, die auf organisatorischer Ebene definiert werden. Die Preisgestaltung und Schätzung für jede Spesenkategorie ist in der Preisliste definiert. 

Führen Sie die folgenden Schritte aus, um Projektkosten anzuzeigen, hinzuzufügen oder zu löschen.

1. Wechseln Sie zu **Projekte** und wählen Sie das Projekt aus, an dem Sie arbeiten möchten.
2. Wählen Sie die Registerkarte **Projektvorkalkulationen** aus und zeigen Sie die Liste der Projektkosten an.
3. Wählen Sie **Neue Ausgabe** aus, um eine neue Ausgabe hinzuzufügen. Oder wählen Sie eine zu löschende Ausgabe aus und wählen Sie dann **Ausgabe löschen**.

Die folgende Tabelle enthält Informationen zu den Feldern auf der **Kostenvorkalkulationszeile** in einem Projekt. 

| **Feld** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- |
| Aufgabe | Eine Liste der Aufgaben im Projekt. Dies umfasst Zusammenfassungs- und Blattknotenaufgaben. | Die Auswahl einer Aufgabe für eine Kostenvorkalkulationszeile wirkt sich auf die geschätzten Kostenkosten und den geschätzten Kostenumsatz für eine Aufgabe aus. Wenn dieses Feld leer ist, werden die entsprechenden Ausgabenvorkalkulationen nur auf Projektebene verfolgt und zusammengefasst. |
| Kateg. | Eine Liste von Transaktionskategorien, die Ausgabenkategorien in der Anwendung verknüpft haben. | Durch Auswahl einer Kategorie werden Preisgestaltung und Kostenberechnung in der Kostenschätzungszeile gesteuert. |
| Startdatum | Das prognostizierte Datum, an dem die Kosten anfallen werden. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Einheitengruppe | Der Standardwert in diesem Feld stammt aus der Einheitengruppe, die als Standard für die ausgewählte Kategorie eingerichtet wurde. Sie können dieses Feld aktualisieren, um eine andere Einheitengruppe auszuwählen. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Einheit | Der Standardwert in diesem Feld ist die Standardeinheit der ausgewählten Kategorie. Sie können dieses Feld aktualisieren, um eine andere Einheit auszuwählen. | Das Ändern der Einheit führt zu einem anderen Standardeinheitspreis und anderen Kosten. |
| Menge | Die Menge der geschätzten Kosten, die Ihnen entstehen. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Stückkosten | Die Kosten der ausgewählten Kategorie- und Einheitenkombination, wie in der entsprechenden Kostenpreisliste angegeben | Die Stückkosten werden immer in der Kostenwährung des Projekts angezeigt. |
| Einheitenpreis | Der Preis der ausgewählten Kategorie- und Stückkombination, wie in der entsprechenden Verkaufspreisliste angegeben. | Die Stückpreise werden immer in der Verkaufswährung des Projekts angezeigt. |
| Gesamtkosten | Der Kostenbetrag wird als Menge \* Kosten pro Einheit berechnet.| Der Kostenbetrag wird immer in der Kostenwährung des Projekts angezeigt. |
| Gesamtumsatz | Der Verkaufsbetrag wird als Menge \* Preis pro Einheit berechnet. | Der Verkaufsbetrag immer in der Verkaufswährung des Projekts angezeigt. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
