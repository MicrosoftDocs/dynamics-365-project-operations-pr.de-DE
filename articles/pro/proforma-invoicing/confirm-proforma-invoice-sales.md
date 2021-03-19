---
title: Eine Proforma-Rechnung bestätigen – Lite
description: Dieses Thema bietet Informationen zur Bestätigung von Proforma-Rechnungen in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3b1818f20a0d54848939b689f87986154943c57a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274277"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="18db3-103">Eine Proforma-Rechnung bestätigen – Lite</span><span class="sxs-lookup"><span data-stu-id="18db3-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="18db3-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="18db3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="18db3-105">Nachdem eine Proforma-Rechnung bestätigt wurde, wird der Status der Projektrechnung auf **Bestätigt** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="18db3-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="18db3-106">Wenn eine Rechnung bestätigt wird, ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="18db3-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="18db3-107">In Zukunft kann die Rechnung nur korrigiert werden, wenn vom Kunden initiierte Korrekturen oder Gutschriften vorliegen, oder wenn die Rechnung als bezahlt markiert ist.</span><span class="sxs-lookup"><span data-stu-id="18db3-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="18db3-108">Die folgende Tabelle führt die Istwerte auf, die vom System erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="18db3-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="18db3-109">Diese Istwerte werden erstellt, wenn bestimmte Vorgänge für den Entwurf der Projektrechnung ausgeführt werden, bevor dieser bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="18db3-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="18db3-110">
                    <strong>Szenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="18db3-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="18db3-111">
                    <strong>Bei Bestätigung erstellte Istwerte</strong>
                </span><span class="sxs-lookup"><span data-stu-id="18db3-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18db3-112">Fakturierung eines Vorschusses oder einer Vorauszahlung</span><span class="sxs-lookup"><span data-stu-id="18db3-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-113">Ein fakturierter tatsächlicher Umsatz vom Typ <strong>Vorauszahlung</strong> wird für den Betrag im Vorschuss oder in der Vorauszahlung erstellt.</span><span class="sxs-lookup"><span data-stu-id="18db3-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-114">Ein nicht fakturierter tatsächlicher Umsatz eines negativen Betrags der Vorauszahlung oder des Vorschusses, der für die Abstimmung verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="18db3-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18db3-115">Nach vollständiger Abstimmung einer Vorauszahlung oder eines Vorschusses auf eine Rechnung</span><span class="sxs-lookup"><span data-stu-id="18db3-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-116">Eine nicht fakturierte Umsatzumkehrung der Vorauszahlung oder des Vorschusses, der für die Abstimmung erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="18db3-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="18db3-117">Dieser Betrag ist positiv, da er das negative Ergebnis aufheben soll, das bei der Rechnungsstellung der Vorauszahlung oder des Vorschusses erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="18db3-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-118">Ein fakturierter tatsächlicher Umsatz für den Betrag auf dieser Rechnung</span><span class="sxs-lookup"><span data-stu-id="18db3-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="18db3-119">Nach teilweiser Abstimmung einer Vorauszahlung oder eines Vorschusses auf eine Rechnung</span><span class="sxs-lookup"><span data-stu-id="18db3-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-120">Eine nicht fakturierte Umsatzumkehrung der Vorauszahlung oder des Vorschusses, der für die Abstimmung erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="18db3-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="18db3-121">Dieser Betrag ist positiv, da er das negative Ergebnis aufheben soll, das bei der Rechnungsstellung der Vorauszahlung oder des Vorschusses erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="18db3-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-122">Ein fakturierter tatsächlicher Umsatz für den Betrag auf dieser Rechnung</span><span class="sxs-lookup"><span data-stu-id="18db3-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-123">Ein negativer nicht fakturierter tatsächlicher Umsatz des verbleibenden Vorauszahlungs- oder Vorschussbetrags, der zur Abstimmung in künftigen Rechnungen verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="18db3-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18db3-124">Fakturierung einer Zeittransaktion ohne Änderungen am Rechnungsentwurf</span><span class="sxs-lookup"><span data-stu-id="18db3-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-125">Eine nicht fakturierte Umsatzumkehrung für die Stunden und den Betrag der ursprünglichen Zeitgenehmigung</span><span class="sxs-lookup"><span data-stu-id="18db3-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-126">Ein fakturierter tatsächlicher Umsatz für die Stunden und den Betrag der ursprünglichen Zeitgenehmigung</span><span class="sxs-lookup"><span data-stu-id="18db3-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="18db3-127">Fakturierung einer Zeittransaktion, die bearbeitet wurde, um die Menge zu reduzieren</span><span class="sxs-lookup"><span data-stu-id="18db3-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-128">Eine nicht fakturierte Umsatzumkehrung für die Stunden und den Betrag der ursprünglichen Zeitgenehmigung</span><span class="sxs-lookup"><span data-stu-id="18db3-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-129">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Stunden und den Betrag im bearbeiteten Rechnungszeilendetail berechnet wird, eine Umkehrung des tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="18db3-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-130">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibenden Stunden und den Betrag nach Abzug der korrigierten Zahlen im bearbeiteten Rechnungszeilendetail nicht fakturierbar ist, eine Umkehrung des tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="18db3-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18db3-131">Fakturierung einer Zeittransaktion, die bearbeitet wurde, um die Menge zu erhöhen</span><span class="sxs-lookup"><span data-stu-id="18db3-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-132">Eine nicht fakturierte Umsatzumkehrung für die Stunden und den Betrag der ursprünglichen Zeitgenehmigung</span><span class="sxs-lookup"><span data-stu-id="18db3-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-133">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Stunden und den Betrag in den bearbeiteten Rechnungszeilendetails berechnet wird, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="18db3-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18db3-134">Fakturierung einer Ausgabentransaktion ohne Änderungen am Rechnungsentwurf</span><span class="sxs-lookup"><span data-stu-id="18db3-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-135">Eine nicht fakturierte Umsatzumkehrung für die Menge und den Betrag der ursprünglichen Auftragsgenehmigung</span><span class="sxs-lookup"><span data-stu-id="18db3-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-136">Ein fakturierter tatsächlicher Umsatz für die Menge und den Betrag der ursprünglichen Auftragsgenehmigung</span><span class="sxs-lookup"><span data-stu-id="18db3-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="18db3-137">Fakturierung einer Ausgabentransaktion, die bearbeitet wurde, um die Menge zu reduzieren</span><span class="sxs-lookup"><span data-stu-id="18db3-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-138">Eine nicht fakturierte Umsatzumkehrung für die Menge und den Betrag der ursprünglichen Auftragsgenehmigung</span><span class="sxs-lookup"><span data-stu-id="18db3-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-139">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im bearbeiteten Rechnungszeilendetail berechnet wird, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="18db3-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-140">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibende Menge und den Betrag nach Abzug der korrigierten Zahlen im bearbeiteten Rechnungszeilendetail nicht fakturierbar ist, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="18db3-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18db3-141">Fakturierung einer Ausgabentransaktion, die bearbeitet wurde, um die Menge zu erhöhen</span><span class="sxs-lookup"><span data-stu-id="18db3-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-142">Eine nicht fakturierte Umsatzumkehrung für die Menge und den Betrag der ursprünglichen Auftragsgenehmigung</span><span class="sxs-lookup"><span data-stu-id="18db3-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-143">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im bearbeiteten Rechnungszeilendetail berechnet wird, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="18db3-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="18db3-144">Fakturieren einer Gebühr</span><span class="sxs-lookup"><span data-stu-id="18db3-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-145">Eine nicht fakturierte Umsatzumkehrung für Gebührenbetrag der ursprünglichen Erfassungsposition</span><span class="sxs-lookup"><span data-stu-id="18db3-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-146">Ein fakturierter tatsächlicher Umsatz für die Menge und den Betrag der ursprünglichen Erfassungsposition der Gebühr.</span><span class="sxs-lookup"><span data-stu-id="18db3-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="18db3-147">Fakturierung eines Meilensteins</span><span class="sxs-lookup"><span data-stu-id="18db3-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-148">Ein in Rechnung gestellter tatsächlicher Umsatz für den Meilensteinbetrag im ursprünglichen Meilenstein in der Projektvertragszeile</span><span class="sxs-lookup"><span data-stu-id="18db3-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="18db3-149">Fakturieren einer produktbasierenden Vertragszeile</span><span class="sxs-lookup"><span data-stu-id="18db3-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="18db3-150">Ein fakturierter tatsächlicher Umsatz für die Produktzeile mit der Menge und dem Betrag aus der produktbasierten Vertragszeile</span><span class="sxs-lookup"><span data-stu-id="18db3-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]