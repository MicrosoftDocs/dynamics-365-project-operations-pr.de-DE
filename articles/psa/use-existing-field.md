---
title: Verwenden Sie ein vorhandenes Feld in Project Service als Preisdimension
description: Dieses Thema enthält Informationen zur Verwendung vorhandener Project Service-Felder als Preisdimensionen.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 09e565c91eda9dee6e0ec479a5c85d94d2591147
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008085"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="3b02c-103">Verwenden Sie ein vorhandenes Feld in Project Service als Preisdimension</span><span class="sxs-lookup"><span data-stu-id="3b02c-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3b02c-104">Project Service Automation (PSA) hat viele Felder in der Entität **Ist-Werte**, die als Preisdimensionen für ressourcenbasierte Preise in Projektorganisationen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3b02c-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="3b02c-105">Beispielsweise ist ein allgemeines Feld **Buchbare Ressource**.</span><span class="sxs-lookup"><span data-stu-id="3b02c-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="3b02c-106">Kleinere Unternehmen mit weniger als 20-30 fakturierbaren Ressourcen finden vielleicht, dass spezifische Fakturierungs- und Kostensätze für jede Ressource eine einfachere Herangehensweise sind.</span><span class="sxs-lookup"><span data-stu-id="3b02c-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="3b02c-107">Mit Zunahme der fakturierbaren Mitarbeiter könnte es jedoch unrealistisch werden, dies zu verwalten, da Ressourcenkosten und spezifische Fakturierungssätze anfangen zu variieren, da Ressourcen befördert werden, mehr Erfahrung gewinnen oder andere Qualifikationssätze erwerben.</span><span class="sxs-lookup"><span data-stu-id="3b02c-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="3b02c-108">Da diese Herangehensweise immer noch für Unternehmen einer bestimmten Größe funktioniert, finden Sie im Thema [eine buchbare Ressource als Preisdimension verwenden](bookable-resource-pricing-dimension.md) Informationen, um zu verstehen, wie ein vorhandenes Project Service-Feld als Preisdimension verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3b02c-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="3b02c-109">Ein weiteres Beispiel ist die Transaktionskategorie.</span><span class="sxs-lookup"><span data-stu-id="3b02c-109">Another example is that of transaction category.</span></span> <span data-ttu-id="3b02c-110">Kunden und Implementierer haben die Transaktionskategorie in PSA verwendet, um Arbeit zu klassifizieren und verwenden das Feld für Preis und Kosten, basierend auf der Arbeitskategorie.</span><span class="sxs-lookup"><span data-stu-id="3b02c-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="3b02c-111">Weitere Informationen finden Sie unter [Transaktionskategorie als Preisdimension verwenden](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="3b02c-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]