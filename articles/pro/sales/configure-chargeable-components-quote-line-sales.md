---
title: Die fakturierbaren Komponenten einer Angebotszeile konfigurieren
description: Dieses Thema enthält Informationen zum Einrichten fakturierbarer und nicht fakturierbarer Komponenten in einer projektbasierten Angebotszeile.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003765"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="11e8f-103">Die kostenpflichtigen Komponenten einer Angebotszeile konfigurieren</span><span class="sxs-lookup"><span data-stu-id="11e8f-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="11e8f-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung Project Operations für Ressourcen/nicht vorrätige Szenarien_</span><span class="sxs-lookup"><span data-stu-id="11e8f-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="11e8f-105">Eine projektbasierte Angebotszeile umfasst das Konzept *enthaltener* Komponenten und *fakturierbarer* Komponenten.</span><span class="sxs-lookup"><span data-stu-id="11e8f-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="11e8f-106">Enthaltene Komponenten unterliegen Folgendem:</span><span class="sxs-lookup"><span data-stu-id="11e8f-106">Included components are subject to:</span></span>

  - <span data-ttu-id="11e8f-107">Fakturierungsmethode und Kundenaufteilung</span><span class="sxs-lookup"><span data-stu-id="11e8f-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="11e8f-108">Nicht zu überschreitende Grenzwerte</span><span class="sxs-lookup"><span data-stu-id="11e8f-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="11e8f-109">In der projektbasierten Angebotszeile definierte Einstellungen für die Rechnungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="11e8f-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="11e8f-110">Eine Teilmenge der eingeschlossenen Komponenten kann mit dem Feld **Fakturierungstyp** als fakturierbar markiert werden.</span><span class="sxs-lookup"><span data-stu-id="11e8f-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="11e8f-111">Das Feld **Fakturierungstyp** ist ein Optionssatz, der die folgenden Werte im Kontext einer Angebotszeile zulässt:</span><span class="sxs-lookup"><span data-stu-id="11e8f-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="11e8f-112">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-112">Chargeable</span></span>
  - <span data-ttu-id="11e8f-113">Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-113">Non-chargeable</span></span>

<span data-ttu-id="11e8f-114">Fakturierbare Komponenten können für die Kategorien Aufgaben, Rollen und Transaktionen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="11e8f-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="11e8f-115">Die Fakturierbarkeit wird für Aufgaben für eine Angebotszeile definiert und gilt für alle in dieser Zeile enthaltenen Transaktionsklassen.</span><span class="sxs-lookup"><span data-stu-id="11e8f-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="11e8f-116">Wenn das Feld **Aufgaben einschließen** auf **Gesamtes Projekt** festgelegt wurde oder leer ist, ist die Registerkarte **Fakturierbare Aufgaben** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="11e8f-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="11e8f-117">Die für Rollen für eine Angebotszeile festgelegte Fakturierbarkeit gilt nur für die Transaktionsklasse **Zeit**.</span><span class="sxs-lookup"><span data-stu-id="11e8f-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="11e8f-118">Wenn das Feld **Zeit einschließen** in einer Projektangebotszeile auf **Nein** festgelegt wurde, ist die Registerkarte **Fakturierbare Rollen** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="11e8f-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="11e8f-119">Die für Transaktionskategorien für eine Angebotszeile festgelegte Fakturierbarkeit gilt nur für die Transaktionsklasse **Ausgaben**.</span><span class="sxs-lookup"><span data-stu-id="11e8f-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="11e8f-120">Wenn das Feld **Ausgaben einschließen** in einer Projektangebotszeile auf **Nein** festgelegt wurde, ist die Registerkarte **Fakturierbare Kategorien** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="11e8f-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="11e8f-121">Eine Projektaufgabe als fakturierbar oder nicht fakturierbar aktualisieren</span><span class="sxs-lookup"><span data-stu-id="11e8f-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="11e8f-122">Eine Projektaufgabe kann im Kontext einer bestimmten projektbasierten Angebotszeile fakturierbar oder nicht fakturierbar sein, wodurch das folgende Setup möglich wird.</span><span class="sxs-lookup"><span data-stu-id="11e8f-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="11e8f-123">Wenn eine projektbasierte Angebotszeile **Zeit** und die Aufgabe **T1** enthält, wird die Aufgabe der Angebotszeile als fakturierbar zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="11e8f-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="11e8f-124">Wenn es eine zweite Angebotszeile gibt, die **Ausgaben** enthält, können Sie die **T1**-Aufgabe in der Angebotszeile als nicht fakturierbar zuordnen.</span><span class="sxs-lookup"><span data-stu-id="11e8f-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="11e8f-125">Das Ergebnis ist, dass die gesamte für die Aufgabe aufgezeichnete Zeit fakturierbar ist und alle für die Aufgabe aufgezeichneten Ausgaben nicht fakturierbar sind.</span><span class="sxs-lookup"><span data-stu-id="11e8f-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="11e8f-126">Der Fakturierungstyp einer Aufgabe kann auf der Registerkarte **Fakturierbare Aufgaben** einer projektbasierten Angebotszeile konfiguriert werden, indem das **Fakturierungstyp**-Feld im Unterraster **Angebotszeilenaufgaben** aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="11e8f-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="11e8f-127">Alternativ können Sie den Fakturierungstyp für eine Projektaufgabe im Feld **Fakturierungstyp** im Unterraster der Aufgabenabrechnungseinrichtung eines Projekts aktualisieren, in dem die einer Aufgabe zugeordneten Angebotszeilen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="11e8f-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="11e8f-128">Eine Rolle als fakturierbar oder nicht fakturierbar aktualisieren</span><span class="sxs-lookup"><span data-stu-id="11e8f-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="11e8f-129">Eine Rolle kann im Kontext einer bestimmten projektbasierten Angebotszeile fakturierbar oder nicht fakturierbar sein.</span><span class="sxs-lookup"><span data-stu-id="11e8f-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="11e8f-130">Der Fakturierungstyp einer Rolle kann auf der Registerkarte **Fakturierbare Rollen** einer Angebotszeile konfiguriert werden, indem das **Fakturierungstyp**-Feld im Unterraster **Fakturierbare Rollen** aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="11e8f-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="11e8f-131">Eine Transaktionskategorie als fakturierbar oder nicht fakturierbar aktualisieren</span><span class="sxs-lookup"><span data-stu-id="11e8f-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="11e8f-132">Eine Transaktionskategorie kann für eine bestimmte Angebotszeile fakturierbar oder nicht fakturierbar sein.</span><span class="sxs-lookup"><span data-stu-id="11e8f-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="11e8f-133">Der Fakturierungstyp einer Transaktion kann auf der Registerkarte **Fakturierbare Kategorien** einer Angebotszeile konfiguriert werden, indem das **Fakturierungstyp**-Feld im Unterraster **Fakturierbare Kategorien** aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="11e8f-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="11e8f-134">Fakturierbarkeit abschließen</span><span class="sxs-lookup"><span data-stu-id="11e8f-134">Resolve chargeability</span></span>
<span data-ttu-id="11e8f-135">Eine für die Zeit erstellte Schätzung oder tatsächliche Schätzung wird nur dann als steuerpflichtig angesehen, wenn:</span><span class="sxs-lookup"><span data-stu-id="11e8f-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="11e8f-136">**Zeit** ist in der Angebotszeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="11e8f-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="11e8f-137">**Rolle** ist in der Angebotszeile als fakturierbar konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="11e8f-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="11e8f-138">**Enthaltene Aufgaben** ist in der Angebotszeile eingestellt auf **Ausgewählte Aufgaben**.</span><span class="sxs-lookup"><span data-stu-id="11e8f-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="11e8f-139">Wenn diese drei Dinge zutreffen, wird die **Aufgabe** auch als fakturierbar konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="11e8f-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="11e8f-140">Eine für den Aufwand erstellte Schätzung oder tatsächliche Werte werden nur dann als fakturierbar angesehen, wenn:</span><span class="sxs-lookup"><span data-stu-id="11e8f-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="11e8f-141">**Ausgaben** ist in der Angebotszeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="11e8f-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="11e8f-142">**Transaktionskategorie** ist in der Angebotszeile als fakturierbar konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="11e8f-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="11e8f-143">**Enthaltene Aufgaben** ist in der Angebotszeile eingestellt auf **Ausgewählte Aufgaben**.</span><span class="sxs-lookup"><span data-stu-id="11e8f-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="11e8f-144">Wenn diese drei Dinge zutreffen, wird die **Aufgabe** auch als fakturierbar konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="11e8f-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="11e8f-145">Eine für die Materialien erstellte Schätzung oder tatsächliche Schätzung wird nur dann als steuerpflichtig angesehen, wenn:</span><span class="sxs-lookup"><span data-stu-id="11e8f-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="11e8f-146">**Material** ist in der Angebotszeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="11e8f-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="11e8f-147">**Enthaltene Aufgaben** ist in der Angebotszeile eingestellt auf **Ausgewählte Aufgaben**.</span><span class="sxs-lookup"><span data-stu-id="11e8f-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="11e8f-148">Wenn diese zwei Dinge zutreffen, wird die **Aufgabe** auch als fakturierbar konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="11e8f-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="11e8f-149">
                    <strong>Schließt Zeit ein</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="11e8f-150">
                    <strong>Schließt Ausgaben ein</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="11e8f-151">
                    <strong>Enthält Material</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="11e8f-152">
                    <strong>Eingeschlossene Aufgaben</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="11e8f-153">
                    <strong>Rolle</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="11e8f-154">
                    <strong>Kateg.</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="11e8f-155">
                    <strong>Aufgabe</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="11e8f-156">
                    <strong>Auswirkungen auf die Fakturierbarkeit</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-157">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="11e8f-158">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="11e8f-159">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="11e8f-160">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="11e8f-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-161">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-162">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-163">Kann nicht eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="11e8f-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="11e8f-164">Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="11e8f-165">Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="11e8f-166">Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-167">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="11e8f-168">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="11e8f-169">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="11e8f-170">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="11e8f-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-171">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-172">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-173">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="11e8f-174">Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="11e8f-175">Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="11e8f-176">Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-177">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="11e8f-178">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="11e8f-179">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="11e8f-180">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="11e8f-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="11e8f-181">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-182">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-183">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="11e8f-184">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-185">Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="11e8f-186">Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-187">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="11e8f-188">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="11e8f-189">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="11e8f-190">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="11e8f-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-191">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-192">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="11e8f-193">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="11e8f-194">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-195">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-196">Fakturierungstyp bei tatsächlichen Materialien: <strong>Nicht Fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-197">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="11e8f-198">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="11e8f-199">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="11e8f-200">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="11e8f-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="11e8f-201">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-202">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="11e8f-203">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="11e8f-204">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-205">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-206">Fakturierungstyp bei tatsächlichen Materialien: <strong>Nicht Fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-207">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="11e8f-208">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="11e8f-209">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="11e8f-210">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="11e8f-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="11e8f-211">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="11e8f-212">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-213">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="11e8f-214">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-215">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-216">Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="11e8f-217">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="11e8f-218">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="11e8f-219">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="11e8f-220">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="11e8f-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-221">Kann nicht eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="11e8f-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="11e8f-222">
                    <strong>Fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-223">Kann nicht eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="11e8f-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="11e8f-224">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht verfügbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-225">Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="11e8f-226">Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="11e8f-227">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="11e8f-228">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="11e8f-229">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="11e8f-230">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="11e8f-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-231">Kann nicht eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="11e8f-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="11e8f-232">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-233">Kann nicht eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="11e8f-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="11e8f-234">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht verfügbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-235">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-236">Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-237">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="11e8f-238">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="11e8f-239">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="11e8f-240">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="11e8f-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-241">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-242">Kann nicht eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="11e8f-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-243">Kann nicht eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="11e8f-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="11e8f-244">Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="11e8f-245">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht verfügbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-246">Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-247">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="11e8f-248">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="11e8f-249">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="11e8f-250">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="11e8f-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="11e8f-251">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-252">Kann nicht eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="11e8f-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-253">Kann nicht eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="11e8f-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="11e8f-254">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-255">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht verfügbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-256">Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-257">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="11e8f-258">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="11e8f-259">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="11e8f-260">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="11e8f-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-261">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-262">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-263">Kann nicht eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="11e8f-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="11e8f-264">Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="11e8f-265">Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="11e8f-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="11e8f-266">Fakturierungstyp bei tatsächlichen Materialien: <strong>Nicht verfügbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="11e8f-267">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="11e8f-268">Ja</span><span class="sxs-lookup"><span data-stu-id="11e8f-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="11e8f-269">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="11e8f-270">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="11e8f-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="11e8f-271">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="11e8f-272">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11e8f-273">Kann nicht eingestellt werden</span><span class="sxs-lookup"><span data-stu-id="11e8f-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="11e8f-274">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-275">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="11e8f-276">Fakturierungstyp bei tatsächlichen Materialien: <strong>Nicht verfügbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11e8f-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
