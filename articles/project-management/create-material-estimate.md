---
title: Finanzielle Vorkalkulationen für die Materialien von Projekten
description: Dieser Artikel enthält Informationen über die Definition oder Schätzung von projektbasierten Materialien.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eb33c8e2ead2a558bf53256095645011212ff343
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925692"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Finanzielle Vorkalkulationen für die Materialien von Projekten

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations ermöglicht es Projektmanagern, projektbasierte Materialkosten für jedes Projekt oder jede Aufgabe zu definieren. Jede Materialschätzung kann einer bestimmten Projektaufgabe zugeordnet werden. Materialien, die in Projekten verwendet werden, können beschreibbare Produkte oder Produkte aus dem Produktkatalog sein. Für jede Kombination aus einem Produkt und einer Einheit kann in den Projektpreislisten für den Verkauf und den Projektpreislisten für die Kosten ein Preis definiert werden.  

Führen Sie die folgenden Schritte aus, um Materialschätzungen für ein Projekt anzuzeigen, hinzuzufügen oder zu löschen:

1. Wechseln Sie zu **Projekte**, und wählen Sie das Projekt aus, das Sie aktualisieren möchten.
2. Zeigen Sie auf der Registerkarte **Materialvorkalkulationen** die Liste der Projektmaterialschätzungen an.
3. Wählen Sie **Neue Materialschätzung** aus, um eine neue Materialschätzung zu erstellen. Oder wählen Sie eine Materialvorkalkulation aus, die gelöscht werden soll, und wählen Sie dann **Materialvorkalkulation löschen** aus.

Die folgende Tabelle enthält Informationen zu den Feldern auf der **Materialvorkalkulationszeile** in einem Projekt. 

| **Feld** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- |
| Aufgabe | Eine Liste der Aufgaben im Projekt. Dies umfasst Zusammenfassungs- und Blattknotenaufgaben. | Wenn Sie eine Aufgabe für eine Materialvorkalkulationszeile auswählen, werden die geschätzten Materialkosten und der geschätzte Materialumsatz für eine Aufgabe beeinflusst. Wenn dieses Feld leer ist, werden die entsprechenden Materialvorkalkulationen nur auf Projektebene verfolgt und zusammengefasst. |
| Produkt auswählen |  Sie können auswählen, ob diese Schätzposition für ein bestimmtes Vorhandenes (Katalog-)Produkt oder ein „Manueller Eintrag“-Produkt ist. | Dieses Feld bestimmt, ob Sie ein Produkt aus dem Katalog oder ein „Manueller Eintrag“-Produkt auswählen. |
| Produkt | Die ID des Produkts aus dem Produktkatalog. Wenn Sie eine Produkt-ID auswählen, wird der Wert im  **Produkt auswählen**-Feld automatisch auf **Vorhandenes Produkt** aktualisiert. Die ID wird verwendet, um Kosten und Verkaufspreise aus der Preisliste abzurufen. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Beschreibung des manuell einzutragenden Produkts | Ein Textfeld zum Schreiben im Namen des Produkts. Dieses Feld sollte verwendet werden, wenn Sie **Manueller Eintrag** im Feld **Produkt auswählen** gewählt haben.| Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Startdatum | Das vorhergesagte Datum, an dem das Material voraussichtlich verwendet wird. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Einheitengruppe | Der Standardwert in diesem Feld stammt aus der Standardeinheitengruppe im Katalogprodukt. Sie können dieses Feld aktualisieren, um eine andere Einheitengruppe auszuwählen. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Einheit | Der Standardwert in diesem Feld entstammt der Standardeinheit des ausgewählten Produkts. Sie können dieses Feld aktualisieren, um eine andere Einheit auszuwählen. | Das Ändern der Einheit führt zu einem anderen Standardeinheitspreis und anderen Kosten. |
| Menge | Die geschätzte Menge des Produkts, die für das Projekt verwendet wird. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Stückkosten | Die Stückkosten der ausgewählten Produkt- und Stückkombination, wie in der entsprechenden Kostenpreisliste angegeben. | Die Stückkosten werden immer in der Kostenwährung des Projekts angezeigt. Wenn in der Preisliste keine Stückkosten für das Kombinationsprodukt und die Einheit eingerichtet sind, werden die Stückkosten standardmäßig auf 0,00 gesetzt. |
| Einheitenpreis | Der Preis der ausgewählten Produkt- und Stückkombination, wie in der entsprechenden Verkaufspreisliste angegeben. | Die Stückpreise werden immer in der Verkaufswährung des Projekts angezeigt. Wenn in der Preisliste keine Preis pro Einheit für das Kombinationsprodukt und die Einheit eingerichtet sind, wird der Einheitenpreis standardmäßig auf 0,00 gesetzt.|
| Gesamtkosten | Der Kostenbetrag wird als Menge \* Kosten pro Einheit berechnet.| Der Kostenbetrag wird immer in der Kostenwährung des Projekts angezeigt. |
| Gesamtumsatz | Der Verkaufsbetrag wird als Menge \* Preis pro Einheit berechnet. | Der Verkaufsbetrag immer in der Verkaufswährung des Projekts angezeigt. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
