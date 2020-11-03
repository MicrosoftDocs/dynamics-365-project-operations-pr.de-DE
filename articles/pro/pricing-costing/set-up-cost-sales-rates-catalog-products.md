---
title: Kostensätze und Verkaufsraten für Katalogprodukte einrichten
description: Dieses Thema enthält Informationen zum Einrichten von Kostensätzen und Verkaufsraten für Artikel in einem Produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076591"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="510cd-103">Kostensätze und Verkaufsraten für Katalogprodukte einrichten</span><span class="sxs-lookup"><span data-stu-id="510cd-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="510cd-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="510cd-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="510cd-105">Das Einrichten der Preise für Produktkatalogelemente in Dynamics 365 Project Operations erfolgt genau wie in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="510cd-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="510cd-106">Da Produkte in Project Operations nicht vorkalkuliert oder für Projekte verwendet werden können, müssen für Projektangebote und Verträge keine Produktkatalogpreise in Projektpreislisten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="510cd-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="510cd-107">Produktkatalogpreise sollten im Feld **Produktpreis** eines Angebots, Vertrags oder Kontos eingerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="510cd-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="510cd-108">Richten Sie für diese Entitäten keine Produktkatalogpreise in den Projektpreislisten ein.</span><span class="sxs-lookup"><span data-stu-id="510cd-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="510cd-109">Projektpreislisten sind für Project Operations exklusiv.</span><span class="sxs-lookup"><span data-stu-id="510cd-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="510cd-110">Es gibt eine anwendungsspezifische Geschäftslogik, die die Preislisten von einem Angebot in einen Vertrag kopiert.</span><span class="sxs-lookup"><span data-stu-id="510cd-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="510cd-111">Das Ergebnis ist eine vertragsspezifische Projektpreisliste.</span><span class="sxs-lookup"><span data-stu-id="510cd-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="510cd-112">Der Kopiervorgang kann den Angebotsgewinn verzögern, wenn die Projektpreisliste im Angebot zu groß wird.</span><span class="sxs-lookup"><span data-stu-id="510cd-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="510cd-113">Produktpreislisten werden nicht kopiert, um benutzerdefinierte Preislisten für Verträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="510cd-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="510cd-114">Dies bedeutet, dass Produktpreislisten keinen Einfluss auf die Leistung des Angebotsgewinnprozesses haben.</span><span class="sxs-lookup"><span data-stu-id="510cd-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
