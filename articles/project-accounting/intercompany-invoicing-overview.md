---
title: Intercompany-Rechnungsstellung – Übersicht
description: Dieses Thema enthält Informationen und Beispiele zur Intercompany-Rechnungsstellung für Projekte.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42af89105f8325f1c94df6d2133d2c329facf2b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002640"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="87305-103">Intercompany-Rechnungsstellung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="87305-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="87305-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="87305-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="87305-105">Ihre Organisation verfügt möglicherweise über mehrere Abteilungen, Tochterunternehmen und andere juristische Personen, die Produkte und Dienstleistungen für Projekte untereinander übertragen.</span><span class="sxs-lookup"><span data-stu-id="87305-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="87305-106">Die juristische Person, die die Dienstleistung oder das Produkt erbringt, wird als *kreditgebende juristische Person* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="87305-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="87305-107">Die juristische Person, die die Dienstleistung oder das Produkt erhält, wird als *kreditnehmende juristische Person* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="87305-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="87305-108">Die folgende Abbildung zeigt ein typisches Szenario, in dem zwei juristische Personen Contoso Robotics USA (die kreditnehmende juristische Person) und Contoso Robotics UK (die verleihende juristische Person) Ressourcen teilen, um ein Projekt für den Kunden zu liefern, Adventure works.</span><span class="sxs-lookup"><span data-stu-id="87305-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="87305-109">Für dieses Szenario wird Contoso Robotics USA beauftragt, die Arbeit an Adventure Works zu liefern.</span><span class="sxs-lookup"><span data-stu-id="87305-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Intercompany-Rechnungsstellung](./media/IntercompanyScenario.png) 

<span data-ttu-id="87305-111">Dynamics 365 Project Operations verwendet den folgenden Ablauf, um Intercompany-Transaktionen zu verarbeiten:</span><span class="sxs-lookup"><span data-stu-id="87305-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="87305-112">Ressourcen der kreditgebenden juristischen Person erfassen Intercompany-Zeit- oder -Aufwandsvorgänge, indem sie Zeit und Kosten für Projekte in der kreditnehmenden juristischen Person buchen.</span><span class="sxs-lookup"><span data-stu-id="87305-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="87305-113">Zeit- und Kostenkosten werden im kreditgebenden Unternehmen anhand der Stückkostenpreisliste des kreditnehmenden Unternehmens erfasst.</span><span class="sxs-lookup"><span data-stu-id="87305-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="87305-114">Nicht in Rechnung gestellte Intercompany-Vertriebstransaktionen werden im kreditgebenden Unternehmen anhand der Stückkostenpreisliste des kreditnehmenden Unternehmens erfasst.</span><span class="sxs-lookup"><span data-stu-id="87305-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="87305-115">Nicht in Rechnung gestellte Einnahmen werden im kreditnehmenden Unternehmen anhand der Verkaufspreisliste für Projektverträge erfasst.</span><span class="sxs-lookup"><span data-stu-id="87305-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="87305-116">Dem Kunden kann eine Rechnung gestellt werden, wenn nicht abgerechnete Einnahmen erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="87305-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="87305-117">Der Kunde muss nicht warten, bis die Intercompany-Rechnungsverarbeitung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="87305-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="87305-118">Intercompany-Kundenrechnungen werden regelmäßig im kreditgebenden Unternehmen erstellt.</span><span class="sxs-lookup"><span data-stu-id="87305-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="87305-119">Die Rechnungen werden manuell oder in regelmäßigen Abständen erstellt.</span><span class="sxs-lookup"><span data-stu-id="87305-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="87305-120">Für jede kreditnehmende juristische Person kann eine einzelne Rechnung erstellt werden, oder es können separate Rechnungen pro Projekt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="87305-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="87305-121">Wenn die Intercompany-Debitorenrechnung in der kreditgebenden juristischen Person gebucht wird, wird die entsprechende ausstehende Kreditorenrechnung in der kreditnehmenden juristischen Person gebucht.</span><span class="sxs-lookup"><span data-stu-id="87305-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="87305-122">Die Kosten in der ausstehenden Kreditorenrechnung werden bei der Buchung der Rechnung im Nebenbuch des Projekts erfasst.</span><span class="sxs-lookup"><span data-stu-id="87305-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="87305-123">Das folgende Diagramm zeigt die Intercompany-Rechnungsstellung in Bezug auf Buchhaltungsereignisse und erwartete Buchungen im Hauptbuch.</span><span class="sxs-lookup"><span data-stu-id="87305-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Intercompany-Flow](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="87305-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="87305-125">Additional resources</span></span>

- [<span data-ttu-id="87305-126">Intercompany-Rechnungsstellung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="87305-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="87305-127">Intercompany-Transaktionen aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="87305-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="87305-128">Intercompany-Debitoren- und -Kreditorenrechnungen erstellen</span><span class="sxs-lookup"><span data-stu-id="87305-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]