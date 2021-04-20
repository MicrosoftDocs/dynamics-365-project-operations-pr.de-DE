---
title: Projektbasierte Korrekturrechnungen erstellen
description: Dieses Thema enthält Informationen zu Korrekturrechnungen in Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788856"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="6bebf-103">Projektbasierte Korrekturrechnungen erstellen</span><span class="sxs-lookup"><span data-stu-id="6bebf-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="6bebf-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="6bebf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6bebf-105">Eine bestätigte Projektrechnung kann korrigiert werden, um Änderungen oder Gutschriften zu verarbeiten, die mit dem Kunden und dem Projektmanager ausgehandelt wurden.</span><span class="sxs-lookup"><span data-stu-id="6bebf-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="6bebf-106">Um eine bestätigte Rechnung zu bearbeiten, öffnen Sie die bestätigte Rechnung und wählen Sie **Korrigieren Sie diese Rechnung** aus.</span><span class="sxs-lookup"><span data-stu-id="6bebf-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="6bebf-107">Diese Auswahl ist nur verfügbar, wenn eine Projektrechnung bestätigt wurde.</span><span class="sxs-lookup"><span data-stu-id="6bebf-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="6bebf-108">Aus der bestätigten Rechnung wird ein neuer Rechnungsentwurf erstellt.</span><span class="sxs-lookup"><span data-stu-id="6bebf-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="6bebf-109">Alle Rechnungszeilendetails aus der zuvor bestätigten Rechnung werden in den neuen Entwurf kopiert.</span><span class="sxs-lookup"><span data-stu-id="6bebf-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="6bebf-110">Im Folgenden finden Sie einige wichtige Punkte, die Ihnen helfen sollen, mehr über die Zeilendetails auf der neuen Korrekturrechnung zu erfahren:</span><span class="sxs-lookup"><span data-stu-id="6bebf-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="6bebf-111">Alle Mengen werden auf Null aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6bebf-111">All quantities are updated to zero.</span></span> <span data-ttu-id="6bebf-112">Dies setzt voraus, dass alle in Rechnung gestellten Artikel vollständig gutgeschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6bebf-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="6bebf-113">Bei Bedarf können Sie diese Mengen manuell aktualisieren, um die in Rechnung gestellte Menge und nicht die gutgeschriebene Menge widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="6bebf-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="6bebf-114">Basierend auf der von Ihnen eingegebenen Menge berechnet die Anwendung die gutgeschriebene Menge.</span><span class="sxs-lookup"><span data-stu-id="6bebf-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="6bebf-115">Dieser Betrag spiegelt sich in den Istwerten wider, die erstellt werden, wenn die korrigierte Rechnung bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="6bebf-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="6bebf-116">Wenn Sie Änderungen am Steuerbetrag vornehmen, müssen Sie den richtigen Steuerbetrag eingeben und nicht den Steuerbetrag, der gutgeschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="6bebf-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="6bebf-117">Meilensteinkorrekturen werden immer als volle Gutschriften verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="6bebf-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="6bebf-118">Vorauszahlungs- oder Vorschussbeträge können korrigiert werden, wenn dem Kunden ein falscher Betrag in Rechnung gestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6bebf-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="6bebf-119">Abstimmungen von Vorauszahlungen und Vorschüssen können korrigiert werden, wenn ein falscher Betrag verwendet wurde, um die Gebühren auf einer zuvor bestätigten Rechnung abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="6bebf-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6bebf-120">Rechnungszeilendetails, bei denen es sich um Korrekturen zu anderen bereits in Rechnung gestellten Gebühren handelt, haben das **Korrektur**-Feld auf **Ja** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="6bebf-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="6bebf-121">Rechnungen mit korrigierten Rechnungszeilendetails haben ein Feld mit dem Namen **Hat Korrekturen**, das auch auf **Ja** eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="6bebf-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="6bebf-122">Istwerten, die bei Bestätigung einer Korrekturrechnung erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="6bebf-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="6bebf-123">In der folgenden Tabelle sind die Istwerte aufgeführt, die erstellt werden, wenn eine Korrekturrechnung bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="6bebf-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="6bebf-124">
                    <strong>Szenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6bebf-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="6bebf-125">
                    <strong>Bei Bestätigung erstellte Istwerte</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6bebf-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="6bebf-126">Bestätigen Sie die Korrektur eines in Rechnung gestellten Vorschusses oder einer Vorauszahlung.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="6bebf-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-127">Eine nicht fakturierte Umsatzumkehrung der Vorauszahlung oder des Vorschusses, der für die Abstimmung erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="6bebf-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="6bebf-128">Dieser Betrag ist positiv, da er das negative Ergebnis aufheben soll, das bei der Rechnungsstellung der Vorauszahlung oder des Vorschusses erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6bebf-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-129">Eine fakturierte Umsatzistwert-Umkehrung wird für den Betrag in der Vorauszahlung oder im Vorschuss erstellt, um den ursprünglich fakturierten Umsatz umzukehren.</span><span class="sxs-lookup"><span data-stu-id="6bebf-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-130">Ein neuer fakturierter Umsatz-Istwert wird für den korrigierten Betrag in der vorauszahlungs- oder vorschussbasierten korrigierten Rechnungszeile erstellt.</span><span class="sxs-lookup"><span data-stu-id="6bebf-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-131">Ein nicht fakturierter tatsächlicher Umsatz eines negativen Betrags einer vorauszahlungs- oder vorschussbasierten korrigierten Rechnungszeile, die für die Abstimmung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bebf-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="6bebf-132">Eine Bestätigung der Korrektur einer zuvor abgestimmten Vorauszahlung oder des Vorschusses.</span><span class="sxs-lookup"><span data-stu-id="6bebf-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-133">Eine nicht fakturierte Umsatzumkehrung der Vorauszahlung oder des Vorschusses, der für die Abstimmung erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="6bebf-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="6bebf-134">Dieser Betrag ist positiv und soll das negative Ergebnis aufhaben, das beim Auftreten der vorherigen Abstimmung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6bebf-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-135">Eine fakturierte Umsatzistwert-Umkehrung für den Betrag auf der vorherigen Rechnung</span><span class="sxs-lookup"><span data-stu-id="6bebf-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-136">Ein neuer fakturierter Umsatz-Istwert für den korrigierten Vorauszahlungsbetrag, der auf die korrigierte Rechnung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bebf-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-137">Ein nicht fakturierter tatsächlicher Umsatz mit einem negativen Betrag aus der korrigierten restlichen Vorauszahlung oder dem Vorschuss, der zur Abstimmung auf späteren Rechnungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6bebf-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6bebf-138">Fakturierung des vollen Guthabens einer zuvor in Rechnung gestellten Zeittransaktion</span><span class="sxs-lookup"><span data-stu-id="6bebf-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-139">Eine fakturierte Umsatzumkehrung für die Stunden und den Betrag des ursprünglichen Rechnungszeilendetails für Zeit</span><span class="sxs-lookup"><span data-stu-id="6bebf-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-140">Ein neuer nicht fakturierter Umsatz-Istwert für die Stunden und den Betrag des ursprünglichen Rechnungszeilendetails für Zeit</span><span class="sxs-lookup"><span data-stu-id="6bebf-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6bebf-141">Fakturierung der Teilgutschrift bei einer Zeittransaktion</span><span class="sxs-lookup"><span data-stu-id="6bebf-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-142">Eine fakturierte Umsatzumkehrung für die Stunden und den Betrag, die im ursprünglichen Rechnungszeilendetail für Zeit in Rechnung gestellt wurden</span><span class="sxs-lookup"><span data-stu-id="6bebf-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-143">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Stunden und den Betrag im bearbeiteten Rechnungszeilendetail berechnet wird, eine Umkehrung des tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="6bebf-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-144">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibenden Stunden und den Betrag nach Abzug der korrigierten Zahlen auf dem Rechnungszeilendetail berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="6bebf-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6bebf-145">Fakturierung des vollen Guthabens einer zuvor in Rechnung gestellten Ausgabentransaktion</span><span class="sxs-lookup"><span data-stu-id="6bebf-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-146">Eine fakturierte Umsatzumkehrung für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6bebf-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-147">Ein neuer nicht fakturierter Umsatz-Istwert für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6bebf-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6bebf-148">Fakturierung der Teilgutschrift einer zuvor in Rechnung gestellten Ausgabentransaktion</span><span class="sxs-lookup"><span data-stu-id="6bebf-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-149">Eine fakturierte Umsatzumkehrung für die Menge und den Betrag, die im ursprünglichen Rechnungszeilendetail für eine Ausgabe in Rechnung gestellt wurden</span><span class="sxs-lookup"><span data-stu-id="6bebf-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-150">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im korrigierten Rechnungszeilendetail berechnet wird, eine Umkehrung hiervon und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="6bebf-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-151">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibende Menge und den Betrag nach Abzug der korrigierten Zahlen im Rechnungszeilendetail berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="6bebf-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6bebf-152">Fakturierung des vollen Guthabens einer zuvor in Rechnung gestellten Gebührentransaktion</span><span class="sxs-lookup"><span data-stu-id="6bebf-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-153">Eine fakturierte Umsatzumkehrung für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Gebühr</span><span class="sxs-lookup"><span data-stu-id="6bebf-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-154">Ein neuer nicht fakturierter Umsatz-Istwert für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Gebühr</span><span class="sxs-lookup"><span data-stu-id="6bebf-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6bebf-155">Fakturierung der Teilgutschrift einer zuvor in Rechnung gestellten Gebührentransaktion</span><span class="sxs-lookup"><span data-stu-id="6bebf-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-156">Eine fakturierte Umsatzumkehrung für die Menge und den Betrag, die im ursprünglichen Rechnungszeilendetail für die Gebühr in Rechnung gestellt wurde</span><span class="sxs-lookup"><span data-stu-id="6bebf-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-157">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im bearbeiteten korrigierten Rechnungszeilendetail berechnet wird, eine Umkehrung hiervon und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="6bebf-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="6bebf-158">Fakturierung des vollen Guthabens eines zuvor in Rechnung gestellten Meilensteins</span><span class="sxs-lookup"><span data-stu-id="6bebf-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-159">Eine fakturierte Umsatzumkehrung für den Betrag im ursprünglichen Rechnungszeilendetail für den Meilenstein</span><span class="sxs-lookup"><span data-stu-id="6bebf-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="6bebf-160">Der Rechnungsstatus des Meilensteins wird von <b>Gebuchte Kundenrechnung</b> zu <b>Bereit für die Rechnungsstellung</b> aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6bebf-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="6bebf-161">Fakturierung der Teilgutschrift eines zuvor in Rechnung gestellten Meilensteins</span><span class="sxs-lookup"><span data-stu-id="6bebf-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6bebf-162">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6bebf-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
