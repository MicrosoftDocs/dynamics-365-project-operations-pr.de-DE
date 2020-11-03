---
title: Massenkorrekturen von Istwerten, die durch genehmigte Zeit- und Kosteneinträge erstellt wurden
description: In diesem Thema wird erläutert, wie ein Administrator Einzel- oder Massenkorrekturen an zuvor genehmigten Zeit- oder Kosteneinträgen vornehmen kann, wenn die Abrechnung nicht abgeschlossen ist.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 6d6c03cc74d47ca3ae7c2bd7d0aa0720bb2f3c01
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076700"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="b5826-103">Massenkorrekturen von Istwerten, die durch genehmigte Zeit- und Kosteneinträge erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="b5826-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

<span data-ttu-id="b5826-104">Gelegentlich kommt es vor, dass ein Zeit- oder Kosteneintrag falsch eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b5826-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="b5826-105">Beispielsweise kann ein Berater beim Erstellen eines Zeiteintrags das falsche Datum auswählen oder die Zahlen bei der Eingabe einer Ausgabe umsetzen.</span><span class="sxs-lookup"><span data-stu-id="b5826-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="b5826-106">Wenn ein Berater die übermittelten Einträge nicht aktualisieren kann, kann ein Administrator den Eintrag für ein Projekt direkt korrigieren.</span><span class="sxs-lookup"><span data-stu-id="b5826-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="b5826-107">Sie benötigen Administratorberechtigungen, um die Verfahren in diesem Artikel nachvollziehen zu können.</span><span class="sxs-lookup"><span data-stu-id="b5826-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="b5826-108">Genehmigte Zeiteinträge korrigieren</span><span class="sxs-lookup"><span data-stu-id="b5826-108">Correct approved time entries</span></span>     

<span data-ttu-id="b5826-109">Führen Sie die folgenden Schritte aus, um einzelne oder mehrere Zeiteinträge für ein Projekt zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="b5826-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="b5826-110">In dem Bereich **Vertrieb** wählen Sie **Buchungen** und dann **Genehmigte Zeit** aus.</span><span class="sxs-lookup"><span data-stu-id="b5826-110">In the **Sales** area, select **Transactions** , and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="b5826-111">Suchen Sie in der Liste **Genehmigte Zeit** einen oder mehrere genehmigte Zeiteinträge, um sie zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="b5826-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="b5826-112">Mit dem Filter können Sie verwandte Einträge suchen.</span><span class="sxs-lookup"><span data-stu-id="b5826-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="b5826-113">Sie können beispielsweise nach einer Projekt-ID filtern und alle genehmigten Zeiteinträge mit dieser Projekt-ID auswählen.</span><span class="sxs-lookup"><span data-stu-id="b5826-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="b5826-114">Wählen Sie **Richtige Einträge** aus.</span><span class="sxs-lookup"><span data-stu-id="b5826-114">Select **Correct entries**.</span></span> <span data-ttu-id="b5826-115">Ein neues Korrekturjournal mit dem zugewiesenen Typ **Zeitkorrektur** wird automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="b5826-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="b5826-116">Die von Ihnen ausgewählten Einträge werden dem Journal hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b5826-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="b5826-117">Geben Sie auf der Seite **Neues Journal** eine **Beschreibung** für Ihr Korrekturjournal ein, und wählen Sie dann die Registerkarte **Zeiteintragskorrekturen** aus.</span><span class="sxs-lookup"><span data-stu-id="b5826-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="b5826-118">Aktualisieren Sie im Abschnitt **Neue Werte für Zeiteinträge** mit den richtigen Informationen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="b5826-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="b5826-119">Sie können beispielsweise das zugewiesene Projekt oder die buchbare Ressource ändern.</span><span class="sxs-lookup"><span data-stu-id="b5826-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="b5826-120">Wählen Sie **Vorschau** aus.</span><span class="sxs-lookup"><span data-stu-id="b5826-120">Select **Preview**.</span></span> <span data-ttu-id="b5826-121">Wählen Sie im Dialogfeld **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b5826-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="b5826-122">Auf der Registerkarte **Erfassungspositionen** können Sie eine Liste der ursprünglichen Istwerte anzeigen, die sich auf die ausgewählten Zeiteinträge beziehen, die rückgängig gemacht wurden, und die korrigierten entsprechenden Zeilen, die erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b5826-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="b5826-123">Wenn zusätzliche Korrekturen erforderlich sind, wiederholen Sie die Schritte 5 und 6.</span><span class="sxs-lookup"><span data-stu-id="b5826-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="b5826-124">Alle korrigierten Istwerte haben dieselben Werte, die Sie im Abschnitt **Neue Werte für Zeiteinträge** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="b5826-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="b5826-125">Wenn die Korrekturen wie erwartet angezeigt werden, wählen Sie **Bestätigen** aus.</span><span class="sxs-lookup"><span data-stu-id="b5826-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="b5826-126">Wählen Sie im Dialogfeld **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b5826-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="b5826-127">Kehren Sie zurück zum Bereich **Vertrieb** , wählen Sie **Projekte** aus, und öffnen Sie dann das Projekt, für das Sie gerade die Zeiteinträge aktualisiert haben.</span><span class="sxs-lookup"><span data-stu-id="b5826-127">Return to the **Sales** area, select **Projects** , and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="b5826-128">Zeigen Sie auf der Seite **Projekte** , auf der Registerkarte **Istwerte** die vorgenommenen Änderungen an.</span><span class="sxs-lookup"><span data-stu-id="b5826-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="b5826-129">Wenn die Registerkarte **Istwerte** nicht sichtbar ist, wählen Sie **Verknüpft** > **Istwerte** aus.</span><span class="sxs-lookup"><span data-stu-id="b5826-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="b5826-130">In der Liste **Zugeordnete Ansicht: Ist-Werte** können Sie sehen, dass die ursprünglichen Zeiteinträge, die rückgängig gemacht wurden, weiterhin aufgelistet sind, ebenso wie die entsprechenden korrigierten Zeiteinträge.</span><span class="sxs-lookup"><span data-stu-id="b5826-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="b5826-131">In der folgenden Grafik sind beispielsweise zwei Werbebuchungen mit einer Menge von 8,00 aufgeführt, deren Belastungen in der Spalte „Betrag“ angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b5826-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="b5826-132">Darüber hinaus gibt es zwei Werbebuchungen mit einer Menge von -8,00, in denen gutgeschriebene Beträge in der Spalte „Betrag“ angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b5826-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="b5826-133">Diese Korrekturen bringen die Menge auf Null.</span><span class="sxs-lookup"><span data-stu-id="b5826-133">These corrections bring the quantity to zero.</span></span>

![Zugeordnete Ansicht: Istwerte](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="b5826-135">Genehmigte Ausgabeneinträge korrigieren</span><span class="sxs-lookup"><span data-stu-id="b5826-135">Correct approved expense entries</span></span>

<span data-ttu-id="b5826-136">Führen Sie die folgenden Schritte aus, um einen oder mehrere Ausgabeneinträge zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="b5826-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="b5826-137">Wählen Sie unter **Vertrieb** im linken Navigationsbereich unter **Buchungen** die Option **Genehmigte Ausgaben** aus.</span><span class="sxs-lookup"><span data-stu-id="b5826-137">In the **Sales** area, in the left navigation pane, under **Transactions** , select **Approved Expenses**.</span></span>

2. <span data-ttu-id="b5826-138">Wählen Sie in der Liste **Genehmigte Ausgaben** das Projekt aus, das Sie korrigieren möchten, und klicken Sie dann auf **Richtige Einträge**.</span><span class="sxs-lookup"><span data-stu-id="b5826-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="b5826-139">Ein neues Korrekturjournal mit dem zugewiesenen Typ **Ausgabenkorrektur** wird automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="b5826-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="b5826-140">Geben Sie auf der Seite **Neues Journal** eine **Beschreibung** für die Korrektur ein. Wählen Sie dann auf der Registerkarte **Ausgabenkorrektur** im Abschnitt **Neue Werte für Ausgaben** die Datenfelder aus, die Sie für die ausgewählten Ausgabenpositionen korrigieren möchten.</span><span class="sxs-lookup"><span data-stu-id="b5826-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="b5826-141">Beispielsweise können Sie die Ausgaben einem anderen **Projekt** zuordnen oder die Felder **Ausgabenkategorie** , **Ausgabendatum** oder **Buchbare Ressource** korrigieren.</span><span class="sxs-lookup"><span data-stu-id="b5826-141">For example, you can assign the expense to another **Project** , or correct the **Expense Category** , **Expense Date** , or **Bookable Resource**.</span></span>

4. <span data-ttu-id="b5826-142">Wählen Sie **Vorschau** aus.</span><span class="sxs-lookup"><span data-stu-id="b5826-142">Select **Preview**.</span></span> <span data-ttu-id="b5826-143">Wählen Sie im Dialogfeld **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b5826-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="b5826-144">Überprüfen Sie die Korrekturen uf der Registerkarte **Erfassungspositionen**. Sie können eine Liste der ursprünglichen Istwerte anzeigen, die sich auf die ausgewählten Ausgabeneinträge beziehen, die rückgängig gemacht wurden, und die korrigierten entsprechenden Zeilen, die erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b5826-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="b5826-145">Wenn die Korrekturen wie erwartet angezeigt werden, wählen Sie **Bestätigen** aus.</span><span class="sxs-lookup"><span data-stu-id="b5826-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="b5826-146">Wählen Sie im Dialogfeld **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b5826-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="b5826-147">Wenn die Werte nicht wie erwartet angezeigt werden, wählen Sie **Stornieren** aus, um zur Liste **Genehmigte Ausgaben** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="b5826-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="b5826-148">Wiederholen Sie die Schritte 2 bis 5.</span><span class="sxs-lookup"><span data-stu-id="b5826-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="b5826-149">Die korrigierten Istwerte haben dieselben Werte, die Sie im Abschnitt **Neue Werte für Ausgaben** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="b5826-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="b5826-150">Navigieren Sie nach Bestätigung des Korrekturjournals zurück zu dem oder den aktualisierten Projekten, um Ihre Änderungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b5826-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="b5826-151">Auf der Projektseite, auf der Registerkarte **Istwerte** überprüfen Sie die **Zugeordnete Ansicht: Istwerte**.</span><span class="sxs-lookup"><span data-stu-id="b5826-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="b5826-152">Die ursprünglichen Einträge und die korrigierten Einträge werden aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b5826-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="b5826-153">Die folgende Grafik zeigt die ursprünglichen Ausgabeneinträge und die entsprechenden korrigierten Ausgabeneinträge.</span><span class="sxs-lookup"><span data-stu-id="b5826-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Tatsächliche Ausgaben](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
