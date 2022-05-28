---
title: Eine Projektkreditorenrechnung bestätigen
description: In diesem Thema wird erläutert, wie Sie eine Projektkreditorenrechnung in Microsoft Dynamics 365 Project Operations bestätigen, und die finanziellen Auswirkungen der Bestätigung einer Projektlieferantenrechnung werden erläutert.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595727"
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
