---
title: Fähigkeiten und Kompetenzstufen definieren
description: Dieses Thema enthält Informationen zur Einrichtung der Fähigkeiten und Kompetenzstufenmodelle, um Ressourcen zu bewerten.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 24538ed1d610a0cae4c2badc0fd33c2f738a8338
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076468"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="cd8ad-103">Fähigkeiten und Kompetenzstufen definieren</span><span class="sxs-lookup"><span data-stu-id="cd8ad-103">Define skills and proficiencies</span></span>

<span data-ttu-id="cd8ad-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="cd8ad-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cd8ad-105">Fähigkeiten sind Ressourceneigenschaften, die zwischen Dynamics 365 Project Operations und, sofern installiert, Dynamics 365 Field Service gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="cd8ad-106">Um das Repository in Project Operations beizubehalten, navigieren Sie zu **Ressourcen** \> **Ressourcenqualifikationen**.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="cd8ad-107">Kompetenzstufenmodelle zur Bewertung von Ressourcen verwenden</span><span class="sxs-lookup"><span data-stu-id="cd8ad-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="cd8ad-108">Fähigkeiten für Ressourcen werden durch Kompetenzstufenmodelle bewertet.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="cd8ad-109">Die einzelnen Bewertungen befinden sich in einem Kompetenzstufenmodell.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="cd8ad-110">Um ein Kompetenzstufenmodell zu erstellen, navigieren Sie zu **Ressourcen** \> **Kompetenzstufenmodelle** und wählen Sie dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="cd8ad-111">Geben Sie im neuen Bewertungsmodell den Mindestbewertungswert, dem Höchstbewertungswert und die bewertet Entität ein.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="cd8ad-112">Im Unterraster **Bewertungswerte** können Sie die verschiedenen Bewertungswerte definieren, vom Mindest- bis zum Höchstwert.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="cd8ad-113">Diese Bewertungswerte werden in den Filtern **Ressourcenanforderungen** , **Zeitplanübersicht** und **Zeitplan-Assistent** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd8ad-113">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
