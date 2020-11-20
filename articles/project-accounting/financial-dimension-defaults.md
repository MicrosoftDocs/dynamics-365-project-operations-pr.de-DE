---
title: Finanzdimensions-Standardeinstellungen
description: Dieses Thema enthält Informationen zum Einrichten von Standardeinstellungen für Finanzdimensionen.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131882"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="2f282-103">Finanzdimensions-Standardeinstellungen</span><span class="sxs-lookup"><span data-stu-id="2f282-103">Financial dimension defaults</span></span>

<span data-ttu-id="2f282-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="2f282-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2f282-105">Dynamics 365 Project Operations verwendet das [Finanzdimensionen](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions)-Framework in Dynamics 365 Finance, um zusätzliche Einblicke in Projekt-Nebenbuch- und Hauptbuchtransaktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2f282-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="2f282-106">Standardmäßige Finanzdimensionen können für einen Kunden, eine Projektfinanzierungsquelle, einen Meilenstein, eine Projektvertragszeile oder ein Projekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2f282-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="2f282-107">Definieren Sie Standardfinanzdimensionen für einen Kunden</span><span class="sxs-lookup"><span data-stu-id="2f282-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="2f282-108">Die Standardeinstellungen für die Kundendimension sind in Finance angegeben.</span><span class="sxs-lookup"><span data-stu-id="2f282-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="2f282-109">Zum Festlegen der Dimensionsstandards müssen Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f282-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="2f282-110">Wechseln Sie zu **Debitorenkonten** > **Debitoren** > **Alle Debitoren**.</span><span class="sxs-lookup"><span data-stu-id="2f282-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="2f282-111">Legen Sie auf der **Kunden**-Seite auf der Registerkarte **Finanzielle Dimensionen** die finanziellen Dimensionswerte für einen bestimmten Kunden fest.</span><span class="sxs-lookup"><span data-stu-id="2f282-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="2f282-112">Definieren Sie Standardfinanzdimensionen für Projektverträge</span><span class="sxs-lookup"><span data-stu-id="2f282-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="2f282-113">Projektverträge werden in Common Data Service (CDS) erstellt und gepflegt.</span><span class="sxs-lookup"><span data-stu-id="2f282-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="2f282-114">Buchhaltungsattribute für Projektverträge werden im **Projektmanagement und Buchhaltung**-Modul in Finance festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2f282-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="2f282-115">Legen Sie finanzielle Dimensionen für eine Projektfinanzierungsquelle fest</span><span class="sxs-lookup"><span data-stu-id="2f282-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="2f282-116">Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Projekte** > **Projektverträge**.</span><span class="sxs-lookup"><span data-stu-id="2f282-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="2f282-117">Wählen Sie den Datensatz aus, den Sie aktualisieren möchten, und wählen Sie auf der **Projektvertrag**-Registerkarte **Standardabrechnung anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f282-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="2f282-118">Erweitern Sie **Verwandte Informationen** und wählen Sie die **Finanzierungsquellen**-Registerkarte aus.</span><span class="sxs-lookup"><span data-stu-id="2f282-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="2f282-119">Legen Sie die Finanzdimensions-Standardeinstellungen fest.</span><span class="sxs-lookup"><span data-stu-id="2f282-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="2f282-120">Beachten Sie, dass die finanziellen Dimensionen standardmäßig vom Kundenkonto ausgehen.</span><span class="sxs-lookup"><span data-stu-id="2f282-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="2f282-121">Legen Sie finanzielle Dimensionen für eine Vertragszeile fest</span><span class="sxs-lookup"><span data-stu-id="2f282-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="2f282-122">Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Projekte** > **Projektverträge**.</span><span class="sxs-lookup"><span data-stu-id="2f282-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="2f282-123">Wählen Sie den Datensatz aus, den Sie aktualisieren möchten, und wählen Sie auf der **Projektvertrag**-Registerkarte **Standardabrechnung anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f282-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="2f282-124">Erweitern Sie **Verwandte Informationen** und wählen Sie die **Vertragszeilen**-Registerkarte aus.</span><span class="sxs-lookup"><span data-stu-id="2f282-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="2f282-125">Legen Sie die Finanzdimensions-Standardeinstellungen fest.</span><span class="sxs-lookup"><span data-stu-id="2f282-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="2f282-126">Die Standardeinstellungen für die finanzielle Dimension gelten und können nur mit Festpreisvertragszeilen (Meilenstein) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f282-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="2f282-127">Diese Standardeinstellungen werden für verwandte Projekttransaktionen und Rechnungspositionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f282-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="2f282-128">Definieren Sie Standardfinanzdimensionen für Projekte</span><span class="sxs-lookup"><span data-stu-id="2f282-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="2f282-129">Projekte werden in CDS erstellt und gepflegt.</span><span class="sxs-lookup"><span data-stu-id="2f282-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="2f282-130">Buchhaltungsattribute für Projekte werden im **Projektmanagement und Buchhaltung**-Modul in Finance festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2f282-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="2f282-131">Wechseln Sie zu **Projektmanagement und -buchhaltung** > **Projekte** > **Alle Projekte**.</span><span class="sxs-lookup"><span data-stu-id="2f282-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="2f282-132">Wählen Sie den Datensatz aus, den Sie aktualisieren möchten, und wählen Sie auf der **Vertrag**-Registerkarte **Standardabrechnung anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f282-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="2f282-133">Erweitern Sie **Verwandte Informationen** und wählen Sie die **Einrichtung**-Registerkarte aus.</span><span class="sxs-lookup"><span data-stu-id="2f282-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="2f282-134">Legen Sie die Finanzdimensions-Standardeinstellungen fest.</span><span class="sxs-lookup"><span data-stu-id="2f282-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="2f282-135">Beachten Sie, dass die finanziellen Dimensionen standardmäßig vom Kundenkonto ausgehen.</span><span class="sxs-lookup"><span data-stu-id="2f282-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="2f282-136">Wenn das Projekt einer Vertragszeile mit mehreren Projektvertragskunden zugeordnet ist, wird der Hauptkunde verwendet, um finanzielle Dimensionen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2f282-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="2f282-137">Die finanziellen Standarddimensionen des Projekts werden verwendet, um die Standardeinstellungen für Journalzeilen für Zeit-, Kosten- und Gebührentransaktionen im **Project Operations-Integrationsjournal** und für verwandte Projektrechnungszeilen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2f282-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
