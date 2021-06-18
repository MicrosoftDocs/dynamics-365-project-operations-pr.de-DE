---
title: Preislisten deaktivieren
description: In diesem Thema wird erläutert, wie nicht verwendete oder alte Preislisten deaktiviert oder entfernt werden.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001335"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="92629-103">Preislisten deaktivieren</span><span class="sxs-lookup"><span data-stu-id="92629-103">Deactivate price lists</span></span> 

<span data-ttu-id="92629-104">_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="92629-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="92629-105">Zum Entfernen von alten oder nicht verwendeten Preislisten aus Dynamics 365 Project Operations gibt es zwei Schritte, die Sie ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="92629-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="92629-106">Entfernen oder löschen Sie die Preisliste von bestimmten Seiten.</span><span class="sxs-lookup"><span data-stu-id="92629-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="92629-107">Deaktivieren oder löschen Sie die Preisliste aus den aktiven Preislisten auf der **Preisliste**-Seite.</span><span class="sxs-lookup"><span data-stu-id="92629-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="92629-108">Sie müssen beide Schritte ausführen, um eine Preisliste vollständig zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="92629-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="92629-109">Es reicht nicht aus, nur Schritt 2 auszuführen, bei dem die Preisliste direkt aus der Ansicht „Aktive Preislisten“ gelöscht oder deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="92629-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="92629-110">Sie müssen auch die Zuordnung dieser Preisliste von allen in Schritt 1 genannten Stellen löschen.</span><span class="sxs-lookup"><span data-stu-id="92629-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="92629-111">Löschen Sie die Preisliste von bestimmten Seiten</span><span class="sxs-lookup"><span data-stu-id="92629-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="92629-112">Gehen Sie zu den folgenden Seiten, um eine Preisliste aus Project Operations zu löschen:</span><span class="sxs-lookup"><span data-stu-id="92629-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="92629-113">**Projektparameter**-Seite > **Preislisten**-Registerkarte</span><span class="sxs-lookup"><span data-stu-id="92629-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="92629-114">**Organisationseinheit**-Seite> **Preisliste**-Raster</span><span class="sxs-lookup"><span data-stu-id="92629-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="92629-115">**Konto**-Seite > **Projektpreislisten**-Raster</span><span class="sxs-lookup"><span data-stu-id="92629-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="92629-116">**Projektangebote**-Seite > **Projektpreislisten**-Raster: Dies gilt für alle aktiven Projektangebote.</span><span class="sxs-lookup"><span data-stu-id="92629-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="92629-117">**Projektverträge**-Seite > **Projektpreislisten**-Raster: Dies gilt für alle aktiven Projektverträge.</span><span class="sxs-lookup"><span data-stu-id="92629-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="92629-118">Für jede Seite müssen Sie die Preisliste auswählen, die Sie löschen möchten, und wählen Sie dann **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="92629-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="92629-119">Löschen oder deaktivieren Sie die Preisliste auf der Preisliste-Seite</span><span class="sxs-lookup"><span data-stu-id="92629-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="92629-120">Um eine Preisliste aus den aktiven Preislisten zu löschen, gehen Sie zu **Vertrieb** > **Kunden** > **Preisliste**.</span><span class="sxs-lookup"><span data-stu-id="92629-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="92629-121">Wählen Sie die Preisliste aus, die Sie löschen möchten, und wählen Sie dann **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="92629-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="92629-122">Wenn bei vorhandenen Transaktionen auf die Preisliste verwiesen wird, können Sie sie nicht löschen.</span><span class="sxs-lookup"><span data-stu-id="92629-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="92629-123">In diesem Fall können Sie die Preisliste deaktivieren, damit sie in keiner Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="92629-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="92629-124">Um die Preisliste zu deaktivieren, wählen Sie die Preisliste erneut aus und wählen Sie dann **Deaktivieren**.</span><span class="sxs-lookup"><span data-stu-id="92629-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
