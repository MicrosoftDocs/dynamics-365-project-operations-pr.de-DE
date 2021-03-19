---
title: Erstellen von benutzerdefinierten Lösungen für Preisdimensionen
description: In diesem Thema wird erläutert, wie Sie eine benutzerdefinierte Lösung erstellen, wenn Sie benutzerdefinierte Preisdimensionen erstellen.
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
ms.openlocfilehash: 1d8117d6f6bcedc97264401fc941470f34efb1ae
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284987"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="b0b6d-103">Erstellen von benutzerdefinierten Lösungen für Preisdimensionen</span><span class="sxs-lookup"><span data-stu-id="b0b6d-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="b0b6d-104">Alle Änderungen der benutzerdefinierten Preisdimension sollten in einer separaten Lösung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="b0b6d-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="b0b6d-105">Diese wichtige bewährte Methode bietet in Zukunft die Flexibilität, Änderungen nach Bedarf zu aktualisieren oder zu entfernen, hilft bei der Wiederverwendung Ihrer Arbeit und erleichtert das Portieren dieser Änderungen auf eine andere Instanz.</span><span class="sxs-lookup"><span data-stu-id="b0b6d-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="b0b6d-106">Nachdem Sie die erforderlichen Änderungen vorgenommen haben, können Sie diese Lösung als **Verwaltete Lösung** exportieren und in andere Instanzen importieren, um Ihre Preiskonfiguration wiederzuverwenden.</span><span class="sxs-lookup"><span data-stu-id="b0b6d-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="b0b6d-107">Wählen Sie **Einstellungen** > **Lösungen** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b0b6d-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="b0b6d-108">Geben Sie der Lösung einen Namen, **\<your organization name> Preisdimensionen**, geben die verbleibenden erforderlichen Informationen ein und wählen dann **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="b0b6d-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Erstellen einer benutzerdefinierten Lösung für Preisdimensionen](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="b0b6d-110">Hinzufügen aller erforderlichen Entitäten und zugehörigen Komponenten zur Preisdimensionslösung</span><span class="sxs-lookup"><span data-stu-id="b0b6d-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="b0b6d-111">Sie müssen Ihrer Preisberechnungslösung die folgenden Project Service-Entitäten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b0b6d-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="b0b6d-112">Schließen Sie die Schritte in diesem Verfahren ab, um einige wichtige Schemaänderungen in der Preisberechnungslösung vorzunehmen, damit die Entitäten die neuen Preisberechnungsdimensionen kennen.</span><span class="sxs-lookup"><span data-stu-id="b0b6d-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="b0b6d-113">Wählen Sie **Einstellungen** > **Lösungen** und doppelklicken Sie dann auf **\<your organization name> Preisdimensionen**.</span><span class="sxs-lookup"><span data-stu-id="b0b6d-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="b0b6d-114">Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Vorh. hinzufügen** > **Entitäten** aus.</span><span class="sxs-lookup"><span data-stu-id="b0b6d-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="b0b6d-115">Wählen Sie im Dialogfeld **Lösungskomponenten** die folgenden Entitäten aus:</span><span class="sxs-lookup"><span data-stu-id="b0b6d-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="b0b6d-116">Tatsächl.</span><span class="sxs-lookup"><span data-stu-id="b0b6d-116">Actual</span></span>
- <span data-ttu-id="b0b6d-117">Buchbare Ressource</span><span class="sxs-lookup"><span data-stu-id="b0b6d-117">Bookable Resource</span></span>
- <span data-ttu-id="b0b6d-118">Vorkalkulationsposition</span><span class="sxs-lookup"><span data-stu-id="b0b6d-118">Estimate Line</span></span>
- <span data-ttu-id="b0b6d-119">Projektaufgabe</span><span class="sxs-lookup"><span data-stu-id="b0b6d-119">Project Task</span></span>
- <span data-ttu-id="b0b6d-120">Rechnungsposition</span><span class="sxs-lookup"><span data-stu-id="b0b6d-120">Invoice Line Detail</span></span>
- <span data-ttu-id="b0b6d-121">Erfassungsposition</span><span class="sxs-lookup"><span data-stu-id="b0b6d-121">Journal Line</span></span>
- <span data-ttu-id="b0b6d-122">Projektvertragsposition</span><span class="sxs-lookup"><span data-stu-id="b0b6d-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="b0b6d-123">Projektteammitglied</span><span class="sxs-lookup"><span data-stu-id="b0b6d-123">Project Team Member</span></span>
- <span data-ttu-id="b0b6d-124">Detailinformationen zur Angebotsposition</span><span class="sxs-lookup"><span data-stu-id="b0b6d-124">Quote Line Detail</span></span>
- <span data-ttu-id="b0b6d-125">Rollenpreisaufschlag</span><span class="sxs-lookup"><span data-stu-id="b0b6d-125">Role Price Markup</span></span>
- <span data-ttu-id="b0b6d-126">Rollenpreis</span><span class="sxs-lookup"><span data-stu-id="b0b6d-126">Role Price</span></span> 
- <span data-ttu-id="b0b6d-127">Zeiteintrag</span><span class="sxs-lookup"><span data-stu-id="b0b6d-127">Time Entry</span></span> 

> ![Hinzufügen vorhandener Entitäten zur Lösung für Preisdimensionen](media/Existing-entities-to-PD-solution.png)

> ![Lösungskomponenten auswählen](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="b0b6d-130">Stellen Sie sicher, dass alle Formulare und Ansichten für jede der ausgewählten Entitäten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b0b6d-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="b0b6d-131">Wenn Sie aufgefordert werden, abhängige Entitäten für die ausgewählten Entitäten einzuschließen, wählen Sie **Nein**.</span><span class="sxs-lookup"><span data-stu-id="b0b6d-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Schließen Sie nicht alle zugehörigen Komponenten ein.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]