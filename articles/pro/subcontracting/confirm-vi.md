---
title: Eine Projektkreditorenrechnung bestätigen
description: Dieser Artikel erklärt, wie Sie eine Projektlieferantenrechnung in Microsoft Dynamics 365 Project Operations bestätigen und welche finanziellen Auswirkungen das Bestätigen einer Projektlieferantenrechnung hat.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261510"
---
# <a name="confirm-a-project-vendor-invoice"></a>Eine Projektkreditorenrechnung bestätigen

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Nachdem Sie alle Zeilen auf einer Kreditorenrechnung in Microsoft Dynamics 365 Project Operations überprüft haben, können Sie die Kreditorenrechnung mit der Aktion „Bestätigen“ bestätigen.

Wenn Sie bei einer Kreditorenrechnung **Bestätigen** auswählen, tritt das folgende Verhalten auf:

1. Der Status der Kreditorenrechnung wird auf **Bestätigt** aktualisiert.
2. Die bestätigte Kreditorenrechnung und die zugehörigen Datensätze werden schreibgeschützt und können nicht bearbeitet oder gelöscht werden.
3. Wenn Ist-Kosten im Rahmen des Abgleichprozesses auf die Kreditorenrechnungsposition verweisen, werden alle Ist-Kosten, die der referenzierten Kreditorenrechnungsposition zugeordnet sind, storniert.
4. Neue Ist-Kosten werden erstellt, indem die Informationen in der Kreditorenrechnungsposition verwendet werden.
5. Nachdem die Kreditorenrechnung bestätigt wurde, können Sie keine Korrekturerfassungen mehr erstellen, Rückrufe von Zeitbuchungen verarbeiten oder die Genehmigung der ursprünglichen Zeit-, Ausgaben- oder Material-Ist-Werte, die sotrniert wurden, stornieren.

> [!NOTE]
> Wenn eine beliebige Zeile einer Kreditorenrechnung einen anderen Überprüfungsstatus als **Abgeschlossen** hat, kann die Kreditorenrechnung nicht bestätigt werden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
