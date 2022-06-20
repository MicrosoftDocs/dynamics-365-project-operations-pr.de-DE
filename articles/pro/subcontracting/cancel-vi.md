---
title: Eine Projektkreditorenrechnung stornieren
description: Dieser Artikel erklärt, wie Sie eine Projektlieferantenrechnung in Microsoft Dynamics 365 Project Operations stornieren und welche finanziellen Auswirkungen das Stornieren einer Projektlieferantenrechnung hat.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911549"
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
