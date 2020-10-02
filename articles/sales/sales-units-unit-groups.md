---
title: Einheiten und Einheitengruppen
description: Dieses Thema enthält Informationen zum Erstellen von Einheiten und Einheitengruppen in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898755"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="dadb5-103">Einheiten und Einheitengruppen</span><span class="sxs-lookup"><span data-stu-id="dadb5-103">Units and unit groups</span></span>

<span data-ttu-id="dadb5-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="dadb5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dadb5-105">Einheiten sind die Mengen oder Maße, in denen Produkte oder Dienstleistungen verkauft werden.</span><span class="sxs-lookup"><span data-stu-id="dadb5-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="dadb5-106">Wenn Sie z. B. Gartenarbeitszubehör verkaufen, bietet sich ein Verkauf in den Einheiten Paletten, Pakete, Kisten an.</span><span class="sxs-lookup"><span data-stu-id="dadb5-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="dadb5-107">Eine Einheitengruppe ist eine Sammlung dieser verschiedenen Einheiten.</span><span class="sxs-lookup"><span data-stu-id="dadb5-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="dadb5-108">Stellen Sie zum Ausführen der Schritte in diesem Thema sicher, dass Sie der Systemrolle Administrator oder Sales Professional Manager zugewiesen wurden oder über entsprechende Berechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="dadb5-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="dadb5-109">Erstellen einer Einheitengruppe</span><span class="sxs-lookup"><span data-stu-id="dadb5-109">Create a unit group</span></span>

1. <span data-ttu-id="dadb5-110">Wählen Sie in der Siteübersicht die Option **Einheiten** aus.</span><span class="sxs-lookup"><span data-stu-id="dadb5-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="dadb5-111">Wählen Sie **Neu** und geben Sie im Dialogfeld **Einheitengruppe erstellen** den Einheitennamen ein.</span><span class="sxs-lookup"><span data-stu-id="dadb5-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="dadb5-112">Geben Sie im Feld **Primäre Einheit** die niedrigste gebräuchliche Maßeinheit für die Einheitengruppe ein, in der das Produkt vertrieben wird.</span><span class="sxs-lookup"><span data-stu-id="dadb5-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="dadb5-113">Beispielsweise können Sie "Stück" oder "Unze" eingeben.</span><span class="sxs-lookup"><span data-stu-id="dadb5-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="dadb5-114">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="dadb5-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="dadb5-115">Einheiten einer Einheitsgruppe hinzufügen</span><span class="sxs-lookup"><span data-stu-id="dadb5-115">Add units to a unit group</span></span>

1. <span data-ttu-id="dadb5-116">Öffnen Sie eine Einheitengruppe und klicken Sie auf die Registerkarte **verbunden** und wählen Sie **Einheiten**.</span><span class="sxs-lookup"><span data-stu-id="dadb5-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="dadb5-117">Sie werden sehen, dass die primäre Einheit bereits hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="dadb5-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="dadb5-118">Wählen Sie **Neue Einheit hinzufügen** und auf der Seite **Schnell erstellen: Einheit** im Feld **Name** geben Sie im Feld das Nanem der Einheit ein.</span><span class="sxs-lookup"><span data-stu-id="dadb5-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="dadb5-119">Geben Sie im Feld **Menge** die Menge ein, die die Einheit enthält.</span><span class="sxs-lookup"><span data-stu-id="dadb5-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="dadb5-120">Wenn eine Kiste z. B. zwei Stück enthält, würden Sie 2 eingeben.</span><span class="sxs-lookup"><span data-stu-id="dadb5-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="dadb5-121">In dem Feld **Grundeinheit** wählen Sie im Feld eine Basiseinheit aus, um die niedrigste Maßeinheit für die Einheit festzulegen.</span><span class="sxs-lookup"><span data-stu-id="dadb5-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="dadb5-122">Zum Beispiel könnten Sie Stück auswählen.</span><span class="sxs-lookup"><span data-stu-id="dadb5-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="dadb5-123">Wählen Sie **Speichern**:</span><span class="sxs-lookup"><span data-stu-id="dadb5-123">Select **Save**:</span></span>
