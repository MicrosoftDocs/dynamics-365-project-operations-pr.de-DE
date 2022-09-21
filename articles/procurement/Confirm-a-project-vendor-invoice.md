---
title: Kreditorenrechnungen des Projekts bestätigen
description: Dieser Artikel erklärt, wie Sie eine Projektlieferantenrechnung in Microsoft Dynamics 365 Project Operations bestätigen und beschreibt die finanziellen Auswirkungen das Bestätigen einer Projektlieferantenrechnung.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475429"
---
# <a name="confirm-project-vendor-invoices"></a>Kreditorenrechnungen des Projekts bestätigen

_ **Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen

Wenn der Parameter **Eine manuelle Bestätigung per PN ist erforderlich** aktiviert ist, sind Kreditorenrechnungen, die in Microsoft Dataverse erstellt werden, im Status **Entwurf**. Auf diese Weise erstellte Lieferantenrechnungen müssen geprüft und manuell bestätigt werden. Wenn der Parameter **Eine manuelle Bestätigung per PN ist erforderlich** aktiviert ist, sind Kreditorenrechnungen, die in Dataverse erstellt werden, automatisch bestätigt. Es ist keine weitere Maßnahme erforderlich. 

Nachdem Sie alle Zeilen auf einer Kreditorenrechnung in Dynamics 365 Project Operations überprüft haben, wählen Sie **Bestätigen** zn due Kreditorenrechnung zu bestätigen.

Wenn Sie bei einer Kreditorenrechnung **Bestätigen** auswählen, tritt das folgende Verhalten auf:

1. Der Status der Kreditorenrechnung wird auf **Bestätigt** aktualisiert.
1. Die bestätigte Kreditorenrechnung und die zugehörigen Datensätze werden schreibgeschützt und können nicht bearbeitet oder gelöscht werden.
1. Wenn Ist-Kosten im Rahmen des Abgleichprozesses auf die Kreditorenrechnungsposition verweisen, werden alle Ist-Kosten, die der referenzierten Kreditorenrechnungsposition zugeordnet sind, storniert.
1. Neue Ist-Kosten werden erstellt, indem die Informationen in der Kreditorenrechnungsposition verwendet werden.
1. Nachdem die Kreditorenrechnung bestätigt wurde, können Sie keine Korrekturerfassungen mehr erstellen, Rückrufe von Zeitbuchungen verarbeiten oder die Genehmigung der ursprünglichen Zeit-, Ausgaben- oder Material-Ist-Werte, die storniert wurden, stornieren.
1. In Dynamics 365 Finance wird der Wert **Projektkosten** mithilfe des Projektintegrationsjournals aktualisiert, und das Procurement-Integrationskonto wird *storniert* nachdem das Projektintegrationsjournal gebucht wurde.

> [!NOTE]
> Wenn eine beliebige Zeile einer Kreditorenrechnung einen anderen Überprüfungsstatus als **Abgeschlossen** hat, kann die Kreditorenrechnung nicht bestätigt werden.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
