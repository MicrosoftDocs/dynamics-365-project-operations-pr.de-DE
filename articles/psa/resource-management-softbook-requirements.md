---
title: Anforderungen für unverbindliches Buchen
description: Dieses Thema enthält Informationen zum unverbindlichen Buchen von Ressourcenanforderungen.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 09f7acb95be014034cc03d7eed9d37363d430601
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147382"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="bfeec-103">Anforderungen für unverbindliches Buchen</span><span class="sxs-lookup"><span data-stu-id="bfeec-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bfeec-104">Eine Ressourcenanforderung kann verbindlich gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="bfeec-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="bfeec-105">Eine verbindliche Buchung erstellt einen Vorschlag, der die Kapazität einer Ressource verbraucht.</span><span class="sxs-lookup"><span data-stu-id="bfeec-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="bfeec-106">Der Vorschlag wird dann zur Genehmigung an den Anforderer zurückgesendet.</span><span class="sxs-lookup"><span data-stu-id="bfeec-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="bfeec-107">Eine unverbindliche Buchung fügt vorläufig eine Ressource zu einem Projektteam hinzu und hat einen anderen Status in der Zeitplanübersicht. Sie verbraucht jedoch keine Kapazität der Ressource.</span><span class="sxs-lookup"><span data-stu-id="bfeec-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="bfeec-108">Um über die Zeitplanübersicht eine Ressource unverbindlich zu buchen, legen Sie für das Feld **Buchungsstatus** den Status **Unverbindlich** fest.</span><span class="sxs-lookup"><span data-stu-id="bfeec-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Auf „Unverbindlich“ festgelegter Buchungsstatus](media/Resource-Management-image77.png)

<span data-ttu-id="bfeec-110">Wenn die Registerkarte **Team** in der Ansicht **Benannte Teammitglieder** vorhanden ist, wird die Ressource dort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bfeec-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="bfeec-111">Die unverbindlich gebuchten Stunden werden in der Spalte **Unverbindlich gebuchte Stunden** angegeben.</span><span class="sxs-lookup"><span data-stu-id="bfeec-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Unverbindlich gebuchte Stunden in der Ansicht „Benannte Teammitglieder“](media/Resource-Management-image78.png)

<span data-ttu-id="bfeec-113">Unverbindlich gebuchte Teammitglieder können Aufgaben zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="bfeec-113">Soft-booked team members can be assigned to tasks.</span></span>

![Unverbindlich gebuchtes Teammitglied, das einer Aufgabe zugewiesen ist](media/Resource-Management-image79.png)

<span data-ttu-id="bfeec-115">Auf der Registerkarte **Abstimmung** werden für eine unverbindlich gebuchte Ressource keine Buchungen angezeigt, weil die Registerkarte **Abstimmung** nur verbindliche Buchungen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="bfeec-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Unverbindlich gebuchte Ressource ohne Buchungen auf der Registerkarte „Abstimmung“](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="bfeec-117">Sie können eine Ressource aus einer Anforderung, die von einem generischen Teammitglied generiert wurde, nicht unverbindlich buchen.</span><span class="sxs-lookup"><span data-stu-id="bfeec-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="bfeec-118">In der Zeitplanübersicht wird für unverbindliche Buchungen für eine Ressource eine andere Farbgebung verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfeec-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Unverbindliche Buchungen in der Zeitplanübersicht](media/Resource-Management-image81.png)

<span data-ttu-id="bfeec-120">Um eine unverbindliche in eine verbindliche Buchung zu konvertieren, klicken Sie in der Zeitplanübersicht mit der rechten Maustaste auf die unverbindliche Buchung und wählen Sie dann **Status ändern** \> **Verbindlich buchen** \> **Verbindlich** aus.</span><span class="sxs-lookup"><span data-stu-id="bfeec-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Ändern des Buchungsstandards in „Verbindlich“](media/Resource-Management-image82.png)

<span data-ttu-id="bfeec-122">Die Buchung sowie der Status in der Zeitplanübersicht werden geändert.</span><span class="sxs-lookup"><span data-stu-id="bfeec-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="bfeec-123">Da für den Buchungsstatus nunmehr **Verbindlich** festgelegt ist, wird die Ressource als gebucht angezeigt und ihre Kapazität und Verfügbarkeit werden angepasst.</span><span class="sxs-lookup"><span data-stu-id="bfeec-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="bfeec-124">Auf dieselbe Weise können Sie eine verbindliche oder eine unverbindliche Buchung in der Zeitplanübersicht stornieren.</span><span class="sxs-lookup"><span data-stu-id="bfeec-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="bfeec-125">Um eine unverbindlich gebuchte Ressource auf der Registerkarte **Team** des Projekts in eine verbindlich gebuchte Ressource zu konvertieren, wählen Sie die Ressource und anschließend **Bestätigen** aus.</span><span class="sxs-lookup"><span data-stu-id="bfeec-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Befehl bestätigen](media/Resource-Management-image83.png)
