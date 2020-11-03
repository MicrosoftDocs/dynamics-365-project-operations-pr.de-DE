---
title: Projektvorgangfelder als Preisdimensionen
description: Dieses Thema enthält Informationen zur Verwendung von Feldern als Preisdimensionen in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 56ff45169058d96d7ef81a710de309eec698a75f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076587"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="18bb7-103">Projektvorgangfelder als Preisdimensionen</span><span class="sxs-lookup"><span data-stu-id="18bb7-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="18bb7-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="18bb7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="18bb7-105">Die **Istwerte** Entität verfügt über viele Felder, die als Preisdimensionen für die ressourcenbasierte Preisgestaltung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="18bb7-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="18bb7-106">Beispielsweise ist ein allgemeines Feld **Buchbare Ressource**.</span><span class="sxs-lookup"><span data-stu-id="18bb7-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="18bb7-107">Kleinere Unternehmen mit weniger als 20-30 fakturierbaren Ressourcen finden vielleicht, dass spezifische Fakturierungs- und Kostensätze für jede Ressource eine einfachere Herangehensweise sind.</span><span class="sxs-lookup"><span data-stu-id="18bb7-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="18bb7-108">Wenn jedoch die abrechnungsfähigen Mitargeiter wachsen, kann es unrealistisch werden, ressourcenschonende Raten beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="18bb7-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="18bb7-109">Die Ressourcenkosten und Rechnungsraten variieren, wenn Ressourcen gefördert werden, mehr Erfahrung gesammelt werden oder andere Fähigkeiten erworben werden.</span><span class="sxs-lookup"><span data-stu-id="18bb7-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="18bb7-110">Ein weiteres Beispiel ist die Transaktionskategorie.</span><span class="sxs-lookup"><span data-stu-id="18bb7-110">Another example is that of transaction category.</span></span> <span data-ttu-id="18bb7-111">Kunden und Implementierer haben die Transaktionskategorie in PSA verwendet, um Arbeit zu klassifizieren und verwenden das Feld für Preis und Kosten, basierend auf der Arbeitskategorie.</span><span class="sxs-lookup"><span data-stu-id="18bb7-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
