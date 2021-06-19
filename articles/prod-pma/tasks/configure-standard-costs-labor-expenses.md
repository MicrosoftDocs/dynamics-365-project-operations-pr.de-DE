---
title: Konfigurieren Sie die Standardkosten für Arbeit und Ausgaben
description: In diesem Thema wird erläutert, wie Standardkosten für Arbeitskräfte und Kosten für ein Projekt eingerichtet werden.
author: Yowelle
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 517e5ae776cff18aec81e5446a7aaedfba61ac0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011010"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="f9e4b-103">Konfigurieren Sie die Standardkosten für Arbeit und Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9e4b-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9e4b-104">In diesem Thema wird erläutert, wie Standardkosten für Arbeitskräfte und Kosten für ein Projekt eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="f9e4b-105">Diese Aufgabe verwendet die USSI Dataset.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f9e4b-106">Gehen Sie im Navigationsbereich zu **Module > Projektmanagement und -buchhaltung > Einrichtung > Preise > Einstandspreis (Stunden)**.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="f9e4b-107">Wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-107">Select **New**.</span></span>
3. <span data-ttu-id="f9e4b-108">Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="f9e4b-109">Geben Sie in das Feld **Einstandspreis** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="f9e4b-110">Sie können einen Standardeinstandspreis für die Projektkategorie oder einen Einstandspreis nach Arbeiternummer, Projektnummer, Kategorie, Datum oder einer beliebigen Kombination davon festlegen.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="f9e4b-111">Der angewandte Einstandspreis ist der Einstandspreis mit dem höchsten Detaillierungsgrad.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="f9e4b-112">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-112">Select **Save**.</span></span>
6. <span data-ttu-id="f9e4b-113">Gehen Sie im Navigationsbereich zu **Module > Projektmanagement und -buchhaltung > Einrichtung > Preise > Verkaufspreis (Stunden)**.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="f9e4b-114">Wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-114">Select **New**.</span></span>
8. <span data-ttu-id="f9e4b-115">Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="f9e4b-116">Wählen Sie im Feld **Gültig zum** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="f9e4b-117">Geben Sie im Feld **Preisberechnung** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="f9e4b-118">Sie können einen Standardverkaufspreis für Stundentransaktionen oder für eine Projektkategorie festlegen.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="f9e4b-119">Sie können Verkaufspreise auch nach Mitarbeiternummer, Projektnummer, Kategorie, Transaktionsdatum oder einer beliebigen Kombination davon einrichten.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="f9e4b-120">Der tatsächliche Verkaufspreis, der angewendet wird, wenn ein Mitarbeiter eine Transaktion in das Stundenjournal eingibt, ist der Verkaufspreis mit dem höchsten Detaillierungsgrad.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="f9e4b-121">Wenn beispielsweise sowohl ein allgemeiner Verkaufspreis als auch ein arbeiterspezifischer Verkaufspreis festgelegt sind, wird der arbeiterspezifische Verkaufspreis verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="f9e4b-122">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-122">Select **Save**.</span></span>
12. <span data-ttu-id="f9e4b-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-123">Close the page.</span></span>
13. <span data-ttu-id="f9e4b-124">Gehen Sie im Navigationsbereich zu **Module > Projektmanagement und -buchhaltung > Einrichtung > Preise > Einstandspreis (Ausgaben)**.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="f9e4b-125">Wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-125">Select **New**.</span></span>
15. <span data-ttu-id="f9e4b-126">Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="f9e4b-127">Geben Sie in das Feld **Einstandspreis** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="f9e4b-128">Es können mehrere Felder ausgefüllt werden, dies ist jedoch das Minimum, das zum Speichern des Datensatzes erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="f9e4b-129">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-129">Select **Save**.</span></span>
18. <span data-ttu-id="f9e4b-130">Gehen Sie im Navigationsbereich zu **Module > Projektmanagement und -buchhaltung > Einrichtung > Preise > Verkaufspreis (Ausgaben)**.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="f9e4b-131">Wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-131">Select **New**.</span></span>
20. <span data-ttu-id="f9e4b-132">Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="f9e4b-133">Wählen Sie im Feld **Gültig zum** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="f9e4b-134">Geben Sie im Feld **Preisberechnung** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="f9e4b-135">Der tatsächliche Verkaufspreis, der angewendet wird, wenn ein Mitarbeiter Transaktionen in die Ausgabenerfassung eingibt, ist der Verkaufspreis mit dem höchsten Detaillierungsgrad.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="f9e4b-136">Wenn beispielsweise sowohl ein allgemeiner Verkaufspreis als auch ein arbeiterspezifischer Verkaufspreis festgelegt sind, wird der arbeiterspezifische Verkaufspreis verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="f9e4b-137">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="f9e4b-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]