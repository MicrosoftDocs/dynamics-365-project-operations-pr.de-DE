---
title: Benutzerdefinierte Felder und Entitäten als Preisdimensionen erstellen
description: Dieses Thema enthält Informationen zum Erstellen benutzerdefinierter Optionssätze oder Entitäten.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275627"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="6e459-103">Benutzerdefinierte Felder und Entitäten als Preisdimensionen erstellen</span><span class="sxs-lookup"><span data-stu-id="6e459-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="6e459-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="6e459-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6e459-105">Führen Sie die folgenden Schritte aus, wenn Sie einen benutzerdefinierten Optionssatz oder eine Entität zur Verwandung als Preisdimension erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="6e459-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="6e459-106">Weitere Informationen finden Sie unter [Preisdimensionen – Übersicht](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6e459-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="6e459-107">Wir empfehlen, alle benutzerdefinierten Preisdimensionsänderungen in einer separaten Lösung vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="6e459-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="6e459-108">Diese wichtige bewährte Methode bietet in Zukunft Flexibilität, um Änderungen nach Bedarf zu aktualisieren oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="6e459-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="6e459-109">Dies hilft auch bei der Wiederverwendung Ihrer Arbeit und erleichtert das Portieren dieser Änderungen auf eine andere Instanz. Nachdem Sie alle erforderlichen Änderungen vorgenommen haben, exportieren Sie diese Lösung als **Verwaltete Lösung** und importieren Sie sie in andere Instanzen, um Ihre Preisgestaltung wiederzuverwenden.</span><span class="sxs-lookup"><span data-stu-id="6e459-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="6e459-110">Erstellen benutzerdefinierter Felder und Optionssätze in der Preisdimensionslösung</span><span class="sxs-lookup"><span data-stu-id="6e459-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="6e459-111">Eine Preisdimension kann ein Optionssatz oder eine Entität sein.</span><span class="sxs-lookup"><span data-stu-id="6e459-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="6e459-112">Beide müssen in der Preisberechnungslösung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6e459-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="6e459-113">In den Schritten in diesem Verfahren wird erläutert, wie entitätsbasierte bzw. optionssatzbasierte Dimensionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6e459-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="6e459-114">Entitätsbasierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="6e459-114">Entity-based dimensions</span></span>
<span data-ttu-id="6e459-115">Führen Sie die folgenden Schritte aus, um entitätsbasierte Dimensionen zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="6e459-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="6e459-116">Gehen Sie zu **Einstellungen** > **Lösungen** und doppelklicken Sie dann auf **\<your organization name> Preisdimensionen**.</span><span class="sxs-lookup"><span data-stu-id="6e459-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="6e459-117">Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Entitäten** aus.</span><span class="sxs-lookup"><span data-stu-id="6e459-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="6e459-118">Wählen Sie **Neu**, um eine neue Entität namens **Standardtitel** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e459-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="6e459-119">Geben Sie die verbleibenden erforderlichen Informationen ein und wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="6e459-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definition der Entität „Standardtitel”](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="6e459-121">Optionssatzbasierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="6e459-121">Option set-based dimensions</span></span> 
<span data-ttu-id="6e459-122">Sie können zwei optionssatzbasierte Dimensionen erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e459-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="6e459-123">Verwenden Sie **Arbeitsort der Ressource**, um den Preis der **Home**-Standortarbeit und **Vor Ort**-Arbeit zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="6e459-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="6e459-124">Verwenden sie **Ressourcenarbeitszeit** mit den Werten **Regulär** und **Überstunden**, um einen Aufschlag anzuwenden, wenn die Arbeit abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6e459-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="6e459-125">Die folgende Grafik bietet eine Ansicht der **Arbeitsort der Ressource**-Dimension.</span><span class="sxs-lookup"><span data-stu-id="6e459-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Optionssatzbasierte Preisdimension namens „Arbeitsstandort der Ressource”](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="6e459-127">Die folgende Grafik bietet eine Ansicht der **Arbeitsstunden der Ressource**-Dimension.</span><span class="sxs-lookup"><span data-stu-id="6e459-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Optionssatzbasierte Preisdimension namens „Arbeitszeiten der Ressource”](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="6e459-129">Gehen Sie zu **Einstellungen** > **Lösungen** und doppelklicken Sie auf  **\<your organization name> Preisdimensionen**.</span><span class="sxs-lookup"><span data-stu-id="6e459-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="6e459-130">Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Optionssätze** aus.</span><span class="sxs-lookup"><span data-stu-id="6e459-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="6e459-131">Wählen Sie **Neu**, um einen neuen Optionssatz zu erstellen, geben Sie die verbleibenden erforderlichen Informationen ein, und wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="6e459-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="6e459-132">Erstellen von Daten für entitätsbasierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="6e459-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="6e459-133">Sie können Daten für entitätsbasierte Dimensionen manuell oder mithilfe von Microsoft Excel-Import- oder -Service-Aufrufen erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e459-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="6e459-134">Führen Sie die in diesem Verfahren beschriebenen Schritte aus, um zwei Standardtitel – **- Systemtechniker** und **Leitender Systemtechniker** – aus der entitätsbasierten Dimension **Standardtitel** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e459-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="6e459-135">Wenn die Datenmenge, die Sie erstellen möchten, gering ist, wie im folgenden Beispiel gezeigt, können Sie ein Standardformular verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e459-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="6e459-136">Wählen Sie **Erweiterte Suche** aus.</span><span class="sxs-lookup"><span data-stu-id="6e459-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="6e459-137">Wählen Sie die Entität **Standardtitel** aus und wählen Sie anschließend **Ergebnisse** aus.</span><span class="sxs-lookup"><span data-stu-id="6e459-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="6e459-138">Alle Zeilen der Entität **Standardtitel** werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6e459-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="6e459-139">Wählen Sie **Neu** und im Feld **Name** geben Sie Systemtechniker ein und wählen dann **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="6e459-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="6e459-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6e459-140">Close the page.</span></span> 
5. <span data-ttu-id="6e459-141">Wiederholen Sie die Schritte 1 - 3, um einen anderen Standardtitel für „Leitender Systemtechniker” zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e459-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Beispieldaten für die Entität „Standardtitel“](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]