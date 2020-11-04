---
title: Rechnungsstellungsrückstand für Projekte und Projektverträge überprüfen
description: Dieses Thema enthält Informationen zur Überprüfung von Zeit-, Ausgaben- und Produktrückständen sowie dazu, wie man sie als bereit für die Rechnungsstellung markiert.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076733"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="88139-103">Rechnungsstellungsrückstand für Projekte und Projektverträge überprüfen</span><span class="sxs-lookup"><span data-stu-id="88139-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="88139-104">Wenn eine Transaktion bereit zur Erstellung und Verarbeitung einer Rechnung ist, sollte die Transaktion als **Bereit für die Rechnungsstellung** markiert werden.</span><span class="sxs-lookup"><span data-stu-id="88139-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="88139-105">Dieses Thema beschreibt die Transaktionstypen, die erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="88139-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="88139-106">Abrechnungsrückstand für Zeit und Material überprüfen</span><span class="sxs-lookup"><span data-stu-id="88139-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="88139-107">Wenn ein Zeit- oder Ausgabeneintrag übermittelt und für ein Projekt genehmigt wird, erstellt PSA einen Projekt-Istwert.</span><span class="sxs-lookup"><span data-stu-id="88139-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="88139-108">Wenn die Kombination aus Projekt und Transaktionsklasse für ein Zeit- und Materialprojekt auf eine Vertragszeile abgebildet wird, werden zwei Istwerte erstellt, wenn der Eintrag genehmigt wird:</span><span class="sxs-lookup"><span data-stu-id="88139-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="88139-109">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="88139-109">Cost actual</span></span> 
- <span data-ttu-id="88139-110">Nicht fakturierter Umsatz-Istwert</span><span class="sxs-lookup"><span data-stu-id="88139-110">Unbilled sales actual</span></span>

<span data-ttu-id="88139-111">Nicht fakturierte Umsatz-Istwerte stehen für den Abrechnungsrückstand und ihr Fakturierungsstatus muss auf **Bereit für die Rechnungsstellung** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="88139-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="88139-112">Wenn eine Projektrechnung erstellt wird, werden mit **Bereit für die Rechnungsstellung** markierte, nicht fakturierte Umsatz-Istwerte als Rechnungspositionsdetails in die Rechnung kopiert.</span><span class="sxs-lookup"><span data-stu-id="88139-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="88139-113">Um den Abrechnungsrückstand für Zeit und Materialien zu überprüfen, navigieren Sie zu **Vertrieb** \> **Abrechnung** \> **Abrechnungsrückstand für Zeit und Material überprüfen**.</span><span class="sxs-lookup"><span data-stu-id="88139-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="88139-114">Wählen Sie alle nicht fakturierten Umsatz-Istwerte aus, die abgerechnet werden können, und wählen Sie dann **Bereit für die Rechnungsstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="88139-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="88139-115">Der Fakturierungsstatus dieser Istwerte wird in **Bereit für die Rechnungsstellung** geändert.</span><span class="sxs-lookup"><span data-stu-id="88139-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Abrechnungsrückstand für Zeit- und Material](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="88139-117">Abrechnungsrückstand für das Produkt überprüfen</span><span class="sxs-lookup"><span data-stu-id="88139-117">Review the product billing backlog</span></span>

<span data-ttu-id="88139-118">Wenn ein Projektvertrag über produktbasierte Vertragszeilen verfügt, werden diese Zeilen in PSA für die Rechnungsstellung berücksichtigt, wann immer eine Rechnung für den Projektvertrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="88139-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="88139-119">Jedes Produkt mit Vertragszeilen, die als **Bereit für die Rechnungsstellung** markiert sind, wird als Projektrechnungszeile in die Projektrechnung kopiert.</span><span class="sxs-lookup"><span data-stu-id="88139-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="88139-120">Um den Abrechnungsrückstand für Produkte zu überprüfen, navigieren Sie zu **Vertrieb** \> **Abrechnung** \> **Abrechnungsrückstand für Produkte**.</span><span class="sxs-lookup"><span data-stu-id="88139-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="88139-121">Wählen Sie alle produktbasierten Vertragszeilen aus, die abgerechnet werden können, und wählen Sie dann **Bereit für die Rechnungsstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="88139-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="88139-122">Der Fakturierungsstatus dieser Zeilen wird in **Bereit für die Rechnungsstellung** geändert.</span><span class="sxs-lookup"><span data-stu-id="88139-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Abrechnungsrückstand für Produkte](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="88139-124">Abrechnungsmeilensteine für Festpreisverträge überprüfen</span><span class="sxs-lookup"><span data-stu-id="88139-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="88139-125">Jede Projektvertragszeile mit einer Festpreis-Fakturierungsmethode muss Vertragsmeilensteine definieren.</span><span class="sxs-lookup"><span data-stu-id="88139-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="88139-126">Diese Vertragsmeilensteine können nur dann in Rechnung gestellt werden, wenn sie als **Bereit für die Rechnungsstellung** markiert sind.</span><span class="sxs-lookup"><span data-stu-id="88139-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="88139-127">Um Abrechnungsmeilensteine zu überprüfen, navigieren Sie zu **Vertrieb** \> **Abrechnung** \> **Festpreismeilensteine**.</span><span class="sxs-lookup"><span data-stu-id="88139-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="88139-128">Wählen Sie die Meilensteine aus, die abgerechnet werden können, und wählen Sie dann **Bereit für die Rechnungsstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="88139-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="88139-129">Der Fakturierungsstatus dieser Meilensteine wird in **Bereit für die Rechnungsstellung** geändert.</span><span class="sxs-lookup"><span data-stu-id="88139-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Festpreismeilensteine](media/FPBacklog.png)