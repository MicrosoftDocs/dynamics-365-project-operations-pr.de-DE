---
title: Genehmigungssätze
description: Dieses Thema enthält Informationen über Genehmigungssätze, Anforderungen und Untergruppen dieser Vorgänge.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116870"
---
# <a name="approval-sets"></a><span data-ttu-id="52303-103">Genehmigungssätze</span><span class="sxs-lookup"><span data-stu-id="52303-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="52303-104">Genehmigungssätze gruppieren Genehmigungsanforderungen in kleinere Teilmengen von Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="52303-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="52303-105">Diese Gruppierung ermöglicht die Verarbeitung von Genehmigungen nach Projektreihenfolge und ermöglicht Wiederholungsversuche und Sequenzierungen.</span><span class="sxs-lookup"><span data-stu-id="52303-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="52303-106">Die Gruppierung verbessert die Zuverlässigkeit und Nachvollziehbarkeit der Genehmigungsverarbeitung bei großen Genehmigungsmengen.</span><span class="sxs-lookup"><span data-stu-id="52303-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="52303-107">Genehmigungssätze geben den Gesamtverarbeitungsstatus ihrer zugehörigen Datensätze an.</span><span class="sxs-lookup"><span data-stu-id="52303-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="52303-108">Wenn ein Genehmigungsdatensatz mit einem Genehmigungssatz verarbeitet wird, verschiebt sich der Datensatz von **Eingereicht** zu **Genehmigt**, und ist nicht mit dem Genehmigungssatz verknüpft.</span><span class="sxs-lookup"><span data-stu-id="52303-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="52303-109">Wenn ein Datensatz beim Einreichen zur Genehmigung fehlschlägt, bleibt der Datensatz im Status **Eingereicht** und der Genehmigungssatz wird als fehlgeschlagen markiert.</span><span class="sxs-lookup"><span data-stu-id="52303-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="52303-110">Der Genehmigungssatz protokolliert die Fehlermeldung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="52303-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="52303-111">Genehmigungen und Genehmigungssets bearbeiten</span><span class="sxs-lookup"><span data-stu-id="52303-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="52303-112">Genehmigungen, die zur Bearbeitung anstehen, sind in der Ansicht **Verarbeitungsgenehmigungen**.</span><span class="sxs-lookup"><span data-stu-id="52303-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="52303-113">Das System versucht, alle Einträge mehrmals asynchron zu verarbeiten, einschließlich eines erneuten Versuchs einer Genehmigung, wenn vorherige Versuche fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="52303-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="52303-114">Das Feld **Gültigkeitsdauer des Genehmigungssatzes** zeichnet die Anzahl der verbleibenden Versuche auf, den Satz zu verarbeiten, bevor er als fehlgeschlagen markiert wird.</span><span class="sxs-lookup"><span data-stu-id="52303-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="52303-115">Fehlgeschlagene Genehmigungen und Genehmigungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="52303-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="52303-116">Die Ansicht **Fehlgeschlagene Genehmigungen** führt alle Genehmigungen auf, die ein Eingreifen des Benutzers erfordern.</span><span class="sxs-lookup"><span data-stu-id="52303-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="52303-117">Öffnen Sie die zugehörigen Genehmigungssatzprotokolle, um die Fehlerursache zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="52303-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="52303-118">Die Auswahl von **Wiederholen** zählt zur Anzahl des Genehmigungssatzes, verschiebt den Genehmigungssatz zurück in den Status **wird bearbeitet** und versucht, die verbleibenden Datensätze zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="52303-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="52303-119">Genehmigungssätze konfigurieren</span><span class="sxs-lookup"><span data-stu-id="52303-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="52303-120">Aktivieren Sie die Funktion Genehmigungssätze</span><span class="sxs-lookup"><span data-stu-id="52303-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="52303-121">Bevor Sie die Funktion Genehmigungssätze aktivieren, vergewissern Sie sich, dass derzeit keine Genehmigungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="52303-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="52303-122">Gehen Sie zur Seite **Projektparameter** und wählen Sie **Funktionssteuerung** > **Moderne Genehmigungen aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="52303-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="52303-123">Deaktivieren Sie die Funktion Genehmigungssätze</span><span class="sxs-lookup"><span data-stu-id="52303-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="52303-124">Bevor Sie die Funktion Genehmigungssätze deaktivieren, vergewissern Sie sich, dass derzeit keine Genehmigungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="52303-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="52303-125">Gehen Sie zur Seite **Parameter** und wählen Sie **Funktionssteuerung** > **Moderne Genehmigungen deaktivieren**.</span><span class="sxs-lookup"><span data-stu-id="52303-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="52303-126">Konfigurieren des asynchronen Schwellenwerts</span><span class="sxs-lookup"><span data-stu-id="52303-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="52303-127">Wenn Genehmigungssätze erstellt werden, verlagert sich die Verarbeitung in den Hintergrund, wenn die ausgewählte Anzahl von zu genehmigenden Datensätzen den angegebenen Schwellenwert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="52303-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="52303-128">Verwenden Sie das Feld **Asynchroner Schwellenwert**, um zu konfigurieren, wann die Genehmigungsverarbeitung synchron oder asynchron ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="52303-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="52303-129">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="52303-129">Valid values are:</span></span>

  - <span data-ttu-id="52303-130">Null: Alle Anfragen sollten asynchron verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="52303-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="52303-131">Zahlen größer als Null: Genehmigungen werden nur dann asynchron verarbeitet, wenn die übermittelte Anzahl der Genehmigungen diesen Wert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="52303-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
