---
title: Produktbasierte Verkaufschancenpositionen
description: Dieses Thema enthält Informationen zu produktbasierten Verkaufschancenpositionen in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076450"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="c96de-103">Produktbasierte Verkaufschancenpositionen</span><span class="sxs-lookup"><span data-stu-id="c96de-103">Product-based opportunity lines</span></span>

<span data-ttu-id="c96de-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="c96de-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c96de-105">Produktbasierte Verkaufschancenpositionen sind Positionen in der Verkaufschance.</span><span class="sxs-lookup"><span data-stu-id="c96de-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="c96de-106">Diese Positionen werden dem Kunden als separate Positionen auf der eventuellen Rechnung ohne weitere Mehrwertdienste bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c96de-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="c96de-107">Die damit verbundenen Ausgaben und der Verbrauch werden nicht für Aufgaben verwandter Projekte erfasst.</span><span class="sxs-lookup"><span data-stu-id="c96de-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="c96de-108">Produktbasierte Positionen können Katalogartikel oder einzutragende Produkte sein.</span><span class="sxs-lookup"><span data-stu-id="c96de-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="c96de-109">Die meisten Funktionen in den produktbasierten Positionen einer Verkaufschance folgen den Funktionen der Dynamics 365 Sales-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c96de-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="c96de-110">Weitere Informationen zu produktbasierten Verkaufschancenpositionen finden Sie unter [Produkte einer Verkaufschance hinzufügen](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="c96de-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="c96de-111">Ein Konzept für produktbasierte Verkaufschancenpositionen, die spezifisch für projektbasierte Verkaufschancen ist, lautet **Kundenbudget**.</span><span class="sxs-lookup"><span data-stu-id="c96de-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="c96de-112">Verwenden Sie dieses Feld, um den Betrag zu verfolgen, den der Kunde bereit ist, für die Position zu zahlen.</span><span class="sxs-lookup"><span data-stu-id="c96de-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="c96de-113">Wenn die Umsatzmethode der Verkaufschancenzusammenfassung auf **Vom System berechnet** festgelegt ist, werden die Kundenbudgetwerte über produkt- und projektbasierte Positionen hinweg zusammengefasst, um den geschätzten Umsatz zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="c96de-113">If the revenue method of the Opportunity summary is set to **System Calculated** , the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
