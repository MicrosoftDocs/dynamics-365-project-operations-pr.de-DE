---
title: Die fakturierbaren Komponenten einer Angebotszeile konfigurieren
description: Dieses Thema enthält Informationen zum Einrichten fakturierbarer und nicht fakturierbarer Komponenten in einer projektbasierten Angebotszeile.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076645"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="11610-103">Die fakturierbaren Komponenten einer Angebotszeile konfigurieren</span><span class="sxs-lookup"><span data-stu-id="11610-103">Configure the chargeable components of a quote line</span></span>

<span data-ttu-id="11610-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="11610-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="11610-105">Eine projektbasierte Angebotszeile umfasst das Konzept *enthaltener* Komponenten und *fakturierbarer* Komponenten.</span><span class="sxs-lookup"><span data-stu-id="11610-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="11610-106">Enthaltene Komponenten unterliegen Folgendem:</span><span class="sxs-lookup"><span data-stu-id="11610-106">Included components are subject to:</span></span>

  - <span data-ttu-id="11610-107">Fakturierungsmethode und Kundenaufteilung</span><span class="sxs-lookup"><span data-stu-id="11610-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="11610-108">Nicht zu überschreitende Grenzwerte</span><span class="sxs-lookup"><span data-stu-id="11610-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="11610-109">In der projektbasierten Angebotszeile definierte Einstellungen für die Rechnungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="11610-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="11610-110">Eine Teilmenge der eingeschlossenen Komponenten kann mit dem Feld **Fakturierungstyp** als fakturierbar markiert werden.</span><span class="sxs-lookup"><span data-stu-id="11610-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="11610-111">Das Feld **Fakturierungstyp** ist ein Optionssatz, der die folgenden Werte im Kontext einer Angebotszeile zulässt:</span><span class="sxs-lookup"><span data-stu-id="11610-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="11610-112">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-112">Chargeable</span></span>
  - <span data-ttu-id="11610-113">Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-113">Non-chargeable</span></span>

<span data-ttu-id="11610-114">Fakturierbare Komponenten können für die Kategorien Aufgaben, Rollen und Transaktionen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="11610-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="11610-115">Die Fakturierbarkeit wird für Aufgaben für eine Angebotszeile definiert und gilt für alle in dieser Zeile enthaltenen Transaktionsklassen.</span><span class="sxs-lookup"><span data-stu-id="11610-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="11610-116">Wenn das Feld **Aufgaben einschließen** auf **Gesamtes Projekt** festgelegt wurde oder leer ist, ist die Registerkarte **Fakturierbare Aufgaben** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="11610-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="11610-117">Die für Rollen für eine Angebotszeile festgelegte Fakturierbarkeit gilt nur für die Transaktionsklasse **Zeit**.</span><span class="sxs-lookup"><span data-stu-id="11610-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="11610-118">Wenn das Feld **Zeit einschließen** in einer Projektangebotszeile auf **Nein** festgelegt wurde, ist die Registerkarte **Fakturierbare Rollen** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="11610-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="11610-119">Die für Transaktionskategorien für eine Angebotszeile festgelegte Fakturierbarkeit gilt nur für die Transaktionsklasse **Ausgaben**.</span><span class="sxs-lookup"><span data-stu-id="11610-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="11610-120">Wenn das Feld **Ausgaben einschließen** in einer Projektangebotszeile auf **Nein** festgelegt wurde, ist die Registerkarte **Fakturierbare Kategorien** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="11610-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="11610-121">Eine Projektaufgabe als fakturierbar oder nicht fakturierbar aktualisieren</span><span class="sxs-lookup"><span data-stu-id="11610-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="11610-122">Eine Projektaufgabe kann im Kontext einer bestimmten projektbasierten Angebotszeile fakturierbar oder nicht fakturierbar sein, wodurch das folgende Setup möglich wird:</span><span class="sxs-lookup"><span data-stu-id="11610-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible:</span></span>

<span data-ttu-id="11610-123">Wenn eine projektbasierte Angebotszeile **Zeit** und die Aufgabe **T1** enthält, wird die Aufgabe der Angebotszeile als fakturierbar zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="11610-123">If a project-based quote line includes **Time** and the task **T1** , the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="11610-124">Wenn es eine zweite Angebotszeile gibt, die **Ausgaben** enthält, können Sie die **T1** -Aufgabe in der Angebotszeile als nicht fakturierbar zuordnen.</span><span class="sxs-lookup"><span data-stu-id="11610-124">If there is a second quote line that includes **Expenses** , you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="11610-125">Das Ergebnis ist, dass die gesamte für die Aufgabe aufgezeichnete Zeit fakturierbar ist und alle für die Aufgabe aufgezeichneten Ausgaben nicht fakturierbar sind.</span><span class="sxs-lookup"><span data-stu-id="11610-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="11610-126">Der Fakturierungstyp einer Aufgabe kann auf der Registerkarte **Fakturierbare Aufgaben** einer projektbasierten Angebotszeile durch Aktualisieren des Felds **Fakturierungstyp** im Unterraster **Angebotszeilenaufgaben** konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="11610-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** sub-grid.</span></span> <span data-ttu-id="11610-127">Alternativ können Sie den Fakturierungstyp für eine Projektaufgabe im Feld **Fakturierungstyp** im Unterraster der Einrichtung der Aufgabenfakturierung eines Projekts aktualisieren, in dem die einer Aufgabe zugeordneten Angebotszeilen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="11610-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the sub-grid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="11610-128">Eine Rolle als fakturierbar oder nicht fakturierbar aktualisieren</span><span class="sxs-lookup"><span data-stu-id="11610-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="11610-129">Eine Rolle kann im Kontext einer bestimmten projektbasierten Angebotszeile fakturierbar oder nicht fakturierbar sein.</span><span class="sxs-lookup"><span data-stu-id="11610-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="11610-130">Der Fakturierungstyp einer Aufgabe kann auf der Registerkarte **Fakturierbare Rollen** einer Angebotszeile durch Aktualisieren des Felds **Fakturierungstyp** im Unterraster **Fakturierbare Rollen** konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="11610-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** sub-grid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="11610-131">Eine Transaktionskategorie als fakturierbar oder nicht fakturierbar aktualisieren</span><span class="sxs-lookup"><span data-stu-id="11610-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="11610-132">Eine Transaktionskategorie kann für eine bestimmte Angebotszeile fakturierbar oder nicht fakturierbar sein.</span><span class="sxs-lookup"><span data-stu-id="11610-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="11610-133">Der Fakturierungstyp einer Transaktion kann auf der Registerkarte **Fakturierbare Kategorien** einer Angebotszeile durch Aktualisieren des Felds **Fakturierungstyp** im Unterraster **Fakturierbare Kategorien** konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="11610-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** sub-grid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="11610-134">Fakturierbarkeit abschließen</span><span class="sxs-lookup"><span data-stu-id="11610-134">Resolve chargeability</span></span>
<span data-ttu-id="11610-135">Eine für die Zeit erstellte Schätzung oder tatsächliche Schätzung wird nur dann als fakturierbar angesehen, wenn **Zeit** in der Angebotszeile enthalten ist und **Aufgabe** und **Rolle** in der Angebotszeile als fakturierbar konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="11610-135">An estimate or actual created for time will only be considered chargeable if **Time** is included on the quote line, and if **Task** and **Role** are configured as chargeable on the quote line.</span></span>

<span data-ttu-id="11610-136">Eine für die Ausgabe erstellte Vorkalkulation oder ein Istwert wird nur dann als fakturierbar angesehen, wenn **Ausgaben** in der Angebotszeile enthalten ist und **Aufgabe** und **Transaktionskategorie** in der Angebotszeile als fakturierbar konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="11610-136">An estimate or actual created for expense will only be considered chargeable if **Expense** is included on the quote line, and if **Task** and **Transaction Category** are configured as chargeable on the quote line.</span></span>

| <span data-ttu-id="11610-137">Schließt Zeit ein</span><span class="sxs-lookup"><span data-stu-id="11610-137">Includes Time</span></span> | <span data-ttu-id="11610-138">Schließt Ausgaben ein</span><span class="sxs-lookup"><span data-stu-id="11610-138">Includes Expense</span></span> | <span data-ttu-id="11610-139">Eingeschlossene Aufgaben</span><span class="sxs-lookup"><span data-stu-id="11610-139">Included Tasks</span></span> | <span data-ttu-id="11610-140">Rolle</span><span class="sxs-lookup"><span data-stu-id="11610-140">Role</span></span> | <span data-ttu-id="11610-141">Kateg.</span><span class="sxs-lookup"><span data-stu-id="11610-141">Category</span></span> | <span data-ttu-id="11610-142">Task</span><span class="sxs-lookup"><span data-stu-id="11610-142">Task</span></span> | <span data-ttu-id="11610-143">Fakturierung</span><span class="sxs-lookup"><span data-stu-id="11610-143">Billing</span></span> |
| --- | --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="11610-144">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-144">Yes</span></span> | <span data-ttu-id="11610-145">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-145">Yes</span></span> | <span data-ttu-id="11610-146">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="11610-146">Entire project</span></span> | <span data-ttu-id="11610-147">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-147">Chargeable</span></span> | <span data-ttu-id="11610-148">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-148">Chargeable</span></span> | <span data-ttu-id="11610-149">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="11610-149">Can't be set</span></span> | <span data-ttu-id="11610-150">Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-150">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="11610-151">Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-151">Billing type on expense actual: Chargeable</span></span> |
| <span data-ttu-id="11610-152">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-152">Yes</span></span> | <span data-ttu-id="11610-153">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-153">Yes</span></span> | <span data-ttu-id="11610-154">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="11610-154">Selected tasks only</span></span> | <span data-ttu-id="11610-155">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-155">Chargeable</span></span> | <span data-ttu-id="11610-156">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-156">Chargeable</span></span> | <span data-ttu-id="11610-157">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-157">Chargeable</span></span> | <span data-ttu-id="11610-158">Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-158">Billing on a time actual: Chargeable</span></span></br><span data-ttu-id="11610-159">Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-159">Billing type on expense actual: Chargeable</span></span> |
| <span data-ttu-id="11610-160">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-160">Yes</span></span> | <span data-ttu-id="11610-161">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-161">Yes</span></span> | <span data-ttu-id="11610-162">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="11610-162">Selected tasks only</span></span> | <span data-ttu-id="11610-163">Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-163">Non-chargeable</span></span> | <span data-ttu-id="11610-164">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-164">Chargeable</span></span> | <span data-ttu-id="11610-165">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-165">Chargeable</span></span> | <span data-ttu-id="11610-166">Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-166">Billing on a time actual: Non-Chargeable</span></span></br><span data-ttu-id="11610-167">Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-167">Billing type on expense actual: Chargeable</span></span> |
| <span data-ttu-id="11610-168">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-168">Yes</span></span> | <span data-ttu-id="11610-169">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-169">Yes</span></span> | <span data-ttu-id="11610-170">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="11610-170">Selected tasks only</span></span> | <span data-ttu-id="11610-171">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-171">Chargeable</span></span> | <span data-ttu-id="11610-172">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-172">Chargeable</span></span> | <span data-ttu-id="11610-173">Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-173">Non-Chargeable</span></span> | <span data-ttu-id="11610-174">Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-174">Billing on a time actual: Non-Chargeable</span></span></br> <span data-ttu-id="11610-175">Fakturierungstyp bei tatsächlichen Ausgaben: Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-175">Billing type on expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="11610-176">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-176">Yes</span></span> | <span data-ttu-id="11610-177">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-177">Yes</span></span> | <span data-ttu-id="11610-178">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="11610-178">Selected tasks only</span></span> | <span data-ttu-id="11610-179">Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-179">Non-Chargeable</span></span> | <span data-ttu-id="11610-180">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-180">Chargeable</span></span> | <span data-ttu-id="11610-181">Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-181">Non- Chargeable</span></span> | <span data-ttu-id="11610-182">Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-182">Billing on a time actual: Non-Chargeable</span></span></br> <span data-ttu-id="11610-183">Fakturierungstyp bei tatsächlichen Ausgaben: Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-183">Billing type on expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="11610-184">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-184">Yes</span></span> | <span data-ttu-id="11610-185">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-185">Yes</span></span> | <span data-ttu-id="11610-186">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="11610-186">Selected tasks only</span></span> | <span data-ttu-id="11610-187">Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-187">Non-Chargeable</span></span> | <span data-ttu-id="11610-188">Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-188">Non-Chargeable</span></span> | <span data-ttu-id="11610-189">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-189">Chargeable</span></span> | <span data-ttu-id="11610-190">Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-190">Billing on a time actual: Non-Chargeable</span></span></br> <span data-ttu-id="11610-191">Fakturierungstyp bei tatsächlichen Ausgaben: Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-191">Billing type on expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="11610-192">Nr.</span><span class="sxs-lookup"><span data-stu-id="11610-192">No</span></span> | <span data-ttu-id="11610-193">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-193">Yes</span></span> | <span data-ttu-id="11610-194">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="11610-194">Entire project</span></span> | <span data-ttu-id="11610-195">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="11610-195">Can't be set</span></span> | <span data-ttu-id="11610-196">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-196">Chargeable</span></span> | <span data-ttu-id="11610-197">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="11610-197">Can't be set</span></span> | <span data-ttu-id="11610-198">Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="11610-198">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="11610-199">Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-199">Billing type on expense actual: Chargeable</span></span> |
| <span data-ttu-id="11610-200">Nr.</span><span class="sxs-lookup"><span data-stu-id="11610-200">No</span></span> | <span data-ttu-id="11610-201">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-201">Yes</span></span> | <span data-ttu-id="11610-202">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="11610-202">Entire project</span></span> | <span data-ttu-id="11610-203">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="11610-203">Can't be set</span></span> | <span data-ttu-id="11610-204">Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-204">Non-chargeable</span></span> | <span data-ttu-id="11610-205">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="11610-205">Can't be set</span></span> | <span data-ttu-id="11610-206">Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="11610-206">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="11610-207">Fakturierungstyp bei tatsächlichen Ausgaben: Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-207">Billing type on expense actual: Non-chargeable</span></span> |
| <span data-ttu-id="11610-208">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-208">Yes</span></span> | <span data-ttu-id="11610-209">Nr.</span><span class="sxs-lookup"><span data-stu-id="11610-209">No</span></span> | <span data-ttu-id="11610-210">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="11610-210">Entire project</span></span> | <span data-ttu-id="11610-211">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-211">Chargeable</span></span> | <span data-ttu-id="11610-212">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="11610-212">Can't be set</span></span> | <span data-ttu-id="11610-213">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="11610-213">Can't be set</span></span> | <span data-ttu-id="11610-214">Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-214">Billing on a time actual: Chargeable</span></span></br><span data-ttu-id="11610-215">Fakturierungstyp bei tatsächlichen Ausgaben: Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="11610-215">Billing type on expense actual: Not available</span></span> |
| <span data-ttu-id="11610-216">Ja</span><span class="sxs-lookup"><span data-stu-id="11610-216">Yes</span></span> | <span data-ttu-id="11610-217">Nr.</span><span class="sxs-lookup"><span data-stu-id="11610-217">No</span></span> | <span data-ttu-id="11610-218">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="11610-218">Entire project</span></span> | <span data-ttu-id="11610-219">Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-219">Non-chargeable</span></span> | <span data-ttu-id="11610-220">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="11610-220">Can't be set</span></span> | <span data-ttu-id="11610-221">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="11610-221">Can't be set</span></span> | <span data-ttu-id="11610-222">Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11610-222">Billing on a time actual: Non-chargeable</span></span> </br><span data-ttu-id="11610-223">Fakturierungstyp bei tatsächlichen Ausgaben: Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="11610-223">Billing type on expense actual: Not available</span></span> |