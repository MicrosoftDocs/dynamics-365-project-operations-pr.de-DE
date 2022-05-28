---
title: Analyse von Projektangeboten
description: Dieses Thema enthält Informationen zur Analyse von Projektangeboten.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: f3bff90f91e1df8bda495912a4aad0fa69342396
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592415"
---
# <a name="analysis-of-project-quotes"></a>Analyse von Projektangeboten

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analysiert Projektangebote zur Schätzung der Rentabilität. Außerdem wird analysiert, wie gut das Angebot mit den Kundenerwartungen hinsichtlich des Liefer- oder Fertigstellungstermins und des Budgets übereinstimmt.

## <a name="profitability-analysis"></a>Rentabilitätsanalyse

Project Service Automation analysiert die Rentabilität anhand des Bruttogewinns und des bereinigten Bruttogewinns.

- Bruttogewinne werden mithilfe der folgenden Formel berechnet:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Der bereinigte Bruttogewinn wird mithilfe der folgenden Formel berechnet:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Wenn sich die Werte für die Bruttogewinne und die bereinigten Bruttogewinne erheblich unterscheiden, wird ein Großteil der Arbeit im Angebot als nicht fakturierbar eingestuft.

## <a name="analysis-of-customer-expectations"></a>Analyse der Kundenerwartungen

Sie können Angebote analysieren und Diagramme für Kundenerwartungen zu Zeitplan und Budget erstellen, wenn Sie für die folgenden Felder Werte eingeben:

- Das Feld **Gewünschtes Lieferdatum** in der Angebotskopfzeile.
- Das Feld **Kundenbudget** für jede Angebotszeile (für projektbasierte Zeilen und produktbasierte Zeilen).

Die Analyse der Kundenerwartungen bezüglich des Zeitplans erfolgt durch Vergleichen des letzten Enddatums des Angebotszeilendetails mit dem angeforderten Lieferdatum über alle Angebotszeilen im Angebot.

Die Analyse der Kundenerwartungen zum Budget erfolgt durch Vergleich der Summe des gesamten Kundenbudgets mit dem Angebotsbetrag über alle Angebotszeilen hinweg.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
