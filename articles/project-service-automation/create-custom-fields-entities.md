---
title: Benutzerdefinierte Felder und Entitäten erstellen
description: In diesem Thema wird erläutert, wie Optionssätze und Entitäten in Ihrer eigenen Lösung auf der Power Apps Plattform erstellt werden.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722039"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="35ffb-103">Benutzerdefinierte Felder und Entitäten erstellen</span><span class="sxs-lookup"><span data-stu-id="35ffb-103">Create custom fields and entities</span></span> 

<span data-ttu-id="35ffb-104">Führen Sie die folgenden Schritte aus, wenn Sie einen benutzerdefinierten Optionssatz oder eine Entität auf der Power Apps-Plattform erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="35ffb-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="35ffb-105">Die Verfahren in diesem Thema sollten über die Weboberfläche von Project Service Automation (PSA) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="35ffb-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35ffb-106">Wir empfehlen, alle benutzerdefinierten Preisdimensionsänderungen in einer separaten Lösung vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="35ffb-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="35ffb-107">Diese wichtige bewährte Methode bietet in Zukunft die Flexibilität, Änderungen nach Bedarf zu aktualisieren oder zu entfernen, hilft bei der Wiederverwendung Ihrer Arbeit und erleichtert das Portieren dieser Änderungen auf eine andere Instanz.</span><span class="sxs-lookup"><span data-stu-id="35ffb-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="35ffb-108">Wenn alle erforderlichen Änderungen vorgenommen wurden, können Sie diese Lösung als **Verwaltete Lösung** exportieren und in andere Instanzen importieren, um Ihre Preiskonfiguration wiederzuverwenden.</span><span class="sxs-lookup"><span data-stu-id="35ffb-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="35ffb-109">Erstellen einer benutzerdefinierten Lösung für Preisdimensionen</span><span class="sxs-lookup"><span data-stu-id="35ffb-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="35ffb-110">Klicken Sie in PSA auf **Einstellungen** > **Lösungen** und dann auf **Neu**, um eine neue Lösung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="35ffb-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="35ffb-111">Geben Sie der Lösung einen Namen, **\<Name Ihrer Organisation name > Preisdimensionen**, geben die verbleibenden erforderlichen Informationen ein und klicken anschließend auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="35ffb-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Erstellen einer benutzerdefinierten Lösung für Preisdimensionen](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="35ffb-113">Erstellen benutzerdefinierter Felder und Optionssätze in der Preisdimensionslösung</span><span class="sxs-lookup"><span data-stu-id="35ffb-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="35ffb-114">Eine Preisdimension kann ein Optionssatz oder eine Entität sein.</span><span class="sxs-lookup"><span data-stu-id="35ffb-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="35ffb-115">Beide müssen in der Preisberechnungslösung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="35ffb-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="35ffb-116">In den Schritten in diesem Verfahren wird erläutert, wie entitätsbasierte bzw. optionssatzbasierte Dimensionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="35ffb-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="35ffb-117">Entitätsbasierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="35ffb-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="35ffb-118">Klicken Sie in PSA auf **Einstellungen** > **Lösungen** und doppelklicken Sie anschließend auf **\<Name Ihrer Organisation > Preisdimensionen**.</span><span class="sxs-lookup"><span data-stu-id="35ffb-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="35ffb-119">Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Entitäten** aus.</span><span class="sxs-lookup"><span data-stu-id="35ffb-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="35ffb-120">Klicken Sie auf **Neu**, um eine neue Entität namens **Standardtitel** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="35ffb-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="35ffb-121">Geben Sie die verbleibenden erforderlichen Informationen ein und klicken Sie anschließend auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="35ffb-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definition der Entität „Standardtitel”](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="35ffb-123">Optionssatzbasierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="35ffb-123">Option set-based dimensions</span></span> 
<span data-ttu-id="35ffb-124">Sie können zwei optionssatzbasierte Dimensionen erstellen.</span><span class="sxs-lookup"><span data-stu-id="35ffb-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="35ffb-125">Verwenden Sie **Arbeitsstandort der Ressource**, um den Preis für die Arbeit am **Wohnort** und  **Vor Ort** nachzuverfolgen. Verwenden Sie für **Arbeitszeiten der Ressource** die Werte **Regulär** bzw. **Überstunden**, um einen Aufschlag anzuwenden, wenn die Arbeit abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="35ffb-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="35ffb-126">Klicken Sie in PSA auf **Einstellungen** > **Lösungen** und doppelklicken Sie anschließend auf **\<Name Ihrer Organisation > Preisdimensionen**.</span><span class="sxs-lookup"><span data-stu-id="35ffb-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="35ffb-127">Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Optionssätze** aus.</span><span class="sxs-lookup"><span data-stu-id="35ffb-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="35ffb-128">Klicken Sie auf **Neu**, um einen neuen Optionssatz zu erstellen, geben Sie die verbleibenden erforderlichen Informationen ein, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="35ffb-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="35ffb-129">Optionssatzbasierte Preisdimension namens „Arbeitsstandort der Ressource”</span><span class="sxs-lookup"><span data-stu-id="35ffb-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="35ffb-130">Optionssatzbasierte Preisdimension namens „Arbeitszeiten der Ressource”</span><span class="sxs-lookup"><span data-stu-id="35ffb-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="35ffb-131">Erstellen von Daten für entitätsbasierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="35ffb-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="35ffb-132">Sie können Daten für entitätsbasierte Dimensionen manuell oder mithilfe von Microsoft Excel-Import- oder -Service-Aufrufen erstellen.</span><span class="sxs-lookup"><span data-stu-id="35ffb-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="35ffb-133">Führen Sie die in diesem Verfahren beschriebenen Schritte aus, um zwei Standardtitel – **- Systemtechniker** und **Leitender Systemtechniker** – aus der entitätsbasierten Dimension **Standardtitel** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="35ffb-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="35ffb-134">Wenn die Datenmenge, die Sie erstellen möchten, gering ist, wie im folgenden Beispiel gezeigt, können Sie ein Standardformular verwenden.</span><span class="sxs-lookup"><span data-stu-id="35ffb-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="35ffb-135">Klicken Sie in PSA auf **Erweiterte Suche**.</span><span class="sxs-lookup"><span data-stu-id="35ffb-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="35ffb-136">Wählen Sie die Entität **Standardtitel** aus und klicken Sie anschließend auf **Ergebnisse**.</span><span class="sxs-lookup"><span data-stu-id="35ffb-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="35ffb-137">Alle Zeilen der Entität **Standardtitel** werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="35ffb-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="35ffb-138">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="35ffb-138">Click **New**.</span></span> <span data-ttu-id="35ffb-139">Geben Sie im Feld **Name** „Systemtechniker” ein und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="35ffb-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="35ffb-140">Schließen Sie das Formular.</span><span class="sxs-lookup"><span data-stu-id="35ffb-140">Close the form.</span></span> 
4. <span data-ttu-id="35ffb-141">Wiederholen Sie die Schritte 1 - 3, um einen anderen Standardtitel für „Leitender Systemtechniker” zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="35ffb-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="35ffb-142">Beispieldaten für die Entität „Standardtitel”</span><span class="sxs-lookup"><span data-stu-id="35ffb-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="35ffb-143">Hinzufügen aller erforderlichen PSA-Entitäten und zugehörigen Komponenten zur Preisdimensionslösung</span><span class="sxs-lookup"><span data-stu-id="35ffb-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="35ffb-144">Sie müssen Ihrer Preisberechnungslösung die folgenden Project Service-Entitäten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="35ffb-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="35ffb-145">Führen Sie die Schritte in diesem Verfahren aus, um einige wichtige Schemaänderungen in der Preisberechnungslösung vorzunehmen, damit die Entitäten die neuen Preisberechnungsdimensionen kennen.</span><span class="sxs-lookup"><span data-stu-id="35ffb-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="35ffb-146">Klicken Sie in PSA auf **Einstellungen** > **Lösungen** und doppelklicken Sie anschließend auf **\<Name Ihrer Organisation > Preisdimensionen**.</span><span class="sxs-lookup"><span data-stu-id="35ffb-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="35ffb-147">Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Vorh. hinzufügen** > **Entitäten** aus.</span><span class="sxs-lookup"><span data-stu-id="35ffb-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="35ffb-148">Wählen Sie im Dialogfeld **Lösungskomponenten** die folgenden Entitäten aus:</span><span class="sxs-lookup"><span data-stu-id="35ffb-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="35ffb-149">Tatsächlich</span><span class="sxs-lookup"><span data-stu-id="35ffb-149">Actual</span></span>
- <span data-ttu-id="35ffb-150">Buchbare Ressource</span><span class="sxs-lookup"><span data-stu-id="35ffb-150">Bookable Resource</span></span>
- <span data-ttu-id="35ffb-151">Vorkalkulationsposition</span><span class="sxs-lookup"><span data-stu-id="35ffb-151">Estimate Line</span></span>
- <span data-ttu-id="35ffb-152">Rechnungsposition</span><span class="sxs-lookup"><span data-stu-id="35ffb-152">Invoice Line Detail</span></span>
- <span data-ttu-id="35ffb-153">Erfassungsposition</span><span class="sxs-lookup"><span data-stu-id="35ffb-153">Journal Line</span></span>
- <span data-ttu-id="35ffb-154">Projektvertragsposition</span><span class="sxs-lookup"><span data-stu-id="35ffb-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="35ffb-155">Projektteammitglied</span><span class="sxs-lookup"><span data-stu-id="35ffb-155">Project Team Member</span></span>
- <span data-ttu-id="35ffb-156">Detailinformationen zur Angebotsposition</span><span class="sxs-lookup"><span data-stu-id="35ffb-156">Quote Line Detail</span></span>
- <span data-ttu-id="35ffb-157">Rollenpreisaufschlag</span><span class="sxs-lookup"><span data-stu-id="35ffb-157">Role Price Markup</span></span>
- <span data-ttu-id="35ffb-158">Rollenpreis</span><span class="sxs-lookup"><span data-stu-id="35ffb-158">Role Price</span></span> 
- <span data-ttu-id="35ffb-159">Zeiteintrag</span><span class="sxs-lookup"><span data-stu-id="35ffb-159">Time Entry</span></span> 

> ![Hinzufügen vorhandener Entitäten zur Lösung für Preisdimensionen](media/Existing-entities-to-PD-solution.png)

> ![Lösungskomponenten auswählen](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="35ffb-162">Stellen Sie sicher, dass alle Formulare und Ansichten für jede der ausgewählten Entitäten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="35ffb-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="35ffb-163">Wenn Sie aufgefordert werden, abhängige Entitäten für die oben ausgewählten Entitäten einzuschließen, klicken Sie auf **Nein**.</span><span class="sxs-lookup"><span data-stu-id="35ffb-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Schließen Sie nicht alle zugehörigen Komponenten ein.](media/Do-not-include-required.png)


