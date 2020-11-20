---
title: Kosten und Verkaufsraten für Katalogprodukte einrichten – Lite
description: Dieses Thema enthält Informationen zum Einrichten von Kostensätzen und Verkaufsraten für Artikel in einem Produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176700"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="49d22-103">Kosten und Verkaufsraten für Katalogprodukte einrichten – Lite</span><span class="sxs-lookup"><span data-stu-id="49d22-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="49d22-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="49d22-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="49d22-105">Das Einrichten der Preise für Produktkatalogelemente in Dynamics 365 Project Operations erfolgt genau wie in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="49d22-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="49d22-106">Da Produkte in Project Operations nicht vorkalkuliert oder für Projekte verwendet werden können, müssen für Projektangebote und Verträge keine Produktkatalogpreise in Projektpreislisten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="49d22-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="49d22-107">Produktkatalogpreise sollten im Feld **Produktpreis** eines Angebots, Vertrags oder Kontos eingerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="49d22-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="49d22-108">Richten Sie für diese Entitäten keine Produktkatalogpreise in den Projektpreislisten ein.</span><span class="sxs-lookup"><span data-stu-id="49d22-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="49d22-109">Projektpreislisten sind für Project Operations exklusiv.</span><span class="sxs-lookup"><span data-stu-id="49d22-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="49d22-110">Es gibt eine anwendungsspezifische Geschäftslogik, die die Preislisten von einem Angebot in einen Vertrag kopiert.</span><span class="sxs-lookup"><span data-stu-id="49d22-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="49d22-111">Das Ergebnis ist eine vertragsspezifische Projektpreisliste.</span><span class="sxs-lookup"><span data-stu-id="49d22-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="49d22-112">Der Kopiervorgang kann den Angebotsgewinn verzögern, wenn die Projektpreisliste im Angebot zu groß wird.</span><span class="sxs-lookup"><span data-stu-id="49d22-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="49d22-113">Produktpreislisten werden nicht kopiert, um benutzerdefinierte Preislisten für Verträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="49d22-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="49d22-114">Dies bedeutet, dass Produktpreislisten keinen Einfluss auf die Leistung des Angebotsgewinnprozesses haben.</span><span class="sxs-lookup"><span data-stu-id="49d22-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
