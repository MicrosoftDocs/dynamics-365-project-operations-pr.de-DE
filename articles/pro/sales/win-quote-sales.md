---
title: Angebote schließen
description: Dieses Thema bietet Informationen zum Abschluss eines Angebots in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076445"
---
# <a name="close-quotes"></a><span data-ttu-id="964bc-103">Angebote schließen</span><span class="sxs-lookup"><span data-stu-id="964bc-103">Close quotes</span></span> 

<span data-ttu-id="964bc-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="964bc-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="964bc-105">Ein Projektangebot kann als „Gewonnen“ oder „Verloren“ geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="964bc-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="964bc-106">Die Vorgänge „Aktivieren“ und „Überarbeiten“ von Angeboten werden in Microsoft Dynamics 365 Project Operations nicht unterstützt, sodass ein Angebotsentwurf geschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="964bc-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="964bc-107">Ein Angebot als „Gewonnen“ schließen</span><span class="sxs-lookup"><span data-stu-id="964bc-107">Close a quote as Won</span></span>

<span data-ttu-id="964bc-108">Wenn Sie ein Projektangebot als „Gewonnen“ schließen, wird das Angebot in den Status „Geschlossen“ und der Statusgrund auf „Gewonnen“ gesetzt.</span><span class="sxs-lookup"><span data-stu-id="964bc-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="964bc-109">Durch das Schließen des Angebots wird das Projektangebot schreibgeschützt, und es wird ein Entwurf eines Projektvertrags erstellt, der die Angebotsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="964bc-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="964bc-110">Ein Bestätigungs-Dialogfeld wird angezeigt, bevor die Änderungen vorgenommen werden, da ein geschlossenes Angebot nicht erneut geöffnet werden kann und die Änderungen nicht rückgängig gemacht werden können.</span><span class="sxs-lookup"><span data-stu-id="964bc-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="964bc-111">Wenn das Angebot an eine Verkaufschance angehängt ist, werden alle anderen Projektangebote für die Verkaufschance automatisch als „Verloren“ geschlossen.</span><span class="sxs-lookup"><span data-stu-id="964bc-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="964bc-112">Finanzielle Auswirkungen des Abschlusses eines Angebots als „Gewonnen“</span><span class="sxs-lookup"><span data-stu-id="964bc-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="964bc-113">Wenn für ein Projekt tatsächliche Zeitangaben aufgezeichnet wurden, während es noch einem Angebotsentwurf beigefügt ist, werden nur die Kosten für die Zeit oder die Kosten erfasst.</span><span class="sxs-lookup"><span data-stu-id="964bc-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="964bc-114">Nachdem ein Angebot als „Gewonnen“ geschlossen wurde, werden die Kosten von der Anwendung umgestaltet, indem die älteren tatsächlichen Kosten zurückgebucht und neue tatsächliche Kosten erneut erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="964bc-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="964bc-115">Die Anwendung verarbeitet diese Istkosten basierend auf der Abrechnungsmethode der zugehörigen Projektvertragszeile.</span><span class="sxs-lookup"><span data-stu-id="964bc-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="964bc-116">Wenn sich die tatsächlichen Kosten auf eine Zeit- und Materialvertragszeile beziehen, erstellt das System automatisch die entsprechenden nicht in Rechnung gestellten Umsatz-Istwerte, wenn das Angebot geschlossen und der Projektvertrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="964bc-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="964bc-117">Wenn sich die tatsächlichen Kosten auf eine Festpreisvertragszeile beziehen, beendet die Anwendung die erneute Verabeitung der tatsächlichen Kosten basierend auf den Regeln für die getrennte Abrechnung für die Projektvertragskunden.</span><span class="sxs-lookup"><span data-stu-id="964bc-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="964bc-118">Ein Angebot als „Verloren“ schließen:</span><span class="sxs-lookup"><span data-stu-id="964bc-118">Closing a quote as lost:</span></span>

<span data-ttu-id="964bc-119">Wenn Sie ein Projektangebot als „Verloren“ schließen, wird der Status auf „Geschlossen“ und der Statusgrund auf „Verloren“ gesetzt.</span><span class="sxs-lookup"><span data-stu-id="964bc-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="964bc-120">Wenn Sie das Angebot schließen, ist das Projektangebot schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="964bc-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="964bc-121">Da ein geschlossenes Angebot nicht erneut geöffnet werden kann, werden Ihre Änderungen in einem Bestätigungsdialogfeld bestätigt, bevor Sie ein Angebot schließen.</span><span class="sxs-lookup"><span data-stu-id="964bc-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="964bc-122">Wenn für das als verloren geschlossene Projektangebot auf ein Projekt in einer seiner Zeilen verwiesen wird, wird dieses Projekt auch als geschlossen markiert und alle Ressourcenbuchungen ab diesem Tag werden storniert.</span><span class="sxs-lookup"><span data-stu-id="964bc-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="964bc-123">In Project Operations wirkt sich das Schließen eines Angebots als „Gewonnen“ oder „Verloren“ nicht auf den Status der Verkaufschance aus, die geöffnet bleibt, bis sie manuell geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="964bc-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
