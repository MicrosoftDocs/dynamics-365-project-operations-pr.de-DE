---
title: Schätzungen
description: Dieses Thema enthält Informationen zu Vorkalkulationen in Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e21511f78d92ff672e462f63f0dd0d098578516a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076726"
---
# <a name="estimates"></a><span data-ttu-id="0ca2b-103">Schätzungen</span><span class="sxs-lookup"><span data-stu-id="0ca2b-103">Estimates</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0ca2b-104">In einem projektbasierten Angebot können Sie die Entität „Detail zur Angebotsposition” verwenden, um die für die Lieferung eines Projekts erforderliche Arbeit abzuschätzen.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-104">On a project-based quote, you can use the Quote line detail entity to estimate the work that is required to deliver a project.</span></span> <span data-ttu-id="0ca2b-105">Sie können diese Schätzung anschließend mit dem Kunden teilen.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-105">You can then share that estimate with the customer.</span></span>

<span data-ttu-id="0ca2b-106">Projektbasierte Angebotszeilen müssen keine Detailinformationen zur Angebotsposition enthalten.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-106">Project-based quote lines don't have to have any quote line details.</span></span> <span data-ttu-id="0ca2b-107">Alternativ können sie viele Angebotspositionsdetails haben.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-107">Alternatively, they can have many quote line details.</span></span> <span data-ttu-id="0ca2b-108">Angebotspositionsdetails werden verwendet, um Zeit, Ausgaben oder Gebühren zu schätzen.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-108">Quote line details are used to estimate time, expenses, or fees.</span></span> <span data-ttu-id="0ca2b-109">PSA lässt keine Materialschätzungen für Angebotspositionsdetails zu.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-109">PSA doesn't allow for material estimates on quote line details.</span></span> <span data-ttu-id="0ca2b-110">Diese werden als Transaktionsklassen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-110">These are called transaction classes.</span></span> <span data-ttu-id="0ca2b-111">Geschätzte Steuerbeträge können ebenfalls für eine Transaktionsklasse eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-111">Estimated tax amounts can also be entered on a transaction class.</span></span>

<span data-ttu-id="0ca2b-112">Zusätzlich zu den Transaktionsklassen enthalten Angebotspositionsdetails einen Transaktionstyp.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-112">In addition to transaction classes, quote line details have a transaction type.</span></span> <span data-ttu-id="0ca2b-113">PSA unterstützt zwei Transaktionstypen für Angebotspositionsdetails: **Kosten** und **Projektvertrag**.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-113">PSA support two transaction types for quote line details: **Cost** and **Project Contract**.</span></span>

## <a name="estimate-by-using-a-contract"></a><span data-ttu-id="0ca2b-114">Schätzung mithilfe eines Vertrags</span><span class="sxs-lookup"><span data-stu-id="0ca2b-114">Estimate by using a contract</span></span>

<span data-ttu-id="0ca2b-115">Wenn Sie beim Erstellen eines projektbasierten Vertrags ein PSA-Angebot verwendet haben, wird die Schätzung, die Sie im Angebot für jede Angebotsposition vorgenommen haben, in den Projektvertrag kopiert.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-115">If you used a PSA quote when you created a project-based contract, the estimate that you did for each quote line on the quote is copied to the project contract.</span></span> <span data-ttu-id="0ca2b-116">Die Struktur eines Projektvertrags ähnelt der Struktur eines Projektangebots mit Positionen, Positionsdetails und Rechnungszeitplänen.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-116">The structure of a project contract is like the structure of project quote that has lines, line details, and invoice schedules.</span></span>

<span data-ttu-id="0ca2b-117">Schätzungen können direkt in einem Projektvertrag wie in einem Projektangebot vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-117">Estimates can be done directly in a project contract, as in a project quote.</span></span> <span data-ttu-id="0ca2b-118">Bei einem Projektangebot wird die Schätzung unter Verwendung der Vertragspositionen und Vertragspositionsdetails vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-118">For a project quotation, the estimate is done by using contract lines and contract line details.</span></span> <span data-ttu-id="0ca2b-119">Vertragspositionsdetails können auch aus einem Projektplan erstellt wurden, der mithilfe des Bottom-up-Schätzungsansatzes erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-119">Contract line details can also be generated from a project plan that was created by using the bottom-up estimate approach.</span></span>

<span data-ttu-id="0ca2b-120">Vertragspositionsdetails können zur Schätzung von Zeit, Ausgaben oder Gebühren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-120">Contract line details can be used to estimate time, expenses, or fees.</span></span> <span data-ttu-id="0ca2b-121">Geschätzte Steuerbeträge können ebenfalls bei den Vertragszeilendetails eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-121">Estimated tax amounts can also be entered on a contract line detail.</span></span>

<span data-ttu-id="0ca2b-122">PSA lässt keine Materialschätzungen für Vertragszeilendetails zu.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-122">PSA doesn't allow for material estimates on contract line details.</span></span>

<span data-ttu-id="0ca2b-123">Die Prozesse, die bei einem Projektvertrag unterstützt werden sind Rechnungserstellung und -bestätigung.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-123">The processes that are supported on a project contract are invoice creation and confirmation.</span></span> <span data-ttu-id="0ca2b-124">Rechnungserstellung erstellt einen Entwurf einer projektbasierten Rechnung, die alle nicht fakturierten vertrieblichen Ist-Werte bis zum aktuellen Datum enthält.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-124">Invoice creation creates a draft of a project-based invoice that includes all unbilled sales actuals until the current date.</span></span>

<span data-ttu-id="0ca2b-125">Durch die Bestätigung wird der Vertrag schreibgeschützt und der Status von **Entwurf** in **Bestätigt** geändert.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-125">Confirmation makes the contract read-only and changes its status from **Draft** to **Confirmed**.</span></span> <span data-ttu-id="0ca2b-126">Nachdem Sie diese Aktion ausgeführt haben, können Sie sie nicht mehr rückgängig machen.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-126">After you take this action, you can't undo it.</span></span> <span data-ttu-id="0ca2b-127">Da es sich bei dieser Aktion um eine permanente Aktion handelt, empfiehlt es sich, den Vertrag im Status **Entwurf** zu belassen.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-127">Because this action is permanent, it's a best practice to keep the contract in a **Draft** status.</span></span>

<span data-ttu-id="0ca2b-128">Die einzigen Unterschiede zwischen Vertragsentwürfen und bestätigten Verträgen sind ihr Status und die Tatsache, dass Vertragsentwürfe bearbeitet werden können, bestätigte Verträge hingegen nicht.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-128">The only differences between draft contracts and confirmed contracts are their status and the fact that draft contracts can be edited whereas confirmed contracts can't.</span></span> <span data-ttu-id="0ca2b-129">Die Rechnungserstellung sowie die Nachverfolgung von Ist-Werten kann sowohl bei Vertragsentwürfen als auch bei bestätigten Verträgen erfolgen.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-129">Invoice creation and tracking actuals can be done on both draft contracts and confirmed contracts.</span></span>

<span data-ttu-id="0ca2b-130">PSA unterstützt keine Änderungsaufträge bei Verträgen bzw. Projekten.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-130">PSA doesn't support change orders on contracts or projects.</span></span>

## <a name="estimating-projects"></a><span data-ttu-id="0ca2b-131">Einschätzen von Projekten</span><span class="sxs-lookup"><span data-stu-id="0ca2b-131">Estimating projects</span></span>

<span data-ttu-id="0ca2b-132">Sie können Zeit und Ausgaben für Projekte schätzen.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-132">You can estimate time and expenses on projects.</span></span> <span data-ttu-id="0ca2b-133">PSA lässt keine Material- bzw. Gebührenschätzungen für Projekte zu.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-133">PSA doesn't allow for estimates of materials or fees on projects.</span></span>

<span data-ttu-id="0ca2b-134">Zeitschätzungen werden generiert, wenn Sie eine Aufgabe erstellen und die Attribute einer allgemeinen Ressource identifizieren, die zur Ausführung der Aufgabe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-134">Time estimates are generated when you create a task and identify the attributes of a generic resource that is required to perform the task.</span></span> <span data-ttu-id="0ca2b-135">Zeitschätzungen werden aus Zeitplanaufgaben generiert.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-135">Time estimates are generated from schedule tasks.</span></span> <span data-ttu-id="0ca2b-136">Zeitschätzungen werden nicht erstellt, wenn Sie allgemeine Teammitglieder außerhalb des Zeitplans erstellen.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-136">Time estimates aren't created if you create generic team members outside the context of the schedule.</span></span>

<span data-ttu-id="0ca2b-137">Ausgabenschätzungen werden in das Raster auf der Seite **Schätzungen** eingegeben.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-137">Expense estimates are entered in the grid on the **Estimates** page.</span></span>

## <a name="understanding-estimation"></a><span data-ttu-id="0ca2b-138">Grundlegendes zur Vorkalkulation</span><span class="sxs-lookup"><span data-stu-id="0ca2b-138">Understanding estimation</span></span>

<span data-ttu-id="0ca2b-139">Verwenden Sie die folgende Tabelle als Leitfaden zum Verständnis der Geschäftslogik in der Vorkalkulationsphase.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-139">Use the following table as a guide for understanding the business logic in the estimation phase.</span></span>

| <span data-ttu-id="0ca2b-140">Szenario</span><span class="sxs-lookup"><span data-stu-id="0ca2b-140">Scenario</span></span>                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="0ca2b-141">Entitätsdatensatz</span><span class="sxs-lookup"><span data-stu-id="0ca2b-141">Entity record</span></span>                                                                                                                                                                                                       | <span data-ttu-id="0ca2b-142">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="0ca2b-142">Transaction Type</span></span> | <span data-ttu-id="0ca2b-143">Transaktionsklasse</span><span class="sxs-lookup"><span data-stu-id="0ca2b-143">Transaction Class</span></span> | <span data-ttu-id="0ca2b-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0ca2b-144">Additional information</span></span>                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0ca2b-145">Wenn Sie den Umsatzwert der Zeit für ein Angebot schätzen müssen</span><span class="sxs-lookup"><span data-stu-id="0ca2b-145">When you need to estimate the sales value of time on a quote</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="0ca2b-146">Datensatz „Detail zur Angebotsposition” (QLD, Quote Line Detail) wird erstellt</span><span class="sxs-lookup"><span data-stu-id="0ca2b-146">Quote line detail (QLD) record is created</span></span>                                                                                                                                                                               | <span data-ttu-id="0ca2b-147">Projektvertrag</span><span class="sxs-lookup"><span data-stu-id="0ca2b-147">Project contract</span></span> | <span data-ttu-id="0ca2b-148">Time</span><span class="sxs-lookup"><span data-stu-id="0ca2b-148">Time</span></span>        | <span data-ttu-id="0ca2b-149">Das Feld „Transaktionsursprung” in der Zeile „QLD” auf der Verkaufsseite verweist auf die QLD auf der Kostenseite</span><span class="sxs-lookup"><span data-stu-id="0ca2b-149">Transaction origin field on the sales side QLD row references the Cost side QLD</span></span> |
|                                                                                                                                                                                                                                                                                     | <span data-ttu-id="0ca2b-150">Ein zweiter QLD-Datensatz wird vom System erstellt, um die entsprechenden Kostenwerte zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-150">A second QLD record is created by the system to store the corresponding cost values.</span></span> <span data-ttu-id="0ca2b-151">Das System kopiert sämtliche Nicht-Geld-Felder aus der Umsatz-QLD in die Kosten-QLD.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-151">All non-money fields are copied from the sales QLD to the Cost QLD by the system.</span></span>                                                                                                                                                                               | <span data-ttu-id="0ca2b-152">Kosten</span><span class="sxs-lookup"><span data-stu-id="0ca2b-152">Cost</span></span> | <span data-ttu-id="0ca2b-153">Time</span><span class="sxs-lookup"><span data-stu-id="0ca2b-153">Time</span></span>        | <span data-ttu-id="0ca2b-154">Das Feld „Transaktionsursprung” in der Zeile „Angebotspositionsdetails” (QLD) auf der Verkaufsseite verweist auf die QLD auf der Kostenseite</span><span class="sxs-lookup"><span data-stu-id="0ca2b-154">Transaction origin field on the sales side quote line detail (QLD) row references the Cost side QLD</span></span> |
| <span data-ttu-id="0ca2b-155">Wenn Sie den Umsatzwert der Zeit für einen Vertrag schätzen müssen</span><span class="sxs-lookup"><span data-stu-id="0ca2b-155">When you need to estimate the sales value of time on a contract</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="0ca2b-156">Datensatz „Projektvertragsposition” (CLD, Contract Line Detail) wird erstellt</span><span class="sxs-lookup"><span data-stu-id="0ca2b-156">Project contract line detail (CLD) record is created</span></span>                                                                                                                                                                    | <span data-ttu-id="0ca2b-157">Projektvertrag</span><span class="sxs-lookup"><span data-stu-id="0ca2b-157">Project Contract</span></span> | <span data-ttu-id="0ca2b-158">Time</span><span class="sxs-lookup"><span data-stu-id="0ca2b-158">Time</span></span>        | <span data-ttu-id="0ca2b-159">Das Feld „Transaktionsursprung” in der Zeile „CLD” auf der Verkaufsseite verweist auf die CLD auf der Kostenseite</span><span class="sxs-lookup"><span data-stu-id="0ca2b-159">Transaction origin field on the sales side CLD row references the cost CLD</span></span>      |
|                                                                                                                                                                                                                                                                                  | <span data-ttu-id="0ca2b-160">Ein zweiter CLD-Datensatz wird vom System erstellt, um die entsprechenden Kostenwerte zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-160">A second CLD record is created by the system to store the corresponding cost values.</span></span> <span data-ttu-id="0ca2b-161">Das System kopiert sämtliche Nicht-Geld-Felder aus der Umsatz-CLD in die Kosten-CLD.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-161">All non-money fields are copied from the sales CLD to the cost CLD by the system.</span></span>                                                                                                                                                                    | <span data-ttu-id="0ca2b-162">Kosten</span><span class="sxs-lookup"><span data-stu-id="0ca2b-162">Cost</span></span> | <span data-ttu-id="0ca2b-163">Time</span><span class="sxs-lookup"><span data-stu-id="0ca2b-163">Time</span></span>        | <span data-ttu-id="0ca2b-164">Das Feld „Transaktionsursprung” in der Zeile „CLD” auf der Verkaufsseite verweist auf die CLD auf der Kostenseite</span><span class="sxs-lookup"><span data-stu-id="0ca2b-164">Transaction origin field on the sales side CLD row references the cost CLD</span></span>      |
| <span data-ttu-id="0ca2b-165">Wenn der Benutzer eine Ressource für eine Projektaufgabe beschreibt</span><span class="sxs-lookup"><span data-stu-id="0ca2b-165">When the user describes a resource on a project task</span></span>                                                                                                                                                                                                                                                                                            | <span data-ttu-id="0ca2b-166">Der Datensatz „Schätzungszeile” zeigt, dass der Umsatzwert der Aufgabe beim Erstellen einer Aufgabe mit allen erforderlichen Preisdimensionen generiert wird.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-166">Estimate line record to show the sales value of the task is created when a task is created with all required pricing dimensions.</span></span> <span data-ttu-id="0ca2b-167">Rolle und Organisationseinheiten sind die Preisdimensionen von OOB Project Service</span><span class="sxs-lookup"><span data-stu-id="0ca2b-167">Role and organizational units are the OOB Project Service pricing dimensions</span></span> | <span data-ttu-id="0ca2b-168">Projektvertrag</span><span class="sxs-lookup"><span data-stu-id="0ca2b-168">Project Contract</span></span> | <span data-ttu-id="0ca2b-169">Time</span><span class="sxs-lookup"><span data-stu-id="0ca2b-169">Time</span></span>        |                                                                                   |
|     | <span data-ttu-id="0ca2b-170">Der Datensatz „Schätzungszeile” zeigt, dass der Kostenwert der Aufgabe beim Erstellen einer Aufgabe mit allen erforderlichen Preisdimensionen generiert wird.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-170">The estimate line record to show the cost value of the task is created when a task is created with all required pricing dimensions.</span></span> <span data-ttu-id="0ca2b-171">Das System kopiert sämtliche Nicht-Geld-Felder aus der Vertriebsvorkalkulationsposition in die Kostenvorkalkulationsposition.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-171">All non-money fields are copied from the sales estimate line to the cost estimate line by the system.</span></span> <span data-ttu-id="0ca2b-172">Rolle und Organisationseinheit sind die OOB PSA Preisdimensionen sowohl für Kosten als auch für Rechnungssätze.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-172">Role and organizational unit are the OOB PSA pricing dimensions for both cost and bill rates.</span></span>                                                                                                                                                                                                                | <span data-ttu-id="0ca2b-173">Kosten</span><span class="sxs-lookup"><span data-stu-id="0ca2b-173">Cost</span></span>             | <span data-ttu-id="0ca2b-174">Zeit</span><span class="sxs-lookup"><span data-stu-id="0ca2b-174">Time</span></span>           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a><span data-ttu-id="0ca2b-175">Anpassen der Entitäten „Detail zur Angebotsposition” und „Detail zur Vertragszeile”</span><span class="sxs-lookup"><span data-stu-id="0ca2b-175">Customizing the Quote line detail and Contract line detail entities</span></span>

<span data-ttu-id="0ca2b-176">Verwenden Sie die Plug-In-Registrierungswerkzeuge PreOperationContractLineDetailUpdate und PreOperationQuoteLineDetailUpdate, wenn Sie den Angebotspositionsdetails ein benutzerdefiniertes Feld hinzugefügt haben und möchten, dass das System den Wert des Felds als Standardwert für die von ihm erstellte zugehörige Kostenposition eingibt.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-176">If you added a custom field on the quote line detail and want the system to enter the value of the field as a default value on the related cost line that it creates, use the PreOperationContractLineDetailUpdate and PreOperationQuoteLineDetailUpdate plug-in registration tools.</span></span> <span data-ttu-id="0ca2b-177">Diese Plug-Ins müssen erneut registriert werden, nachdem das Angebotspositionsdetail oder das Vertragspositionsdetail geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-177">These plug-ins must be re-registered after the quote line detail or the contract line detail is changed.</span></span> <span data-ttu-id="0ca2b-178">Befolgen Sie diese Schritte, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-178">Follow these steps to complete the process.</span></span>

1. <span data-ttu-id="0ca2b-179">Öffnen Sie PluginRegistrationTool, und stellen Sie eine Verbindung mit Ihrer Online-Instanz her.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-179">Open PluginRegistrationTool, and connect to your online instance.</span></span>
2. <span data-ttu-id="0ca2b-180">Wählen Sie **Suchen** aus und suchen Sie nach dem zu aktualisierenden Plug-In.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-180">Select **Search** , and search for the plug-in to update.</span></span>

    ![Dialogfeld „Suchstruktur”](media/basic-guide-19.png)

3. <span data-ttu-id="0ca2b-182">Wählen Sie das Plug-In aus und wählen Sie dann auf der Hauptseite **Auswählen** aus.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-182">Select the plug-in, and then, on the main page, select **Select**.</span></span>
4. <span data-ttu-id="0ca2b-183">Wählen Sie den Schritt des zu aktualisierenden Plug-Ins aus, klicken Sie mit der rechten Maustaste, und wählen Sie dann **Aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-183">Select the step of the plug-in to update, right-click, and then select **Update**.</span></span>

    ![Auswählen eines Schritts im Plug-In](media/basic-guide-20.png)

5. <span data-ttu-id="0ca2b-185">Wählen Sie im Dialogfeld **Vorhandenen Schritt aktualisieren** im Feld **Filterattribute** die Schaltfläche mit den Auslassungspunkten ( **...** ) aus:</span><span class="sxs-lookup"><span data-stu-id="0ca2b-185">In the **Update Existing Step** dialog box, in the **Filtering Attributes** field, select the ellipsis button ( **...** ):</span></span>
 
    ![Dialogfeld „Vorhandenen Schritt aktualisieren”](media/basic-guide-21.png)

6. <span data-ttu-id="0ca2b-187">Aktivieren Sie im Dialogfeld **Attribute auswählen** Kontrollkästchen für benutzerdefinierte Attribute.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-187">In the **Select Attributes** dialog box, select check boxes for custom attributes.</span></span>

    ![Dialogfeld „Attribute auswählen”](media/basic-guide-22.png)

7. <span data-ttu-id="0ca2b-189">Wählen Sie **OK** aus, um das Dialogfeld zu schließen, und wählen Sie dann **Schritt aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-189">Select **OK** to close the dialog box, and then select **Update Step**.</span></span>
 
    ![Schaltfläche „Schritt aktualisieren”](media/basic-guide-23.png)

8. <span data-ttu-id="0ca2b-191">Wiederholen Sie die Schritte 1 bis 7 für das zweite Plug-In.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-191">Repeat steps 1 through 7 for the second plug-in.</span></span>
9. <span data-ttu-id="0ca2b-192">Schließen Sie das PluginRegistrationTool.</span><span class="sxs-lookup"><span data-stu-id="0ca2b-192">Close the PluginRegistrationTool.</span></span>