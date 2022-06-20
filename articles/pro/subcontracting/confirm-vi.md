---
title: Eine Projektkreditorenrechnung bestätigen
description: Dieser Artikel erklärt, wie Sie eine Projektlieferantenrechnung in Microsoft Dynamics 365 Project Operations bestätigen und welche finanziellen Auswirkungen das Bestätigen einer Projektlieferantenrechnung hat.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932433"
---
# <a name="confirm-a-project-vendor-invoice"></a>Eine Projektkreditorenrechnung bestätigen

[!include [banner](../../includes/dataverse-preview.md)]

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
