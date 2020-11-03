---
title: Kreditkartentransaktionen importieren und verwalten
description: In diesem Thema wird erläutert, wie kostenbezogene Kreditkartentransaktionen importiert und verwaltet werden. Diese Transaktionen können so eingerichtet werden, dass sie automatisch nach einem wiederkehrenden Zeitplan importiert werden, oder sie können bei Bedarf manuell importiert werden.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6cec15e436bc699e361577c970dd5845c6c68908
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076677"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="f7805-104">Kreditkartentransaktionen importieren und verwalten</span><span class="sxs-lookup"><span data-stu-id="f7805-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7805-105">Ausgabenbezogene Kreditkartentransaktionen können so eingerichtet werden, dass sie automatisch nach einem wiederkehrenden Zeitplan importiert werden.</span><span class="sxs-lookup"><span data-stu-id="f7805-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="f7805-106">Alternativ können die Transaktionen bei Bedarf manuell importiert werden.</span><span class="sxs-lookup"><span data-stu-id="f7805-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="f7805-107">Die Kreditkartentransaktionen werden über die Dateneinheit Kreditkartentransaktionen importiert.</span><span class="sxs-lookup"><span data-stu-id="f7805-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="f7805-108">Weitere Informationen zu Datenentitäten finden Sie unter [Datenentitäten](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="f7805-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="f7805-109">Kreditkartentransaktionen importieren</span><span class="sxs-lookup"><span data-stu-id="f7805-109">Import credit card transactions</span></span>

1. <span data-ttu-id="f7805-110">Auf der Seite **Kreditkartentransaktionen** wählen Sie **Transaktionen importieren**.</span><span class="sxs-lookup"><span data-stu-id="f7805-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="f7805-111">Wenn Sie die Datenverwaltung zum ersten Mal öffnen, muss das System die Liste der Datenentitäten aktualisieren, bevor Sie fortfahren können.</span><span class="sxs-lookup"><span data-stu-id="f7805-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="f7805-112">Geben Sie im Feld **Name** eine eindeutige Beschreibung des Importauftrags ein.</span><span class="sxs-lookup"><span data-stu-id="f7805-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="f7805-113">In dem Feld **Quelldatenformat** wählen Sie im Feld das Format der Datei aus, die die zu importierenden Kreditkartentransaktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="f7805-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="f7805-114">Wählen Sie **Hochladen** u d suchen Sie die zu importierende Datei und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="f7805-114">Select **Upload** , and then find and select the file to import.</span></span>
5. <span data-ttu-id="f7805-115">Überprüfen Sie nach dem Hochladen der Datei die Zuordnung der Kreditkartentransaktionsdatei und der Spalten der Entität der Kreditkartentransaktionsdaten, indem Sie den Link **Karte auswählen** auf der Kachel aus.</span><span class="sxs-lookup"><span data-stu-id="f7805-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="f7805-116">Wenn Zuordnungsfehler vorliegen oder wenn Sie die Zuordnung ändern müssen, nehmen Sie die Zuordnungsänderungen entweder über die **Mapping-Visualisierung** Registerkarte oder die **Mapping-Details** Registerkarte vor..</span><span class="sxs-lookup"><span data-stu-id="f7805-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="f7805-117">Um die Kreditkartentransaktionen zu automatisieren, wählen Sie **Erstellen Sie einen wiederkehrenden Datenjob** aus.</span><span class="sxs-lookup"><span data-stu-id="f7805-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="f7805-118">Anschließend können Sie die Wiederholung festlegen, die definiert, wie oft Kreditkartentransaktionen importiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7805-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="f7805-119">Wenn Sie fertig sind, wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f7805-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="f7805-120">Um die ausgewählte Datei jetzt zu importieren, wählen Sie **Importieren**.</span><span class="sxs-lookup"><span data-stu-id="f7805-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="f7805-121">Wenn während des Imports Fehler auftreten, können Sie das Ausführungsprotokoll oder die Staging-Daten anzeigen, um die Fehler anzuzeigen, die Sie beheben müssen, um einen erfolgreichen Import zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="f7805-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="f7805-122">Wenn Sie mehr als ein Dateiformat importieren müssen, müssen Sie für jeden Formattyp separate Importaufträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7805-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="f7805-123">Ordnen Sie die Kreditkartentransaktionen für gekündigte Mitarbeiter neu zu</span><span class="sxs-lookup"><span data-stu-id="f7805-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="f7805-124">Nach Beendigung eines Mitarbeiterdatensatzes ist das Active Directory Domain Services (AD DS) Konto des Mitarbeiters deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f7805-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="f7805-125">Es kann jedoch aktive Kreditkartentransaktionen geben, die noch als Aufwand erfasst und erstattet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f7805-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="f7805-126">Von der Seite **Kreditkartentransaktionen** können Sie den Mitarbeiter für jede Kreditkartentransaktion neu zuweisen, bei der der zugehörige Mitarbeiter gekündigt wurde.</span><span class="sxs-lookup"><span data-stu-id="f7805-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="f7805-127">Wählen Sie eine oder mehrere Kreditkartentransaktionen aus und wählen Sie dann **Transaktionen neu zuweisen** aus.</span><span class="sxs-lookup"><span data-stu-id="f7805-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="f7805-128">Sie können dann einen anderen Mitarbeiter auswählen, dem die Kreditkartentransaktionen zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7805-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="f7805-129">Nachdem die Kreditkartentransaktionen neu zugewiesen wurden, können sie für eine Spesenabrechnung ausgewählt und nach dem üblichen Verfahren für die Erstattung von Spesenabrechnungen bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="f7805-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
