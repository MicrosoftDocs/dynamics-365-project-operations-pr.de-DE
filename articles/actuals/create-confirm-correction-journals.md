---
title: Korrekturerfassungen erstellen und bestätigen
description: Dieses Thema bietet Informationen zur Vorgehensweise beim Erstellen und Bestätigen von Korrekturerfassungen.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 274f99527804b0db81b26201a22eb5a8cbe86c9a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896955"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="fa409-103">Korrekturerfassungen erstellen und bestätigen</span><span class="sxs-lookup"><span data-stu-id="fa409-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="fa409-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="fa409-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fa409-105">Gelegentlich kommt es vor, dass ein Zeit- oder Kosteneintrag falsch eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fa409-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="fa409-106">Beispielsweise kann ein Berater beim Erstellen eines Zeiteintrags das falsche Datum auswählen oder die Zahlen bei der Eingabe einer Ausgabe umsetzen.</span><span class="sxs-lookup"><span data-stu-id="fa409-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="fa409-107">Wenn ein Berater die übermittelten Einträge nicht aktualisieren kann, kann ein Administrator den Eintrag für ein Projekt direkt korrigieren.</span><span class="sxs-lookup"><span data-stu-id="fa409-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="fa409-108">Sie benötigen Administratorberechtigungen, um die Verfahren in diesem Artikel nachvollziehen zu können.</span><span class="sxs-lookup"><span data-stu-id="fa409-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="fa409-109">Genehmigte Zeiteinträge korrigieren</span><span class="sxs-lookup"><span data-stu-id="fa409-109">Correct approved time entries</span></span>     

<span data-ttu-id="fa409-110">Führen Sie die folgenden Schritte aus, um einzelne oder mehrere Zeiteinträge für ein Projekt zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="fa409-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="fa409-111">In dem Bereich **Vertrieb** wählen Sie **Buchungen** und dann **Genehmigte Zeit** aus.</span><span class="sxs-lookup"><span data-stu-id="fa409-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="fa409-112">Suchen Sie in der Liste **Genehmigte Zeit** einen oder mehrere genehmigte Zeiteinträge, um sie zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="fa409-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="fa409-113">Mit dem Filter können Sie verwandte Einträge suchen.</span><span class="sxs-lookup"><span data-stu-id="fa409-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="fa409-114">Sie können beispielsweise nach einer Projekt-ID filtern und alle genehmigten Zeiteinträge mit dieser Projekt-ID auswählen.</span><span class="sxs-lookup"><span data-stu-id="fa409-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="fa409-115">Wählen Sie **Richtige Einträge** aus.</span><span class="sxs-lookup"><span data-stu-id="fa409-115">Select **Correct entries**.</span></span> <span data-ttu-id="fa409-116">Ein neues Korrekturjournal mit dem zugewiesenen Typ **Zeitkorrektur** wird automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="fa409-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="fa409-117">Die von Ihnen ausgewählten Einträge werden dem Journal hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fa409-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="fa409-118">Geben Sie auf der Seite **Neues Journal** eine **Beschreibung** für Ihr Korrekturjournal ein, und wählen Sie dann die Registerkarte **Zeiteintragskorrekturen** aus.</span><span class="sxs-lookup"><span data-stu-id="fa409-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="fa409-119">Aktualisieren Sie im Abschnitt **Neue Werte für Zeiteinträge** mit den richtigen Informationen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="fa409-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="fa409-120">Sie können beispielsweise das zugewiesene Projekt oder die buchbare Ressource ändern.</span><span class="sxs-lookup"><span data-stu-id="fa409-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="fa409-121">Wählen Sie **Vorschau** aus.</span><span class="sxs-lookup"><span data-stu-id="fa409-121">Select **Preview**.</span></span> <span data-ttu-id="fa409-122">Wählen Sie im Dialogfeld **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="fa409-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="fa409-123">Auf der Registerkarte **Erfassungspositionen** können Sie eine Liste der ursprünglichen Istwerte anzeigen, die sich auf die ausgewählten Zeiteinträge beziehen, die rückgängig gemacht wurden, und die korrigierten entsprechenden Zeilen, die erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="fa409-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="fa409-124">Wenn zusätzliche Korrekturen erforderlich sind, wiederholen Sie die Schritte 5 und 6.</span><span class="sxs-lookup"><span data-stu-id="fa409-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="fa409-125">Alle korrigierten Istwerte haben dieselben Werte, die Sie im Abschnitt **Neue Werte für Zeiteinträge** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="fa409-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="fa409-126">Wenn die Korrekturen wie erwartet angezeigt werden, wählen Sie **Bestätigen** aus.</span><span class="sxs-lookup"><span data-stu-id="fa409-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="fa409-127">Wählen Sie im Dialogfeld **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="fa409-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="fa409-128">Kehren Sie zurück zum Bereich **Vertrieb**, wählen Sie **Projekte** aus, und öffnen Sie dann das Projekt, für das Sie gerade die Zeiteinträge aktualisiert haben.</span><span class="sxs-lookup"><span data-stu-id="fa409-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="fa409-129">Zeigen Sie auf der Seite **Projekte**, auf der Registerkarte **Istwerte** die vorgenommenen Änderungen an.</span><span class="sxs-lookup"><span data-stu-id="fa409-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="fa409-130">Wenn die Registerkarte **Istwerte** nicht sichtbar ist, wählen Sie **Verknüpft** > **Istwerte** aus.</span><span class="sxs-lookup"><span data-stu-id="fa409-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="fa409-131">In der Liste **Zugeordnete Ansicht: Ist-Werte** können Sie sehen, dass die ursprünglichen Zeiteinträge, die rückgängig gemacht wurden, weiterhin aufgelistet sind, ebenso wie die entsprechenden korrigierten Zeiteinträge.</span><span class="sxs-lookup"><span data-stu-id="fa409-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="fa409-132">In der folgenden Grafik sind beispielsweise zwei Werbebuchungen mit einer Menge von 8,00 aufgeführt, deren Belastungen in der Spalte „Betrag“ angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fa409-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="fa409-133">Darüber hinaus gibt es zwei Werbebuchungen mit einer Menge von -8,00, in denen gutgeschriebene Beträge in der Spalte „Betrag“ angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fa409-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="fa409-134">Diese Korrekturen bringen die Menge auf Null.</span><span class="sxs-lookup"><span data-stu-id="fa409-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="fa409-135">Genehmigte Ausgabeneinträge korrigieren</span><span class="sxs-lookup"><span data-stu-id="fa409-135">Correct approved expense entries</span></span>

<span data-ttu-id="fa409-136">Führen Sie die folgenden Schritte aus, um einen oder mehrere Ausgabeneinträge zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="fa409-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="fa409-137">Wählen Sie unter **Vertrieb** im linken Navigationsbereich unter **Buchungen** die Option **Genehmigte Ausgaben** aus.</span><span class="sxs-lookup"><span data-stu-id="fa409-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="fa409-138">Wählen Sie in der Liste **Genehmigte Ausgaben** das Projekt aus, das Sie korrigieren möchten, und klicken Sie dann auf **Richtige Einträge**.</span><span class="sxs-lookup"><span data-stu-id="fa409-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="fa409-139">Ein neues Korrekturjournal mit dem zugewiesenen Typ **Ausgabenkorrektur** wird automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="fa409-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="fa409-140">Geben Sie auf der Seite **Neues Journal** eine **Beschreibung** für die Korrektur ein. Wählen Sie dann auf der Registerkarte **Ausgabenkorrektur** im Abschnitt **Neue Werte für Ausgaben** die Datenfelder aus, die Sie für die ausgewählten Ausgabenpositionen korrigieren möchten.</span><span class="sxs-lookup"><span data-stu-id="fa409-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="fa409-141">Beispielsweise können Sie die Ausgaben einem anderen **Projekt** zuordnen oder die Felder **Ausgabenkategorie**, **Ausgabendatum** oder **Buchbare Ressource** korrigieren.</span><span class="sxs-lookup"><span data-stu-id="fa409-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="fa409-142">Wählen Sie **Vorschau** aus.</span><span class="sxs-lookup"><span data-stu-id="fa409-142">Select **Preview**.</span></span> <span data-ttu-id="fa409-143">Wählen Sie im Dialogfeld **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="fa409-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="fa409-144">Überprüfen Sie die Korrekturen uf der Registerkarte **Erfassungspositionen**. Sie können eine Liste der ursprünglichen Istwerte anzeigen, die sich auf die ausgewählten Ausgabeneinträge beziehen, die rückgängig gemacht wurden, und die korrigierten entsprechenden Zeilen, die erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="fa409-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="fa409-145">Wenn die Korrekturen wie erwartet angezeigt werden, wählen Sie **Bestätigen** aus.</span><span class="sxs-lookup"><span data-stu-id="fa409-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="fa409-146">Wählen Sie im Dialogfeld **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="fa409-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="fa409-147">Wenn die Werte nicht wie erwartet angezeigt werden, wählen Sie **Stornieren** aus, um zur Liste **Genehmigte Ausgaben** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="fa409-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="fa409-148">Wiederholen Sie die Schritte 2 bis 5.</span><span class="sxs-lookup"><span data-stu-id="fa409-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="fa409-149">Die korrigierten Istwerte haben dieselben Werte, die Sie im Abschnitt **Neue Werte für Ausgaben** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="fa409-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="fa409-150">Navigieren Sie nach Bestätigung des Korrekturjournals zurück zu dem oder den aktualisierten Projekten, um Ihre Änderungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fa409-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="fa409-151">Auf der Projektseite, auf der Registerkarte **Istwerte** überprüfen Sie die **Zugeordnete Ansicht: Istwerte**.</span><span class="sxs-lookup"><span data-stu-id="fa409-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="fa409-152">Die ursprünglichen Einträge und die korrigierten Einträge werden aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fa409-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="fa409-153">Die folgende Grafik zeigt die ursprünglichen Ausgabeneinträge und die entsprechenden korrigierten Ausgabeneinträge.</span><span class="sxs-lookup"><span data-stu-id="fa409-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


