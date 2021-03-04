---
title: Warum kann ich keine Datensätze aus der Ist-Werte-Entität löschen?
description: In diesem Thema erfahren Sie, warum Sie keine Datensätze aus der Ist-Werte-Entität löschen können.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 36cd241c7c7a2ff6ae018c94d691bc95d1f0c912
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148957"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="c444b-103">Warum kann ich keine Datensätze aus der Ist-Werte-Entität löschen?</span><span class="sxs-lookup"><span data-stu-id="c444b-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c444b-104">Project Service Automation (PSA) können Sie Ist-Werte nicht löschen, da sie als Wahrheitsquelle für Transaktionen dienen, die finanzielle Auswirkungen auf nachgelagerte Systeme haben, z. B. das Sachkonto.</span><span class="sxs-lookup"><span data-stu-id="c444b-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="c444b-105">Wenn Ist-Werte gelöscht werden könnten, könnte die Integrität der Finanzberichterstattungstransaktionen in Frage gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c444b-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="c444b-106">Um einen Audit-Trail einzurichten, sollten Kunden Journale verwenden, um Ausgleichstransaktionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c444b-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

