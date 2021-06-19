---
title: Zeitplan der Ausgaben für Bundeszuschüsse
description: Diese Thema enthält Informationen zum Zeitplan der Ausgaben der Federal Awards-Anfrage.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010065"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="99c08-103">Zeitplan der Ausgaben für Bundeszuschüsse</span><span class="sxs-lookup"><span data-stu-id="99c08-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99c08-104">Laut Rundschreiben A-133 des Amtes für Verwaltung und Haushalt unterliegen Agenturen, die Bundesmittel erhalten, Prüfungsanforderungen, die auch als Einzelprüfungen bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="99c08-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="99c08-105">Der Prüfungsprozess wird verwendet, um regelmäßig über die Einnahmen und Ausgaben von Bundeszuschüssen zu berichten.</span><span class="sxs-lookup"><span data-stu-id="99c08-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="99c08-106">Ein Teil des Einzelprüfungsberichts enthält die Aufstellung der Ausgaben für Bundeszuschüsse (SEFA).</span><span class="sxs-lookup"><span data-stu-id="99c08-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="99c08-107">Der Zeitplan für Ausgaben der Bundeszuschüsse enthält den Titel und die Nummer des Catalog of Federal Domestic Assistance (CFDA) (CFDA), die Zuschussnummer, das Jahr des Zuschusses, den Namen der Bundesbehörde, die die Mittel bereitstellt, und den Namen der Durchlauf-Entität.</span><span class="sxs-lookup"><span data-stu-id="99c08-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="99c08-108">Die Anfrage ist für einen bestimmten Zeitraum vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="99c08-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="99c08-109">In der Regel entspricht dieser Zeitraum dem Abschlusszeitraum, bei dem es sich um ein Geschäftsjahr handelt.</span><span class="sxs-lookup"><span data-stu-id="99c08-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="99c08-110">Die Anfrage umfasst Zuschüsse mit Projektionsdaten im ausgewählten Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="99c08-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="99c08-111">Die Spalte **Geberbehörde** in der Anfrage zeigt den gebenden Kunden oder bei einem durchlaufenden Zuschuss, die Geberbehörde.</span><span class="sxs-lookup"><span data-stu-id="99c08-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="99c08-112">Bei einem durchlaufenden Zuschuss zeigt die Spalte **Durchlaufbehörde** den gebenden Kunden an.</span><span class="sxs-lookup"><span data-stu-id="99c08-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="99c08-113">Wenn es sich bei dem Zuschuss nicht um einen Durchlaufzuschuss handelt, ist die Spalte **Durchlaufbehörde** leer.</span><span class="sxs-lookup"><span data-stu-id="99c08-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="99c08-114">Die CFDA-Cluster einrichten</span><span class="sxs-lookup"><span data-stu-id="99c08-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="99c08-115">Sie müssen die CFDA-Cluster einrichten, die mit CFDA-Nummern in der Anfrage „Plan der Ausgaben der Bundeszuschüsse“ verknüpft werden können.</span><span class="sxs-lookup"><span data-stu-id="99c08-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="99c08-116">Navigieren Sie zu **Projektmanagement und -buchhaltung \> Einrichtung \> Zuschüsse \> Catalog of Federal Domestic Assistance-Cluster**.</span><span class="sxs-lookup"><span data-stu-id="99c08-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="99c08-117">Wählen Sie **Neu** aus, um das CFDA-Cluster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="99c08-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="99c08-118">Geben Sie den Clusternamen ein.</span><span class="sxs-lookup"><span data-stu-id="99c08-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="99c08-119">Wählen Sie **Speichern** aus, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="99c08-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="99c08-120">CFDA-Nummern einrichten</span><span class="sxs-lookup"><span data-stu-id="99c08-120">Set up CFDA numbers</span></span>

<span data-ttu-id="99c08-121">Sie müssen die CFDA-Nummern einrichten, die Zuschüssen hinzugefügt werden können und die in der Anfrage „Plan der Ausgaben der Bundeszuschüsse“ enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="99c08-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="99c08-122">Navigieren Sie zu **Projektmanagement und -buchhaltung \> Einrichtung \> Zuschüsse \> Catalog of Federal Domestic Assistance-Nummern**.</span><span class="sxs-lookup"><span data-stu-id="99c08-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="99c08-123">Wählen Sie **Neu** aus, um eine CFDA-Nummer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="99c08-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="99c08-124">Geben Sie in der Spalte **Nummer** die CFDA-Nummer ein.</span><span class="sxs-lookup"><span data-stu-id="99c08-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="99c08-125">Drücken Sie die **Tab**-Taste.</span><span class="sxs-lookup"><span data-stu-id="99c08-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="99c08-126">Geben Sie in der Spalte **Beschreibung** den CFDA-Titel ein.</span><span class="sxs-lookup"><span data-stu-id="99c08-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="99c08-127">Drücken Sie die **Tab**-Taste.</span><span class="sxs-lookup"><span data-stu-id="99c08-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="99c08-128">Optional: Fügen Sie im Feld **Programmcluster** den entsprechenden CFDA-Cluster hinzu.</span><span class="sxs-lookup"><span data-stu-id="99c08-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="99c08-129">Wählen Sie **Speichern** aus, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="99c08-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="99c08-130">Zuschüsse einrichten, um diese der Anfrage „Plan der Ausgaben der Bundeszuschüsse“ zu melden</span><span class="sxs-lookup"><span data-stu-id="99c08-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="99c08-131">Navigieren Sie zu **Projektmanagement und -buchhaltung \> Zuschüsse \> Zuschüsse**, und wählen Sie einen vorhandenen Zuschuss aus.</span><span class="sxs-lookup"><span data-stu-id="99c08-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="99c08-132">Weisen Sie im Inforegister **Einrichtung** im Feld **Catalog of Federal Domestic Assistance** die CFDA-Nummer zu.</span><span class="sxs-lookup"><span data-stu-id="99c08-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="99c08-133">Die CFDA-Nummer auf dem Zuschuss bestimmt den CFDA-Cluster für die Meldung.</span><span class="sxs-lookup"><span data-stu-id="99c08-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="99c08-134">Geben Sie im Inforegister **Kontaktinformationen** die Informationen des Gebers ein, indem Sie diese Schritte befolgen:</span><span class="sxs-lookup"><span data-stu-id="99c08-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="99c08-135">Geben Sie im Feld **Zuschusskunde** den Kunden ein, der für den Zuschuss verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="99c08-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="99c08-136">Bei einem vorhandenen Zuschuss sind diese Informationen möglicherweise bereits eingegeben.</span><span class="sxs-lookup"><span data-stu-id="99c08-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="99c08-137">Geben Sie an, ob der Zuschusskunde der Geldgeber ist.</span><span class="sxs-lookup"><span data-stu-id="99c08-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="99c08-138">Wenn der Zuschusskunde der Geldgeber ist, lassen Sie das Kontrollkästchen **Durchlauf** deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="99c08-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="99c08-139">Wenn ein anderer Kunde der Geldgeber ist und der Zuschusskunde für die Ausgabe und Nachverfolgung des Geldes verantwortlich ist, aktivieren Sie die Option **Durchlauf**.</span><span class="sxs-lookup"><span data-stu-id="99c08-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="99c08-140">Wenn Sie das Kontrollkästchen **Durchlauf** im vorherigen Schritt im Feld **Geberbehörde** aktiviert haben, geben Sie den Kunden ein, der den Zuschuss bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="99c08-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="99c08-141">Die Geberbehörde und der Zuschusskunde können nicht derselbe Kunde sein.</span><span class="sxs-lookup"><span data-stu-id="99c08-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="99c08-142">Hier ist ein Beispiel für einen durchlaufenden Zuschuss:</span><span class="sxs-lookup"><span data-stu-id="99c08-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="99c08-143">Die Bundesregierung hat ein Infrastrukturprojekt für einen Staat finanziert.</span><span class="sxs-lookup"><span data-stu-id="99c08-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="99c08-144">Die Bundesregierung gab dem Staat das Geld zum Ausgeben.</span><span class="sxs-lookup"><span data-stu-id="99c08-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="99c08-145">In diesem Fall ist die Bundesregierung die Förderstelle und der Staat der Förderkunde.</span><span class="sxs-lookup"><span data-stu-id="99c08-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="99c08-146">Wenn Sie die Funktion zum ersten Mal aktivieren, werden die anfänglichen CFDA-Nummern unter Verwendung der vorhandenen Nummern für Zuschüsse eingegeben.</span><span class="sxs-lookup"><span data-stu-id="99c08-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="99c08-147">Zuschüsse von der SEFA-Meldung basierend auf der Zuschussart ausschließen</span><span class="sxs-lookup"><span data-stu-id="99c08-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="99c08-148">Navigieren Sie zu **Projektmanagement und -buchhaltung \> Einrichtung \> Zuschüsse \> Zuschusstypen**.</span><span class="sxs-lookup"><span data-stu-id="99c08-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="99c08-149">Aktivieren Sie im Inforegister **Standardinformationen** das Kontrollkästchen **Vom Plan der Ausgaben für Bundeszuschüsse ausschließen**.</span><span class="sxs-lookup"><span data-stu-id="99c08-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="99c08-150">Wählen Sie **Speichern** aus, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="99c08-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="99c08-151">Den Plan für die Ausgaben der Bundeszuschüsse ausführen</span><span class="sxs-lookup"><span data-stu-id="99c08-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="99c08-152">Navigieren Sie zu **Projektmanagement und -buchhaltung \> Abfragen und Berichte \> Zuschussanfrage \> Plan der Ausgaben der Bundeszuschüsse**.</span><span class="sxs-lookup"><span data-stu-id="99c08-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="99c08-153">Befolgen Sie im Abschnitt **Parameter** diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="99c08-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="99c08-154">Wählen Sie im Feld **Datumsintervall** den Code für das Datumsintervall aus.</span><span class="sxs-lookup"><span data-stu-id="99c08-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="99c08-155">Definieren Sie alternativ in den Feldern **Von Datum** und **Bis Datum** das Datumsintervall.</span><span class="sxs-lookup"><span data-stu-id="99c08-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="99c08-156">Optional: Um nur in Rechnung gestellte Transaktionen als Umsatz in die Anfrage einzubeziehen, legen Sie die Option **Nur fakturierte Umsätze einbeziehen** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="99c08-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="99c08-157">Spalten</span><span class="sxs-lookup"><span data-stu-id="99c08-157">Columns</span></span>

<span data-ttu-id="99c08-158">Die Abfrage des Zeitplans der Ausgaben für Bundeszuschüsse umfasst die folgenden Spalten:</span><span class="sxs-lookup"><span data-stu-id="99c08-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="99c08-159">Catalog of Federal Domestic Assistance-Clustername</span><span class="sxs-lookup"><span data-stu-id="99c08-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="99c08-160">Zuschussgeberbehörde</span><span class="sxs-lookup"><span data-stu-id="99c08-160">Grantor agency</span></span>
- <span data-ttu-id="99c08-161">Durchlaufbehörde</span><span class="sxs-lookup"><span data-stu-id="99c08-161">Pass-through agency</span></span>
- <span data-ttu-id="99c08-162">Zuschussname</span><span class="sxs-lookup"><span data-stu-id="99c08-162">Grant name</span></span>
- <span data-ttu-id="99c08-163">Zuschuss-ID</span><span class="sxs-lookup"><span data-stu-id="99c08-163">Grant ID</span></span>
- <span data-ttu-id="99c08-164">Zuschuss-Antrags-ID</span><span class="sxs-lookup"><span data-stu-id="99c08-164">Grant application ID</span></span>
- <span data-ttu-id="99c08-165">Catalog of Federal Domestic Assistance</span><span class="sxs-lookup"><span data-stu-id="99c08-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="99c08-166">Quittungen</span><span class="sxs-lookup"><span data-stu-id="99c08-166">Receipts</span></span>
- <span data-ttu-id="99c08-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99c08-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]