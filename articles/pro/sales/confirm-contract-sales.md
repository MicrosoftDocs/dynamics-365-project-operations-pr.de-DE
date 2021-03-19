---
title: Projektvertrag bestätigen
description: Dieses Thema enthält Informationen zum Bestätigen eines Vertrags in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d807d3631f40a93ec7dbd918b64c287fd4875c79
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273827"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="3539a-103">Projektvertrag bestätigen</span><span class="sxs-lookup"><span data-stu-id="3539a-103">Confirm a project contract</span></span>

<span data-ttu-id="3539a-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="3539a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3539a-105">In Dynamics 365 Project Operations kann ein Projektvertrag mit dem Grund **Bestätigt** aktiv oder mit dem Grund **Verloren** geschlossen sein.</span><span class="sxs-lookup"><span data-stu-id="3539a-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="3539a-106">Wenn Sie einen Projektvertrag bestätigen, wird der Status von **Entwurf** in **Aktiv** aktualisiert, und der Statusgrund lautet **Bestätigt**.</span><span class="sxs-lookup"><span data-stu-id="3539a-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="3539a-107">Ein aktiver oder geschlossener Vertrag kann nicht bearbeitet oder erneut geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="3539a-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="3539a-108">Finanzielle Auswirkungen der Bestätigung eines Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="3539a-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="3539a-109">Nachdem ein Projektvertrag bestätigt wurde, werden die Kosten von der Anwendung neu berechnet, indem die älteren tatsächlichen Kosten zurückgebucht und neue tatsächliche Kosten erneut erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3539a-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="3539a-110">Die neuen tatsächlichen Kosten werden dann basierend auf der Fakturierungsmethode der zugehörigen Projektvertragszeile verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="3539a-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="3539a-111">Wenn die tatsächlichen Kosten auf eine Vertragszeile für Zeit und Material verweisen, erstellt die Anwendung automatisch die entsprechenden nicht fakturierten Umsatz-Istwerte neu.</span><span class="sxs-lookup"><span data-stu-id="3539a-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="3539a-112">Wenn sich die tatsächlichen Kosten auf eine Festpreisvertragszeile beziehen, beendet die Anwendung die erneute Verarbeitung der tatsächlichen Kosten.</span><span class="sxs-lookup"><span data-stu-id="3539a-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="3539a-113">Nicht zu überschreitende Grenzwerte, die Einrichtung der Fakturierbarkeit sowie die Preis- und Kostenberechnung für die Istwerte werden bewertet und dann im Rahmen des Bestätigungsprozesses aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3539a-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="3539a-114">Einen Projektvertrag als verloren abschließen</span><span class="sxs-lookup"><span data-stu-id="3539a-114">Close a project contract as lost</span></span>

<span data-ttu-id="3539a-115">Wenn Sie einen Projektvertrag als verloren schließen, wird der Vertragsstatus auf **Geschlossen** aktualisiert und der Statusgrund lautet **Verloren**.</span><span class="sxs-lookup"><span data-stu-id="3539a-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="3539a-116">Der Projektvertrag ist daraufhin schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3539a-116">The project contract becomes read-only.</span></span> <span data-ttu-id="3539a-117">Vor Abschluss der Änderungen wird ein Bestätigungsdialogfeld angezeigt, da Sie einen geschlossenen Projektvertrag nicht erneut öffnen können.</span><span class="sxs-lookup"><span data-stu-id="3539a-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="3539a-118">Wenn der als verloren geschlossene Projektvertrag auf ein Projekt in seinen Zeilen verweist, wird dieses Projekt auch als geschlossen markiert.</span><span class="sxs-lookup"><span data-stu-id="3539a-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="3539a-119">Alle Ressourcenbuchungen ab diesem Tag werden storniert.</span><span class="sxs-lookup"><span data-stu-id="3539a-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="3539a-120">Alle nicht fakturierten Umsatz-Istwerte des Projektvertrags, die noch nicht auf einer Rechnung stehen, werden storniert.</span><span class="sxs-lookup"><span data-stu-id="3539a-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="3539a-121">Das Schließen eines Projektvertrags in Dynamics 365 Project Operations als „Verloren“ hat keinen Einfluss auf den Status der zugeordneten Verkaufschance.</span><span class="sxs-lookup"><span data-stu-id="3539a-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="3539a-122">Die Verkaufschance bleibt offen und muss manuell geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="3539a-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]