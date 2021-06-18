---
title: Ein Angebot schließen – Lite
description: Dieses Thema bietet Informationen zum Abschluss eines Angebots in Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994135"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="fa669-103">Ein Angebot schließen – Lite</span><span class="sxs-lookup"><span data-stu-id="fa669-103">Close a quote - lite</span></span>

<span data-ttu-id="fa669-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="fa669-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fa669-105">Ein Projektangebot kann als „Gewonnen“ oder „Verloren“ geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="fa669-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="fa669-106">Ein Angebotsentwurf kann geschlossen werden, da die Vorgänge Aktivieren und Überarbeiten von Angeboten in Microsoft Dynamics 365 Project Operations nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="fa669-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="fa669-107">Ein Angebot als „Gewonnen“ schließen</span><span class="sxs-lookup"><span data-stu-id="fa669-107">Close a quote as Won</span></span>

<span data-ttu-id="fa669-108">Wenn Sie ein Projektangebot als gewonnen schließen, wird der Status auf geschlossen gesetzt und Statusgrund lautet gewonnen.</span><span class="sxs-lookup"><span data-stu-id="fa669-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="fa669-109">Durch das Schließen des Angebots wird das Projektangebot schreibgeschützt, und es wird ein Entwurf eines Projektvertrags erstellt, der die Angebotsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="fa669-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="fa669-110">Da ein geschlossenes Angebot nicht erneut geöffnet werden kann, werden Ihre Änderungen in einem Bestätigungsdialogfeld bestätigt.</span><span class="sxs-lookup"><span data-stu-id="fa669-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="fa669-111">Wenn das Angebot an eine Verkaufschance angehängt ist, werden alle anderen Projektangebote für die Verkaufschance automatisch als „Verloren“ geschlossen.</span><span class="sxs-lookup"><span data-stu-id="fa669-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="fa669-112">Finanzielle Auswirkungen des Abschlusses eines Angebots als „Gewonnen“</span><span class="sxs-lookup"><span data-stu-id="fa669-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="fa669-113">Wenn ein Projekt tatsächlich Zeit enthält, während es noch einem Angebotsentwurf beigefügt ist, werden nur die Kosten für die Zeit oder die Kosten erfasst.</span><span class="sxs-lookup"><span data-stu-id="fa669-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="fa669-114">Nachdem ein Angebot als „Gewonnen“ geschlossen wurde, werden die Kosten von der Anwendung umgestaltet, indem die älteren tatsächlichen Kosten zurückgebucht und neue tatsächliche Kosten erneut erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fa669-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="fa669-115">Die Anwendung verarbeitet diese Istkosten basierend auf der Abrechnungsmethode der zugehörigen Projektvertragszeile.</span><span class="sxs-lookup"><span data-stu-id="fa669-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="fa669-116">Wenn sich die tatsächlichen Kosten auf eine Zeit- und Materialvertragszeile beziehen, werden entsprechende nicht in Rechnung gestellte Verkaufszahlen erstellt, wenn das Angebot geschlossen und der Projektvertrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fa669-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="fa669-117">Wenn sich die tatsächlichen Kosten auf eine Festpreisvertragszeile beziehen, beendet die Anwendung die Wiederaufbereitung der tatsächlichen Kosten, die auf den Regeln für die getrennte Abrechnung für die Projektvertragskunden basieren.</span><span class="sxs-lookup"><span data-stu-id="fa669-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="fa669-118">Ein Angebot als „Verloren“ schließen:</span><span class="sxs-lookup"><span data-stu-id="fa669-118">Closing a quote as lost:</span></span>

<span data-ttu-id="fa669-119">Wenn Sie ein Projektangebot als verloren schließen, wird der Status auf geschlossen gesetzt und Statusgrund lautet verloren.</span><span class="sxs-lookup"><span data-stu-id="fa669-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="fa669-120">Wenn Sie das Angebot schließen, ist das Projektangebot schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fa669-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="fa669-121">Da ein geschlossenes Angebot nicht erneut geöffnet werden kann, werden Ihre Änderungen in einem Bestätigungsdialogfeld bestätigt, bevor Sie ein Angebot schließen.</span><span class="sxs-lookup"><span data-stu-id="fa669-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="fa669-122">Wenn das als verloren geschlossene Projektangebot in einer seiner Zeilen auf ein Projekt verweist, wird dieses Projekt auch als geschlossen markiert.</span><span class="sxs-lookup"><span data-stu-id="fa669-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="fa669-123">Alle Ressourcenbuchungen ab diesem Tag werden storniert.</span><span class="sxs-lookup"><span data-stu-id="fa669-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="fa669-124">In Project Operations wirkt sich das Schließen eines Angebots als „Gewonnen“ oder „Verloren“ nicht auf den Status der Verkaufschance aus, die geöffnet bleibt, bis sie manuell geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="fa669-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]