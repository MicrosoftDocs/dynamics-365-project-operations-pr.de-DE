---
title: Projektangebote aus Verkaufschancen erstellen
description: Dieses Thema enthält Informationen zum Erstellen eines Projektangebots aus einer Verkaufschance.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076436"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="9a218-103">Projektangebote aus Verkaufschancen erstellen</span><span class="sxs-lookup"><span data-stu-id="9a218-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="9a218-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="9a218-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9a218-105">Angebote können auf folgende Weise aus Projektverkaufschancen erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="9a218-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="9a218-106">Von der **Angebote** -Registerkarte auf der **Projektverkaufschance** -Seite</span><span class="sxs-lookup"><span data-stu-id="9a218-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="9a218-107">Mit dem Verkaufschancen-Vertriebsprozesses-Flow</span><span class="sxs-lookup"><span data-stu-id="9a218-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="9a218-108">Durch Aktualisieren der Verkaufschancenreferenz für ein vorhandenes Angebot</span><span class="sxs-lookup"><span data-stu-id="9a218-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="9a218-109">Von der Angebote-Registerkarte der Projektverkaufschance-Seite</span><span class="sxs-lookup"><span data-stu-id="9a218-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="9a218-110">Führen Sie die folgenden Schritte aus, um aus einer Verkaufschance ein Projektangebot zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a218-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="9a218-111">Öffnen Sie die **Angebote** -Registerkarte auf der **Projektverkaufschance** -Seite.</span><span class="sxs-lookup"><span data-stu-id="9a218-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="9a218-112">Wählen Sie auf dem **Angebote** -Unterraster das **+** -Zeichen aus, um ein neues Projektangebot basierend auf der Verkaufschance zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a218-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="9a218-113">Alle Verkaufschancenpositionen und zugehörigen Projektpreislisten werden aus der Verkaufschance in das neue Angebot kopiert.</span><span class="sxs-lookup"><span data-stu-id="9a218-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="9a218-114">Mit dem Verkaufschancen-Vertriebsprozesses-Flow</span><span class="sxs-lookup"><span data-stu-id="9a218-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="9a218-115">Führen Sie die folgenden Schritte aus, um aus dem Verkaufschancen-Vertriebsprozess-Flow ein Angebot zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a218-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="9a218-116">Öffnen Sie die Verkaufschance im Verkaufschancen-Verkaufsprozess-Flow.</span><span class="sxs-lookup"><span data-stu-id="9a218-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="9a218-117">Wählen Sie die Phase **Qualifizieren** aus.</span><span class="sxs-lookup"><span data-stu-id="9a218-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="9a218-118">Wählen **Weiter** und dann **+ Erstellen** aus, um ein neues Angebot zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a218-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="9a218-119">Die meisten Informationen auf der **Zusammenfassung** -Registerkarte für dieses neue Angebot wurden standardmäßig aus der Verkaufschance entfernt.</span><span class="sxs-lookup"><span data-stu-id="9a218-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="9a218-120">Geben Sie alle erforderlichen Informationen ein, die fehlen, oder aktualisieren Sie die Standardwerte nach Bedarf auf der **Zusammenfassung** -Registerkarte,</span><span class="sxs-lookup"><span data-stu-id="9a218-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="9a218-121">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="9a218-121">Select **Save**.</span></span> <span data-ttu-id="9a218-122">Das neue Angebot wird erstellt und der Verkaufschance zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9a218-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="9a218-123">Sie können jetzt die Angebotsinformationen auf der **Angebote** -Registerkarte der **Verkaufschance** -Seite anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9a218-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="9a218-124">Der Verkaufschance-Verkaufsprozess geht zur nächsten Phase über: **Vorschlagen**.</span><span class="sxs-lookup"><span data-stu-id="9a218-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="9a218-125">Durch Aktualisieren der Verkaufschancenreferenz für ein vorhandenes Angebot</span><span class="sxs-lookup"><span data-stu-id="9a218-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="9a218-126">Ein vorhandenes Angebot kann mit einer Verkaufschance verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="9a218-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="9a218-127">Führen Sie die folgenden Schritte aus, um die Verkaufschance-Informationen zu einem vorhandenen Angebot zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9a218-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="9a218-128">Öffnen Sie die **Zusammenfassung** -Registerkarte auf der **Angebot** -Seite.</span><span class="sxs-lookup"><span data-stu-id="9a218-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="9a218-129">Wählen Sie in dem **Verkaufschance** -Feld die Verkaufschance aus, die Sie mit dem Angebot verknüpfen möchten.</span><span class="sxs-lookup"><span data-stu-id="9a218-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="9a218-130">Sie können das Angebot im **Angebote** -Raster der Verkaufschance sehen.</span><span class="sxs-lookup"><span data-stu-id="9a218-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="9a218-131">Mit dem Verkaufschance-Verkaufsprozess kann die Verkaufschance in die nächste Phase **Vorschlagen** verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="9a218-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="9a218-132">Wenn Sie eine Verkaufschance in diese Phase verschieben, können Sie dieses Angebot aus einer Liste von Angeboten auswählen, die dieser Verkaufschance zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9a218-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="9a218-133">Wenn Sie dieses Angebot auswählen, bedeutet dies, dass Sie damit fortfahren.</span><span class="sxs-lookup"><span data-stu-id="9a218-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="9a218-134">Alle anderen mit der Verkaufschance verbundenen Angebote sind weiterhin verfügbar und aktiv, bis eines davon gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="9a218-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="9a218-135">Sie können den Verkaufsprozess wieder in die vorherige Phase **Qualifizieren** verschieben und ein anderes Angebot auswählen, um mit diesem weiterzumachen.</span><span class="sxs-lookup"><span data-stu-id="9a218-135">You can move the sales process back to the previous stage **Qualify** , and pick another quote to move forward with.</span></span>
