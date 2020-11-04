---
title: Ausgabenkategorien einrichten
description: Dieses Thema enthält Informationen zum Einrichten von Ausgabenkategorien und freigegebenen Kategorien für Spesenabrechnungen.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076414"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="40f31-103">Ausgabenkategorien einrichten</span><span class="sxs-lookup"><span data-stu-id="40f31-103">Set up expense categories</span></span>

<span data-ttu-id="40f31-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="40f31-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="40f31-105">Wenn Mitarbeiter Spesenabrechnungen erstellen, muss jede von ihnen erfasste Ausgabe einer Ausgabenkategorie zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="40f31-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="40f31-106">Ausgabenkategorien werden aus gemeinsam genutzten Kategorien abgeleitet, die von den juristischen Personen in Ihrer Organisation gemeinsam genutzt werden können.</span><span class="sxs-lookup"><span data-stu-id="40f31-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="40f31-107">Abhängig von der Definition Ihrer Organisation können diese Ausgabenkategorien auch in anderen Bereichen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="40f31-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="40f31-108">Basierend auf der Definition Ihrer Organisation und den Anweisungen des Implementierungsteams müssen Sie festlegen, ob die in der Ausgabenverwaltung verwendeten Kategorien nur in der Ausgabenverwaltung verwendet werden oder in anderen Bereichen gemeinsam genutzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="40f31-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="40f31-109">Diese Kategorien können zwischen Projektmanagement und Buchhaltung und Ausgabenmanagement oder zwischen Projektmanagement und Buchhaltung und Produktion geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="40f31-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="40f31-110">Sie können jedoch nicht zwischen Ausgabenverwaltung und Produktion aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="40f31-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="40f31-111">Bevor Sie mit dem Einrichtungsprozess beginnen können, müssen für jede Ausgabenkategorie die folgenden Entscheidungen getroffen werden:</span><span class="sxs-lookup"><span data-stu-id="40f31-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="40f31-112">Was ist die Ausgabenkategorie?</span><span class="sxs-lookup"><span data-stu-id="40f31-112">What is the expense category?</span></span> <span data-ttu-id="40f31-113">Beispiele sind Kategorien für Flüge, Hotel oder Kilometerstand.</span><span class="sxs-lookup"><span data-stu-id="40f31-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="40f31-114">Kann die Ausgabenkategorie auch im Projektmanagement und in der Buchhaltung verwendet werden?</span><span class="sxs-lookup"><span data-stu-id="40f31-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="40f31-115">Falls ja, müssen Sie auch die folgenden Entscheidungen treffen:</span><span class="sxs-lookup"><span data-stu-id="40f31-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="40f31-116">Welche Kostenkonten werden für die folgenden Ausgaben verwendet?</span><span class="sxs-lookup"><span data-stu-id="40f31-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="40f31-117">Kosten</span><span class="sxs-lookup"><span data-stu-id="40f31-117">Cost</span></span>
        - <span data-ttu-id="40f31-118">Lohnzuweisung</span><span class="sxs-lookup"><span data-stu-id="40f31-118">Payroll allocation</span></span>
        - <span data-ttu-id="40f31-119">WIP-Einstandswert</span><span class="sxs-lookup"><span data-stu-id="40f31-119">WIP-cost value</span></span>
        - <span data-ttu-id="40f31-120">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="40f31-120">Cost-item</span></span>
        - <span data-ttu-id="40f31-121">WIP-Einstandswertelement</span><span class="sxs-lookup"><span data-stu-id="40f31-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="40f31-122">Antizipierter Verlust</span><span class="sxs-lookup"><span data-stu-id="40f31-122">Accrued loss</span></span>
        - <span data-ttu-id="40f31-123">WIP - Antizipierter Verlust</span><span class="sxs-lookup"><span data-stu-id="40f31-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="40f31-124">Welche Umsatzkonten werden für die folgenden Umsatzquellen verwendet?</span><span class="sxs-lookup"><span data-stu-id="40f31-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="40f31-125">Rechnungsumsatz</span><span class="sxs-lookup"><span data-stu-id="40f31-125">Invoiced revenue</span></span>
        - <span data-ttu-id="40f31-126">Antizipierter Umsatzerlös - Verkaufswert</span><span class="sxs-lookup"><span data-stu-id="40f31-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="40f31-127">WIP - Verkaufswert</span><span class="sxs-lookup"><span data-stu-id="40f31-127">WIP-sales value</span></span>
        - <span data-ttu-id="40f31-128">Antizipierter Umsatzerlös - Produktion</span><span class="sxs-lookup"><span data-stu-id="40f31-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="40f31-129">WIP - Produktion</span><span class="sxs-lookup"><span data-stu-id="40f31-129">WIP-production</span></span>
        - <span data-ttu-id="40f31-130">Antizipierter Umsatzerlös - Gewinn</span><span class="sxs-lookup"><span data-stu-id="40f31-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="40f31-131">WIP - Gewinn</span><span class="sxs-lookup"><span data-stu-id="40f31-131">WIP-profit</span></span>
        - <span data-ttu-id="40f31-132">Antizipierter Umsatz - Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="40f31-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="40f31-133">WIP - Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="40f31-133">WIP-subscription</span></span>

- <span data-ttu-id="40f31-134">Was ist der Ausgabentyp?</span><span class="sxs-lookup"><span data-stu-id="40f31-134">What is the expense type?</span></span>
- <span data-ttu-id="40f31-135">Was ist die Standardzahlungsmethode für die Ausgabenkategorie?</span><span class="sxs-lookup"><span data-stu-id="40f31-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="40f31-136">Müssen Ausgaben in der Ausgabenkategorie aufgelistet werden?</span><span class="sxs-lookup"><span data-stu-id="40f31-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="40f31-137">Was ist das Haupt-Standardkonto für die Ausgabenkategorie?</span><span class="sxs-lookup"><span data-stu-id="40f31-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="40f31-138">Was ist die Standard-Artikel-Mehrwertsteuergruppe für die Ausgabenkategorie?</span><span class="sxs-lookup"><span data-stu-id="40f31-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="40f31-139">Sind zusätzliche Zahlungsmethoden für die Ausgabenkategorie zulässig?</span><span class="sxs-lookup"><span data-stu-id="40f31-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="40f31-140">Wenn ja, wie lauten diese?</span><span class="sxs-lookup"><span data-stu-id="40f31-140">If so, what are they?</span></span>
- <span data-ttu-id="40f31-141">Gibt es Unterkategorien in dieser Ausgabenkategorie?</span><span class="sxs-lookup"><span data-stu-id="40f31-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="40f31-142">Falls es Unterkategorien gibt, müssen Sie auch die folgenden Entscheidungen treffen:</span><span class="sxs-lookup"><span data-stu-id="40f31-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="40f31-143">Sind einige der Unterkategorien von der Steuerrückerstattung ausgeschlossen?</span><span class="sxs-lookup"><span data-stu-id="40f31-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="40f31-144">Was ist die Artikel-Mehrwertsteuergruppe der Unterkategorien?</span><span class="sxs-lookup"><span data-stu-id="40f31-144">What is the item sales tax group of the subcategories?</span></span>