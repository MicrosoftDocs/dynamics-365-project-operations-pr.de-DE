---
title: Erhalten Sie Artikel auf Bestellung aus Artikelanforderung
description: In diesem Thema wird erläutert, wie Sie Artikel auf einer Bestellung aus einer Artikelanforderung erhalten.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011685"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="8cb91-103">Erhalten Sie Artikel auf Bestellung aus Artikelanforderung</span><span class="sxs-lookup"><span data-stu-id="8cb91-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8cb91-104">In diesem Thema wird erläutert, wie Sie Artikel auf einer Bestellung aus einer Artikelanforderung erhalten.</span><span class="sxs-lookup"><span data-stu-id="8cb91-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="8cb91-105">Durch die Verwendung einer Artikelanforderung anstelle einer Artikeltransaktion können Sie die Lieferung unmittelbar vor der tatsächlichen Verwendung des Artikels planen, eine Bestellung erstellen, den Artikel in das Rahmenwerk für Handelsvereinbarungen aufnehmen und den Artikelbedarf in die Produktionsplanung einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="8cb91-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="8cb91-106">Diese Aufgabe verwendet die USSI Dataset.</span><span class="sxs-lookup"><span data-stu-id="8cb91-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="8cb91-107">Gehen Sie im Navigationsbereich zu **Module> Projektmanagement und Buchhaltung> Projekte> Alle Projekte**.</span><span class="sxs-lookup"><span data-stu-id="8cb91-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="8cb91-108">Wählen Sie in der Liste den Link in der gewünschten Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="8cb91-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="8cb91-109">Wählen Sie im Aktivitätsbereich **Plan** aus.</span><span class="sxs-lookup"><span data-stu-id="8cb91-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="8cb91-110">Wählen Sie **Artikelanforderung** aus.</span><span class="sxs-lookup"><span data-stu-id="8cb91-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="8cb91-111">Wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="8cb91-111">Select **New**.</span></span>
6. <span data-ttu-id="8cb91-112">Geben Sie in der neuen Zeile einen Wert einen oder wählen Sie einen aus im Feld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="8cb91-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="8cb91-113">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="8cb91-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="8cb91-114">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="8cb91-114">Select **Save**.</span></span>
9. <span data-ttu-id="8cb91-115">Wählen Sie im Aktivitätsbereich **Verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="8cb91-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="8cb91-116">Wählen Sie **Funktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="8cb91-116">Select **Functions**.</span></span>
11. <span data-ttu-id="8cb91-117">Wählen Sie **Bestellung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="8cb91-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="8cb91-118">Aktivieren Sie das Kontrollkästchen **Alle einschließen**.</span><span class="sxs-lookup"><span data-stu-id="8cb91-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="8cb91-119">Geben Sie im Feld **Kreditorenkonto** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8cb91-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="8cb91-120">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8cb91-120">Select **OK**.</span></span>
15. <span data-ttu-id="8cb91-121">Im Navigationsbereich gehen Sie zu **Module > Kreditoren > Einkaufsbestellungen > Alle Einkaufsbestellungen**.</span><span class="sxs-lookup"><span data-stu-id="8cb91-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="8cb91-122">Wählen Sie in der Liste den Link in der gewünschten Zeile aus.</span><span class="sxs-lookup"><span data-stu-id="8cb91-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="8cb91-123">Wählen Sie im Aktionsbereich **Einkauf** aus.</span><span class="sxs-lookup"><span data-stu-id="8cb91-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="8cb91-124">Wählen Sie **Bestätigen** aus.</span><span class="sxs-lookup"><span data-stu-id="8cb91-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="8cb91-125">Wählen Sie im Aktionsbereich **Empfangen** aus.</span><span class="sxs-lookup"><span data-stu-id="8cb91-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="8cb91-126">Wählen Sie **Produktzugang** aus.</span><span class="sxs-lookup"><span data-stu-id="8cb91-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="8cb91-127">Geben Sie in das Feld **Produktzugang** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8cb91-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="8cb91-128">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8cb91-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]