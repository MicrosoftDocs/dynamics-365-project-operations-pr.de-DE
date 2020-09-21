---
title: Fähigkeiten und Kompetenzstufenmodelle
description: Dieses Thema enthält Informationen zur Verwendung der Fähigkeiten und Kompetenzstufenmodelle.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: d55a6d72-905f-4b82-a9fe-0b6b082473a6
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe4c9a62cd2ec1365daa09714fa6fa19210a7770
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722049"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="85dd7-103">Fähigkeiten und Kompetenzstufenmodelle</span><span class="sxs-lookup"><span data-stu-id="85dd7-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="85dd7-104">Fähigkeiten sind Ressourceneigenschaften, die von Dynamics 365 Project Service Automation und, sofern installiert, Dynamics 365 Field Service gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="85dd7-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="85dd7-105">Um das Repository in Project Service Automation beizubehalten, navigieren Sie zu **Ressourcen** \> **Ressourcenqualifikationen**.</span><span class="sxs-lookup"><span data-stu-id="85dd7-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Ressourcenqualifikationen](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="85dd7-107">Kompetenzstufenmodelle zur Bewertung von Ressourcen verwenden</span><span class="sxs-lookup"><span data-stu-id="85dd7-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="85dd7-108">Fähigkeiten für Ressourcen werden durch Kompetenzstufenmodelle bewertet.</span><span class="sxs-lookup"><span data-stu-id="85dd7-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="85dd7-109">Die einzelnen Bewertungen befinden sich in einem Kompetenzstufenmodell.</span><span class="sxs-lookup"><span data-stu-id="85dd7-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="85dd7-110">Um ein Kompetenzstufenmodell zu erstellen, navigieren Sie zu **Ressourcen** \> **Kompetenzstufenmodelle** und wählen Sie dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="85dd7-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="85dd7-111">Geben Sie im neuen Bewertungsmodell den Mindestbewertungswert, dem Höchstbewertungswert und die bewertet Entität ein.</span><span class="sxs-lookup"><span data-stu-id="85dd7-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="85dd7-112">Im Unterraster **Bewertungswerte** können Sie die verschiedenen Bewertungswerte definieren, vom Mindest- bis zum Höchstwert.</span><span class="sxs-lookup"><span data-stu-id="85dd7-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Definierte Mindest- und Höchstbewertungswerte](media/Resource-Management-image85.png)

<span data-ttu-id="85dd7-114">Diese Bewertungswerte werden in den Filtern **Ressourcenanforderungen**, **Zeitplanübersicht** und **Zeitplan-Assistent** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="85dd7-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
