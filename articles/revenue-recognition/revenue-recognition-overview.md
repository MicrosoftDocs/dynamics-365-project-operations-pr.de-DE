---
title: Umsatzrealisierungsübersicht
description: Dieses Thema enthält Informationen zur Umsatzrealisierung in Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531428"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="51114-103">Umsatzrealisierungsübersicht</span><span class="sxs-lookup"><span data-stu-id="51114-103">Revenue recognition overview</span></span>

<span data-ttu-id="51114-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="51114-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="51114-105">In Dynamics 365 Project Operations variieren die Grundsätze für die Umsatzrealisierung je nach ausgewählter Abrechnungsmethode für ein Projekt oder einen Teil des Projekts.</span><span class="sxs-lookup"><span data-stu-id="51114-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="51114-106">Dieses Thema enthält Informationen zur Umsatzrealisierung in Project Operations.</span><span class="sxs-lookup"><span data-stu-id="51114-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="51114-107">Zugeordnete Transaktionen mit Zeit- und Materialabrechnungsmethode</span><span class="sxs-lookup"><span data-stu-id="51114-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="51114-108">Kosten- und Ertragsrealisierung sind miteinander verbunden.</span><span class="sxs-lookup"><span data-stu-id="51114-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="51114-109">Transaktionskosten und nicht abgerechnete Verkäufe werden mit dem [Project Operations-Integrationsjournal](../project-accounting/project-operations-integration-journal.md) gebucht.</span><span class="sxs-lookup"><span data-stu-id="51114-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="51114-110">Das Projektkosten- und Ertragsprofil bestimmt, ob nicht in Rechnung gestellte Verkaufstransaktionen in das Hauptbuch gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="51114-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="51114-111">Wenn **Einnahmen erzielen** ausgewählt ist, verwendet das System den **WIP-Verkaufswert** und die **Aufgelaufene Umsatzerlös**-Konten während der Buchung.</span><span class="sxs-lookup"><span data-stu-id="51114-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="51114-112">Nachfolgend ist ein Beispiel für diese Methode aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="51114-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="51114-113">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="51114-113">Transaction type</span></span> | <span data-ttu-id="51114-114">Soll/Haben</span><span class="sxs-lookup"><span data-stu-id="51114-114">Debit/Credit</span></span> | <span data-ttu-id="51114-115">Betrag</span><span class="sxs-lookup"><span data-stu-id="51114-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="51114-116">WIP-Verkaufswert</span><span class="sxs-lookup"><span data-stu-id="51114-116">WIP Sales value</span></span> | <span data-ttu-id="51114-117">Belastung</span><span class="sxs-lookup"><span data-stu-id="51114-117">Debit</span></span> | <span data-ttu-id="51114-118">100</span><span class="sxs-lookup"><span data-stu-id="51114-118">100</span></span> |
  | <span data-ttu-id="51114-119">Antizipierter Umsatzerlös - Verkaufswert</span><span class="sxs-lookup"><span data-stu-id="51114-119">Accrued revenue sales value</span></span> | <span data-ttu-id="51114-120">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="51114-120">Credit</span></span> | <span data-ttu-id="51114-121">100</span><span class="sxs-lookup"><span data-stu-id="51114-121">100</span></span> |

- <span data-ttu-id="51114-122">Der Umsatz wird bei Rechnungsstellung erfasst.</span><span class="sxs-lookup"><span data-stu-id="51114-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="51114-123">Das System verwendet das **Abgerechnete Einnahmen**-Konto während der Buchung.</span><span class="sxs-lookup"><span data-stu-id="51114-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="51114-124">Nachfolgend ist ein Beispiel für diese Methode aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="51114-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="51114-125">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="51114-125">Transaction type</span></span> | <span data-ttu-id="51114-126">Soll/Haben</span><span class="sxs-lookup"><span data-stu-id="51114-126">Debit/Credit</span></span> | <span data-ttu-id="51114-127">Betrag</span><span class="sxs-lookup"><span data-stu-id="51114-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="51114-128">Kundenguthaben</span><span class="sxs-lookup"><span data-stu-id="51114-128">Customer balance</span></span> | <span data-ttu-id="51114-129">Belastung</span><span class="sxs-lookup"><span data-stu-id="51114-129">Debit</span></span> | <span data-ttu-id="51114-130">120</span><span class="sxs-lookup"><span data-stu-id="51114-130">120</span></span> |
  | <span data-ttu-id="51114-131">Zu zahlende Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="51114-131">Sales tax payable</span></span> | <span data-ttu-id="51114-132">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="51114-132">Credit</span></span> | <span data-ttu-id="51114-133">20</span><span class="sxs-lookup"><span data-stu-id="51114-133">20</span></span> |
  | <span data-ttu-id="51114-134">Rechnungsumsatz</span><span class="sxs-lookup"><span data-stu-id="51114-134">Invoiced Revenue</span></span> | <span data-ttu-id="51114-135">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="51114-135">Credit</span></span> | <span data-ttu-id="51114-136">100</span><span class="sxs-lookup"><span data-stu-id="51114-136">100</span></span> |

- <span data-ttu-id="51114-137">Wenn bei der Buchung der nicht in Rechnung gestellten Verkäufe Umsatzerlöse angefallen sind, storniert das System die aufgelaufenen Umsatzerlöse bei Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="51114-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="51114-138">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="51114-138">Transaction type</span></span> | <span data-ttu-id="51114-139">Soll/Haben</span><span class="sxs-lookup"><span data-stu-id="51114-139">Debit/Credit</span></span> | <span data-ttu-id="51114-140">Betrag</span><span class="sxs-lookup"><span data-stu-id="51114-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="51114-141">WIP-Verkaufswert</span><span class="sxs-lookup"><span data-stu-id="51114-141">WIP Sales value</span></span> | <span data-ttu-id="51114-142">Gutschrift</span><span class="sxs-lookup"><span data-stu-id="51114-142">Credit</span></span> | <span data-ttu-id="51114-143">100</span><span class="sxs-lookup"><span data-stu-id="51114-143">100</span></span> |
  | <span data-ttu-id="51114-144">Antizipierter Umsatzerlös - Verkaufswert</span><span class="sxs-lookup"><span data-stu-id="51114-144">Accrued revenue sales value</span></span> | <span data-ttu-id="51114-145">Belastung</span><span class="sxs-lookup"><span data-stu-id="51114-145">Debit</span></span> | <span data-ttu-id="51114-146">100</span><span class="sxs-lookup"><span data-stu-id="51114-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="51114-147">Zugeordnete Transaktionen mit Festpreisabrechnungsmethode</span><span class="sxs-lookup"><span data-stu-id="51114-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="51114-148">Kosten- und Ertragsrealisierung sind separat.</span><span class="sxs-lookup"><span data-stu-id="51114-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="51114-149">Transaktionskosten werden mit dem [Project Operations-Integrationsjournal](../project-accounting/project-operations-integration-journal.md) gebucht.</span><span class="sxs-lookup"><span data-stu-id="51114-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="51114-150">Nicht in Rechnung gestellte Verkaufstransaktionen werden nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="51114-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="51114-151">Umsatzerlöse können während der Rechnungsstellung erfasst werden, wenn für das Projektkosten- und Umsatzprofil **Prinzip für Projektabschlussberechnungen** auf **Kein WIP** eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="51114-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="51114-152">Verwenden Sie diese Methode nur für kurzfristige, einfache Projekte.</span><span class="sxs-lookup"><span data-stu-id="51114-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="51114-153">Umsatzerlöse können anhand von Festpreisschätzungen mit den Mthoden **Vertrag abgeschlossen** oder **Umsatzrealisierung in Prozent** erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="51114-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51114-154">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="51114-154">Additional resources</span></span>
[<span data-ttu-id="51114-155">Artikel „Buchhaltung für fakturierbare Projekte konfigurieren“</span><span class="sxs-lookup"><span data-stu-id="51114-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="51114-156">Projektvorkalkulation (Festpreis) des Umsatzes</span><span class="sxs-lookup"><span data-stu-id="51114-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="51114-157">Umsatzschätzungen verwalten</span><span class="sxs-lookup"><span data-stu-id="51114-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="51114-158">Methoden für die Kosten zur Fertigstellung</span><span class="sxs-lookup"><span data-stu-id="51114-158">Cost to complete methods</span></span>](cost-complete-methods.md)
