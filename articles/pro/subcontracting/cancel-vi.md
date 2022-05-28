---
title: Eine Projektkreditorenrechnung stornieren
description: In diesem Thema wird erläutert, wie Sie eine Projektkreditorenrechnung in Microsoft Dynamics 365 Project Operations stornieren, und die finanziellen Auswirkungen der Stornierung einer Projektlieferantenrechnung werden erläutert.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580639"
---
# <a name="cancel-a-project-vendor-invoice"></a>Eine Projektkreditorenrechnung stornieren

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Nach der Bestätigung einer Kreditorenrechnung kann diese nicht bearbeitet oder gelöscht werden. Wenn bei einer bestätigten Kreditorenrechnung ein Fehler aufgetreten ist, können Sie die Aktion Stornieren verwenden, um die Auswirkung der Kreditorenrechnung rückgängig zu machen und eine neue Kreditorenrechnung zu erstellen.

Wenn Sie bei einer Kreditorenrechnung **Stornieren** auswählen, tritt das folgende Verhalten auf:

1. Der Status der Kreditorenrechnung wird auf **Storniert** aktualisiert.
2. Die stornierte Kreditorenrechnung und die zugehörigen Datensätze werden schreibgeschützt und können nicht bearbeitet oder gelöscht werden.
3. Alle tatsächlichen Kosten, die basierend auf Kreditorenrechnungspositionen als Teil der Bestätigung der Kreditorenrechnung erstellt wurden, werden storniert.
4. Wenn im Rahmen des Abgleichs Ist-Kosten mit den Kreditorenrechnungspositionen verknüpft wurden, wurden sie durch die ursprüngliche Kreditorenrechnungsbestätigung storniert. Während der Kreditorenrechnungsstornierung werden diese Kosten-Ist-Werte neu erstellt. Die Ursprünge zeigen auf die Zeit-, Aufwands- oder Materialverbrauchseinträge.
5. Nachdem die Kreditorenrechnung storniert wurde, können Sie erneut Korrekturerfassungen erstellen, Rückrufe von Zeitbuchungen verarbeiten und die Genehmigung der ursprünglichen Zeit-, Ausgaben- oder Material-Ist-Werte stornieren.

> [!NOTE]
> Nur bestätigte Kreditorenrechnungen für ein Projekt können storniert werden. Kreditorenrechnungen in anderen Status können nicht storniert werden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
