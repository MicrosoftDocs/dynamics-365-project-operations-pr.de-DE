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
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012450"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="7b927-103">Analyse von Projektangeboten</span><span class="sxs-lookup"><span data-stu-id="7b927-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7b927-104">Dynamics 365 Project Service Automation analysiert Projektangebote zur Schätzung der Rentabilität.</span><span class="sxs-lookup"><span data-stu-id="7b927-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="7b927-105">Außerdem wird analysiert, wie gut das Angebot mit den Kundenerwartungen hinsichtlich des Liefer- oder Fertigstellungstermins und des Budgets übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7b927-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="7b927-106">Rentabilitätsanalyse</span><span class="sxs-lookup"><span data-stu-id="7b927-106">Profitability analysis</span></span>

<span data-ttu-id="7b927-107">Project Service Automation analysiert die Rentabilität anhand des Bruttogewinns und des bereinigten Bruttogewinns.</span><span class="sxs-lookup"><span data-stu-id="7b927-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="7b927-108">Bruttogewinne werden mithilfe der folgenden Formel berechnet:</span><span class="sxs-lookup"><span data-stu-id="7b927-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="7b927-109">Der bereinigte Bruttogewinn wird mithilfe der folgenden Formel berechnet:</span><span class="sxs-lookup"><span data-stu-id="7b927-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="7b927-110">Wenn sich die Werte für die Bruttogewinne und die bereinigten Bruttogewinne erheblich unterscheiden, wird ein Großteil der Arbeit im Angebot als nicht fakturierbar eingestuft.</span><span class="sxs-lookup"><span data-stu-id="7b927-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="7b927-111">Analyse der Kundenerwartungen</span><span class="sxs-lookup"><span data-stu-id="7b927-111">Analysis of customer expectations</span></span>

<span data-ttu-id="7b927-112">Sie können Angebote analysieren und Diagramme für Kundenerwartungen zu Zeitplan und Budget erstellen, wenn Sie für die folgenden Felder Werte eingeben:</span><span class="sxs-lookup"><span data-stu-id="7b927-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="7b927-113">Das Feld **Gewünschtes Lieferdatum** in der Angebotskopfzeile.</span><span class="sxs-lookup"><span data-stu-id="7b927-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="7b927-114">Das Feld **Kundenbudget** für jede Angebotszeile (für projektbasierte Zeilen und produktbasierte Zeilen).</span><span class="sxs-lookup"><span data-stu-id="7b927-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="7b927-115">Die Analyse der Kundenerwartungen bezüglich des Zeitplans erfolgt durch Vergleichen des letzten Enddatums des Angebotszeilendetails mit dem angeforderten Lieferdatum über alle Angebotszeilen im Angebot.</span><span class="sxs-lookup"><span data-stu-id="7b927-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="7b927-116">Die Analyse der Kundenerwartungen zum Budget erfolgt durch Vergleich der Summe des gesamten Kundenbudgets mit dem Angebotsbetrag über alle Angebotszeilen hinweg.</span><span class="sxs-lookup"><span data-stu-id="7b927-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]