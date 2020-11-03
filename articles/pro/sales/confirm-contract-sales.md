---
title: Projektvertrag bestätigen
description: Dieses Thema enthält Informationen zum Bestätigen eines Vertrags in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076644"
---
# <a name="confirm-a-project-contract"></a>Projektvertrag bestätigen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Ein Projektvertrag in Dynamics 365 Project Operations kann aus dem Grund **Bestätigt** aktiv oder durch den Grund **Verloren** geschlossen sein. Wenn Sie einen Projektvertrag bestätigen, wird der Status von **Entwurf** in **Aktiv** aktualisiert, und der Statusgrund lautet **Bestätigt**. Ein aktiver oder geschlossener Vertrag kann nicht bearbeitet oder erneut geöffnet werden. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Finanzielle Auswirkungen der Bestätigung eines Projektvertrags

Nachdem ein Projektvertrag bestätigt wurde, werden die Kosten von der Anwendung neu berechnet, indem die älteren tatsächlichen Kosten zurückgebucht und neue tatsächliche Kosten erneut erstellt werden. Die neuen tatsächlichen Kosten werden dann basierend auf der Fakturierungsmethode der zugehörigen Projektvertragszeile verarbeitet. Wenn die tatsächlichen Kosten auf eine Vertragszeile für Zeit und Material verweisen, erstellt die Anwendung automatisch die entsprechenden nicht fakturierten Umsatz-Istwerte neu. Wenn sich die tatsächlichen Kosten auf eine Festpreisvertragszeile beziehen, beendet die Anwendung die erneute Verarbeitung der tatsächlichen Kosten.

Nicht zu überschreitende Grenzwerte, die Einrichtung der Fakturierbarkeit sowie die Preis- und Kostenberechnung für die Istwerte werden bewertet und dann im Rahmen des Bestätigungsprozesses aktualisiert.

## <a name="close-a-project-contract-as-lost"></a>Einen Projektvertrag als verloren abschließen

Wenn Sie einen Projektvertrag als verloren schließen, wird der Vertragsstatus auf **Geschlossen** aktualisiert und der Statusgrund lautet **Verloren**. Der Projektvertrag ist daraufhin schreibgeschützt. Vor Abschluss der Änderungen wird ein Bestätigungsdialogfeld angezeigt, da Sie einen geschlossenen Projektvertrag nicht erneut öffnen können.

Wenn der als verloren geschlossene Projektvertrag auf ein Projekt in seinen Zeilen verweist, wird dieses Projekt auch als geschlossen markiert. Alle Ressourcenbuchungen ab diesem Tag werden storniert. Alle nicht fakturierten Umsatz-Istwerte des Projektvertrags, die noch nicht auf einer Rechnung stehen, werden storniert.

> [!NOTE]
> In Dynamics 365 Project Operations wirkt sich das Schließen eines Projektvertrags als „Verloren“ nicht auf diesen Status der zugeordneten Verkaufschance aus. Die Verkaufschance bleibt offen und muss manuell geschlossen werden.
