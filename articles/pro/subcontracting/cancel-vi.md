---
title: Eine Projektkreditorenrechnung stornieren
description: Dieser Artikel erklärt, wie Sie eine Projektlieferantenrechnung in Microsoft Dynamics 365 Project Operations stornieren und welche finanziellen Auswirkungen das Stornieren einer Projektlieferantenrechnung hat.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261089"
---
# <a name="cancel-a-project-vendor-invoice"></a>Eine Projektkreditorenrechnung stornieren

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
