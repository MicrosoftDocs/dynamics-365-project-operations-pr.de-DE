---
title: Automatisierte Rechnungserstellung konfigurieren
description: Dieses Thema enthält Informationen zu heißen Ebenen, um das System so zu konfigurieren, dass Rechnungen automatisch generiert werden.
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
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898125"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="daeae-103">Automatisierte Rechnungserstellung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="daeae-103">Configure automated invoice creation</span></span>

<span data-ttu-id="daeae-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="daeae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="daeae-105">Führen Sie die folgenden Schritte aus, um einen automatisierten Rechnungslauf im Projektbetrieb zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="daeae-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="daeae-106">Gehen Sie zu **Einstellungen** \> **Batch-Auftrag**.</span><span class="sxs-lookup"><span data-stu-id="daeae-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="daeae-107">Erstellen Sie einen Batchauftrag und nennen Sie ihn **Projektvorgang zum Erstellen von Rechnungen**.</span><span class="sxs-lookup"><span data-stu-id="daeae-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="daeae-108">Der Name des Batchauftrags muss den Wortlaut Rechnungen erstellen enthalten.</span><span class="sxs-lookup"><span data-stu-id="daeae-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="daeae-109">Wählen Sie im Feld **Auftragstyp** **Keiner** aus.</span><span class="sxs-lookup"><span data-stu-id="daeae-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="daeae-110">Standardmäßig sind die Optionen **Frequenz täglich** und **Ist aktiv** auf **Ja** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="daeae-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="daeae-111">Wählen Sie **Workflow ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="daeae-111">Select **Run Workflow**.</span></span> <span data-ttu-id="daeae-112">Im Dialogfeld **Datensatz nachschlagen** finden Sie drei Workflows:</span><span class="sxs-lookup"><span data-stu-id="daeae-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="daeae-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="daeae-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="daeae-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="daeae-114">ProcessRunner</span></span>
    - <span data-ttu-id="daeae-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="daeae-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="daeae-116">Wählen Sie **ProcessRunCaller** und dann **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="daeae-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="daeae-117">Wählen Sie im nächsten Dialogfeld **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="daeae-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="daeae-118">Einem **Sleep**-Workflow folgt ein **Process** -Workflow.</span><span class="sxs-lookup"><span data-stu-id="daeae-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="daeae-119">In Schritt 5 können Sie auch **ProcessRunner** auswählen.</span><span class="sxs-lookup"><span data-stu-id="daeae-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="daeae-120">Wenn Sie dann **OK** auswählen, folgt auf einen **Process**-Workflow ein **Sleep**-Workflow.</span><span class="sxs-lookup"><span data-stu-id="daeae-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="daeae-121">Die Workflows **ProcessRunCaller** und **ProcessRunner** erstellen Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="daeae-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="daeae-122">**ProcessRunCaller** ruft **ProcessRunner** auf.</span><span class="sxs-lookup"><span data-stu-id="daeae-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="daeae-123">**ProcessRunner** ist der Workflow, der die Rechnungen tatsächlich erstellt.</span><span class="sxs-lookup"><span data-stu-id="daeae-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="daeae-124">Es durchläuft alle Vertragszeilen, für die Rechnungen erstellt werden sollen, und erstellt Rechnungen für diese Zeilen.</span><span class="sxs-lookup"><span data-stu-id="daeae-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="daeae-125">Zur Bestimmung der Vertragszeilen, für die Rechnungen erstellt werden sollen, überprüft der Job die Rechnungsdurchlaufdaten für die Vertragszeilen.</span><span class="sxs-lookup"><span data-stu-id="daeae-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="daeae-126">Wenn Vertragszeilen, die zu einem Vertrag gehören, dasselbe Rechnungsdurchlaufdatum aufweisen, werden die Transaktionen zu einer Rechnung mit zwei Rechnungszeilen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="daeae-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="daeae-127">Wenn keine Transaktionen zum Erstellen von Rechnungen vorhanden sind, überspringt der Job die Rechnungserstellung.</span><span class="sxs-lookup"><span data-stu-id="daeae-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="daeae-128">Nachdem **ProcessRunner** ausgeführt wurde, ruft es **ProcessRunCaller** auf, gibt die Endzeit an und wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="daeae-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="daeae-129">**ProcessRunCaller** startet dann einen Zeitgeber, der ab der angegebenen Endzeit 24 Stunden lang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="daeae-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="daeae-130">Am Ende des Zeitgebers wird **ProcessRunCaller** geschlossen.</span><span class="sxs-lookup"><span data-stu-id="daeae-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="daeae-131">Beim Stapelverarbeitungsjob zum Erstellen von Rechnungen handelt es sich um einen wiederkehrenden Job.</span><span class="sxs-lookup"><span data-stu-id="daeae-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="daeae-132">Wenn diese Stapelverarbeitung mehrmals ausgeführt wird, werden mehrere Instanzen des Jobs erstellt und verursachen Fehler.</span><span class="sxs-lookup"><span data-stu-id="daeae-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="daeae-133">Deshalb sollten Sie die Stapelverarbeitung nur einmal starten und nur dann neu starten, wenn sie nicht mehr ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="daeae-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="daeae-134">Die Stapelabrechnung wird nur für Projektvertragszeilen ausgeführt, die durch Rechnungspläne konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="daeae-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="daeae-135">Für eine Vertragsposition mit einer Festpreis-Abrechnungsmethode müssen Meilensteine konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="daeae-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="daeae-136">Für eine Projektvertragsposition mit einer Zeit- und Materialabrechnungsmethode muss ein datumsbasierter Rechnungszeitplan erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="daeae-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="daeae-137">Gleiches gilt für eine projektbasierte Vertragslinie.</span><span class="sxs-lookup"><span data-stu-id="daeae-137">The same applies to a project-based contract line.</span></span>     
