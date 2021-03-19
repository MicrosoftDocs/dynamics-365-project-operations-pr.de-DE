---
title: Prognosemodelle für Projektbudgets erstellen
description: In diesem Thema wird beschrieben, wie Sie ein Prognosemodell für verbleibende Budgets erstellen.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271037"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="7dfd8-103">Prognosemodelle für Projektbudgets erstellen</span><span class="sxs-lookup"><span data-stu-id="7dfd8-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7dfd8-104">In diesem Thema wird beschrieben, wie Sie ein Prognosemodell für verbleibende Budgets erstellen.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="7dfd8-105">Ein Projekt, das der Budgetkontrolle unterliegt, verwendet zwei Arten von Budgets: ursprünglich und verbleibend.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="7dfd8-106">Wenn Sie ein Projektbudget erstellen, müssen Sie die ursprünglichen und verbleibenden Budgetprognosemodelle angeben, die auf der Seite **Prognosemodelle** erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="7dfd8-107">Projektbudgets, die auf den angegebenen Modellen basieren, werden erstellt, wenn Sie das Projektbudget festlegen.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="7dfd8-108">Ein Prognosemodell, das für die Budgetkontrolle verwendet wird, kann kein Untermodell haben oder als Untermodell verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="7dfd8-109">Wählen Sie **Projektmanagement und -buchhaltung** > **Einrichtung** > **Prognosen**  > **Prognosemodelle** aus.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="7dfd8-110">Wählen Sie **Neu** aus, um ein neues Prognosemodell zu erstellen, und geben Sie dann eine Modell-ID-Nummer und einen Namen für das neue Modell ein.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="7dfd8-111">Legen Sie die Option **Angehalten** auf **Ja** fest, um Änderungen an den Prognosezeilen für das Prognosemodell zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="7dfd8-112">Wenn die Prognosezeilen, mit denen das Modell verknüpft ist, Cashflow-Prognosen in der Finanzbuchhaltung generieren sollen, legen Sie **In Cashflowplanungen einbeziehen** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="7dfd8-113">Um das Projektdatum als Rechnungsdatum zu verwenden, legen Sie **Datum der Planungsrechnung** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="7dfd8-114">Wählen Sie im Feld **Budgettyp** eines der folgenden Modelltypen aus:</span><span class="sxs-lookup"><span data-stu-id="7dfd8-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="7dfd8-115">**Ursprüngliches Budget**: Verwenden Sie die ursprünglichen Budgetbeträge, die bei der Erstellung und Genehmigung des ursprünglichen Budgets festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="7dfd8-116">**Übriges Budget**: Verwenden Sie die verbleibenden Budgetbeträge während der Laufzeit des Projekts.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="7dfd8-117">Die Salden in diesem Prognosemodell werden durch tatsächliche Transaktionen reduziert und durch Budgetüberarbeitungen erhöht oder verringert.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="7dfd8-118">**Vortrag**: Verwenden Sie die Vortragsbudgetbeträge für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="7dfd8-119">Ein Vortrag ist ein optionaler Prozess, der ausgeführt werden kann, um nicht verwendete Budgetbeträge von einem Geschäftsjahr in ein anderes zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="7dfd8-120">Legen Sie bei Bedarf die folgenden Optionen fest:</span><span class="sxs-lookup"><span data-stu-id="7dfd8-120">Set the following options as required:</span></span>

   - <span data-ttu-id="7dfd8-121">Aktivieren Sie **Datum der Planungsrechnung**, um das Projektdatum als Rechnungsdatum zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="7dfd8-122">Aktivieren Sie **Planung mit WIP**, um basierend auf WIP zu prognostizieren. Wählen Sie dann die Art der WIP aus.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="7dfd8-123">Sie können die Standardeinstellung für **Budgettyp** als **Keiner** beibehalten, oder einen neuen Typ eingeben.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="7dfd8-124">Der Budgettyp kann nicht geändert werden, nachdem Sie einen Datensatz geändert haben.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="7dfd8-125">Wenn Sie den Standardbudgettyp ändern, stehen alle anderen Optionen nicht mehr für Aktualisierungen zur Verfügung, und Sie können dieses Prognosemodell nicht wiederverwenden.</span><span class="sxs-lookup"><span data-stu-id="7dfd8-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]