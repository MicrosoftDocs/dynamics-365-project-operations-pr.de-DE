---
title: Schätzen Sie den Projektumsatz und die Projektkosten, wenn eine buchbare Ressource mehrere Rollen in einem Projekt ausfüllt
description: Dieses Thema enthält Informationen darüber, wie Preisdimensionen verwendet werden können, um die Preisgestaltung und Kostenberechnung für eine Ressource zu unterstützen, die mehrere Rollen in einem Projekt ausfüllt.
author: rumant
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
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076576"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="8fc1e-103">Schätzen Sie den Projektumsatz und die Projektkosten, wenn eine buchbare Ressource mehrere Rollen in einem Projekt ausfüllt</span><span class="sxs-lookup"><span data-stu-id="8fc1e-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="8fc1e-104">Projektbasierte Unternehmen benötigen häufig eine Ressource, um mehrere Rollen in einem Projekt zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="8fc1e-105">Jede dieser Rollen kann unterschiedlich bewertet und kostenpflichtig sein, was bedeutet, dass die Zeit derselben Ressource für das Projekt abhängig von der Rechnung und den Kostensätzen für jede der Rollen eine andere finanzielle Schätzung erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="8fc1e-106">Project Service Automation ermöglicht die Einrichtung der Werte im Teammitgliedsdatensatz für die benannte Ressource und unterschiedliche Überschreibungen für jede der Aufgaben, denen das Teammitglied zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="8fc1e-107">Im folgenden Beispiel wird erläutert, wie durch die einfache Überschreibung dieses Werts eine Ressource mehrere Rollen in einem Projekt mit unterschiedlichen Kosten und Abrechnungssätzen haben kann.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="8fc1e-108">Aufgaben erstellen</span><span class="sxs-lookup"><span data-stu-id="8fc1e-108">Create tasks</span></span>
<span data-ttu-id="8fc1e-109">Erstellen Sie zwei Projektaufgaben für jeweils 40 Stunden, Aufgabe A und Aufgabe B. Wählen Sie Aufgabe A als Vorgänger von Aufgabe B aus.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="8fc1e-110">Richten Sie die Rollen- und Organisationseinheit für ein generisches Projektteammitglied ein</span><span class="sxs-lookup"><span data-stu-id="8fc1e-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="8fc1e-111">Auf der Seite **Zeitplan** wählen Sie die Zeile **Aufgabe** für Aufgabe A.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="8fc1e-112">Wählen Sie im Feld **Ressourcen** in der Dropdownliste **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="8fc1e-113">Geben Sie auf der Seite **Schnellerfassung: Teammitglied** die Attribute des generischen Teammitglieds an, das diese Aufgabe ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="8fc1e-114">Wählen Sie die entsprechende Rolle und Organisationseinheit aus, und wählen Sie dann **Speichern und schließen**.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="8fc1e-115">Ein generisches Teammitglied wird erstellt und dieser Aufgabe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="8fc1e-116">Wiederholen Sie diese Schritte für Aufgabe B und stellen Sie sicher, dass sich die Rolle und Organisationseinheit des für Aufgabe B erstellten generischen Teammitglieds von Aufgabe A unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="8fc1e-117">Richten Sie die Rollen- und Organisationseinheit für eine Projektaufgabe ein</span><span class="sxs-lookup"><span data-stu-id="8fc1e-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="8fc1e-118">Nachdem Sie Aufgabe A erstellt haben, wählen Sie die Aufgabe aus, und wählen Sie dann **Aufgabe bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="8fc1e-119">Suchen Sie auf der Seite **Aufgabendetails** die **Rolle** und **Organisationseinheit** , und fügen Sie in den Feldern die Werte hinzu, die für eine Ressource erforderlich sind, die diese Aufgabe ausführen würde.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="8fc1e-120">Wenn Sie diese Szenarien mit Project Service Automation-Demodaten abschließen, wählen Sie **Beratungs-Lead** für die Rolle und **Fabrikam USA** als Organisationseinheit.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="8fc1e-121">Wählen Sie Aufgabe B aus, und wählen Sie dann **Aufgabe bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="8fc1e-122">Suchen Sie auf der Seite **Aufgabendetails** die **Rolle** und **Organisationseinheit** , und fügen Sie in den Feldern die Werte hinzu, die für eine Ressource erforderlich sind, die diese Aufgabe ausführen würde.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="8fc1e-123">Stellen Sie sicher, dass die Werte in den Feldern **Rolle** und **Organisationseinheit** für Aufgabe B sich von denen für Aufgabe A unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="8fc1e-124">Wenn Sie diese Szenarien mit Project Service Automation-Demodaten abschließen, wählen Sie **Netzwerktechniker** für die Rolle und **Fabrikam USA** als Organisationseinheit.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="8fc1e-125">Wählen Sie auf der Seite **Aufgabendetails** „Speichern und schließen“ aus.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="8fc1e-126">Teammitglied und geschätztes Verhalten</span><span class="sxs-lookup"><span data-stu-id="8fc1e-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="8fc1e-127">Wählen Sie auf der Seite **Aufgabendetails** unter **Teammitglied** die beiden allgemeinen Teammitglieder aus, und wählen Sie dann **Anforderungen generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="8fc1e-128">Dadurch werden Ressourcenanforderungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="8fc1e-129">Wählen Sie die Teammitgliedszeile für **Beratungs-Lead** und dann **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="8fc1e-130">Die Zeitplanübersicht wird geöffnet und eine Ressource für diese Anforderung wird gebucht.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="8fc1e-131">Wählen Sie die Teammitgliedszeile für **Netzwerktechniker** und dann **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="8fc1e-132">Die Zeitplanübersicht wird geöffnet und die gleiche Ressource für diese Anforderung wird gebucht.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="8fc1e-133">Teammitgliedsraster</span><span class="sxs-lookup"><span data-stu-id="8fc1e-133">Team Member grid</span></span> 
<span data-ttu-id="8fc1e-134">Im Raster **Teammitglied** sehen Sie, dass die beiden generischen Teammitgliedsdatensätze gelöscht wurden und durch eine Ressource ersetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="8fc1e-135">Für diese Ressource gibt es einen Wertesatz, für den ein Standardwertsatz für **Rolle** und **Organisationseinheit** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="8fc1e-136">Wenn Sie die Zeile dieses Teammitgliedsdatensatzes erweitern, werden im Teammitgliedsdatensatz für beide Aufgaben unterschiedliche Zuordnungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="8fc1e-137">Jede Zuweisungszeile hat aufgabenspezifische Werte für **Rolle** und **Organisationseinheit**.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="8fc1e-138">Vorkalkulationsraster</span><span class="sxs-lookup"><span data-stu-id="8fc1e-138">Estimates grid</span></span> 
<span data-ttu-id="8fc1e-139">Wenn Sie zum Raster **Schätzungen** navigieren, werden Sie feststellen, dass beide Zuweisungen für dieselbe Ressource unterschiedliche Preise haben.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="8fc1e-140">Die Zuordnung für die Ressource zu Aufgabe A erfolgt über den **Rolle** -Attributwert von **Beratungs-Lead**.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="8fc1e-141">Die Zuordnung für die gleiche Ressource zu Aufgabe B erfolgt über den **Rolle** -Attributwert von **Netzwerktechniker**.</span><span class="sxs-lookup"><span data-stu-id="8fc1e-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





