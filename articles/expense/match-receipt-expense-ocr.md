---
title: Einen Beleg mithilfe von OCR an eine Ausgabe anpassen
description: Dieses Thema enthält Informationen zur optischen Zeichenerkennung (OCR) für Quittungen.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897000"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="dd3eb-103">Einen Beleg mithilfe von OCR an eine Ausgabe anpassen</span><span class="sxs-lookup"><span data-stu-id="dd3eb-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="dd3eb-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="dd3eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dd3eb-105">Die Ausgabenerfassung wurde durch die Einführung der optischen Zeichenerkennungsverarbeitung (OCR) für Belege verbessert.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="dd3eb-106">Diese Funktionalität soll die Benutzererfahrung beim Erstellen von Ausgabenabrechnungen verbessern.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="dd3eb-107">Schlüsselfunktionen</span><span class="sxs-lookup"><span data-stu-id="dd3eb-107">Key features</span></span>

- <span data-ttu-id="dd3eb-108">Das System extrahiert den Händlernamen, das Datum und den Gesamtbetrag aus den Belegen.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="dd3eb-109">Das System versucht, nicht angehängte Belege mit nicht angehängten Kostentransaktionen abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="dd3eb-110">Sie können manuell eingegebene Aufwandsbuchungen aus Belegen erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="dd3eb-111">Anhängen von Belegen an eine Spesenabrechnung</span><span class="sxs-lookup"><span data-stu-id="dd3eb-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="dd3eb-112">Führen Sie die folgenden Schritte aus, um beim Erstellen einer Spesenabrechnung automatisch Belege mit Kreditkartentransaktionen anzuhängen.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="dd3eb-113">Öffnen des Arbeitsplatzes **Ausgabenmanagement**.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="dd3eb-114">Auf der Registerkarte **Quittungen** überprüfen Sie auf der Registerkarte, ob nicht angehängte Belege vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="dd3eb-115">Sie können auch Belege auf die Registerkarte **Quittungen** hochladen.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="dd3eb-116">Auf der Registerkarte **Ausgaben** überprüfen Sie, dass  nicht angehängte Ausgaben vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="dd3eb-117">In der Regel importiert der Ausgabenadministrator diese Ausgaben vom Kreditkartenanbieter.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="dd3eb-118">**Neuer Ausgabenbericht** auswählen.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-118">Select **New expense report**.</span></span> <span data-ttu-id="dd3eb-119">Beachten Sie, dass Sie jetzt auch Ausgaben und Belege einbeziehen können, wenn Sie eine Ausgabenabrechnung erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="dd3eb-120">Wenn Sie sowohl Ausgaben als auch Belege hinzufügen, wird ein automatischer Abgleich der Belege mit den Ausgaben ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="dd3eb-121">Belege für einen Ausgabenbericht erstellen oder abgleichen</span><span class="sxs-lookup"><span data-stu-id="dd3eb-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="dd3eb-122">Führen Sie die folgenden Schritte aus, um eine Ausgabe zu erstellen oder eine Ausgabe aus einer Quittung abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="dd3eb-123">Auf einem Ausgabenbericht auf der Registerkarte **Quittungen** fügen Sie eine Quittung hinzu, indem Sie **Quittungen hinzufügen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="dd3eb-124">Beachten Sie unter dem hochgeladenen Bild der Quittung die Optionen **Erstellen** und **Abstimmen**.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="dd3eb-125">Wählen Sie **Erstellen**, um eine manuell eingegebene Aufwandsbuchung zu erstellen und die Werte einzugeben, die aus dem Beleg extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="dd3eb-126">Wenn Sie **Abstimmen** auswählen, versucht das System, eine vorhandene Ausgabe mit der Quittung abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="dd3eb-127">Installation</span><span class="sxs-lookup"><span data-stu-id="dd3eb-127">Installation</span></span>

<span data-ttu-id="dd3eb-128">Um diese erweiteren Ausgabenfunktionen zu nutzen, installieren Sie Ausgabenverwaltungs-Service-Add-In für Microsoft Dynamics 365 Finance und aktivieren Sie die Funktionen in Ihrer Instanz.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="dd3eb-129">Sie können von Ihrem Projekt aus auf das Add-In Microsoft Dynamics Lifecycle Services (LCS) zugreifen.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="dd3eb-130">Melden Sie sich bei LCS an, und öffnen Sie die gewünschte Umgebung.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="dd3eb-131">Gehen Sie zu **Alle Einzelheiten**.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="dd3eb-132">Wählen Sie **Verwalten** oder blättern Sie nach unten zur Registerkarte **Umgebungs-Add-Ins**.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="dd3eb-133">Wählen Sie **Installieren Sie ein neues Add-In**.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="dd3eb-134">Wählen Sie **Ausgabenberwaltungsdienst** aus.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="dd3eb-135">Befolgen Sie die Installationsanleitung und stimmen Sie den Nutzungsbedingungen zu.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="dd3eb-136">Wählen Sie **Installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-136">Select **Install**.</span></span>

<span data-ttu-id="dd3eb-137">In dem Arbeitsbereich **Funktionsverwaltung** aktivieren Sie die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="dd3eb-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="dd3eb-138">Neu gestaltete Ausgabenabrechnungen</span><span class="sxs-lookup"><span data-stu-id="dd3eb-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="dd3eb-139">Automatische Zuordnung und Erstellung von Kosten ab Quittung</span><span class="sxs-lookup"><span data-stu-id="dd3eb-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="dd3eb-140">Wenn Sie diese Funktionen aktivieren, werden die folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="dd3eb-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="dd3eb-141">Der bestehende Arbeitsbereich **Ausgabenmanagement** wird durch den neuen Arbeitsbereich ersetzt.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="dd3eb-142">Ein neuer Menüpunkt für die Sichtbarkeit der Kostenfelder wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="dd3eb-143">Sie können die Seite **Ausgabenbericht** immer noch öffnen. Gehen Sie dazu zu **Ausgabenmanagement > Meine Ausgaben> Ausgabenabrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="dd3eb-144">Workflows und Genehmigungen führen Sie weiterhin zur vorhandenen Seite mit den Ausgabenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="dd3eb-145">Quittungen werden durch Microsoft Azure Cognitive Services verarbeitet und Metadaten werden extrahiert und hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="dd3eb-146">Es wurde eine Option hinzugefügt, mit der Sie eine Ausgabenabrechnung erstellen können, die übereinstimmende, nicht angehängte Belege enthält.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="dd3eb-147">Mit einer Option, die Ausgabenabrechnungen hinzugefügt wird, können Sie eine Ausgabenzeile aus einer Quittung erstellen oder versuchen, eine vorhandene Quittung einer vorhandenen Ausgabenzeile zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="dd3eb-148">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="dd3eb-148">Frequently asked questions</span></span>

<span data-ttu-id="dd3eb-149">**Verwendet Microsoft meine Daten für seine Modelle?**</span><span class="sxs-lookup"><span data-stu-id="dd3eb-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="dd3eb-150">Nein, Microsoft hat ein allgemeines Maschinelles Lernen-Modell für seinen Belegverarbeitungsdienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="dd3eb-151">Dieses Modell basiert nicht auf den von Ihnen hochgeladenen Belegen.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="dd3eb-152">**Wo ist diese Funktion verfügbar und wird sie verarbeitet?**</span><span class="sxs-lookup"><span data-stu-id="dd3eb-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="dd3eb-153">Derzeit werden die USA unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="dd3eb-154">**Wohin gehen meine Quittungen?**</span><span class="sxs-lookup"><span data-stu-id="dd3eb-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="dd3eb-155">Finance wird sich an Cognitive Services wenden, um die Felddaten zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="dd3eb-156">Cognitive Services bewahrt eine Kopie Ihrer Quittung bis zu 24 Stunden lang auf, während die Verarbeitung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="dd3eb-157">Nach Abschluss der Verarbeitung entfernt Cognitive Services die Quittung.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="dd3eb-158">Belege werden weiterhin in Finanzen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dd3eb-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="dd3eb-159">Weitere Informationen finden Sie unter [Aktivieren Sie das Belegverständnis mit der neuen Funktion der Formularerkennung](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="dd3eb-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
