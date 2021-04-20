---
title: Kreditkartenintegration einrichten
description: In diesem Thema wird erläutert, wie Sie mit kostenbezogenen Kreditkartentransaktionen arbeiten.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866682"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="3e6d1-103">Kreditkartenintegration einrichten</span><span class="sxs-lookup"><span data-stu-id="3e6d1-103">Set up credit card integration</span></span>

<span data-ttu-id="3e6d1-104">_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="3e6d1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3e6d1-105">Ausgabenbezogene Kreditkartentransaktionen können so eingerichtet werden, dass sie automatisch nach einem wiederkehrenden Zeitplan importiert werden.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="3e6d1-106">Alternativ können die Transaktionen bei Bedarf manuell importiert werden.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="3e6d1-107">Die Kreditkartentransaktionen werden über die Dateneinheit Kreditkartentransaktionen importiert.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="3e6d1-108">Kreditkartentransaktionen importieren</span><span class="sxs-lookup"><span data-stu-id="3e6d1-108">Import credit card transactions</span></span>

<span data-ttu-id="3e6d1-109">Gehen Sie folgendermaßen vor, um Kreditkartentransaktionen zu importieren:</span><span class="sxs-lookup"><span data-stu-id="3e6d1-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="3e6d1-110">Auf der Seite **Kreditkartentransaktionen** wählen Sie **Transaktionen importieren**.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="3e6d1-111">Wenn Sie die Datenverwaltung zum ersten Mal öffnen, muss das System die Liste der Datenentitäten aktualisieren, bevor Sie fortfahren können.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="3e6d1-112">Im Feld **Name** geben Sie eine eindeutige Beschreibung für den Importauftrag ein.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="3e6d1-113">In dem Feld **Quelldatenformat** wählen Sie im Feld das Format der Datei aus, die die zu importierenden Kreditkartentransaktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="3e6d1-114">Wählen Sie **Hochladen** u d suchen Sie die zu importierende Datei und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="3e6d1-115">Überprüfen Sie nach dem Hochladen der Datei die Zuordnung der Kreditkartentransaktionsdatei und der Spalten der Entität der Kreditkartentransaktionsdaten, indem Sie den Link **Karte auswählen** auf der Kachel aus.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="3e6d1-116">Wenn Zuordnungsfehler vorliegen oder wenn Sie die Zuordnung ändern müssen, nehmen Sie die Zuordnungsänderungen entweder über die **Mapping-Visualisierung** Registerkarte oder die **Mapping-Details** Registerkarte vor..</span><span class="sxs-lookup"><span data-stu-id="3e6d1-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="3e6d1-117">Um die Kreditkartentransaktionen zu automatisieren, wählen Sie **Erstellen Sie einen wiederkehrenden Datenjob** aus.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="3e6d1-118">Anschließend können Sie die Wiederholung festlegen, die definiert, wie oft Kreditkartentransaktionen importiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="3e6d1-119">Wenn Sie fertig sind, wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="3e6d1-120">Um die ausgewählte Datei jetzt zu importieren, wählen Sie **Importieren**.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="3e6d1-121">Wenn während des Imports Fehler auftreten, können Sie das Ausführungsprotokoll oder die Staging-Daten anzeigen, um die Fehler anzuzeigen, die Sie beheben müssen, um einen erfolgreichen Import sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="3e6d1-122">Wenn Sie mehr als ein Dateiformat importieren müssen, müssen Sie für jeden Formattyp separate Importaufträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="3e6d1-123">Ordnen Sie die Kreditkartentransaktionen für gekündigte Mitarbeiter neu zu</span><span class="sxs-lookup"><span data-stu-id="3e6d1-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="3e6d1-124">Nach Beendigung eines Mitarbeiterdatensatzes ist das Active Directory Domain Services (AD DS) Konto des Mitarbeiters deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="3e6d1-125">Es kann jedoch aktive Kreditkartentransaktionen geben, die noch als Aufwand erfasst und erstattet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="3e6d1-126">Auf der Seite **Kreditkartentransaktionen** können Sie den Mitarbeiter für jede Kreditkartentransaktion neu zuweisen, bei der der zugehörige Mitarbeiter gekündigt wurde.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="3e6d1-127">Wählen Sie eine oder mehrere Kreditkartentransaktionen aus und wählen Sie dann **Transaktionen neu zuweisen** aus.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="3e6d1-128">Sie können dann einen anderen Mitarbeiter auswählen, dem die Kreditkartentransaktionen zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="3e6d1-129">Nachdem die Kreditkartentransaktionen neu zugewiesen wurden, können sie für eine Spesenabrechnung ausgewählt und nach dem üblichen Verfahren für die Erstattung von Spesenabrechnungen bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="3e6d1-130">Kreditkartentransaktionen löschen</span><span class="sxs-lookup"><span data-stu-id="3e6d1-130">Delete credit card transactions</span></span> 

<span data-ttu-id="3e6d1-131">Manchmal müssen nach dem Import von Kreditkartentransaktionen bestimmte Transaktionen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="3e6d1-132">Dies kann daran liegen, dass es sich bei den Transaktionen um Duplikate handelt oder dass die Daten möglicherweise nicht korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="3e6d1-133">Administratoren können die Funktion **Kreditkartentransaktionen löschen** zum Auswählen und Löschen von Kreditkartentransaktionen, die einer Spesenabrechnung **nicht angehängt** sind.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="3e6d1-134">Gehen Sie zu **Periodische Aufgaben** > **Kreditkartentransaktionen löschen**.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="3e6d1-135">Wählen Sie **Filter** und Informationen bereitstellen, um die einzuschließenden Datensätze zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="3e6d1-136">Um die Datensätze zu löschen, wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="3e6d1-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
