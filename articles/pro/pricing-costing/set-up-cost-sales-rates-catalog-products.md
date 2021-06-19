---
title: Kosten und Verkaufsraten für Katalogprodukte einrichten – Lite
description: Dieses Thema enthält Informationen zum Einrichten von Kostensätzen und Verkaufsraten für Artikel in einem Produktkatalog.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004320"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="9ad32-103">Kosten und Verkaufsraten für Katalogprodukte einrichten – Lite</span><span class="sxs-lookup"><span data-stu-id="9ad32-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="9ad32-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="9ad32-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9ad32-105">Einrichten der Preise für Produktkatalogartikel in Dynamics 365 Project Operations ist dasselbe wie in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="9ad32-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="9ad32-106">In Project Operations können Produkte nicht geschätzt oder für Projekte verwendet werden, sodass die Produktkatalogpreise nicht in den Projektpreislisten für Angebote und Verträge festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9ad32-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="9ad32-107">Verwenden Sie das **Produktpreis** Feld eines Angebots, Vertrags oder Kontos zum Einrichten der Produktkatalogpreise.</span><span class="sxs-lookup"><span data-stu-id="9ad32-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="9ad32-108">Richten Sie keine Produktkatalogpreise in den Projektpreislisten ein.</span><span class="sxs-lookup"><span data-stu-id="9ad32-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="9ad32-109">Projektpreislisten sind für Project Operations exklusiv.</span><span class="sxs-lookup"><span data-stu-id="9ad32-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="9ad32-110">Die anwendungsspezifische Geschäftslogik kopiert die Preislisten aus einem Angebot in einen Vertrag.</span><span class="sxs-lookup"><span data-stu-id="9ad32-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="9ad32-111">Das Ergebnis ist eine vertragsspezifische Projektpreisliste.</span><span class="sxs-lookup"><span data-stu-id="9ad32-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="9ad32-112">Der Kopiervorgang kann den Angebotsgewinn verzögern, wenn die Projektpreisliste im Angebot zu groß wird.</span><span class="sxs-lookup"><span data-stu-id="9ad32-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="9ad32-113">Produktpreislisten werden nicht kopiert, um benutzerdefinierte Preislisten für Verträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9ad32-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="9ad32-114">Da kein Kopieren erforderlich ist, wird die Leistung des Angebotsprozesses nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="9ad32-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]