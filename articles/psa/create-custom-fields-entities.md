---
title: Benutzerdefinierte Felder und Entitäten erstellen
description: In diesem Thema wird erläutert, wie Optionssätze und Entitäten in Ihrer eigenen Lösung auf der Power Apps Plattform erstellt werden.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c58745a46e84a40b90fbb3cbf89b10e293588fc3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290531"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="2bda2-103">Benutzerdefinierte Felder und Entitäten erstellen</span><span class="sxs-lookup"><span data-stu-id="2bda2-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2bda2-104">Führen Sie die folgenden Schritte aus, wenn Sie einen benutzerdefinierten Optionssatz oder eine Entität auf der Power Apps-Plattform erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="2bda2-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="2bda2-105">Die Verfahren in diesem Thema sollten über die Weboberfläche von Project Service Automation (PSA) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2bda2-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2bda2-106">Wir empfehlen, alle benutzerdefinierten Preisdimensionsänderungen in einer separaten Lösung vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="2bda2-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="2bda2-107">Diese wichtige bewährte Methode bietet in Zukunft die Flexibilität, Änderungen nach Bedarf zu aktualisieren oder zu entfernen, hilft bei der Wiederverwendung Ihrer Arbeit und erleichtert das Portieren dieser Änderungen auf eine andere Instanz.</span><span class="sxs-lookup"><span data-stu-id="2bda2-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="2bda2-108">Wenn alle erforderlichen Änderungen vorgenommen wurden, können Sie diese Lösung als **Verwaltete Lösung** exportieren und in andere Instanzen importieren, um Ihre Preiskonfiguration wiederzuverwenden.</span><span class="sxs-lookup"><span data-stu-id="2bda2-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="2bda2-109">Erstellen benutzerdefinierter Felder und Optionssätze in der Preisdimensionslösung</span><span class="sxs-lookup"><span data-stu-id="2bda2-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="2bda2-110">Eine Preisdimension kann ein Optionssatz oder eine Entität sein.</span><span class="sxs-lookup"><span data-stu-id="2bda2-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="2bda2-111">Beide müssen in der Preisberechnungslösung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2bda2-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="2bda2-112">In den Schritten in diesem Verfahren wird erläutert, wie entitätsbasierte bzw. optionssatzbasierte Dimensionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2bda2-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="2bda2-113">Entitätsbasierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="2bda2-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="2bda2-114">Wählen Sie in PSA **Einstellungen** > **Lösungen** und doppelklicken Sie dann auf **\<your organization name> Preisdimensionen**.</span><span class="sxs-lookup"><span data-stu-id="2bda2-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="2bda2-115">Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Entitäten** aus.</span><span class="sxs-lookup"><span data-stu-id="2bda2-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="2bda2-116">Klicken Sie auf **Neu**, um eine neue Entität namens **Standardtitel** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2bda2-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="2bda2-117">Geben Sie die verbleibenden erforderlichen Informationen ein und klicken Sie anschließend auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="2bda2-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definition der Entität „Standardtitel”](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="2bda2-119">Optionssatzbasierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="2bda2-119">Option set-based dimensions</span></span> 
<span data-ttu-id="2bda2-120">Sie können zwei optionssatzbasierte Dimensionen erstellen.</span><span class="sxs-lookup"><span data-stu-id="2bda2-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="2bda2-121">Verwenden Sie **Arbeitsstandort der Ressource**, um den Preis für die Arbeit am **Wohnort** und  **Vor Ort** nachzuverfolgen. Verwenden Sie für **Arbeitszeiten der Ressource** die Werte **Regulär** bzw. **Überstunden**, um einen Aufschlag anzuwenden, wenn die Arbeit abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2bda2-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="2bda2-122">Wählen Sie in PSA **Einstellungen** > **Lösungen** und doppelklicken Sie dann auf **\<your organization name> Preisdimensionen**.</span><span class="sxs-lookup"><span data-stu-id="2bda2-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="2bda2-123">Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Optionssätze** aus.</span><span class="sxs-lookup"><span data-stu-id="2bda2-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="2bda2-124">Klicken Sie auf **Neu**, um einen neuen Optionssatz zu erstellen, geben Sie die verbleibenden erforderlichen Informationen ein, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="2bda2-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="2bda2-125">Optionssatzbasierte Preisdimension namens „Arbeitsstandort der Ressource”</span><span class="sxs-lookup"><span data-stu-id="2bda2-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="2bda2-126">Optionssatzbasierte Preisdimension namens „Arbeitszeiten der Ressource”</span><span class="sxs-lookup"><span data-stu-id="2bda2-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="2bda2-127">Erstellen von Daten für entitätsbasierte Dimensionen</span><span class="sxs-lookup"><span data-stu-id="2bda2-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="2bda2-128">Sie können Daten für entitätsbasierte Dimensionen manuell oder mithilfe von Microsoft Excel-Import- oder -Service-Aufrufen erstellen.</span><span class="sxs-lookup"><span data-stu-id="2bda2-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="2bda2-129">Führen Sie die in diesem Verfahren beschriebenen Schritte aus, um zwei Standardtitel – **- Systemtechniker** und **Leitender Systemtechniker** – aus der entitätsbasierten Dimension **Standardtitel** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2bda2-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="2bda2-130">Wenn die Datenmenge, die Sie erstellen möchten, gering ist, wie im folgenden Beispiel gezeigt, können Sie ein Standardformular verwenden.</span><span class="sxs-lookup"><span data-stu-id="2bda2-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="2bda2-131">Klicken Sie in PSA auf **Erweiterte Suche**.</span><span class="sxs-lookup"><span data-stu-id="2bda2-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="2bda2-132">Wählen Sie die Entität **Standardtitel** aus und klicken Sie anschließend auf **Ergebnisse**.</span><span class="sxs-lookup"><span data-stu-id="2bda2-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="2bda2-133">Alle Zeilen der Entität **Standardtitel** werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2bda2-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="2bda2-134">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="2bda2-134">Click **New**.</span></span> <span data-ttu-id="2bda2-135">Geben Sie im Feld **Name** „Systemtechniker” ein und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="2bda2-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="2bda2-136">Schließen Sie das Formular.</span><span class="sxs-lookup"><span data-stu-id="2bda2-136">Close the form.</span></span> 
4. <span data-ttu-id="2bda2-137">Wiederholen Sie die Schritte 1 - 3, um einen anderen Standardtitel für „Leitender Systemtechniker” zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2bda2-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="2bda2-138">Beispieldaten für die Entität „Standardtitel”</span><span class="sxs-lookup"><span data-stu-id="2bda2-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]