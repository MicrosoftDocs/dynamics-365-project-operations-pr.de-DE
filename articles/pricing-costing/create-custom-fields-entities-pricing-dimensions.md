---
title: Benutzerdefinierte Felder und Entitäten als Preisdimensionen erstellen
description: Dieses Thema enthält Informationen zum Erstellen benutzerdefinierter Optionssätze oder Entitäten.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076562"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="48834-103">Benutzerdefinierte Felder und Entitäten als Preisdimensionen erstellen</span><span class="sxs-lookup"><span data-stu-id="48834-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="48834-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="48834-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="48834-105">Führen Sie die folgenden Schritte aus, wenn Sie einen benutzerdefinierten Optionssatz oder eine Entität erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="48834-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48834-106">Wir empfehlen, alle benutzerdefinierten Preisdimensionsänderungen in einer separaten Lösung vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="48834-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="48834-107">Diese wichtige bewährte Methode bietet in Zukunft die Flexibilität, Änderungen nach Bedarf zu aktualisieren oder zu entfernen, hilft bei der Wiederverwendung Ihrer Arbeit und erleichtert das Portieren dieser Änderungen auf eine andere Instanz.</span><span class="sxs-lookup"><span data-stu-id="48834-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="48834-108">Wenn alle erforderlichen Änderungen vorgenommen wurden, können Sie diese Lösung als **Verwaltete Lösung** exportieren und in andere Instanzen importieren, um Ihre Preiskonfiguration wiederzuverwenden.</span><span class="sxs-lookup"><span data-stu-id="48834-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="48834-109">Erstellen einer benutzerdefinierten Lösung für Preisdimensionen</span><span class="sxs-lookup"><span data-stu-id="48834-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="48834-110">Gehen Sie zu **Einstellungen** > **Lösungen** und wählen **Neu** , um eine neue Lösung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="48834-110">Go to **Settings** > **Solutions** , and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="48834-111">Geben Sie der Lösung einen Namen, **\<your organization name> Preisdimensionen** , geben die verbleibenden erforderlichen Informationen ein und wählen dann **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="48834-111">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="48834-112">Erstellen benutzerdefinierter Felder und Optionssätze in der Preisdimensionslösung</span><span class="sxs-lookup"><span data-stu-id="48834-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="48834-113">Eine Preisdimension kann ein Optionssatz oder eine Entität sein.</span><span class="sxs-lookup"><span data-stu-id="48834-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="48834-114">Beide müssen in der Preisberechnungslösung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="48834-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="48834-115">In den Schritten in diesem Verfahren wird erläutert, wie entitätsbasierte bzw. optionssatzbasierte Dimensionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="48834-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="48834-116">Entitätsbasierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="48834-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="48834-117">Gehen Sie zu **Einstellungen** > **Lösungen** und doppelklicken Sie dann auf **\<your organization name> Preisdimensionen**.</span><span class="sxs-lookup"><span data-stu-id="48834-117">Go to **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="48834-118">Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Entitäten** aus.</span><span class="sxs-lookup"><span data-stu-id="48834-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="48834-119">Wählen Sie **Neu** , um eine neue Entität namens **Standardtitel** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="48834-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="48834-120">Geben Sie die verbleibenden erforderlichen Informationen ein und wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="48834-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="48834-121">Optionssatzbasierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="48834-121">Option set-based dimensions</span></span> 
<span data-ttu-id="48834-122">Sie können zwei optionssatzbasierte Dimensionen erstellen.</span><span class="sxs-lookup"><span data-stu-id="48834-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="48834-123">Verwenden Sie **Arbeitsstandort der Ressource** , um den Preis für die Arbeit am **Wohnort** und  **Vor Ort** nachzuverfolgen. Verwenden Sie für **Arbeitszeiten der Ressource** die Werte **Regulär** bzw. **Überstunden** , um einen Aufschlag anzuwenden, wenn die Arbeit abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="48834-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="48834-124">Gehen Sie zu **Einstellungen** > **Lösungen** und doppelklicken Sie auf  **\<your organization name> Preisdimensionen**.</span><span class="sxs-lookup"><span data-stu-id="48834-124">Go to **Settings** > **Solutions** , and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="48834-125">Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Optionssätze** aus.</span><span class="sxs-lookup"><span data-stu-id="48834-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="48834-126">Wählen Sie **Neu** , um einen neuen Optionssatz zu erstellen, geben Sie die verbleibenden erforderlichen Informationen ein, und wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="48834-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="48834-127">Erstellen von Daten für entitätsbasierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="48834-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="48834-128">Sie können Daten für entitätsbasierte Dimensionen manuell oder mithilfe von Microsoft Excel-Import- oder -Service-Aufrufen erstellen.</span><span class="sxs-lookup"><span data-stu-id="48834-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="48834-129">Führen Sie die in diesem Verfahren beschriebenen Schritte aus, um zwei Standardtitel – **- Systemtechniker** und **Leitender Systemtechniker** – aus der entitätsbasierten Dimension **Standardtitel** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="48834-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="48834-130">Wenn die Datenmenge, die Sie erstellen möchten, gering ist, wie im folgenden Beispiel gezeigt, können Sie ein Standardformular verwenden.</span><span class="sxs-lookup"><span data-stu-id="48834-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="48834-131">Wählen Sie **Erweiterte Suche** und wählen Sie die Entität **Standardtitel** und dann **Ergebnisse**.</span><span class="sxs-lookup"><span data-stu-id="48834-131">Select **Advanced Find** , select the entity **Standard Title** , and then select **Results**.</span></span> <span data-ttu-id="48834-132">Alle Zeilen der Entität **Standardtitel** werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="48834-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="48834-133">Wählen Sie **Neu** und im Feld **Name** geben Sie Systemtechniker ein und wählen dann **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="48834-133">Select **New** , and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="48834-134">Schließen Sie das Formular.</span><span class="sxs-lookup"><span data-stu-id="48834-134">Close the form.</span></span> 
4. <span data-ttu-id="48834-135">Wiederholen Sie die Schritte 1 - 3, um einen anderen Standardtitel für „Leitender Systemtechniker” zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="48834-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="48834-136">Hinzufügen aller erforderlichen Entitäten und zugehörigen Komponenten zur Preisdimensionslösung</span><span class="sxs-lookup"><span data-stu-id="48834-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="48834-137">Sie müssen Ihrer Preisberechnungslösung die folgenden Entitäten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48834-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="48834-138">Führen Sie die Schritte in diesem Verfahren aus, um einige wichtige Schemaänderungen in der Preisberechnungslösung vorzunehmen, damit die Entitäten die neuen Preisberechnungsdimensionen kennen.</span><span class="sxs-lookup"><span data-stu-id="48834-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="48834-139">Wählen Sie **Einstellungen** > **Lösungen** und doppelklicken Sie auf **\<your organization name> Preisdimensionen**.</span><span class="sxs-lookup"><span data-stu-id="48834-139">Select **Settings** > **Solutions** , and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="48834-140">Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Vorh. hinzufügen** > **Entitäten** aus.</span><span class="sxs-lookup"><span data-stu-id="48834-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="48834-141">Wählen Sie im Dialogfeld **Lösungskomponenten** die folgenden Entitäten aus:</span><span class="sxs-lookup"><span data-stu-id="48834-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="48834-142">Tatsächlich</span><span class="sxs-lookup"><span data-stu-id="48834-142">Actual</span></span>
  - <span data-ttu-id="48834-143">Buchbare Ressource</span><span class="sxs-lookup"><span data-stu-id="48834-143">Bookable Resource</span></span>
  - <span data-ttu-id="48834-144">Vorkalkulationsposition</span><span class="sxs-lookup"><span data-stu-id="48834-144">Estimate Line</span></span>
  - <span data-ttu-id="48834-145">Rechnungsposition</span><span class="sxs-lookup"><span data-stu-id="48834-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="48834-146">Erfassungsposition</span><span class="sxs-lookup"><span data-stu-id="48834-146">Journal Line</span></span>
  - <span data-ttu-id="48834-147">Projektvertragsposition</span><span class="sxs-lookup"><span data-stu-id="48834-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="48834-148">Projektteammitglied</span><span class="sxs-lookup"><span data-stu-id="48834-148">Project Team Member</span></span>
  - <span data-ttu-id="48834-149">Detailinformationen zur Angebotsposition</span><span class="sxs-lookup"><span data-stu-id="48834-149">Quote Line Detail</span></span>
  - <span data-ttu-id="48834-150">Rollenpreisaufschlag</span><span class="sxs-lookup"><span data-stu-id="48834-150">Role Price Markup</span></span>
  - <span data-ttu-id="48834-151">Rollenpreis</span><span class="sxs-lookup"><span data-stu-id="48834-151">Role Price</span></span> 
  - <span data-ttu-id="48834-152">Zeiteintrag</span><span class="sxs-lookup"><span data-stu-id="48834-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="48834-153">Stellen Sie sicher, dass alle Formulare und Ansichten für jede der ausgewählten Entitäten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="48834-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="48834-154">Wenn Sie aufgefordert werden, abhängige Entitäten für die oben ausgewählten Entitäten einzuschließen, wählen Sie **Nein**.</span><span class="sxs-lookup"><span data-stu-id="48834-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

