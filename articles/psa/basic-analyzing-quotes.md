---
title: Analyse von Projektangeboten
description: Dieses Thema enthält Informationen zur Analyse von Projektangeboten.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 6ed900620f92e76d293f6b533b101be94b25cff3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127022"
---
# <a name="analysis-of-project-quotes"></a>Analyse von Projektangeboten

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
