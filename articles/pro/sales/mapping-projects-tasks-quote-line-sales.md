---
title: Projekte und Aufgaben einer projektbasierten Angebotsposition zuordnen
description: Dieses Thema enthält Informationen zum Zuordnen von Projekten und Aufgaben zu einer projektbasierten Aufgabenposition.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d714304f408050babae1a6ba74268979e0b6ea4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272747"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="3475c-103">Projekte und Aufgaben einer projektbasierten Angebotsposition zuordnen</span><span class="sxs-lookup"><span data-stu-id="3475c-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="3475c-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="3475c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3475c-105">In projektbasierten Angebotspositionen können Sie die spezifischen Aufgaben eines Projekts zuordnen, die bereits einer Angebotsposition zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3475c-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="3475c-106">Wenn Sie Aufgaben einer Angebotsposition zuordnen, gelten die folgenden Elemente, die Sie in der Angebotsposition definiert haben, nur für diese Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="3475c-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="3475c-107">Fakturierungsmethode</span><span class="sxs-lookup"><span data-stu-id="3475c-107">Billing method</span></span>
- <span data-ttu-id="3475c-108">Fakturierbarkeitsoptionen</span><span class="sxs-lookup"><span data-stu-id="3475c-108">Chargeability options</span></span>
- <span data-ttu-id="3475c-109">Nicht zu überschreitende Grenzwerte</span><span class="sxs-lookup"><span data-stu-id="3475c-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="3475c-110">Kunden</span><span class="sxs-lookup"><span data-stu-id="3475c-110">Customers</span></span>

<span data-ttu-id="3475c-111">Beispielsweise könnten Sie ein Projekt haben, bei dem eine Phase der Festpreis ist und alle anderen Phasen Zeit und Material sind.</span><span class="sxs-lookup"><span data-stu-id="3475c-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="3475c-112">In diesem Fall können Sie die erste Phase und alle untergeordneten Aufgaben der Angebotsposition für diese Phase mit einer Festpreis-Abrechnungsmethode zuordnen.</span><span class="sxs-lookup"><span data-stu-id="3475c-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="3475c-113">Sie können dann alle anderen Phasen der zeit- und materialbasierten Angebotsposition zuordnen.</span><span class="sxs-lookup"><span data-stu-id="3475c-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="3475c-114">Aufgaben projektbasierten Aufgabenpositionen zuweisen</span><span class="sxs-lookup"><span data-stu-id="3475c-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="3475c-115">Sie können Aufgaben mit Angebotspositionen über folgende Stellen verknüpfen:</span><span class="sxs-lookup"><span data-stu-id="3475c-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="3475c-116">Seite **Projekt** Registerkarte > **Aufgabenfakturierung** (optimal)</span><span class="sxs-lookup"><span data-stu-id="3475c-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="3475c-117">Seite **Angebotszeile** Registerkarte > **Fakturierbare Aufgaben**</span><span class="sxs-lookup"><span data-stu-id="3475c-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="3475c-118">Über die Seite „Projekt“</span><span class="sxs-lookup"><span data-stu-id="3475c-118">From the Project page</span></span>

<span data-ttu-id="3475c-119">Die Seite **Projekt** bietet die optimale Erfahrung für die Zuordnung von Aufgaben zu Angebotspositionen.</span><span class="sxs-lookup"><span data-stu-id="3475c-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="3475c-120">Auf dieser Seite können Sie mehrere Aufgaben auswählen und alle sowie ihre untergeordneten Aufgaben der ausgewählten Angebotsposition zuordnen.</span><span class="sxs-lookup"><span data-stu-id="3475c-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="3475c-121">Überprüfen Sie auf der Registerkarte **Allgemein** einer projektbasierten Angebotsposition, ob das Feld **Projekt** ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="3475c-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="3475c-122">Wählen Sie im Feld **Eingeschlossene Aufgaben** die Option **Nur ausgewählte Aufgaben** aus.</span><span class="sxs-lookup"><span data-stu-id="3475c-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="3475c-123">Speichern Sie die projektbasierten Angebotspositionen.</span><span class="sxs-lookup"><span data-stu-id="3475c-123">Save the project-based quote line.</span></span> <span data-ttu-id="3475c-124">Wenn das Formular aktualisiert wird, wird die Registerkarte **Fakturierbare Aufgaben** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3475c-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="3475c-125">Wählen Sie auf der Registerkarte **Allgemein** den Link für das Projekt über das Feld **Projekt** aus.</span><span class="sxs-lookup"><span data-stu-id="3475c-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="3475c-126">Wählen Sie auf der Seite **Projekt** die Registerkarte **Aufgabenfakturierung** aus.</span><span class="sxs-lookup"><span data-stu-id="3475c-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="3475c-127">Wählen Sie im zweiten Raster, die sich auf die aufgabenspezifische Fakturierungseinrichtung bezieht, eine oder mehrere Aufgaben und dann **Angebotspositionen zuordnen** aus.</span><span class="sxs-lookup"><span data-stu-id="3475c-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="3475c-128">Wählen Sie auf der angezeigten Dialogseite eine Angebotsposition aus, in der projektbasierte Angebotspositionen im Angebot angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3475c-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="3475c-129">Geben Sie im Feld **Fakturierungstyp** an, ob diese Aufgaben kostenpflichtig oder nicht kostenpflichtig sind.</span><span class="sxs-lookup"><span data-stu-id="3475c-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="3475c-130">Aktivieren Sie das Kontrollkästchen, um anzugeben, ob die Zuordnung untergeordnete Aufgaben der ausgewählten Aufgaben enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="3475c-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="3475c-131">Durch Aktivieren des Kontrollkästchens werden die untergeordneten Aufgaben der ausgewählten Aufgaben der Angebotsposition zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3475c-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="3475c-132">Schließen Sie das Dialogfenster mit **OK**.</span><span class="sxs-lookup"><span data-stu-id="3475c-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="3475c-133">Über die Angebotspositionsseite</span><span class="sxs-lookup"><span data-stu-id="3475c-133">From the Quote line page</span></span>

<span data-ttu-id="3475c-134">Sie können über die Registerkarte **Fakturierbare Aufgaben** auf der Seite **Angebotsposition** Projektaufgaben zu Angebotspositionen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="3475c-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="3475c-135">Der optimale Ort, um Projektaufgaben zu Angebotspositionen zuzuordnen, befindet sich auf der Registerkarte **Aufgabenfakturierung** auf der Seite **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="3475c-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="3475c-136">Wenn Sie Aufgaben über die Registerkarte **Fakturierbare Aufgaben** auf der Seite **Angebotsposition** zuordnen, müssen Sie jedes Projekt manuell zuweisen.</span><span class="sxs-lookup"><span data-stu-id="3475c-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="3475c-137">Überprüfen Sie auf der Registerkarte **Allgemein** einer projektbasierten Angebotsposition, ob im Feld **Projekt** ein Projekt ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="3475c-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="3475c-138">Wählen Sie im Feld **Eingeschlossene Aufgaben** die Option **Nur ausgewählte Aufgaben** aus.</span><span class="sxs-lookup"><span data-stu-id="3475c-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="3475c-139">Speichern Sie die projektbasierten Angebotspositionen.</span><span class="sxs-lookup"><span data-stu-id="3475c-139">Save the project-based quote line.</span></span> <span data-ttu-id="3475c-140">Wenn das Formular aktualisiert wird, wird die Registerkarte **Fakturierbare Aufgaben** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3475c-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="3475c-141">Wählen Sie auf der Registerkarte **Fakturierbare Aufgaben** die Option **Projektangebotszeile hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="3475c-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="3475c-142">Wählen Sie auf der Seite **Angebotszeilenaufgabe** im Feld **Aufgaben** die Aufgabe und im Feld **Fakturierungstyp** die Option **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="3475c-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="3475c-143">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3475c-143">Close the page.</span></span> <span data-ttu-id="3475c-144">Die ausgewählte Aufgabe ist jetzt der Angebotsposition zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3475c-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="3475c-145">Aufgaben von projektbasierten Aufgabenpositionen trennen</span><span class="sxs-lookup"><span data-stu-id="3475c-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="3475c-146">Über die Seite „Projekt“</span><span class="sxs-lookup"><span data-stu-id="3475c-146">From the Project page</span></span>

<span data-ttu-id="3475c-147">Diese Methode beitet die optimale Erfahrung zum Trennen von Aufgaben aus Angebotspositionen.</span><span class="sxs-lookup"><span data-stu-id="3475c-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="3475c-148">Sie können mehrere Aufgaben auswählen und alle sowie ihre untergeordneten Aufgaben aus der ausgewählten Angebotsposition trennen.</span><span class="sxs-lookup"><span data-stu-id="3475c-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="3475c-149">Wählen Sie auf der Registerkarte **Allgemein** einer projektbasierten Angebotsposition im Feld **Projekt** den Projektlink aus.</span><span class="sxs-lookup"><span data-stu-id="3475c-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="3475c-150">Wählen Sie auf der Seite **Projekt** die Registerkarte **Aufgabenfakturierung** aus.</span><span class="sxs-lookup"><span data-stu-id="3475c-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="3475c-151">Wählen Sie im zweiten Raster, das sich auf die aufgabenspezifische Fakturierungseinrichtung bezieht, eine oder mehrere Aufgaben und dann **Angebotspositionen trennen** aus.</span><span class="sxs-lookup"><span data-stu-id="3475c-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="3475c-152">Wählen Sie auf der angezeigten Dialogseite eine Angebotsposition aus.</span><span class="sxs-lookup"><span data-stu-id="3475c-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="3475c-153">Aktivieren Sie das Kontrollkästchen, um anzugeben, ob die Zuordnung auch aus den untergeordneten Aufgaben der ausgewählten Aufgaben entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3475c-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="3475c-154">Durch Aktivieren des Kontrollkästchens werden auch die untergeordneten Aufgaben der ausgewählten Aufgaben von der Angebotsposition getrennt.</span><span class="sxs-lookup"><span data-stu-id="3475c-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="3475c-155">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="3475c-155">Select **OK**.</span></span> <span data-ttu-id="3475c-156">Eine Warnmeldung informiert Sie darüber, dass beim Entfernen dieser Zuordnung alle zuvor für die Aufgabe aufgezeichneten Istwerte rückgängig gemacht werden können.</span><span class="sxs-lookup"><span data-stu-id="3475c-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="3475c-157">Wählen Sie **OK** aus, um fortzufahren, und die Zuordnung zwischen der Aufgabe und der projektbasierten Angebotsposition zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="3475c-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="3475c-158">Über die Angebotspositionsseite</span><span class="sxs-lookup"><span data-stu-id="3475c-158">From the Quote line page</span></span>

<span data-ttu-id="3475c-159">Sie können Projektaufgaben auch über die Registerkarte **Fakturierbare Aufgaben** auf der Seite **Angebotsposition** trennen.</span><span class="sxs-lookup"><span data-stu-id="3475c-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="3475c-160">Wählen Sie auf der Registerkarte **Fakturierbare Aufgaben** die Option **Projektangebotszeile löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="3475c-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="3475c-161">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="3475c-161">Select **OK**.</span></span> <span data-ttu-id="3475c-162">Eine Warnmeldung informiert Sie darüber, dass beim Entfernen dieser Zuordnung alle zuvor für die Aufgabe aufgezeichneten Istwerte rückgängig gemacht werden können.</span><span class="sxs-lookup"><span data-stu-id="3475c-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="3475c-163">Wählen Sie **OK** aus, um fortzufahren, und die Zuordnung zwischen der Aufgabe und der projektbasierten Angebotsposition zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="3475c-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="3475c-164">Durch diesen Vorgang wird die Aufgabe nicht aus dem Projekt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3475c-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="3475c-165">Es wird nur die Aufgabenzuordnung aus der projektbasierten Angebotsposition entfernt.</span><span class="sxs-lookup"><span data-stu-id="3475c-165">It only removes the task association from the project-based quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]