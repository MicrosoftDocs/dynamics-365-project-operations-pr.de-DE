---
title: Projektvorgangfelder als Preisdimensionen
description: Dieses Thema enthält Informationen zum Verwenden von Feldern als Preisdimensionen in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 04b823e8237590a294ed0706e64d0ecb9d2cf56f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274637"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="92ca5-103">Project Operations-Felder als Preisdimensionen</span><span class="sxs-lookup"><span data-stu-id="92ca5-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="92ca5-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="92ca5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="92ca5-105">Die **Istwerte** Entität verfügt über viele Felder, die als Preisdimensionen für die ressourcenbasierte Preisgestaltung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="92ca5-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="92ca5-106">Beispielsweise ist ein allgemeines Feld **Buchbare Ressource**.</span><span class="sxs-lookup"><span data-stu-id="92ca5-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="92ca5-107">Kleinere Unternehmen mit weniger als 20-30 fakturierbaren Ressourcen finden vielleicht, dass spezifische Fakturierungs- und Kostensätze für jede Ressource eine einfachere Herangehensweise sind.</span><span class="sxs-lookup"><span data-stu-id="92ca5-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="92ca5-108">Wenn jedoch die abrechnungsfähigen Mitargeiter wachsen, kann es unrealistisch werden, ressourcenschonende Raten beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="92ca5-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="92ca5-109">Die Ressourcenkosten und Rechnungsraten variieren, wenn Ressourcen gefördert werden, mehr Erfahrung gesammelt werden oder andere Fähigkeiten erworben werden.</span><span class="sxs-lookup"><span data-stu-id="92ca5-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="92ca5-110">Ein weiteres Beispiel ist die Transaktionskategorie.</span><span class="sxs-lookup"><span data-stu-id="92ca5-110">Another example is that of transaction category.</span></span> <span data-ttu-id="92ca5-111">Kunden und Implementierer haben die Transaktionskategorie in PSA verwendet, um Arbeit zu klassifizieren und verwenden das Feld für Preis und Kosten, basierend auf der Arbeitskategorie.</span><span class="sxs-lookup"><span data-stu-id="92ca5-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]