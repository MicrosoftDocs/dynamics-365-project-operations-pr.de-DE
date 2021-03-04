---
title: Fakturierbare Nutzung für Ressourcen anzeigen
description: Dieses Thema enthält Informationen zur Ressourcennutzungsansicht.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 4516c562e7eaf35c5fef638183967eef5a033b11
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146392"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="3d3fc-103">Fakturierbare Nutzung für Ressourcen anzeigen</span><span class="sxs-lookup"><span data-stu-id="3d3fc-103">View chargeable utilization for resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]
 
<span data-ttu-id="3d3fc-104">In der **Nutzungsansicht** auf der Seite **Project Service Ressourcennutzung** wird die fakturierbare Nutzung für jede buchbare Ressource angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="3d3fc-105">Da die Ansicht auf der Zeitplanübersicht basiert, sehen Sie viele der gleichen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Screenshot der Nutzungsansicht](media/FAQ-utilization-1.png)
 

<span data-ttu-id="3d3fc-107">Anrechenbare Nutzungsberechnungsverwendung funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3d3fc-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="3d3fc-108">Fakturierbare Nutzung = (Fakturierbare tatsächliche Stunden) / (Ressourcenkapazität)</span><span class="sxs-lookup"><span data-stu-id="3d3fc-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="3d3fc-109">Die Zellen repräsentieren die berechnete fakturierbare Nutzung für den ausgewählten Zeitraum (Tage, Wochen oder Monate).</span><span class="sxs-lookup"><span data-stu-id="3d3fc-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="3d3fc-110">Die Farben in jeder Zelle zeigen die fakturierbare Nutzung für eine Ressource verglichen mit der Zielvorgabe der fakturierbaren Nutzung an.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="3d3fc-111">Die Zielnutzung kann auf die Standardrolle der Ressource oder auf die einzelne Ressource selbst festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="3d3fc-112">Bei der Berechnung wird zuerst die Person für das Ziel und dann die Standardrolle der Ressource betrachtet.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="3d3fc-113">Festlegen des Ziels für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="3d3fc-113">Set target on a resource</span></span>

1. <span data-ttu-id="3d3fc-114">Navigieren Sie zu **Ressourcen** \> **Ressourcen**.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="3d3fc-115">Wählen Sie eine Ressource aus, um den Datensatz zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="3d3fc-116">Auf der Registerkarte **Project Service** können Sie die Zielnutzung der Ressource festlegen.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Screenshot der Verwendung der Project Service Registerkarte, um die Zielnutzung festzulegen](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="3d3fc-118">Festlegen der Zielnutzung für eine Rolle</span><span class="sxs-lookup"><span data-stu-id="3d3fc-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="3d3fc-119">Wechseln Sie zu **Ressourcen** \> **Ressourcenrollen**.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="3d3fc-120">Wählen Sie eine Rolle aus und öffnen Sie den Datensatz.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="3d3fc-121">Prozentsatz der Zielnutzung für die Rolle festlegen.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-121">Set the target utilization for the role.</span></span>

> ![Screenshot der Verwendung der Project Service Registerkarte, um die Zielnutzung festzulegen](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="3d3fc-123">Berechnen der fakturierbaren Nutzung für eine Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3d3fc-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="3d3fc-124">Um die fakturierbare Nutzung für eine Ressource zu berechnen, müssen Sie einige Voraussetzungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="3d3fc-125">Festlegen der Standardrolle für einzelne Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3d3fc-125">Set default role for individual resource</span></span>

<span data-ttu-id="3d3fc-126">Zunächst muss die Zielnutzung entweder für die einzelne Ressource oder für Ressourcenrollen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="3d3fc-127">Wenn Sie Ressourcenrollen für Ziele verwenden, muss jede einzelne Ressource eine Standardrolle haben.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="3d3fc-128">Wechseln Sie dazu zu **Ressourcen** \> **Ressourcen**.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="3d3fc-129">Wählen Sie eine Ressource aus, öffnen Sie den Datensatz, und wählen Sie dann die Registerkarte **Project Service** aus.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="3d3fc-130">Stellen Sie im Raster **Ressourcenrolle** sicher, dass es eine Rolle für die Ressource gibt und dass der Wert **Ist Standard** auf **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="3d3fc-131">Ändern des Rechnungstyps für die Ressourcenrolle</span><span class="sxs-lookup"><span data-stu-id="3d3fc-131">Change billing type for resource role</span></span>

<span data-ttu-id="3d3fc-132">Die Ressourcenrollen müssen festgelegt werden, damit ein Fakturierungstyp **Fakturierbar** verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="3d3fc-133">Wechseln Sie zu **Ressourcen** \> **Ressourcenrollen**.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="3d3fc-134">Öffnen Sie den Datensatz, den Sie aktualisieren möchten, und setzen Sie den Fakturierungstyp auf **Fakturierbar**.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="3d3fc-135">Festlegen der Arbeitsstunden für die Ressourcenrolle</span><span class="sxs-lookup"><span data-stu-id="3d3fc-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="3d3fc-136">Die Ressource muss Arbeitszeit haben für die Kapazitätsberechnung.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="3d3fc-137">Navigieren Sie zu **Ressourcen** \> **Ressourcen**.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="3d3fc-138">Wählen Sie eine Ressource aus, um den Datensatz zu öffnen, und wählen Sie dann **Arbeitsstunden anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="3d3fc-139">Sie können auf der Ressourcenliste ein Bulk-Update durchführen, indem Sie eine **Arbeitszeitvorlage** aus der Ansicht **Ressourcenliste** anwenden.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="3d3fc-140">Problembehandlung bei fakturierbaren tatsächlichen Stunden</span><span class="sxs-lookup"><span data-stu-id="3d3fc-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="3d3fc-141">Die fakturierbaren tatsächlichen Arbeitsstunden werden aus der Entität **Ist-Werte** erstellt.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="3d3fc-142">Ist-Werte mit dem Fakturierungstyp **Fakturierbar** werden in die Berechnung einbezogen. Aus diesem Grund müssen Projekte vorhanden sein, bei denen die Ist-Werte fakturierbar sind.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="3d3fc-143">Wenn Sie keine fakturierbare Nutzung finden, sind hier einige Dinge, die Sie überprüfen können:</span><span class="sxs-lookup"><span data-stu-id="3d3fc-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="3d3fc-144">Die Ressourcen mit Arbeitszeit, die für Kapazität definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="3d3fc-145">Die Ressource hat entweder einzelne definierte Nutzungsziele oder eine zugewiesene Standardrolle.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="3d3fc-146">Die Rolle verfügt über ein Nutzungsziel, das dafür definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="3d3fc-147">Ist-Werte weisen für den Zeitraum, für den Sie eine Nutzungsberechnung erwarten, den Fakturierungstyp **Fakturierbar** auf.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="3d3fc-148">Überprüfen Sie Folgendes, wenn Ist-Werte mit Fakturierungstypen anders als „fakturierbar” angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="3d3fc-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="3d3fc-149">Die Rolle, die für die Ist-Werte verwendet wird, hat einen Standardfakturierungstyp, der nicht anrechenbar ist.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="3d3fc-150">Die Rolle in der Projektvertragszeile, die das Projekt unterstützen, sind auf nicht verrechenbar festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="3d3fc-151">Das Projekt hat keine zugewiesenen Vertragszeilen.</span><span class="sxs-lookup"><span data-stu-id="3d3fc-151">The project does not have an associated contract line.</span></span>

