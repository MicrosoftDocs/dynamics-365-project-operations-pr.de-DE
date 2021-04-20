---
title: Preislisten deaktivieren
description: In diesem Thema wird erläutert, wie nicht verwendete oder alte Preislisten deaktiviert oder entfernt werden.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701932"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="47926-103">Preislisten deaktivieren</span><span class="sxs-lookup"><span data-stu-id="47926-103">Deactivate price lists</span></span> 

<span data-ttu-id="47926-104">_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="47926-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="47926-105">Zum Entfernen von alten oder nicht verwendeten Preislisten aus Dynamics 365 Project Operations gibt es zwei Schritte, die Sie ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="47926-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="47926-106">Entfernen oder löschen Sie die Preisliste von bestimmten Seiten.</span><span class="sxs-lookup"><span data-stu-id="47926-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="47926-107">Deaktivieren oder löschen Sie die Preisliste aus den aktiven Preislisten auf der **Preisliste**-Seite.</span><span class="sxs-lookup"><span data-stu-id="47926-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="47926-108">Sie müssen beide Schritte ausführen, um eine Preisliste vollständig zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="47926-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="47926-109">Es reicht nicht aus, nur Schritt 2 auszuführen, bei dem die Preisliste direkt aus der Ansicht „Aktive Preislisten“ gelöscht oder deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="47926-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="47926-110">Sie müssen auch die Zuordnung dieser Preisliste von allen in Schritt 1 genannten Stellen löschen.</span><span class="sxs-lookup"><span data-stu-id="47926-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="47926-111">Löschen Sie die Preisliste von bestimmten Seiten</span><span class="sxs-lookup"><span data-stu-id="47926-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="47926-112">Gehen Sie zu den folgenden Seiten, um eine Preisliste aus Project Operations zu löschen:</span><span class="sxs-lookup"><span data-stu-id="47926-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="47926-113">**Projektparameter**-Seite > **Preislisten**-Registerkarte</span><span class="sxs-lookup"><span data-stu-id="47926-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="47926-114">**Organisationseinheit**-Seite> **Preisliste**-Raster</span><span class="sxs-lookup"><span data-stu-id="47926-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="47926-115">**Konto**-Seite > **Projektpreislisten**-Raster</span><span class="sxs-lookup"><span data-stu-id="47926-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="47926-116">**Projektangebote**-Seite > **Projektpreislisten**-Raster: Dies gilt für alle aktiven Projektangebote.</span><span class="sxs-lookup"><span data-stu-id="47926-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="47926-117">**Projektverträge**-Seite > **Projektpreislisten**-Raster: Dies gilt für alle aktiven Projektverträge.</span><span class="sxs-lookup"><span data-stu-id="47926-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="47926-118">Für jede Seite müssen Sie die Preisliste auswählen, die Sie löschen möchten, und wählen Sie dann **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="47926-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="47926-119">Löschen oder deaktivieren Sie die Preisliste auf der Preisliste-Seite</span><span class="sxs-lookup"><span data-stu-id="47926-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="47926-120">Um eine Preisliste aus den aktiven Preislisten zu löschen, gehen Sie zu **Vertrieb** > **Kunden** > **Preisliste**.</span><span class="sxs-lookup"><span data-stu-id="47926-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="47926-121">Wählen Sie die Preisliste aus, die Sie löschen möchten, und wählen Sie dann **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="47926-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="47926-122">Wenn bei vorhandenen Transaktionen auf die Preisliste verwiesen wird, können Sie sie nicht löschen.</span><span class="sxs-lookup"><span data-stu-id="47926-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="47926-123">In diesem Fall können Sie die Preisliste deaktivieren, damit sie in keiner Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="47926-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="47926-124">Um die Preisliste zu deaktivieren, wählen Sie die Preisliste erneut aus und wählen Sie dann **Deaktivieren**.</span><span class="sxs-lookup"><span data-stu-id="47926-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
