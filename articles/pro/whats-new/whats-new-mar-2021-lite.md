---
title: Neuerungen im März 2021 – Bereitstellung von Project Operations Lite
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der März 2021-Veröffentlichung von Project Operations-Lite-Bereitstellung verfügbar sind.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd1518ef8f5645bace63a222b92cfd16d9c19a21
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500000"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="c6ac8-103">Neuerungen im März 2021 – Bereitstellung von Project Operations Lite</span><span class="sxs-lookup"><span data-stu-id="c6ac8-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="c6ac8-104">_Gilt für: Lite Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="c6ac8-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c6ac8-105">Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:</span><span class="sxs-lookup"><span data-stu-id="c6ac8-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="c6ac8-106">Project Operations in Dataverse, Umgebungsversion 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="c6ac8-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="c6ac8-107">Qualitätsupdates</span><span class="sxs-lookup"><span data-stu-id="c6ac8-107">Quality updates</span></span>

| <span data-ttu-id="c6ac8-108">**Funktionsbereich**</span><span class="sxs-lookup"><span data-stu-id="c6ac8-108">**Feature area**</span></span> | <span data-ttu-id="c6ac8-109">**Referenznummer**</span><span class="sxs-lookup"><span data-stu-id="c6ac8-109">**Reference number**</span></span> | <span data-ttu-id="c6ac8-110">**Qualitätsupdate**</span><span class="sxs-lookup"><span data-stu-id="c6ac8-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c6ac8-111">Preise und Abrechnung</span><span class="sxs-lookup"><span data-stu-id="c6ac8-111">Billing and pricing</span></span> | <span data-ttu-id="c6ac8-112">2133873</span><span class="sxs-lookup"><span data-stu-id="c6ac8-112">2133873</span></span> | <span data-ttu-id="c6ac8-113">Das Problem bei der Anzeige des Währungssymbols für **Verkaufspreis pro Einheit** im Raster **Kostenschätzungen** wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="c6ac8-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="c6ac8-114">Preise und Abrechnung</span><span class="sxs-lookup"><span data-stu-id="c6ac8-114">Billing and pricing</span></span> | <span data-ttu-id="c6ac8-115">2174616</span><span class="sxs-lookup"><span data-stu-id="c6ac8-115">2174616</span></span> | <span data-ttu-id="c6ac8-116">Erhält ein Angebot den Zuschlag, wird auf die benutzerdefinierte Preisliste des Vertrags in den Detaisl der Vertragszeilen verwiesen, die aus dem Angebot übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="c6ac8-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="c6ac8-117">Verkaufschancenmanagement</span><span class="sxs-lookup"><span data-stu-id="c6ac8-117">Opportunity Management</span></span> | <span data-ttu-id="c6ac8-118">2167475</span><span class="sxs-lookup"><span data-stu-id="c6ac8-118">2167475</span></span> | <span data-ttu-id="c6ac8-119">Fester Steuerbetrag in der Korrekturrechnung, aus dem ein nicht abgerechneter tatsächlicher Eintrag hervorgegangen ist.</span><span class="sxs-lookup"><span data-stu-id="c6ac8-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="c6ac8-120">Verkaufschancenmanagement</span><span class="sxs-lookup"><span data-stu-id="c6ac8-120">Opportunity Management</span></span> | <span data-ttu-id="c6ac8-121">2176285</span><span class="sxs-lookup"><span data-stu-id="c6ac8-121">2176285</span></span> | <span data-ttu-id="c6ac8-122">Der Steuerbetrag darf nicht aus den Details des Kaufvertrags/der Angebotszeile in die Details des Kostenvertrags/der Angebotszeile übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="c6ac8-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="c6ac8-123">Verkaufschancenmanagement</span><span class="sxs-lookup"><span data-stu-id="c6ac8-123">Opportunity Management</span></span> | <span data-ttu-id="c6ac8-124">2188079</span><span class="sxs-lookup"><span data-stu-id="c6ac8-124">2188079</span></span> | <span data-ttu-id="c6ac8-125">Für Verträge, die nicht arbeitsbezogen sind, darf keine geteilte Abrechnungsregel erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c6ac8-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="c6ac8-126">Planung und Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="c6ac8-126">Planning and Tracking</span></span> | <span data-ttu-id="c6ac8-127">2138853</span><span class="sxs-lookup"><span data-stu-id="c6ac8-127">2138853</span></span> | <span data-ttu-id="c6ac8-128">Die Projektkopierfunktion wurde aktualisiert, um sicherzustellen, dass Kostenschätzungspositionen, die auf Aufgaben verweisen, in das Zielprojekt übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="c6ac8-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="c6ac8-129">Planung und Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="c6ac8-129">Planning and Tracking</span></span> | <span data-ttu-id="c6ac8-130">2173259</span><span class="sxs-lookup"><span data-stu-id="c6ac8-130">2173259</span></span> | <span data-ttu-id="c6ac8-131">Die Projektkopierfunktion wurde aktualisiert, um sicherzustellen, dass in bestimmten Szenarien nicht die Fehlermeldung **PSP wird kopiert** erscheint.</span><span class="sxs-lookup"><span data-stu-id="c6ac8-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="c6ac8-132">Zeit und Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6ac8-132">Time and Expense</span></span> | <span data-ttu-id="c6ac8-133">2148910</span><span class="sxs-lookup"><span data-stu-id="c6ac8-133">2148910</span></span> | <span data-ttu-id="c6ac8-134">Anzeigeproblem der Seite **Eintrag bearbeiten** im Raster **Zeiteintrag** wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="c6ac8-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="c6ac8-135">Zeit und Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6ac8-135">Time and Expense</span></span> | <span data-ttu-id="c6ac8-136">2159798</span><span class="sxs-lookup"><span data-stu-id="c6ac8-136">2159798</span></span> | <span data-ttu-id="c6ac8-137">Engere Steuerung, um sicherzustellen, dass genehmigte Ausgabeneinträge nicht bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="c6ac8-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


