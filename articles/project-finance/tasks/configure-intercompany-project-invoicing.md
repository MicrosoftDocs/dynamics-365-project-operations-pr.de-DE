---
title: Konfigurieren Sie die Intercompany-Projektabrechnung
description: Dieses Thema zeigt, wie Sie die Projektabrechnung zwischen zwei Unternehmen in Ihrer Organisation einrichten.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: 72d6c257-f2d3-483b-8ff2-445263796963
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b199c85736f6268bc5914fddaa10e4cabd44ef1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3716485"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="35742-103">Konfigurieren Sie die Intercompany-Projektabrechnung</span><span class="sxs-lookup"><span data-stu-id="35742-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35742-104">Dieses Thema zeigt, wie Sie die Projektabrechnung zwischen zwei Unternehmen in Ihrer Organisation einrichten.</span><span class="sxs-lookup"><span data-stu-id="35742-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="35742-105">Diese Aufgabe verwendet die USSI Dataset.</span><span class="sxs-lookup"><span data-stu-id="35742-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="35742-106">Im Navigationsbereich gehen Sie zu **Module > Kreditorenkonten > Kreditoren > Alle Kreditoren**.</span><span class="sxs-lookup"><span data-stu-id="35742-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="35742-107">Suchen Sie in der Liste **Alle Anbieter** den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="35742-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="35742-108">Wählen Sie im Aktionsbereich **Allgemein** aus.</span><span class="sxs-lookup"><span data-stu-id="35742-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="35742-109">Wählen Sie **Intercompany** aus.</span><span class="sxs-lookup"><span data-stu-id="35742-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="35742-110">Legen Sie **Aktiv** auf **Ja** fest, um den Intercompany-Handel zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="35742-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="35742-111">Geben Sie im Feld **Debitorenunternehmen** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="35742-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="35742-112">Geben Sie im Feld **Mein Konto** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="35742-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="35742-113">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="35742-113">Select **Save**.</span></span>
9. <span data-ttu-id="35742-114">Schließen Sie die Seiten, um zur Startseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="35742-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="35742-115">Gehen Sie im Navigationsbereich zu **Module> Projektmanagement und -buchhaltung> Einrichtung > Projektmanagement- und Buchhaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="35742-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="35742-116">Wählen Sie die Registerkarte **Intercompany** aus.</span><span class="sxs-lookup"><span data-stu-id="35742-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="35742-117">Bewegen Sie den Schieberegler auf **Ja**, um Intercompany-Ressourcenplanung und Intercompany-Arbeitszeittabellen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="35742-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="35742-118">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="35742-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="35742-119">Wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="35742-119">Select **New**.</span></span>
15. <span data-ttu-id="35742-120">Geben Sie im Feld **Kreditgebende juristische Person** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="35742-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="35742-121">Aktivieren Sie das Kontrollkästchen **Einnahmen erzielen**.</span><span class="sxs-lookup"><span data-stu-id="35742-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="35742-122">Geben Sie im Feld **Standardarbeitszeittabellen-Kategorie** einen Wert ein, oder wählen Sie einen aus.</span><span class="sxs-lookup"><span data-stu-id="35742-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="35742-123">Geben Sie im Feld **Standardausgabenkategorie** einen Wert ein, oder wählen Sie einen aus.</span><span class="sxs-lookup"><span data-stu-id="35742-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="35742-124">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="35742-124">Select **Save**.</span></span>
20. <span data-ttu-id="35742-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="35742-125">Close the page.</span></span>
21. <span data-ttu-id="35742-126">Gehen Sie im Navigationsbereich zu **Module > Projektmanagement und -buchhaltung > Einrichtung > Buchung > Sachkontobuchungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="35742-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="35742-127">Wählen Sie im Feld **Sachkontentypen** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="35742-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="35742-128">Wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="35742-128">Select **New**.</span></span>
24. <span data-ttu-id="35742-129">Geben Sie im Feld **Hauptkonto** der neuen Zeile die gewünschten Werte ein.</span><span class="sxs-lookup"><span data-stu-id="35742-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="35742-130">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="35742-130">Select **Save**.</span></span>
26. <span data-ttu-id="35742-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="35742-131">Close the page.</span></span>
27. <span data-ttu-id="35742-132">Gehen Sie im Navigationsbereich zu **Module > Projektmanagement und -buchhaltung > Einrichtung > Preise > Übertragungspreis**.</span><span class="sxs-lookup"><span data-stu-id="35742-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="35742-133">Wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="35742-133">Select **New**.</span></span>
29. <span data-ttu-id="35742-134">Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="35742-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="35742-135">Geben Sie im Feld **Kreditgebende juristische Person** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="35742-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="35742-136">Wählen Sie im Feld **Transferpreismodell** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="35742-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="35742-137">Geben Sie im Feld **Preisberechnung** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="35742-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="35742-138">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="35742-138">Select **Save**.</span></span>

