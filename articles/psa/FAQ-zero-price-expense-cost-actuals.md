---
title: Warum ist der Standardpreis bei tatsächlichen Werten für Ausgabenkosten null?
description: Fehlerbehebung warum der Standardpreis bei tatsächlichen Werten für Ausgabenkosten null ist.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122117"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="331df-103">Warum ist der Standardpreis bei tatsächlichen Werten für Ausgabenkosten null?</span><span class="sxs-lookup"><span data-stu-id="331df-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="331df-104">Dieses FAQ gilt für tatsächliche Ausgabenwerte, bei denen die Transaktionsklasse auf „Ausgabe” und der Transaktionstyp auf „Kosten” festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="331df-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="331df-105">Problembehandlung von Kostenraten bei tatsächlichen Werten für Augabenkosten</span><span class="sxs-lookup"><span data-stu-id="331df-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="331df-106">Rufen Sie den entsprechenden Ausgabeneintrag auf und stellen Sie sicher, dass ein Betrag im Ausgabeneingabefeld steht.</span><span class="sxs-lookup"><span data-stu-id="331df-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="331df-107">Falls beim ursprüngliche Ausgabeneintrag das Betragsfeld nicht ausgefüllt war, haben Sie das Problem isoliert.</span><span class="sxs-lookup"><span data-stu-id="331df-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="331df-108">Um dieses Problem zu beheben, erstellen Sie den Ausgabeneintrag erneut mit einem gültigen Betrag und genehmigen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="331df-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
