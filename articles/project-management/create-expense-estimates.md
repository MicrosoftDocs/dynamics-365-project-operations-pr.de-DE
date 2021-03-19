---
title: Ausgabenschätzungen
description: Dieses Thema enthält Informationen zum Definieren oder Kalkulieren projektbasierter Ausgaben.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3f0429366c69346113003355679c055cd2c74ca3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287057"
---
# <a name="expense-estimates"></a><span data-ttu-id="d85d2-103">Ausgabenschätzungen</span><span class="sxs-lookup"><span data-stu-id="d85d2-103">Expense estimates</span></span>
<span data-ttu-id="d85d2-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="d85d2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d85d2-105">Zusammen mit der Definition von ressourcenbasierten Schätzungen ermöglicht es Dynamics 365 Project Operations Projektmanagern, projektbasierte Ausgaben für jedes Projekt zu definieren.</span><span class="sxs-lookup"><span data-stu-id="d85d2-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="d85d2-106">Jeder Ausgabenposten kann einer bestimmten Projektaufgabe oder Ausgabenkategorie zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="d85d2-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="d85d2-107">Ausgabenkategorien werden normalerweise auf organisatorischer Ebene definiert.</span><span class="sxs-lookup"><span data-stu-id="d85d2-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="d85d2-108">Die Preisgestaltung für jede Ausgabenkategorie wird normalerweise in der folgenden Hierarchie definiert:</span><span class="sxs-lookup"><span data-stu-id="d85d2-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="d85d2-109">Organisation</span><span class="sxs-lookup"><span data-stu-id="d85d2-109">Organization</span></span>
- <span data-ttu-id="d85d2-110">Kunde</span><span class="sxs-lookup"><span data-stu-id="d85d2-110">Customer</span></span>
- <span data-ttu-id="d85d2-111">Angebot/Vertrag</span><span class="sxs-lookup"><span data-stu-id="d85d2-111">Quote/contract</span></span>

<span data-ttu-id="d85d2-112">Führen Sie die folgenden Schritte aus, um Projektkosten anzuzeigen, hinzuzufügen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d85d2-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="d85d2-113">Wechseln Sie zu **Projekte** und wählen Sie das Projekt aus, an dem Sie arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="d85d2-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="d85d2-114">Wählen Sie die Registerkarte **Projektschätzungen** aus und zeigen Sie die Liste der Projektkosten an.</span><span class="sxs-lookup"><span data-stu-id="d85d2-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="d85d2-115">Wählen Sie **Neue Ausgabe** aus, um eine neue Ausgabe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d85d2-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="d85d2-116">Oder wählen Sie eine zu löschende Ausgabe aus und wählen Sie dann **Ausgabe löschen**.</span><span class="sxs-lookup"><span data-stu-id="d85d2-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="d85d2-117">Die folgenden Attribute sind für jede Ausgabenposition definiert:</span><span class="sxs-lookup"><span data-stu-id="d85d2-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="d85d2-118">**Kategorie** : Die gemeinsamen Gruppierungen, mit denen alle für ein Projekt anfallenden Ausgaben beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d85d2-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="d85d2-119">**Anfangsdatum** : Das Datum, an dem die Ausgaben voraussichtlich anfallen werden.</span><span class="sxs-lookup"><span data-stu-id="d85d2-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="d85d2-120">**Menge** : Die geschätzte Anzahl von Ausgabenposten für eine bestimmte Kategorie.</span><span class="sxs-lookup"><span data-stu-id="d85d2-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="d85d2-121">**Stückpreis** : Der Einheitspreis, der zur Berechnung der Ausgabenkosten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d85d2-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="d85d2-122">**Stückverkaufspreis** : Der Einheitspreis, der zur Berechnung des Verkaufspreises verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d85d2-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]