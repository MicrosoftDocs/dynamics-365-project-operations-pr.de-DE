---
title: Projektvertrag bestätigen
description: Dieses Thema enthält Informationen zum Bestätigen eines Vertrags in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d807d3631f40a93ec7dbd918b64c287fd4875c79
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273827"
---
# <a name="confirm-a-project-contract"></a>Projektvertrag bestätigen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

In Dynamics 365 Project Operations kann ein Projektvertrag mit dem Grund **Bestätigt** aktiv oder mit dem Grund **Verloren** geschlossen sein. Wenn Sie einen Projektvertrag bestätigen, wird der Status von **Entwurf** in **Aktiv** aktualisiert, und der Statusgrund lautet **Bestätigt**. Ein aktiver oder geschlossener Vertrag kann nicht bearbeitet oder erneut geöffnet werden. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Finanzielle Auswirkungen der Bestätigung eines Projektvertrags

Nachdem ein Projektvertrag bestätigt wurde, werden die Kosten von der Anwendung neu berechnet, indem die älteren tatsächlichen Kosten zurückgebucht und neue tatsächliche Kosten erneut erstellt werden. Die neuen tatsächlichen Kosten werden dann basierend auf der Fakturierungsmethode der zugehörigen Projektvertragszeile verarbeitet. Wenn die tatsächlichen Kosten auf eine Vertragszeile für Zeit und Material verweisen, erstellt die Anwendung automatisch die entsprechenden nicht fakturierten Umsatz-Istwerte neu. Wenn sich die tatsächlichen Kosten auf eine Festpreisvertragszeile beziehen, beendet die Anwendung die erneute Verarbeitung der tatsächlichen Kosten.

Nicht zu überschreitende Grenzwerte, die Einrichtung der Fakturierbarkeit sowie die Preis- und Kostenberechnung für die Istwerte werden bewertet und dann im Rahmen des Bestätigungsprozesses aktualisiert.

## <a name="close-a-project-contract-as-lost"></a>Einen Projektvertrag als verloren abschließen

Wenn Sie einen Projektvertrag als verloren schließen, wird der Vertragsstatus auf **Geschlossen** aktualisiert und der Statusgrund lautet **Verloren**. Der Projektvertrag ist daraufhin schreibgeschützt. Vor Abschluss der Änderungen wird ein Bestätigungsdialogfeld angezeigt, da Sie einen geschlossenen Projektvertrag nicht erneut öffnen können.

Wenn der als verloren geschlossene Projektvertrag auf ein Projekt in seinen Zeilen verweist, wird dieses Projekt auch als geschlossen markiert. Alle Ressourcenbuchungen ab diesem Tag werden storniert. Alle nicht fakturierten Umsatz-Istwerte des Projektvertrags, die noch nicht auf einer Rechnung stehen, werden storniert.

> [!NOTE]
> Das Schließen eines Projektvertrags in Dynamics 365 Project Operations als „Verloren“ hat keinen Einfluss auf den Status der zugeordneten Verkaufschance. Die Verkaufschance bleibt offen und muss manuell geschlossen werden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]