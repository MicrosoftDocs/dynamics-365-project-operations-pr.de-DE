---
title: Warum ist der Standardpreis bei tatsächlichen Werten für Ausgabenkosten null?
description: Fehlerbehebung warum der Standardpreis bei tatsächlichen Werten für Ausgabenkosten null ist.
author: rumant
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7de9f660bf38629bb2af4e0fb1ebf815f5e525e2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595589"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Warum ist der Standardpreis bei tatsächlichen Transaktionen für Ausgabenkosten null

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dieses FAQ gilt für tatsächliche Ausgabenwerte, bei denen die Transaktionsklasse auf „Ausgabe“ und der Transaktionstyp auf „Kosten“ festgelegt ist.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Problembehandlung von Kostenraten bei tatsächlichen Werten für Augabenkosten

Rufen Sie den entsprechenden Ausgabeneintrag auf und stellen Sie sicher, dass ein Betrag im Ausgabeneingabefeld steht. Falls beim ursprüngliche Ausgabeneintrag das Betragsfeld nicht ausgefüllt war, haben Sie das Problem isoliert.
 
Um dieses Problem zu beheben, erstellen Sie den Ausgabeneintrag erneut mit einem gültigen Betrag und genehmigen Sie ihn.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
