---
title: Ausgabenschätzungen
description: Dieses Thema enthält Informationen zum Definieren oder Kalkulieren projektbasierter Ausgaben.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076446"
---
# <a name="expense-estimates"></a><span data-ttu-id="14554-103">Ausgabenschätzungen</span><span class="sxs-lookup"><span data-stu-id="14554-103">Expense estimates</span></span>
<span data-ttu-id="14554-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="14554-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="14554-105">Mit Dynamics 365 Project Operations können Projektmanager nicht nur ressourcenbasierte Schätzungen definieren, sondern auch projektbasierte Ausgaben für jedes Projekt definieren.</span><span class="sxs-lookup"><span data-stu-id="14554-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="14554-106">Jeder Ausgabenposten kann einer bestimmten Projektaufgabe oder Ausgabenkategorie zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="14554-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="14554-107">Ausgabenkategorien werden normalerweise auf organisatorischer Ebene definiert.</span><span class="sxs-lookup"><span data-stu-id="14554-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="14554-108">Die Preisgestaltung für jede Ausgabenkategorie wird normalerweise in der folgenden Hierarchie definiert:</span><span class="sxs-lookup"><span data-stu-id="14554-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="14554-109">Organisation</span><span class="sxs-lookup"><span data-stu-id="14554-109">Organization</span></span>
- <span data-ttu-id="14554-110">Kunde</span><span class="sxs-lookup"><span data-stu-id="14554-110">Customer</span></span>
- <span data-ttu-id="14554-111">Angebot/Vertrag</span><span class="sxs-lookup"><span data-stu-id="14554-111">Quote/contract</span></span>

<span data-ttu-id="14554-112">Führen Sie die folgenden Schritte aus, um Projektkosten anzuzeigen, hinzuzufügen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="14554-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="14554-113">Wechseln Sie zu **Projekte** und wählen Sie das Projekt aus, an dem Sie arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="14554-113">Go to **Projects** , and select the project you want to work on.</span></span>
2. <span data-ttu-id="14554-114">Wählen Sie die Registerkarte **Projektschätzungen** aus und zeigen Sie die Liste der Projektkosten an.</span><span class="sxs-lookup"><span data-stu-id="14554-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="14554-115">Wählen Sie **Neue Ausgabe** aus, um eine neue Ausgabe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="14554-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="14554-116">Oder wählen Sie eine zu löschende Ausgabe aus und wählen Sie dann **Ausgabe löschen**.</span><span class="sxs-lookup"><span data-stu-id="14554-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="14554-117">Die folgenden Attribute sind für jede Ausgabenposition definiert:</span><span class="sxs-lookup"><span data-stu-id="14554-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="14554-118">**Kategorie** : Die gemeinsamen Gruppierungen, mit denen alle für ein Projekt anfallenden Ausgaben beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="14554-118">**Category** : The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="14554-119">**Anfangsdatum** : Das Datum, an dem die Ausgaben voraussichtlich anfallen werden.</span><span class="sxs-lookup"><span data-stu-id="14554-119">**Start Date** : The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="14554-120">**Menge** : Die geschätzte Anzahl von Ausgabenposten für eine bestimmte Kategorie.</span><span class="sxs-lookup"><span data-stu-id="14554-120">**Quantity** : The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="14554-121">**Stückpreis** : Der Einheitspreis, der zur Berechnung der Ausgabenkosten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14554-121">**Unit Cost Price** : The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="14554-122">**Stückverkaufspreis** : Der Einheitspreis, der zur Berechnung des Verkaufspreises verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14554-122">**Unit Sales Price** : The unit price used to calculate the sale prices of the expense.</span></span>
