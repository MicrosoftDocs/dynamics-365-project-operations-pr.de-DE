---
title: Preislisten kopieren
description: Dieses Thema bietet Informationen zum Kopieren von Preislisten in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91ee798a206ea5200780c8ebafc8f99cd9a3e219
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076563"
---
# <a name="copy-price-lists"></a>Preislisten kopieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Sie können Kopien von Preislisten in Dynamics 365 Project Operations erstellen. Sie können beispielsweise Preislisten für das kommende Jahr mithilfe einer Preisliste aus dem aktuellen Jahr erstellen.  Sie können auch eine Preisliste für Rechnungssätze und Verkaufspreise aus den Preislisten für die Kosten kopieren. 

Führen Sie die folgenden Schritte aus, um eine Kopie der Preisliste zu erstellen.

1. Öffnen Sie die Preisliste, von der Sie eine Kopie erstellen möchten, und wählen Sie **Kopieren** aus.
2. Geben Sie alle erforderlichen Informationen ein, um die Preisliste zu kopieren. Die folgende Tabelle enthält Überlegungen, die bei der Eingabe von Informationen zu berücksichtigen sind.

| Feld | Relevanz, Zweck und Anleitung | Nachgelagerte Auswirkungen |
| --- | --- | --- |
| Name des Dataflows | Der Name der Quellpreisliste mit angehängtem **-copy**. | Die Preisliste enthält diesen Wert auf allen Listenseiten und Dropdownoptionen. |
| Kontext | Geben Sie den gewünschten Kontext für die Zielpreisliste ein. | Eine Preisliste, für die der Kontext auf **Kosten** festgelegt ist, wird verwendet, um den Preis für Kostenvoranschläge und tatsächliche Kosten zu suchen. Eine Preisliste, für die der Kontext auf **Umsatz** festgelegt ist, wird verwendet, um den Preis für Umsatzschätzungen und Umsatz-Istwerte zu suchen. Nur Preislisten, für die der Kontext auf **Umsatz** festgelegt ist, können an eine Projektpreisliste für einen Kunden, Angebote oder Verträge angehängt werden. |
| Startdatum | Das Startdatum des Zeitraums, in dem sich die Preisliste befindet, ist wirksam. | Zusammen mit dem **Enddatum** wird dieses Feld verwendet, um festzulegen, welche Preisliste für eine bestimmte Schätzung oder tatsächliche Zeile gilt. |
| Enddatum | Das Enddatum des Zeitraums, in dem sich die Preisliste befindet, ist wirksam. | Zusammen mit dem **Startdatum** wird dieses Feld verwendet, um festzulegen, welche Preisliste für eine bestimmte Schätzung oder tatsächliche Zeile gilt. |
| Währung | Die Währung der Quellpreisliste. Dies kann geändert werden. | Wenn dies geändert wird, werden alle resultierenden Preiszeilen für Arbeits-, Kosten- und Produktkatalogelemente während des Kopierens in die Zielpreislistenwährung konvertiert. |
| Zeiteinheit | Die Währung der Quellpreisliste. Dies kann geändert werden. | Wenn dies geändert wird, werden alle resultierenden Preiszeilen für Arbeitselemente während des Kopierens in die Zielpreislisteneinheit konvertiert. Die Umrechnung aus dem Einheiten-Setup für die Zeiteinheit der Quellpreisliste und die Zeiteinheit der Zielpreisliste werden verwendet. |
| Beschreibung des Dataflows | Eine Beschreibung der Quellpreisliste mit angehängtem **-copy**. Dies ist ein Textfeld, mit dem Sie die Preisliste mehrzeilig beschreiben können. | Dieses Feld wird in den Ansichten **Zugeordnet** in der Preisliste in verschiedenen Entitäten angezeigt, die zugehörige Preislisten haben. |

3. Speichern Sie die Preisliste. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Eine Preisliste aktualisieren, indem Sie auf alle Preise einen Aufschlag anwenden

1. Auf der Registerkarte **Rolle**, **Kategorie** und **Preislistenelement** einer Preisliste, können Sie **Preise aktualisieren** auswählen, um einen Aufschlag auf alle Preise im Unterraster anzuwenden. 
2. Geben Sie auf der sich öffnenden Dialogseite einen Aufschlag ein. Sie können auch einen negativen Aufschlag in Prozent eingeben, um die Preise um einen bestimmten Prozentsatz zu senken. 
3. Wählen Sie **OK** auf der Dialogseite aus, und prüfen Sie dann, ob die Preise im Unterraster die von Ihnen durchgeführten Änderungen widerspiegeln.
