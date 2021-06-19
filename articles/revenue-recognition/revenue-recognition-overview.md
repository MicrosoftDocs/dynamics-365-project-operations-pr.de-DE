---
title: Umsatzrealisierungsübersicht
description: Dieses Thema enthält Informationen zur Umsatzrealisierung in Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013755"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="c2b6f-103">Umsatzrealisierungsübersicht</span><span class="sxs-lookup"><span data-stu-id="c2b6f-103">Revenue recognition overview</span></span>

<span data-ttu-id="c2b6f-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="c2b6f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c2b6f-105">In Dynamics 365 Project Operations variieren die Grundsätze für die Umsatzrealisierung je nach ausgewählter Abrechnungsmethode für ein Projekt oder einen Teil des Projekts.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="c2b6f-106">Dieses Thema enthält Informationen zur Umsatzrealisierung in Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="c2b6f-107">Zugeordnete Transaktionen mit Zeit- und Materialabrechnungsmethode</span><span class="sxs-lookup"><span data-stu-id="c2b6f-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="c2b6f-108">Kosten- und Ertragsrealisierung sind miteinander verbunden.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="c2b6f-109">Transaktionskosten und nicht abgerechnete Verkäufe werden mit dem [Project Operations-Integrationsjournal](../project-accounting/project-operations-integration-journal.md) gebucht.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="c2b6f-110">Das Projektkosten- und Ertragsprofil bestimmt, ob nicht in Rechnung gestellte Verkaufstransaktionen in das Hauptbuch gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="c2b6f-111">Wenn **Einnahmen erzielen** ausgewählt ist, verwendet das System den **WIP-Verkaufswert** und die **Aufgelaufene Umsatzerlös**-Konten während der Buchung.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="c2b6f-112">Folgend sehen Sie ein Beispiel für diese Methode.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="c2b6f-113">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="c2b6f-113">Transaction type</span></span> | <span data-ttu-id="c2b6f-114">Soll/Haben</span><span class="sxs-lookup"><span data-stu-id="c2b6f-114">Debit/Credit</span></span> | <span data-ttu-id="c2b6f-115">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2b6f-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="c2b6f-116">WIP-Verkaufswert</span><span class="sxs-lookup"><span data-stu-id="c2b6f-116">WIP Sales value</span></span> | <span data-ttu-id="c2b6f-117">Soll</span><span class="sxs-lookup"><span data-stu-id="c2b6f-117">Debit</span></span> | <span data-ttu-id="c2b6f-118">100</span><span class="sxs-lookup"><span data-stu-id="c2b6f-118">100</span></span> |
  | <span data-ttu-id="c2b6f-119">Antizipierter Umsatzerlös - Verkaufswert</span><span class="sxs-lookup"><span data-stu-id="c2b6f-119">Accrued revenue sales value</span></span> | <span data-ttu-id="c2b6f-120">Haben</span><span class="sxs-lookup"><span data-stu-id="c2b6f-120">Credit</span></span> | <span data-ttu-id="c2b6f-121">100</span><span class="sxs-lookup"><span data-stu-id="c2b6f-121">100</span></span> |

- <span data-ttu-id="c2b6f-122">Umsatzerlöse werden bei der Rechnungsstellung erfasst.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="c2b6f-123">Das System verwendet das **Abgerechnete Einnahmen**-Konto während der Buchung.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="c2b6f-124">Folgend sehen Sie ein Beispiel für diese Methode.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="c2b6f-125">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="c2b6f-125">Transaction type</span></span> | <span data-ttu-id="c2b6f-126">Soll/Haben</span><span class="sxs-lookup"><span data-stu-id="c2b6f-126">Debit/Credit</span></span> | <span data-ttu-id="c2b6f-127">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2b6f-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="c2b6f-128">Kundenguthaben</span><span class="sxs-lookup"><span data-stu-id="c2b6f-128">Customer balance</span></span> | <span data-ttu-id="c2b6f-129">Belastung</span><span class="sxs-lookup"><span data-stu-id="c2b6f-129">Debit</span></span> | <span data-ttu-id="c2b6f-130">120</span><span class="sxs-lookup"><span data-stu-id="c2b6f-130">120</span></span> |
  | <span data-ttu-id="c2b6f-131">Zu zahlende Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="c2b6f-131">Sales tax payable</span></span> | <span data-ttu-id="c2b6f-132">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="c2b6f-132">Credit</span></span> | <span data-ttu-id="c2b6f-133">20</span><span class="sxs-lookup"><span data-stu-id="c2b6f-133">20</span></span> |
  | <span data-ttu-id="c2b6f-134">Rechnungsumsatz</span><span class="sxs-lookup"><span data-stu-id="c2b6f-134">Invoiced Revenue</span></span> | <span data-ttu-id="c2b6f-135">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="c2b6f-135">Credit</span></span> | <span data-ttu-id="c2b6f-136">100</span><span class="sxs-lookup"><span data-stu-id="c2b6f-136">100</span></span> |

- <span data-ttu-id="c2b6f-137">Wenn bei der Buchung der nicht in Rechnung gestellten Verkäufe Umsatzerlöse angefallen sind, storniert das System die aufgelaufenen Umsatzerlöse bei Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="c2b6f-138">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="c2b6f-138">Transaction type</span></span> | <span data-ttu-id="c2b6f-139">Soll/Haben</span><span class="sxs-lookup"><span data-stu-id="c2b6f-139">Debit/Credit</span></span> | <span data-ttu-id="c2b6f-140">Betrag</span><span class="sxs-lookup"><span data-stu-id="c2b6f-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="c2b6f-141">WIP-Verkaufswert</span><span class="sxs-lookup"><span data-stu-id="c2b6f-141">WIP Sales value</span></span> | <span data-ttu-id="c2b6f-142">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="c2b6f-142">Credit</span></span> | <span data-ttu-id="c2b6f-143">100</span><span class="sxs-lookup"><span data-stu-id="c2b6f-143">100</span></span> |
  | <span data-ttu-id="c2b6f-144">Antizipierter Umsatzerlös - Verkaufswert</span><span class="sxs-lookup"><span data-stu-id="c2b6f-144">Accrued revenue sales value</span></span> | <span data-ttu-id="c2b6f-145">Belastung</span><span class="sxs-lookup"><span data-stu-id="c2b6f-145">Debit</span></span> | <span data-ttu-id="c2b6f-146">100</span><span class="sxs-lookup"><span data-stu-id="c2b6f-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="c2b6f-147">Zugeordnete Transaktionen mit Festpreisabrechnungsmethode</span><span class="sxs-lookup"><span data-stu-id="c2b6f-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="c2b6f-148">Kosten- und Ertragsrealisierung sind separat.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="c2b6f-149">Transaktionskosten werden mit dem [Project Operations-Integrationsjournal](../project-accounting/project-operations-integration-journal.md) gebucht.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="c2b6f-150">Nicht in Rechnung gestellte Verkaufstransaktionen werden nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="c2b6f-151">Umsatzerlöse können während der Rechnungsstellung erfasst werden, wenn für das Projektkosten- und Umsatzprofil **Prinzip für Projektabschlussberechnungen** auf **Kein WIP** eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="c2b6f-152">Verwenden Sie diese Methode nur für kurzfristige, einfache Projekte.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="c2b6f-153">Umsatzerlöse können anhand von Festpreisschätzungen mit den Mthoden **Vertrag abgeschlossen** oder **Umsatzrealisierung in Prozent** erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="c2b6f-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2b6f-154">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c2b6f-154">Additional resources</span></span>
[<span data-ttu-id="c2b6f-155">Artikel „Buchhaltung für fakturierbare Projekte konfigurieren“</span><span class="sxs-lookup"><span data-stu-id="c2b6f-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="c2b6f-156">Projektvorkalkulation (Festpreis) des Umsatzes</span><span class="sxs-lookup"><span data-stu-id="c2b6f-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="c2b6f-157">Umsatzschätzungen verwalten</span><span class="sxs-lookup"><span data-stu-id="c2b6f-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="c2b6f-158">Methoden für die Kosten zur Fertigstellung</span><span class="sxs-lookup"><span data-stu-id="c2b6f-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]