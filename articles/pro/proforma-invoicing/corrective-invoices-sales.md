---
title: Korrigierte Rechnungen – Lite
description: Dieses Thema bietet Informationen zu korrigierten Rechnungen in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb949ff3a53bcba19d44e1c3d6fe08a6b368108d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274232"
---
# <a name="corrected-invoices---lite"></a><span data-ttu-id="7f3e0-103">Korrigierte Rechnungen – Lite</span><span class="sxs-lookup"><span data-stu-id="7f3e0-103">Corrected invoices - lite</span></span>

<span data-ttu-id="7f3e0-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="7f3e0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7f3e0-105">Eine bestätigte Projektrechnung kann korrigiert werden, um Änderungen oder Gutschriften zu verarbeiten, die mit dem Kunden und dem Projektmanager ausgehandelt wurden.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="7f3e0-106">Um eine bestätigte Rechnung zu bearbeiten, öffnen Sie die bestätigte Rechnung und wählen Sie **Korrigieren Sie diese Rechnung** aus.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="7f3e0-107">Diese Auswahl ist nur verfügbar, wenn eine Projektrechnung bestätigt wurde.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="7f3e0-108">Aus der bestätigten Rechnung wird ein neuer Rechnungsentwurf erstellt.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="7f3e0-109">Alle Rechnungszeilendetails aus der zuvor bestätigten Rechnung werden in den neuen Entwurf kopiert.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="7f3e0-110">Im Folgenden sind einige der wichtigsten Punkte aufgeführt, die Sie zum Verständnis der Zeilendetails auf der neuen korrigierten Rechnung beachten sollten:</span><span class="sxs-lookup"><span data-stu-id="7f3e0-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="7f3e0-111">Alle Mengen werden auf Null aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-111">All quantities are updated to zero.</span></span> <span data-ttu-id="7f3e0-112">Die Anwendung geht davon aus, dass alle in Rechnung gestellten Artikel vollständig gutgeschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="7f3e0-113">Bei Bedarf können Sie diese Mengen manuell aktualisieren, um die in Rechnung gestellte Menge und nicht die gutgeschriebene Menge widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="7f3e0-114">Basierend auf der von Ihnen eingegebenen Menge berechnet die Anwendung die gutgeschriebene Menge.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="7f3e0-115">Dieser Betrag spiegelt sich in den Istwerten wider, die erstellt werden, wenn die korrigierte Rechnung bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="7f3e0-116">Wenn Sie Änderungen am Steuerbetrag vornehmen, müssen Sie den richtigen Steuerbetrag eingeben und nicht den Steuerbetrag, der gutgeschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="7f3e0-117">Zuvor bestätigte produktbasierte Vertragszeilen werden nicht kopiert.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="7f3e0-118">Die Verarbeitung von Korrekturen auf einer produktbasierten Projektrechnung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="7f3e0-119">Meilensteinkorrekturen werden immer als volle Gutschriften verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="7f3e0-120">Vorauszahlungs- oder Vorschussbeträge können korrigiert werden, wenn dem Kunden ein falscher Betrag in Rechnung gestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="7f3e0-121">Abstimmungen von Vorauszahlungen und Vorschüssen können korrigiert werden, wenn ein falscher Betrag verwendet wurde, um die Gebühren auf einer zuvor bestätigten Rechnung abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f3e0-122">Bei Rechnungszeilendetails, die Korrekturen zu anderen bereits in Rechnung gestellten Gebühren darstellen, ist das Feld **Korrektur** auf **Ja** eingestellt.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="7f3e0-123">Rechnungen mit korrigierten Rechnungszeilendetails haben ein Feld mit dem Namen **Hat Korrekturen**, das auch auf **Ja** eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="7f3e0-124">Istwerten, die bei Bestätigung einer Korrekturrechnung erstellt wurden:</span><span class="sxs-lookup"><span data-stu-id="7f3e0-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="7f3e0-125">Nachfolgend sind die Istwerte aufgeführt, die von der Anwendung bei Bestätigung einer Korrektur erstellt wurden, basierend auf den Vorgängen, die auf dem Entwurf der Korrekturrechnung vor der Bestätigung ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="7f3e0-126">
                    <strong>Szenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7f3e0-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="7f3e0-127">
                    <strong>Bei Bestätigung erstellte Istwerte</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7f3e0-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="7f3e0-128">Bestätigen Sie die Korrektur eines in Rechnung gestellten Vorschusses oder einer Vorauszahlung.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7f3e0-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-129">Eine nicht fakturierte Umsatzumkehrung der Vorauszahlung oder des Vorschusses, der für die Abstimmung erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="7f3e0-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="7f3e0-130">Dieser Betrag ist positiv, da er das negative Ergebnis aufheben soll, das bei der Rechnungsstellung der Vorauszahlung oder des Vorschusses erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-131">Eine fakturierte Umsatzistwert-Umkehrung wird für den Betrag in der Vorauszahlung oder im Vorschuss erstellt, um den ursprünglich fakturierten Umsatz umzukehren.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-132">Ein neuer fakturierter Umsatz-Istwert wird für den korrigierten Betrag in der vorauszahlungs- oder vorschussbasierten korrigierten Rechnungszeile erstellt.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-133">Ein nicht fakturierter tatsächlicher Umsatz eines negativen Betrags einer vorauszahlungs- oder vorschussbasierten korrigierten Rechnungszeile, die für die Abstimmung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="7f3e0-134">Eine Bestätigung der Korrektur einer zuvor abgestimmten Vorauszahlung oder des Vorschusses.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-135">Eine nicht fakturierte Umsatzumkehrung der Vorauszahlung oder des Vorschusses, der für die Abstimmung erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="7f3e0-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="7f3e0-136">Dieser Betrag ist positiv und soll das negative Ergebnis aufhaben, das beim Auftreten der vorherigen Abstimmung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-137">Eine fakturierte Umsatzistwert-Umkehrung für den Betrag auf der vorherigen Rechnung</span><span class="sxs-lookup"><span data-stu-id="7f3e0-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-138">Ein neuer fakturierter Umsatz-Istwert für den korrigierten Vorauszahlungsbetrag, der auf die korrigierte Rechnung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-139">Ein nicht fakturierter tatsächlicher Umsatz mit einem negativen Betrag aus der korrigierten restlichen Vorauszahlung oder dem Vorschuss, der zur Abstimmung auf späteren Rechnungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7f3e0-140">Fakturierung des vollen Guthabens einer zuvor in Rechnung gestellten Zeittransaktion</span><span class="sxs-lookup"><span data-stu-id="7f3e0-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-141">Eine fakturierte Umsatzumkehrung für die Stunden und den Betrag des ursprünglichen Rechnungszeilendetails für Zeit</span><span class="sxs-lookup"><span data-stu-id="7f3e0-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-142">Ein neuer nicht fakturierter Umsatz-Istwert für die Stunden und den Betrag des ursprünglichen Rechnungszeilendetails für Zeit</span><span class="sxs-lookup"><span data-stu-id="7f3e0-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7f3e0-143">Fakturierung der Teilgutschrift bei einer Zeittransaktion</span><span class="sxs-lookup"><span data-stu-id="7f3e0-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-144">Eine fakturierte Umsatzumkehrung für die Stunden und den Betrag, die im ursprünglichen Rechnungszeilendetail für Zeit in Rechnung gestellt wurden</span><span class="sxs-lookup"><span data-stu-id="7f3e0-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-145">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Stunden und den Betrag im bearbeiteten Rechnungszeilendetail berechnet wird, eine Umkehrung des tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="7f3e0-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-146">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibenden Stunden und den Betrag nach Abzug der korrigierten Zahlen auf dem Rechnungszeilendetail berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7f3e0-147">Fakturierung des vollen Guthabens einer zuvor in Rechnung gestellten Ausgabentransaktion</span><span class="sxs-lookup"><span data-stu-id="7f3e0-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-148">Eine fakturierte Umsatzumkehrung für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f3e0-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-149">Ein neuer nicht fakturierter Umsatz-Istwert für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f3e0-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7f3e0-150">Fakturierung der Teilgutschrift einer zuvor in Rechnung gestellten Ausgabentransaktion</span><span class="sxs-lookup"><span data-stu-id="7f3e0-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-151">Eine fakturierte Umsatzumkehrung für die Menge und den Betrag, die im ursprünglichen Rechnungszeilendetail für eine Ausgabe in Rechnung gestellt wurden</span><span class="sxs-lookup"><span data-stu-id="7f3e0-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-152">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im korrigierten Rechnungszeilendetail berechnet wird, eine Umkehrung hiervon und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="7f3e0-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-153">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibende Menge und den Betrag nach Abzug der korrigierten Zahlen im Rechnungszeilendetail berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7f3e0-154">Fakturierung des vollen Guthabens einer zuvor in Rechnung gestellten Gebührentransaktion</span><span class="sxs-lookup"><span data-stu-id="7f3e0-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-155">Eine fakturierte Umsatzumkehrung für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Gebühr</span><span class="sxs-lookup"><span data-stu-id="7f3e0-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-156">Ein neuer nicht fakturierter Umsatz-Istwert für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Gebühr</span><span class="sxs-lookup"><span data-stu-id="7f3e0-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7f3e0-157">Fakturierung der Teilgutschrift einer zuvor in Rechnung gestellten Gebührentransaktion</span><span class="sxs-lookup"><span data-stu-id="7f3e0-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-158">Eine fakturierte Umsatzumkehrung für die Menge und den Betrag, die im ursprünglichen Rechnungszeilendetail für die Gebühr in Rechnung gestellt wurde</span><span class="sxs-lookup"><span data-stu-id="7f3e0-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-159">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im bearbeiteten korrigierten Rechnungszeilendetail berechnet wird, eine Umkehrung hiervon und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="7f3e0-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7f3e0-160">Fakturierung des vollen Guthabens eines zuvor in Rechnung gestellten Meilensteins</span><span class="sxs-lookup"><span data-stu-id="7f3e0-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-161">Eine fakturierte Umsatzumkehrung für den Betrag im ursprünglichen Rechnungszeilendetail für den Meilenstein</span><span class="sxs-lookup"><span data-stu-id="7f3e0-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="7f3e0-162">Die Rechnung oder der Fakturierungsstatus des Meilensteins in der Projektvertragszeile wird auf **Bereit für die Rechnungsstellung** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7f3e0-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7f3e0-163">Fakturierung der Teilgutschrift eines zuvor in Rechnung gestellten Meilensteins</span><span class="sxs-lookup"><span data-stu-id="7f3e0-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-164">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7f3e0-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7f3e0-165">Gutschriften und Korrekturen einer zuvor in Rechnung gestellten produktbasierten Vertragszeile</span><span class="sxs-lookup"><span data-stu-id="7f3e0-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7f3e0-166">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7f3e0-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]