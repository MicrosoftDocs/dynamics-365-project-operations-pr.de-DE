---
title: Bestellungen für ein Projekt
description: Dieser Artikel beschreibt die verschiedenen Methoden, mit denen Sie Bestellungen für ein Projekt erstellen können. Die Methode, die Sie verwenden, hängt vom Zweck der Bestellung ab und wann die bestellen Artikel verbraucht werden und wann Artikel für ein Projekt belastet werden.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076512"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="614ff-104">Bestellungen für ein Projekt</span><span class="sxs-lookup"><span data-stu-id="614ff-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="614ff-105">Dieser Artikel beschreibt die verschiedenen Methoden, mit denen Sie Bestellungen für ein Projekt erstellen können.</span><span class="sxs-lookup"><span data-stu-id="614ff-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="614ff-106">Die Methode, die Sie verwenden, hängt vom Zweck der Bestellung ab und wann die bestellen Artikel verbraucht werden und wann Artikel für ein Projekt belastet werden.</span><span class="sxs-lookup"><span data-stu-id="614ff-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="614ff-107">Methoden zum Anlegen einer Bestellung</span><span class="sxs-lookup"><span data-stu-id="614ff-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="614ff-108">Mit einer der folgenden Methoden können Sie eine Bestellung in Projektmanagement und Buchhaltung anlegen.</span><span class="sxs-lookup"><span data-stu-id="614ff-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="614ff-109">Der Zweck der Bestellung bestimmt, wann die Bestellung verbraucht wird und wann die Artikel für ein Projekt belastet werden.</span><span class="sxs-lookup"><span data-stu-id="614ff-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="614ff-110">Methode</span><span class="sxs-lookup"><span data-stu-id="614ff-110">Method</span></span></th>
<th><span data-ttu-id="614ff-111">Zweck</span><span class="sxs-lookup"><span data-stu-id="614ff-111">Purpose</span></span></th>
<th><span data-ttu-id="614ff-112">Verbrauch von Gegenständen</span><span class="sxs-lookup"><span data-stu-id="614ff-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="614ff-113">Eine Bestellung auf Grundlage eines Projekts direkt anlegen.</span><span class="sxs-lookup"><span data-stu-id="614ff-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="614ff-114">Verwenden Sie diese Methode, um Artikel von einem externen Lieferanten zum Verbrauch in einem Projekt zu kaufen.</span><span class="sxs-lookup"><span data-stu-id="614ff-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="614ff-115">Sie können die Bestellung in zwei Arten erstellen:</span><span class="sxs-lookup"><span data-stu-id="614ff-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="614ff-116">Vom Projekt selber.</span><span class="sxs-lookup"><span data-stu-id="614ff-116">From the project itself.</span></span> <span data-ttu-id="614ff-117">In diesem Fall ist das Projekt bereits für die Bestellung definiert.</span><span class="sxs-lookup"><span data-stu-id="614ff-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="614ff-118">Durch Navigieren zur Projektbestellung.</span><span class="sxs-lookup"><span data-stu-id="614ff-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="614ff-119">Sie müssen sowohl den Lieferanten als auch das Projekt auswählen, für das Sie die Bestellung erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="614ff-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="614ff-120">Artikel werden verbraucht, wenn die Lieferantenrechnung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="614ff-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="614ff-121">Eine Bestellung auf Grundlage eines Auftrags anlegen</span><span class="sxs-lookup"><span data-stu-id="614ff-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="614ff-122">Verwenden Sie diese Methode, um Artikel zu kaufen, wenn Sie einen Kundenauftrag aus einem Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="614ff-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="614ff-123">Artikel werden verbraucht, wenn der Kundenauftrag dem Kunden in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="614ff-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="614ff-124">Erstellen Sie eine Bestellung aus einer Artikelanforderung.</span><span class="sxs-lookup"><span data-stu-id="614ff-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="614ff-125">Verwenden Sie diese Methode, um Artikel zu kaufen, wenn Sie eine Artikelanforderung aus einem Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="614ff-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="614ff-126">Artikel werden verbraucht, wenn der Lieferschein der Artikelanforderung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="614ff-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="614ff-127">Wenn Sie die Lieferantenrechnung oder den Packzettel aktualisieren, werden Sie aufgefordert, den Packzettel für die Artikelanforderung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="614ff-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="614ff-128">Weitere Informationen finden Sie unter [Erhalten Sie Artikel auf Bestellung aus Artikelanforderung](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="614ff-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

