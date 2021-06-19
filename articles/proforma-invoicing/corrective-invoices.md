---
title: Projektbasierte Korrekturrechnungen
description: Dieses Thema enthält Informationen zum Erstellen und Bestätigen von projektbasierten Korrekturrechnungen in Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012270"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="ab60c-103">Projektbasierte Korrekturrechnungen</span><span class="sxs-lookup"><span data-stu-id="ab60c-103">Corrective project-based invoices</span></span>

<span data-ttu-id="ab60c-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="ab60c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ab60c-105">Eine bestätigte Projektrechnung kann korrigiert werden, um Änderungen oder Gutschriften zu verarbeiten, die mit dem Kunden und dem Projektmanager ausgehandelt wurden.</span><span class="sxs-lookup"><span data-stu-id="ab60c-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="ab60c-106">Um eine bestätigte Rechnung zu bearbeiten, öffnen Sie die bestätigte Rechnung und wählen Sie **Korrigieren Sie diese Rechnung** aus.</span><span class="sxs-lookup"><span data-stu-id="ab60c-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="ab60c-107">Diese Auswahl ist nur verfügbar, wenn eine Projektrechnung bestätigt wurde oder die projektbasierte Rechnung Vorschüsse oder Vorbehalte oder Abstimmungen von Vorschüssen oder Vorbehalten enthält.</span><span class="sxs-lookup"><span data-stu-id="ab60c-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="ab60c-108">Aus der bestätigten Rechnung wird ein neuer Rechnungsentwurf erstellt.</span><span class="sxs-lookup"><span data-stu-id="ab60c-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="ab60c-109">Alle Rechnungszeilendetails aus der zuvor bestätigten Rechnung werden in den neuen Entwurf kopiert.</span><span class="sxs-lookup"><span data-stu-id="ab60c-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="ab60c-110">Im Folgenden sind einige der wichtigsten Punkte aufgeführt, die Sie zum Verständnis der Zeilendetails auf der neuen korrigierten Rechnung beachten sollten:</span><span class="sxs-lookup"><span data-stu-id="ab60c-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="ab60c-111">Alle Mengen werden auf Null aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ab60c-111">All quantities are updated to zero.</span></span> <span data-ttu-id="ab60c-112">Dynamics 365 Project Operations setzt voraus, dass alle in Rechnung gestellten Artikel vollständig gutgeschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ab60c-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="ab60c-113">Bei Bedarf können Sie diese Mengen manuell aktualisieren, um die in Rechnung gestellte Menge und nicht die gutgeschriebene Menge widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="ab60c-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="ab60c-114">Basierend auf der von Ihnen eingegebenen Menge berechnet die Anwendung die gutgeschriebene Menge.</span><span class="sxs-lookup"><span data-stu-id="ab60c-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="ab60c-115">Dieser Betrag spiegelt sich in den Istwerten wider, die erstellt werden, wenn die korrigierte Rechnung bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="ab60c-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="ab60c-116">Wenn Sie Änderungen am Steuerbetrag vornehmen, müssen Sie den richtigen Steuerbetrag eingeben und nicht den Steuerbetrag, der gutgeschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ab60c-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="ab60c-117">Meilensteinkorrekturen werden immer als volle Gutschriften verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ab60c-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="ab60c-118">Für Rechnungszeilendetails, bei denen es sich um Korrekturen zu anderen bereits in Rechnung gestellten Gebühren handelt, wird das **Korrektur**-Feld auf **Ja** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="ab60c-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="ab60c-119">Für Rechnungen mit korrigierten Rechnungszeilendetails wird das **Hat Korrekturen**-Feld auf **Ja** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="ab60c-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="ab60c-120">Tatsächliche Transaktionen werden erstellt, wenn eine Korrekturrechnung bestätigt wird</span><span class="sxs-lookup"><span data-stu-id="ab60c-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="ab60c-121">In der folgenden Tabelle sind die Istwerte aufgeführt, die erstellt werden, wenn eine Korrekturrechnung bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="ab60c-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="ab60c-122">
                    <strong>Szenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ab60c-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="ab60c-123">
                    <strong>Bei Bestätigung erstellte Istwerte</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ab60c-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ab60c-124">Fakturierung des vollen Guthabens einer zuvor in Rechnung gestellten Zeittransaktion</span><span class="sxs-lookup"><span data-stu-id="ab60c-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-125">Eine fakturierte Umsatzumkehrung für die Stunden und den Betrag des ursprünglichen Rechnungszeilendetails für Zeit</span><span class="sxs-lookup"><span data-stu-id="ab60c-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-126">Ein neuer nicht fakturierter Umsatz-Istwert für die Stunden und den Betrag des ursprünglichen Rechnungszeilendetails für Zeit</span><span class="sxs-lookup"><span data-stu-id="ab60c-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ab60c-127">Fakturierung der Teilgutschrift bei einer Zeittransaktion</span><span class="sxs-lookup"><span data-stu-id="ab60c-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-128">Eine fakturierte Umsatzumkehrung für die Stunden und den Betrag, die im ursprünglichen Rechnungszeilendetail für Zeit in Rechnung gestellt wurden</span><span class="sxs-lookup"><span data-stu-id="ab60c-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-129">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Stunden und den Betrag im bearbeiteten Rechnungszeilendetail berechnet wird, eine Umkehrung des tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="ab60c-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-130">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibenden Stunden und den Betrag nach Abzug der korrigierten Zahlen auf dem Rechnungszeilendetail berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="ab60c-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ab60c-131">Fakturierung des vollen Guthabens einer zuvor in Rechnung gestellten Ausgabentransaktion</span><span class="sxs-lookup"><span data-stu-id="ab60c-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-132">Eine fakturierte Umsatzumkehrung für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab60c-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-133">Ein neuer nicht fakturierter Umsatz-Istwert für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab60c-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ab60c-134">Fakturierung der Teilgutschrift einer zuvor in Rechnung gestellten Ausgabentransaktion</span><span class="sxs-lookup"><span data-stu-id="ab60c-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-135">Eine fakturierte Umsatzumkehrung für die Menge und den Betrag, die im ursprünglichen Rechnungszeilendetail für eine Ausgabe in Rechnung gestellt wurden</span><span class="sxs-lookup"><span data-stu-id="ab60c-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-136">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im korrigierten Rechnungszeilendetail berechnet wird, eine Umkehrung hiervon und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="ab60c-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-137">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibende Menge und den Betrag nach Abzug der korrigierten Zahlen im Rechnungszeilendetail berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="ab60c-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ab60c-138">Fakturierung des vollen Guthabens einer zuvor in Rechnung gestellten Materialtransaktion.</span><span class="sxs-lookup"><span data-stu-id="ab60c-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-139">Eine in Rechnung gestellte Umsatzstornierung für die Menge und den Betrag in der ursprünglichen Rechnungszeile für das Material.</span><span class="sxs-lookup"><span data-stu-id="ab60c-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-140">Eine neue noch nicht in Rechnung gestellte tatsächliche Verkaufstransaktion für die Menge und den Betrag in der ursprünglichen Rechnungszeile für das Material.</span><span class="sxs-lookup"><span data-stu-id="ab60c-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ab60c-141">Fakturierung der Teilgutschrift für eine Materialtransaktion.</span><span class="sxs-lookup"><span data-stu-id="ab60c-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-142">Eine in Rechnung gestellte Umsatzstornierung für die Menge und den berechneten Betrag in der ursprünglichen Rechnungszeile für das Material.</span><span class="sxs-lookup"><span data-stu-id="ab60c-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-143">Ein neuer nicht in Rechnung gestellter tatsächlicher Umsatz, der für die Menge und den Betrag in den bearbeiteten Rechnungszeilendetails berechnet wird, eine Umkehrung davon und ein gleichwertiger in Rechnung gestellter tatsächlicher Umsatz.</span><span class="sxs-lookup"><span data-stu-id="ab60c-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-144">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibende Menge und den Betrag nach Abzug der korrigierten Zahlen im Rechnungszeilendetail berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="ab60c-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ab60c-145">Fakturierung des vollen Guthabens einer zuvor in Rechnung gestellten Gebührentransaktion</span><span class="sxs-lookup"><span data-stu-id="ab60c-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-146">Eine fakturierte Umsatzumkehrung für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Gebühr</span><span class="sxs-lookup"><span data-stu-id="ab60c-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-147">Ein neuer nicht fakturierter Umsatz-Istwert für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Gebühr</span><span class="sxs-lookup"><span data-stu-id="ab60c-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ab60c-148">Fakturierung der Teilgutschrift einer zuvor in Rechnung gestellten Gebührentransaktion</span><span class="sxs-lookup"><span data-stu-id="ab60c-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-149">Eine fakturierte Umsatzumkehrung für die Menge und den Betrag, die im ursprünglichen Rechnungszeilendetail für die Gebühr in Rechnung gestellt wurde</span><span class="sxs-lookup"><span data-stu-id="ab60c-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-150">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im bearbeiteten korrigierten Rechnungszeilendetail berechnet wird, eine Umkehrung hiervon und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="ab60c-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="ab60c-151">Fakturierung des vollen Guthabens eines zuvor in Rechnung gestellten Meilensteins</span><span class="sxs-lookup"><span data-stu-id="ab60c-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-152">Eine fakturierte Umsatzumkehrung für den Betrag im ursprünglichen Rechnungszeilendetail für den Meilenstein</span><span class="sxs-lookup"><span data-stu-id="ab60c-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="ab60c-153">Der Rechnungsstatus des Meilensteins wird von <b>Gebuchte Kundenrechnung</b> zu <b>Bereit für die Rechnungsstellung</b> aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ab60c-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="ab60c-154">Fakturierung der Teilgutschrift eines zuvor in Rechnung gestellten Meilensteins</span><span class="sxs-lookup"><span data-stu-id="ab60c-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ab60c-155">Dies ist kein unterstütztes Szenario.</span><span class="sxs-lookup"><span data-stu-id="ab60c-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
