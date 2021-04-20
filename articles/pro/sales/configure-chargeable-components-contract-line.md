---
title: Kostenpflichtige Komponenten einer projektbasierten Vertragszeile konfigurieren
description: Dieses Thema enthält Informationen zum Hinzufügen fakturierbarer Komponenten zu Vertragszeilen in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858472"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="54d3b-103">Kostenpflichtige Komponenten einer projektbasierten Vertragszeile konfigurieren</span><span class="sxs-lookup"><span data-stu-id="54d3b-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="54d3b-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung Project Operations für Ressourcen/nicht vorrätige Szenarien_</span><span class="sxs-lookup"><span data-stu-id="54d3b-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="54d3b-105">Eine projektbasierte Vertragszeile hat *eingeschlossene* Komponenten und *fakturierbare* Komponenten.</span><span class="sxs-lookup"><span data-stu-id="54d3b-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="54d3b-106">Eingeschlossene Komponenten sind Komponenten, die Folgendem unterliegen:</span><span class="sxs-lookup"><span data-stu-id="54d3b-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="54d3b-107">Fakturierungsmethode und Kundenaufteilung</span><span class="sxs-lookup"><span data-stu-id="54d3b-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="54d3b-108">Nicht zu überschreitende Grenzwerte</span><span class="sxs-lookup"><span data-stu-id="54d3b-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="54d3b-109">In der projektbasierten Vertragszeile definierte Einstellungen für die Rechnungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="54d3b-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="54d3b-110">Eine Teilmenge der eingeschlossenen Komponenten kann mit dem Feld **Fakturierungstyp** als fakturierbar markiert werden.</span><span class="sxs-lookup"><span data-stu-id="54d3b-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="54d3b-111">Das Feld **Fakturierungstyp** ist ein Optionssatz, der die folgenden Werte im Kontext einer Vertragszeile zulässt:</span><span class="sxs-lookup"><span data-stu-id="54d3b-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="54d3b-112">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-112">Chargeable</span></span>
  - <span data-ttu-id="54d3b-113">Nicht fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-113">Non-chargeable</span></span>

<span data-ttu-id="54d3b-114">Fakturierbare Komponenten können für die Kategorien Aufgaben, Rollen und Transaktionen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="54d3b-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="54d3b-115">Die Fakturierbarkeit wird für Aufgaben für eine Projektvertragszeile definiert und gilt für alle in der Zeile enthaltenen Transaktionsklassen.</span><span class="sxs-lookup"><span data-stu-id="54d3b-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="54d3b-116">Wenn das Feld **Aufgaben einschließen** in einer Vertragszeile leer ist oder auf **Gesamtes Projekt** festgelegt wurde, ist die Registerkarte **Fakturierbare Aufgaben** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="54d3b-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="54d3b-117">Die für Rollen für eine Projektvertragszeile festgelegte Fakturierbarkeit gilt nur für die Transaktionsklasse **Zeit**.</span><span class="sxs-lookup"><span data-stu-id="54d3b-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="54d3b-118">Wenn das Feld **Zeit einschließen** in einer Vertragszeile leer ist oder auf **Nein** festgelegt wurde, ist die Registerkarte **Fakturierbare Rollen** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="54d3b-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="54d3b-119">Die für Transaktionskategorien für eine Projektvertragszeile festgelegte Fakturierbarkeit gilt nur für die Transaktionsklasse **Ausgaben**.</span><span class="sxs-lookup"><span data-stu-id="54d3b-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="54d3b-120">Wenn das Feld **Ausgaben einschließen** in einer Vertragszeile auf **Nein** festgelegt wurde, ist die Registerkarte **Fakturierbare Kategorien** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="54d3b-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="54d3b-121">Eine Projektaufgabe als fakturierbar oder nicht fakturierbar aktualisieren</span><span class="sxs-lookup"><span data-stu-id="54d3b-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="54d3b-122">Eine Projektaufgabe kann für eine bestimmte Vertragszeile fakturierbar oder nicht fakturierbar sein, wodurch das folgende Setup möglich wird:</span><span class="sxs-lookup"><span data-stu-id="54d3b-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="54d3b-123">Wenn eine projektbasierte Vertragszeile **Zeit** enthält und eine bestimmte Aufgabe, **T1**, dieser Zeile als fakturierbar zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="54d3b-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="54d3b-124">Wenn es eine zweite Vertragszeile gibt, die **Ausgaben** enthält, können Sie die T1-Aufgabe in der Vertragszeile als nicht fakturierbar zuordnen.</span><span class="sxs-lookup"><span data-stu-id="54d3b-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="54d3b-125">Das Ergebnis ist, dass die gesamte für die Aufgabe aufgezeichnete Zeit fakturierbar ist und alle Ausgaben nicht fakturierbar sind.</span><span class="sxs-lookup"><span data-stu-id="54d3b-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="54d3b-126">Der Fakturierungstyp einer Aufgabe kann auf der Registerkarte **Fakturierbare Aufgaben** der Vertragszeile konfiguriert werden, indem das **Fakturierungstyp**-Feld im Unterraster für Vertragszeilenaufgaben aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="54d3b-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="54d3b-127">Alternativ können Sie das **Fakturierungstyp**-Feld im Unterraster der Aufgabenabrechnungseinrichtung eines Projekts aktualisieren, in dem die einer Aufgabe zugeordneten Vertragszeilen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="54d3b-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="54d3b-128">Eine Rolle als fakturierbar oder nicht fakturierbar aktualisieren</span><span class="sxs-lookup"><span data-stu-id="54d3b-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="54d3b-129">Eine Rolle kann für eine bestimmte Vertragszeile fakturierbar oder nicht fakturierbar sein.</span><span class="sxs-lookup"><span data-stu-id="54d3b-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="54d3b-130">Der Fakturierungstyp einer Rolle kann auf der Registerkarte **Fakturierbare Rollen** einer Vertragszeile konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="54d3b-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="54d3b-131">Aktualisieren Sie dazu das **Fakturierungstyp**-Feld auf dem Unterraster **Fakturierbare Rollen**.</span><span class="sxs-lookup"><span data-stu-id="54d3b-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="54d3b-132">Eine Transaktionskategorie als fakturierbar oder nicht fakturierbar aktualisieren</span><span class="sxs-lookup"><span data-stu-id="54d3b-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="54d3b-133">Eine Transaktionskategorie kann für eine bestimmte Vertragszeile fakturierbar oder nicht fakturierbar sein.</span><span class="sxs-lookup"><span data-stu-id="54d3b-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="54d3b-134">Der Fakturierungstyp einer Transaktion kann auf der Registerkarte **Fakturierbare Kategorien** einer projektbasierten Vertragszeile konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="54d3b-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="54d3b-135">Aktualisieren Sie dazu das **Fakturierungstyp**-Feld auf dem Unterraster **Fakturierbare Kategorien**.</span><span class="sxs-lookup"><span data-stu-id="54d3b-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="54d3b-136">Fakturierbarkeit abschließen</span><span class="sxs-lookup"><span data-stu-id="54d3b-136">Resolve chargeability</span></span>

<span data-ttu-id="54d3b-137">Eine für die Zeit erstellte Schätzung oder tatsächliche Schätzung wird nur dann als steuerpflichtig angesehen, wenn:</span><span class="sxs-lookup"><span data-stu-id="54d3b-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="54d3b-138">**Zeit** ist in der Vertragszeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="54d3b-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="54d3b-139">**Rolle** ist in der Vertragszeile als fakturierbar konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="54d3b-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="54d3b-140">**Enthaltene Aufgaben** ist in der Vertragszeile eingestellt auf **Ausgewählte Aufgaben**.</span><span class="sxs-lookup"><span data-stu-id="54d3b-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="54d3b-141">Wenn diese drei Dinge zutreffen, wird die Aufgabe als fakturierbar konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="54d3b-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="54d3b-142">Eine für den Aufwand erstellte Schätzung oder tatsächliche Werte werden nur dann als fakturierbar angesehen, wenn:</span><span class="sxs-lookup"><span data-stu-id="54d3b-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="54d3b-143">**Aufwand** in der Vertragszeile enthalten ist</span><span class="sxs-lookup"><span data-stu-id="54d3b-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="54d3b-144">**Transaktionskategorie** ist in der Vertragszeile als fakturierbar konfiguriert</span><span class="sxs-lookup"><span data-stu-id="54d3b-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="54d3b-145">**Enthaltene Aufgaben** ist in der Vertragszeile eingestellt auf **Ausgewählte Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="54d3b-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="54d3b-146">Wenn diese drei Dinge zutreffen, wird die **Aufgabe** als fakturierbar konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="54d3b-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="54d3b-147">Eine für Materialien erstellte Schätzung oder tatsächliche Werte werden nur dann als fakturierbar angesehen, wenn:</span><span class="sxs-lookup"><span data-stu-id="54d3b-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="54d3b-148">**Materialien** in der Vertragszeile enthalten ist</span><span class="sxs-lookup"><span data-stu-id="54d3b-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="54d3b-149">**Enthaltene Aufgaben** ist in der Vertragszeile eingestellt auf **Ausgewählte Aufgaben**</span><span class="sxs-lookup"><span data-stu-id="54d3b-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="54d3b-150">Wenn diese zwei Dinge zutreffen, wird die **Aufgabe** als fakturierbar konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="54d3b-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="54d3b-151">
                    <strong>Schließt Zeit ein</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="54d3b-152">
                    <strong>Schließt Ausgaben ein</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="54d3b-153">
                    <strong>Enthält Material</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="54d3b-154">
                    <strong>Eingeschlossene Aufgaben</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="54d3b-155">
                    <strong>Rolle</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="54d3b-156">
                    <strong>Kateg.</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="54d3b-157">
                    <strong>Aufgabe</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="54d3b-158">
                    <strong>Auswirkungen auf die Fakturierbarkeit</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-159">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="54d3b-160">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="54d3b-161">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="54d3b-162">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="54d3b-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-163">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-164">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-165">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="54d3b-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="54d3b-166">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-167">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-168">Fakturierungstyp bei tatsächlichen Materialien: <strong>Fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-169">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="54d3b-170">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="54d3b-171">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="54d3b-172">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="54d3b-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-173">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-174">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-175">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="54d3b-176">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-177">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-178">Fakturierungstyp bei tatsächlichen Materialien: <strong>Fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-179">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="54d3b-180">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="54d3b-181">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="54d3b-182">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="54d3b-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="54d3b-183">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-184">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-185">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="54d3b-186">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-187">Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="54d3b-188">Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-189">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="54d3b-190">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="54d3b-191">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="54d3b-192">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="54d3b-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-193">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-194">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="54d3b-195">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="54d3b-196">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-197">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-198">Fakturierungstyp bei tatsächlichen Materialien: <strong>Nicht Fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-199">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="54d3b-200">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="54d3b-201">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="54d3b-202">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="54d3b-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="54d3b-203">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-204">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="54d3b-205">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="54d3b-206">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-207">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-208">Fakturierungstyp bei tatsächlichen Materialien: <strong>Nicht Fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-209">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="54d3b-210">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="54d3b-211">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="54d3b-212">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="54d3b-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="54d3b-213">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="54d3b-214">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-215">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="54d3b-216">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-217">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-218">Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="54d3b-219">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="54d3b-220">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="54d3b-221">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="54d3b-222">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="54d3b-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-223">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="54d3b-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="54d3b-224">
                    <strong>Fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-225">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="54d3b-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="54d3b-226">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht verfügbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-227">Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="54d3b-228">Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="54d3b-229">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="54d3b-230">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="54d3b-231">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="54d3b-232">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="54d3b-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-233">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="54d3b-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="54d3b-234">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-235">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="54d3b-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="54d3b-236">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht verfügbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-237">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-238">Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-239">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="54d3b-240">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="54d3b-241">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="54d3b-242">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="54d3b-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-243">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-244">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="54d3b-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-245">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="54d3b-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="54d3b-246">Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="54d3b-247">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht verfügbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-248">Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-249">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="54d3b-250">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="54d3b-251">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="54d3b-252">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="54d3b-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="54d3b-253">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-254">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="54d3b-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-255">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="54d3b-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="54d3b-256">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-257">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht verfügbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-258">Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-259">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="54d3b-260">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="54d3b-261">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="54d3b-262">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="54d3b-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-263">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-264">Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-265">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="54d3b-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="54d3b-266">Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="54d3b-267">Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="54d3b-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="54d3b-268">Fakturierungstyp bei tatsächlichen Materialien: <strong>Nicht verfügbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="54d3b-269">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="54d3b-270">Ja</span><span class="sxs-lookup"><span data-stu-id="54d3b-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="54d3b-271">
                    <strong>Nr.</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="54d3b-272">Gesamtes Projekt</span><span class="sxs-lookup"><span data-stu-id="54d3b-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="54d3b-273">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="54d3b-274">
                    <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="54d3b-275">Kann nicht festgelegt werden</span><span class="sxs-lookup"><span data-stu-id="54d3b-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="54d3b-276">Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-277">Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="54d3b-278">Fakturierungstyp bei tatsächlichen Materialien: <strong>Nicht verfügbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54d3b-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
