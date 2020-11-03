---
title: Eine Proforma-Rechnung bestätigen
description: Diese Thema enthält Informationen zum Bestätigen einer Proforma-Rechnung.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 560bb68cba865a6af60504114126ae6ea73dde2d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076369"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="be6df-103">Eine Proforma-Rechnung bestätigen</span><span class="sxs-lookup"><span data-stu-id="be6df-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="be6df-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="be6df-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="be6df-105">Nachdem eine Proforma-Rechnung bestätigt wurde, wird der Status der Projektrechnung auf **Bestätigt** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="be6df-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="be6df-106">Wenn eine Rechnung bestätigt wird, ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="be6df-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="be6df-107">In Zukunft kann die Rechnung nur korrigiert werden, wenn vom Kunden initiierte Korrekturen oder Gutschriften vorliegen oder wenn sie als bezahlt markiert ist.</span><span class="sxs-lookup"><span data-stu-id="be6df-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="be6df-108">Die folgende Tabelle führt die Istwerte auf, die vom System erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="be6df-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="be6df-109">Diese Istwerte werden erstellt, wenn bestimmte Vorgänge für den Entwurf der Projektrechnung ausgeführt werden, bevor dieser bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="be6df-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="be6df-110">
                    <strong>Szenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be6df-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="be6df-111">
                    <strong>Bei Bestätigung erstellte Istwerte</strong>
                </span><span class="sxs-lookup"><span data-stu-id="be6df-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be6df-112">Fakturierung einer Zeittransaktion ohne Änderungen am Rechnungsentwurf</span><span class="sxs-lookup"><span data-stu-id="be6df-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-113">Eine nicht fakturierte Umsatzumkehrung für die Stunden und den Betrag der ursprünglichen Zeitgenehmigung</span><span class="sxs-lookup"><span data-stu-id="be6df-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-114">Ein fakturierter tatsächlicher Umsatz für die Stunden und den Betrag der ursprünglichen Zeitgenehmigung</span><span class="sxs-lookup"><span data-stu-id="be6df-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="be6df-115">Fakturierung einer Zeittransaktion, die bearbeitet wurde, um die Menge zu reduzieren</span><span class="sxs-lookup"><span data-stu-id="be6df-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-116">Eine nicht fakturierte Umsatzumkehrung für die Stunden und den Betrag der ursprünglichen Zeitgenehmigung</span><span class="sxs-lookup"><span data-stu-id="be6df-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-117">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Stunden und den Betrag in den bearbeiteten Rechnungszeilendetails berechnet wird, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="be6df-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-118">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibenden Stunden und den Betrag nach Abzug der korrigierten Zahlen im bearbeiteten Rechnungszeilendetail nicht fakturierbar ist, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="be6df-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be6df-119">Fakturierung einer Zeittransaktion, die bearbeitet wurde, um die Menge zu erhöhen</span><span class="sxs-lookup"><span data-stu-id="be6df-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-120">Eine nicht fakturierte Umsatzumkehrung für die Stunden und den Betrag der ursprünglichen Zeitgenehmigung</span><span class="sxs-lookup"><span data-stu-id="be6df-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-121">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Stunden und den Betrag in den bearbeiteten Rechnungszeilendetails berechnet wird, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="be6df-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be6df-122">Fakturierung einer Ausgabentransaktion ohne Änderungen am Rechnungsentwurf</span><span class="sxs-lookup"><span data-stu-id="be6df-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-123">Eine nicht fakturierte Umsatzumkehrung für die Menge und den Betrag der ursprünglichen Auftragsgenehmigung</span><span class="sxs-lookup"><span data-stu-id="be6df-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-124">Ein fakturierter tatsächlicher Umsatz für die Menge und den Betrag der ursprünglichen Auftragsgenehmigung</span><span class="sxs-lookup"><span data-stu-id="be6df-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="be6df-125">Fakturierung einer Ausgabentransaktion, die bearbeitet wurde, um die Menge zu reduzieren</span><span class="sxs-lookup"><span data-stu-id="be6df-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-126">Eine nicht fakturierte Umsatzumkehrung für die Menge und den Betrag der ursprünglichen Auftragsgenehmigung</span><span class="sxs-lookup"><span data-stu-id="be6df-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-127">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im bearbeiteten Rechnungszeilendetail berechnet wird, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="be6df-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-128">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibende Menge und den Betrag nach Abzug der korrigierten Zahlen im bearbeiteten Rechnungszeilendetail nicht fakturierbar ist, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="be6df-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be6df-129">Fakturierung einer Ausgabentransaktion, die bearbeitet wurde, um die Menge zu erhöhen</span><span class="sxs-lookup"><span data-stu-id="be6df-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-130">Eine nicht fakturierte Umsatzumkehrung für die Menge und den Betrag der ursprünglichen Auftragsgenehmigung</span><span class="sxs-lookup"><span data-stu-id="be6df-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-131">Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im bearbeiteten Rechnungszeilendetail berechnet wird, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz</span><span class="sxs-lookup"><span data-stu-id="be6df-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="be6df-132">Fakturieren einer Gebühr</span><span class="sxs-lookup"><span data-stu-id="be6df-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-133">Eine nicht fakturierte Umsatzumkehrung für Gebührenbetrag der ursprünglichen Erfassungsposition</span><span class="sxs-lookup"><span data-stu-id="be6df-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-134">Ein fakturierter tatsächlicher Umsatz für die Menge und den Betrag der ursprünglichen Erfassungsposition der Gebühr.</span><span class="sxs-lookup"><span data-stu-id="be6df-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="be6df-135">Fakturierung eines Meilensteins</span><span class="sxs-lookup"><span data-stu-id="be6df-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="be6df-136">Ein in Rechnung gestellter tatsächlicher Umsatz für den Meilensteinbetrag im ursprünglichen Meilenstein in der Projektvertragszeile</span><span class="sxs-lookup"><span data-stu-id="be6df-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
