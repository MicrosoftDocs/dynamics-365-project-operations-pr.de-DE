---
title: Eine Lösung für benutzerdefinierte Preisdimensionen erstellen
description: Dieses Thema enthält Informationen zum Erstellen von Lösungen für benutzerdefinierte Preisdimensionen.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010335"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="05b3a-103">Eine Lösung für benutzerdefinierte Preisdimensionen erstellen</span><span class="sxs-lookup"><span data-stu-id="05b3a-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="05b3a-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="05b3a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="05b3a-105">Alle Änderungen der benutzerdefinierten Preisdimension sollten in einer separaten Lösung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="05b3a-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="05b3a-106">Diese wichtige bewährte Methode bietet die Flexibilität, Änderungen nach Bedarf zu aktualisieren oder zu entfernen, hilft bei der Wiederverwendung Ihrer Arbeit und erleichtert das Portieren dieser Änderungen auf andere Instanzen.</span><span class="sxs-lookup"><span data-stu-id="05b3a-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="05b3a-107">Wenn alle erforderlichen Änderungen vorgenommen wurden, können Sie diese Lösung als **Verwaltete Lösung** exportieren und in andere Instanzen importieren, um sie wiederzuverwenden.</span><span class="sxs-lookup"><span data-stu-id="05b3a-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="05b3a-108">Eine Lösung für benutzerdefinierte Preisdimensionen erstellen</span><span class="sxs-lookup"><span data-stu-id="05b3a-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="05b3a-109">Wählen Sie **Einstellungen** > **Lösungen** und dann **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="05b3a-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="05b3a-110">Nennen Sie die Lösung *<your organization name>-Preisdimensionen*.</span><span class="sxs-lookup"><span data-stu-id="05b3a-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="05b3a-111">Geben Sie die verbleibenden erforderlichen Informationen ein und wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="05b3a-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Erstellen einer Lösung für benutzerdefinierte Preisdimensionen](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="05b3a-113">Hinzufügen aller erforderlichen Entitäten und zugehörigen Komponenten zur Preisdimensionslösung</span><span class="sxs-lookup"><span data-stu-id="05b3a-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="05b3a-114">Fügen Sie Ihrer Preislösung die folgenden Project Service-Entitäten hinzu, um wichtige Schemaänderungen in der Preislösung vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="05b3a-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="05b3a-115">Nachdem Sie dieses Verfahren abgeschlossen haben, erkennen die Entitäten die neuen Preisdimensionen.</span><span class="sxs-lookup"><span data-stu-id="05b3a-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="05b3a-116">Wählen Sie **Einstellungen** > **Lösungen** und doppelklicken Sie anschließend auf **<*Name Ihrer Organisation*> Preisdimensionen**.</span><span class="sxs-lookup"><span data-stu-id="05b3a-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="05b3a-117">Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Vorh. hinzufügen** > **Entitäten** aus.</span><span class="sxs-lookup"><span data-stu-id="05b3a-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="05b3a-118">Wählen Sie im Dialogfeld **Lösungskomponenten** die folgenden Entitäten aus:</span><span class="sxs-lookup"><span data-stu-id="05b3a-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="05b3a-119">**Tatsächl.**</span><span class="sxs-lookup"><span data-stu-id="05b3a-119">**Actual**</span></span>
   - <span data-ttu-id="05b3a-120">**Buchbare Ressource**</span><span class="sxs-lookup"><span data-stu-id="05b3a-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="05b3a-121">**Vorkalkulationsposition**</span><span class="sxs-lookup"><span data-stu-id="05b3a-121">**Estimate Line**</span></span>
   - <span data-ttu-id="05b3a-122">**Projektaufgabe**</span><span class="sxs-lookup"><span data-stu-id="05b3a-122">**Project Task**</span></span>
   - <span data-ttu-id="05b3a-123">**Rechnungsposition**</span><span class="sxs-lookup"><span data-stu-id="05b3a-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="05b3a-124">**Erfassungsposition**</span><span class="sxs-lookup"><span data-stu-id="05b3a-124">**Journal Line**</span></span>
   - <span data-ttu-id="05b3a-125">**Projektvertragsposition**</span><span class="sxs-lookup"><span data-stu-id="05b3a-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="05b3a-126">**Projektteammitglied**</span><span class="sxs-lookup"><span data-stu-id="05b3a-126">**Project Team Member**</span></span>
   - <span data-ttu-id="05b3a-127">**Detailinformationen zur Angebotsposition**</span><span class="sxs-lookup"><span data-stu-id="05b3a-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="05b3a-128">**Rollenpreisaufschlag**</span><span class="sxs-lookup"><span data-stu-id="05b3a-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="05b3a-129">**Rollenpreis**</span><span class="sxs-lookup"><span data-stu-id="05b3a-129">**Role Price**</span></span>
   - <span data-ttu-id="05b3a-130">**Zeiteintrag**</span><span class="sxs-lookup"><span data-stu-id="05b3a-130">**Time Entry**</span></span>
 
   ![Hinzufügen vorhandener Entitäten zur Lösung für benutzerdefinierte Preisdimensionen](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="05b3a-132">Überprüfen Sie für jede Entität die hinzugefügten Komponenten und die endgültige Liste der Entitätsressourcen für jede Entität.</span><span class="sxs-lookup"><span data-stu-id="05b3a-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="05b3a-133">Beziehen Sie alle Formulare und Ansichten für jede der ausgewählten Entitäten ein.</span><span class="sxs-lookup"><span data-stu-id="05b3a-133">Include all forms and views for each of the selected entities.</span></span>

  ![Entitäten hinzugefügt](./media/solution-component-selection.png)


5.  <span data-ttu-id="05b3a-135">Wenn Sie aufgefordert werden, abhängige Entitäten für die ausgewählten Entitäten einzuschließen, wählen Sie **Nein, erforderliche Komponenten nicht einschließen.**</span><span class="sxs-lookup"><span data-stu-id="05b3a-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Einschließlich abhängiger Einheiten](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]