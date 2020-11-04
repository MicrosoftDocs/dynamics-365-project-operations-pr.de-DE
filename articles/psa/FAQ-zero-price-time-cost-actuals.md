---
title: Warum ist der Standardpreis bei tatsächlichen Werten für Zeitkosten null?
description: Fehlerbehebung warum der Standardpreis bei tatsächlichen Werten für Zeitkosten null ist.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 44d4952b77ac0a541cdf8e3e55f202c9209efdf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076543"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="8b59f-103">Warum ist der Standardpreis bei tatsächlichen Werten für Zeitkosten null?</span><span class="sxs-lookup"><span data-stu-id="8b59f-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8b59f-104">Dieses FAQ gilt für Ist-Werte, bei denen die Transaktionsklasse auf „Zeit” und der Transaktionstyp auf „Kosten” festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8b59f-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="8b59f-105">Die folgenden drei Überprüfungen helfen bei der Problembehebung, warum der Preis bei Zeitkosten-Ist-Werten 0 ist.</span><span class="sxs-lookup"><span data-stu-id="8b59f-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="8b59f-106">Überprüfung 1: Ermitteln Sie die Kostenpreisliste für das Projekt</span><span class="sxs-lookup"><span data-stu-id="8b59f-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="8b59f-107">Suchen Sie des Projekt im Projektfeld des Ist-Werts und rufen Sie dann die Projektseite auf.</span><span class="sxs-lookup"><span data-stu-id="8b59f-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="8b59f-108">Klicken Sie im Vertragseinheitenlink in das Feld.</span><span class="sxs-lookup"><span data-stu-id="8b59f-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="8b59f-109">Prüfen Sie auf der Vertragseinheitsseite, ob die Vertragseinheit eine Preisliste im Raster der Einstandspreisliste aufweist.</span><span class="sxs-lookup"><span data-stu-id="8b59f-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="8b59f-110">Bei mehr als einer Preisliste haben Sie das Problem isoliert.</span><span class="sxs-lookup"><span data-stu-id="8b59f-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="8b59f-111">Project Service unterstützt nur eine Preisliste pro Organisationseinheit.</span><span class="sxs-lookup"><span data-stu-id="8b59f-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="8b59f-112">Entfernen Sie alle Preislisten aus dieser Entität, bis nur eine Preisliste am Einstandspreislistenraster der Organisationseinheit angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="8b59f-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="8b59f-113">Wenn der Organisationseinheit keine Preislisten angefügt sind, notieren Sie die Währung der Organisationseinheit.</span><span class="sxs-lookup"><span data-stu-id="8b59f-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="8b59f-114">Wechseln Sie zu „Project Service” und dann zu „Parameter” und öffnen Sie die Registerkarte „Preislisten”. Überprüfen Sie, ob es Preislisten mit einem Kontext gibt, der auf „Kosten” festgelegt ist, und der Währung der Organisationseinheit entspricht.</span><span class="sxs-lookup"><span data-stu-id="8b59f-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="8b59f-115">Wenn keine Preislisten vorhanden sind, die diesen Kriterien entsprechen, haben Sie das Problem isoliert.</span><span class="sxs-lookup"><span data-stu-id="8b59f-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="8b59f-116">Stellen Sie sicher, dass Sie mindestens über eine Preisliste verfügen, deren Kontext auf „Kosten” gesetzt ist und deren Währung der Währung der Organisationseinheit entspricht.</span><span class="sxs-lookup"><span data-stu-id="8b59f-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="8b59f-117">Bei mehr als einer Preisliste, die den Kriterien entsprechen, lesen Sie dieses Dokument weiter, um mehr Überprüfungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="8b59f-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="8b59f-118">Überprüfung 2: Gelten irgendwelche der oben identifizierten Preislisten für ein bestimmtes Datum des Zeitkosten-Ist-Werts?</span><span class="sxs-lookup"><span data-stu-id="8b59f-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="8b59f-119">Damit Project Service eine Preisliste als Standardpreis annimmt muss diese Preisliste für das Datum des vertrieblichen Zeitkosten-Ist-Werts gelten.</span><span class="sxs-lookup"><span data-stu-id="8b59f-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="8b59f-120">Überprüfen Sie Folgendes, um zu überprüfen, ob die oben identifizierten Preisliste(n) anwendbar sind:</span><span class="sxs-lookup"><span data-stu-id="8b59f-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="8b59f-121">Überprüfen Sie, ob die Start- und Enddaten auf der Registerkarte „Allgemein” für die angefügten Preisliste nicht leer sind.</span><span class="sxs-lookup"><span data-stu-id="8b59f-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="8b59f-122">Wenn die Start- und Enddaten auf den oben identifizierten Preislisten leer sind, haben Sie das Problem isoliert.</span><span class="sxs-lookup"><span data-stu-id="8b59f-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="8b59f-123">Notieren Sie das Startdatumfeld auf Ihrem vertrieblichen Zeitkosten-Ist-Wert und überprüfen Sie, ob eine der identifizierten Preislisten für das Datum gilt.</span><span class="sxs-lookup"><span data-stu-id="8b59f-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="8b59f-124">Beispielsweise sollte das Datum des Zeitkosten-Ist-Werts innerhalb eines Startdatums und des Enddatums auf der Preisliste liegen.</span><span class="sxs-lookup"><span data-stu-id="8b59f-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="8b59f-125">Wenn keine Preisliste für das Datum im Zeitkosten-Ist-Wert vorhanden ist, haben Sie das Problem isoliert.</span><span class="sxs-lookup"><span data-stu-id="8b59f-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="8b59f-126">Ändern Sie die Start- und Enddaten der Preisliste, um sicherzustellen, dass die Preisliste für das Datum des Zeitkosten-Ist-Werts gilt.</span><span class="sxs-lookup"><span data-stu-id="8b59f-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="8b59f-127">Wenn mehr als eine Preisliste für das Datum im Zeitkosten-Ist-Wert vorhanden ist, haben Sie das Problem isoliert.</span><span class="sxs-lookup"><span data-stu-id="8b59f-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="8b59f-128">Sie können dies beheben, indem Sie die Start- und Enddaten der Preisliste(n) bearbeiten, sodass nur eine Preisliste vorhanden ist, die für das Datum des Zeitkosten-Ist-Werts gilt.</span><span class="sxs-lookup"><span data-stu-id="8b59f-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="8b59f-129">Bei nur einer Preisliste, die den Datums- und Zeitkosten-Ist-Wert abdeckt, machen Sie bei der nächsten Überprüfung im Dokument weiter.</span><span class="sxs-lookup"><span data-stu-id="8b59f-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="8b59f-130">Wenn Sie die erforderlichen Fehlerbehebungen vorgenommen haben, erstellen Sie erneut einen Zeiteintrag, genehmigen Sie ihn und stellen Sie sicher, dass der Zeitkosten-Ist-Wert einen gültigen Preis anzeigt.</span><span class="sxs-lookup"><span data-stu-id="8b59f-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="8b59f-131">Überprüfung 3: Gibt es einen Preis in der Preisliste für die Preisberechnungsdimensionen auf dem Zeitkosten-Ist-Wert?</span><span class="sxs-lookup"><span data-stu-id="8b59f-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="8b59f-132">Wenn Sie Überprüfung 1 und 2 erfolgreich abgeschlossen haben, sollte nur eine Preisliste für das Datum des Zeitkosten-Ist-Werts vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="8b59f-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="8b59f-133">Öffnen Sie diese Preisliste und wechseln Sie zur Registerkarte „Rollenpreise”. Stellen Sie sicher, dass im Raster eine Zeile für die Preisberechnungsdimensionen auf dem Zeitkosten-Ist-Wert vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8b59f-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="8b59f-134">Wenn keine Zeile im Rollenpreisraster für die Preisberechnungsdimensionen auf dem Zeitkosten-Ist-Wert vorhanden ist, haben Sie das Problem isoliert.</span><span class="sxs-lookup"><span data-stu-id="8b59f-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="8b59f-135">Erstellen Sie eine Zeile im Rollenpreisraster für die Preisberechnungsdimensionen auf dem Zeitkosten-Ist-Wert.</span><span class="sxs-lookup"><span data-stu-id="8b59f-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="8b59f-136">Wenn dies durchgeführt ist, erstellen Sie erneut einen Zeiteintrag, genehmigen Sie ihn und stellen Sie sicher, dass der nicht Zeitkosten-Ist-Wert einen gültigen Preis anzeigt.</span><span class="sxs-lookup"><span data-stu-id="8b59f-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="8b59f-137">Wird weiterhin keine gültiger Preis auf Ihrem Zeitkosten-Ist-Wert angezeigt, nachdem alle drei oben genannten Überprüfungen durchgeführt wurden, reichen Sie ein Support-Ticket ein.</span><span class="sxs-lookup"><span data-stu-id="8b59f-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>


