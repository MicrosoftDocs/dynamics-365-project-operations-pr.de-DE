---
title: Finanzielle Vorkalkulationen für die Materialien von Projekten
description: Dieses Thema enthält Informationen zum Definieren oder Schätzen von projektbasierten Materialien.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 98e3611b2b3948aab09a3eadeac7b95b893812e9
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788855"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Finanzielle Vorkalkulationen für die Materialien von Projekten

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations ermöglicht es Projektmanagern, projektbasierte Materialkosten für jedes Projekt oder jede Aufgabe zu definieren. Jeder Materialvoranschlag kann einer bestimmten Projektaufgabe zugeordnet werden. Ausgaben werden in verschiedene Ausgabenkategorien eingeteilt, die auf organisatorischer Ebene definiert werden. Die Preisgestaltung und Kalkulation für jede Ausgabenkategorie ist in der Preisliste definiert. 

Führen Sie die folgenden Schritte aus, um eine Projektmaterialvorkalkulation anzuzeigen, hinzuzufügen oder zu löschen.

1. Gehen Sie zu **Projekte**, und wählen Sie das Projekt aus, das Sie aktualisieren möchten.
2. Auf der **Materialvorkalkulationen**-Registerkarte zeigen Sie die Liste der Projektmaterialvorkalkulation an.
3. Wählen Sie **Neue Materialvorkalkulation** aus, um eine neue Materialvorkalkulation zu erstellen. Oder wählen Sie eine Materialvorkalkulation aus, die gelöscht werden soll, und wählen Sie dann **Materialvorkalkulation löschen** aus.

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
