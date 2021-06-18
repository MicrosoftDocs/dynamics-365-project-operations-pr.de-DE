---
title: Standardeinstellungen für Projektvertriebs-Preislisten außer Kraft setzen
description: Dieses Thema enthält Informationen zum Erstellen benutzerdefinierter Verkaufspreislisten.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: db2ff6acaad6ab4cbcc98d3d5b06b36ed23b758f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995080"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="33062-103">Standardeinstellungen für Projektvertriebs-Preislisten außer Kraft setzen</span><span class="sxs-lookup"><span data-stu-id="33062-103">Override project sales price lists</span></span>

<span data-ttu-id="33062-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="33062-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="33062-105">Kundenspezifische Projektpreislisten</span><span class="sxs-lookup"><span data-stu-id="33062-105">Customer-specific project price lists</span></span>

<span data-ttu-id="33062-106">Kundenspezifische Preisvereinbarungen können als Projektpreislisten in einem Kontodatensatz in Dynamics 365 Project Operations eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="33062-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="33062-107">Um eine kundenspezifische Projektpreisliste einzurichten, navigieren Sie im Bereich **Vertrieb** zum Kontodatensatz.</span><span class="sxs-lookup"><span data-stu-id="33062-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="33062-108">Öffnen Sie die **Konten**-Listenseite.</span><span class="sxs-lookup"><span data-stu-id="33062-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="33062-109">Suchen Sie einen Kundendatensatz und doppelklicken Sie darauf, um die **Konto**-Detailseite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="33062-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="33062-110">Wählen Sie auf der **Projektpreislisten**-Registerkarte **+ Neue Projektpreisliste hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="33062-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="33062-111">Auf der Seite **Neue Projektpreisliste** wählen Sie eine Preisliste aus der Dropdown-Liste aus.</span><span class="sxs-lookup"><span data-stu-id="33062-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="33062-112">Nur Preislisten, für die der Kontext auf **Vertrieb** festgelegt ist und deren Währung mit der Kontowährung übereinstimmt, sind enthalten.</span><span class="sxs-lookup"><span data-stu-id="33062-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="33062-113">Geben Sie einen Namen für die Zuordnung ein, und wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="33062-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="33062-114">Es wird eine kundenspezifische Projektpreisliste erstellt.</span><span class="sxs-lookup"><span data-stu-id="33062-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="33062-115">Diese Preisliste wird verwendet, um Projektpreise für Projektangebote oder Verträge, die für diesen Kunden erstellt wurden, als Standard festzulegen, wenn das Erstellungsdatum des Angebots oder des Projektvertrags innerhalb des Datums der Gültigkeitsdauer der Preisliste liegt.</span><span class="sxs-lookup"><span data-stu-id="33062-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="33062-116">Benutzerdefinierte Preisgestaltung für Projektangebote</span><span class="sxs-lookup"><span data-stu-id="33062-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="33062-117">In Projektangeboten können Sie Projektpreise festlegen, die mit einer Standardpreisliste beginnen, die standardmäßig vom Kunden oder von den Projektparametern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="33062-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="33062-118">Wenn Sie benutzerdefinierte Preise für projektbezogene Arbeiten an einem bestimmten Angebot benötigen, können Sie diese aus den zugehörigen Entitäten der Projektpreislisten abrufen.</span><span class="sxs-lookup"><span data-stu-id="33062-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="33062-119">Führen Sie die folgenden Schritte aus, um die angebotsspezifische Projektpreisgestaltung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="33062-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="33062-120">Öffnen Sie im Projektangebot die Registerkarte **Projektpreislisten**.</span><span class="sxs-lookup"><span data-stu-id="33062-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="33062-121">Wählen Sie im Untergitter **Benutzerdefinierte Preisberechnung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="33062-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="33062-122">Alle dem Angebot beigefügten Projektpreislisten werden in neue Preislisten kopiert.</span><span class="sxs-lookup"><span data-stu-id="33062-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="33062-123">Die Namen der neuen Preislisten geben den Namen des Angebots mit einem Datums-/Zeitstempel für die Erstellung dieser Preislisten wieder.</span><span class="sxs-lookup"><span data-stu-id="33062-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="33062-124">Sie können jede dieser Preislisten verwenden und die Preise für Arbeit (Rollenpreis) und Kosten (Kategoriepreis) aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="33062-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="33062-125">Diese Preise gelten nur für dieses Projektangebot.</span><span class="sxs-lookup"><span data-stu-id="33062-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="33062-126">Preislisten in einem Projektvertrag</span><span class="sxs-lookup"><span data-stu-id="33062-126">Price lists on a project contract</span></span>

<span data-ttu-id="33062-127">Bei einem Projektvertrag wird die Projektpreisgestaltung standardmäßig immer als benutzerdefinierte Preisliste mit dem Namen des Vertrags und dem an den Namen angehängten erstellten Datums- und Zeitstempel verwendet.</span><span class="sxs-lookup"><span data-stu-id="33062-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="33062-128">Dies gilt unabhängig davon, ob der Vertrag zum Zeitpunkt des Gewinns des Angebots erstellt wurde oder ob der Vertrag von Grund auf neu erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="33062-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="33062-129">Bei Bedarf können Sie diese Zuordnung zur benutzerdefinierten Preisliste entfernen und stattdessen dem Projektvertrag eine Standardpreisliste zuordnen.</span><span class="sxs-lookup"><span data-stu-id="33062-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="33062-130">Wenn Sie den Projektpreislisten auf Angebot oder Vertrag eine Standardpreisliste zuordnen, wirken sich Änderungen an den Preisen in der Preisliste auf alle Angebote und Verträge aus, die die Preisliste verwenden.</span><span class="sxs-lookup"><span data-stu-id="33062-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]