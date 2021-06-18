---
title: Ausgabenbelegverarbeitung
description: Dieses Thema enthält Informationen zur optischen Zeichenerkennung (OCR) für Quittungen. Diese Funktionalität soll die Benutzererfahrung beim Erstellen von Spesenabrechnungen verbessern, die in Microsoft Dynamics 365 Finance erstellt wurden.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ed9c97ba9cc505106599c2896dc2112358d0c408
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993505"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="c2c85-104">Ausgabenbelegverarbeitung</span><span class="sxs-lookup"><span data-stu-id="c2c85-104">Expense receipt processing</span></span>

<span data-ttu-id="c2c85-105">Die Ausgabenerfassung wurde durch die Einführung der optischen Zeichenerkennungsverarbeitung (OCR) für Belege verbessert.</span><span class="sxs-lookup"><span data-stu-id="c2c85-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="c2c85-106">Diese Funktionalität soll die Benutzererfahrung beim Erstellen von Spesenabrechnungen verbessern.</span><span class="sxs-lookup"><span data-stu-id="c2c85-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="c2c85-107">Schlüsselfunktionen</span><span class="sxs-lookup"><span data-stu-id="c2c85-107">Key features</span></span>

- <span data-ttu-id="c2c85-108">Der Händlername, das Datum und der Gesamtbetrag werden aus den Belegen extrahiert.</span><span class="sxs-lookup"><span data-stu-id="c2c85-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="c2c85-109">Die Funktion versucht, nicht angehängte Belege mit nicht angehängten Kostentransaktionen abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="c2c85-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="c2c85-110">Benutzer können manuell eingegebene Ausgabentransaktionen aus Belegen erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2c85-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="c2c85-111">Verwendungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="c2c85-111">Usage examples</span></span>

<span data-ttu-id="c2c85-112">Führen Sie die folgenden Schritte aus, um beim Erstellen einer Spesenabrechnung automatisch Belege mit Kreditkartentransaktionen anzuhängen.</span><span class="sxs-lookup"><span data-stu-id="c2c85-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="c2c85-113">Öffnen des Arbeitsplatzes **Ausgabenmanagement**.</span><span class="sxs-lookup"><span data-stu-id="c2c85-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="c2c85-114">Auf der Registerkarte **Quittungen** überprüfen Sie auf der Registerkarte, ob nicht angehängte Belege vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c2c85-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="c2c85-115">Sie können auch Belege auf die Registerkarte **Quittungen** hochladen.</span><span class="sxs-lookup"><span data-stu-id="c2c85-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="c2c85-116">Auf der Registerkarte **Ausgaben** überprüfen Sie, dass  nicht angehängte Ausgaben vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c2c85-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="c2c85-117">In der Regel importiert der Ausgabenadministrator diese Ausgaben vom Kreditkartenanbieter.</span><span class="sxs-lookup"><span data-stu-id="c2c85-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="c2c85-118">**Neuer Ausgabenbericht** auswählen.</span><span class="sxs-lookup"><span data-stu-id="c2c85-118">Select **New expense report**.</span></span> <span data-ttu-id="c2c85-119">Beachten Sie, dass Sie jetzt auch Ausgaben und Belege einbeziehen können, wenn Sie eine Ausgabenabrechnung erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2c85-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="c2c85-120">Wenn Sie sowohl Ausgaben als auch Belege hinzufügen, wird ein automatischer Abgleich der Belege mit den Ausgaben ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="c2c85-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="c2c85-121">Führen Sie die folgenden Schritte aus, um eine Ausgabe zu erstellen oder eine Ausgabe aus einer Quittung abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="c2c85-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="c2c85-122">Auf einem Ausgabenbericht auf der Registerkarte **Quittungen** fügen Sie eine Quittung hinzu, indem Sie **Quittungen hinzufügen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="c2c85-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="c2c85-123">Beachten Sie unter dem hochgeladenen Bild der Quittung die Optionen **Erstellen** und **Abstimmen**.</span><span class="sxs-lookup"><span data-stu-id="c2c85-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="c2c85-124">Wählen Sie **Erstellen**, um eine manuell eingegebene Aufwandsbuchung zu erstellen und die Werte einzugeben, die aus dem Beleg extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="c2c85-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="c2c85-125">Wenn Sie **Abstimmen** auswählen, versucht das System, eine vorhandene Ausgabe mit der Quittung abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="c2c85-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="c2c85-126">Installation</span><span class="sxs-lookup"><span data-stu-id="c2c85-126">Installation</span></span>

<span data-ttu-id="c2c85-127">Diese Funktion funktioniert in Kombination mit der Funktion **Neu gestaltete Spesenabrechnungen** zur Vereinfachung der Kostenerfahrung.</span><span class="sxs-lookup"><span data-stu-id="c2c85-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="c2c85-128">Diese Funktion ist nur für Umgebungen mit Tier 2+ verfügbar, bei denen es sich um Sandbox und Produktion handelt.</span><span class="sxs-lookup"><span data-stu-id="c2c85-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="c2c85-129">Um diese erweiteren Ausgabenfunktionen zu nutzen, installieren Sie Ausgabenverwaltungs-Service-Add-In für Microsoft Dynamics 365 Finance und aktivieren Sie die Funktionen in Ihrer Instanz.</span><span class="sxs-lookup"><span data-stu-id="c2c85-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="c2c85-130">Sie können von Ihrem Projekt aus auf das Add-In Microsoft Dynamics Lifecycle Services (LCS) zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c2c85-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="c2c85-131">Melden Sie sich bei LCS an, und öffnen Sie die gewünschte Umgebung.</span><span class="sxs-lookup"><span data-stu-id="c2c85-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="c2c85-132">Gehen Sie zu **Alle Einzelheiten**.</span><span class="sxs-lookup"><span data-stu-id="c2c85-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="c2c85-133">Wählen Sie **Verwalten** oder blättern Sie nach unten zur Registerkarte **Umgebungs-Add-Ins**.</span><span class="sxs-lookup"><span data-stu-id="c2c85-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="c2c85-134">Wählen Sie **Installieren Sie ein neues Add-In**.</span><span class="sxs-lookup"><span data-stu-id="c2c85-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="c2c85-135">Wählen Sie **Ausgabenberwaltungsdienst** aus.</span><span class="sxs-lookup"><span data-stu-id="c2c85-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="c2c85-136">Befolgen Sie die Installationsanleitung und stimmen Sie den Nutzungsbedingungen zu.</span><span class="sxs-lookup"><span data-stu-id="c2c85-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="c2c85-137">Wählen Sie **Installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="c2c85-137">Select **Install**.</span></span>

<span data-ttu-id="c2c85-138">In dem Arbeitsbereich **Funktionsverwaltung** aktivieren Sie die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="c2c85-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="c2c85-139">Neu gestaltete Ausgabenabrechnungen</span><span class="sxs-lookup"><span data-stu-id="c2c85-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="c2c85-140">Automatische Zuordnung und Erstellung von Kosten ab Quittung</span><span class="sxs-lookup"><span data-stu-id="c2c85-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="c2c85-141">Wenn Sie diese Funktionen aktivieren, werden die folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="c2c85-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="c2c85-142">Der bestehende Arbeitsbereich **Ausgabenmanagement** wird durch den neuen Arbeitsbereich ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c2c85-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="c2c85-143">Ein neuer Menüpunkt für die Sichtbarkeit der Kostenfelder wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c2c85-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="c2c85-144">Sie können die Seite **Ausgabenbericht** immer noch öffnen. Gehen Sie dazu zu **Ausgabenmanagement > Meine Ausgaben> Ausgabenabrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="c2c85-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="c2c85-145">Workflows und Genehmigungen führen Sie weiterhin zur vorhandenen Seite mit den Ausgabenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="c2c85-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="c2c85-146">Quittungen werden durch Microsoft Azure Cognitive Services verarbeitet und Metadaten werden extrahiert und hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c2c85-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="c2c85-147">Es wurde eine Option hinzugefügt, mit der Sie eine Ausgabenabrechnung erstellen können, die übereinstimmende, nicht angehängte Belege enthält.</span><span class="sxs-lookup"><span data-stu-id="c2c85-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="c2c85-148">Mit einer Option, die Ausgabenabrechnungen hinzugefügt wird, können Sie eine Ausgabenzeile aus einer Quittung erstellen oder versuchen, eine vorhandene Quittung einer vorhandenen Ausgabenzeile zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c2c85-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="c2c85-149">Weitere Informationen zu der überarbeiteten Funktion „Spesenabrechnungen“ finden Sie unter [Neu gestaltete Spesenabrechnungen](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="c2c85-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="c2c85-150">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="c2c85-150">Frequently asked questions</span></span>

<span data-ttu-id="c2c85-151">**Verwendet Microsoft meine Daten für seine Modelle?**</span><span class="sxs-lookup"><span data-stu-id="c2c85-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="c2c85-152">Nein, Microsoft hat ein allgemeines Maschinelles Lernen-Modell für seinen Belegverarbeitungsdienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="c2c85-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="c2c85-153">Dieses Modell basiert nicht auf den von Ihnen hochgeladenen Belegen.</span><span class="sxs-lookup"><span data-stu-id="c2c85-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="c2c85-154">**Wo ist diese Funktion verfügbar und wird sie verarbeitet?**</span><span class="sxs-lookup"><span data-stu-id="c2c85-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="c2c85-155">Derzeit werden die USA unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2c85-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="c2c85-156">**Wohin gehen meine Quittungen?**</span><span class="sxs-lookup"><span data-stu-id="c2c85-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="c2c85-157">Finance wird sich an Cognitive Services wenden, um die Felddaten zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="c2c85-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="c2c85-158">Cognitive Services bewahrt eine Kopie Ihrer Quittung bis zu 24 Stunden lang auf, während die Verarbeitung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c2c85-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="c2c85-159">Nach Abschluss der Verarbeitung entfernt Cognitive Services die Quittung.</span><span class="sxs-lookup"><span data-stu-id="c2c85-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="c2c85-160">Belege werden weiterhin in Finanzen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c2c85-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="c2c85-161">Weitere Informationen finden Sie unter [Aktivieren Sie das Belegverständnis mit der neuen Funktion der Formularerkennung](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="c2c85-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]