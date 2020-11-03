---
title: Planen Sie Ressourcen für ein Projekt.
description: Ressourcen für ein Projekt planen (Project Service)
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076730"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="375d8-103">Ressourcen für ein Projekt planen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="375d8-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="375d8-104">Sie können die Verfügbarkeit von Ressourcen überprüfen, um einen Gesamtüberblick darüber zu erhalten, wie stark Ihre Ressourcen gebucht sind. Sie können die Ansicht auch nach Qualifikationen, Team, Standort und anderen Optionen filtern.</span><span class="sxs-lookup"><span data-stu-id="375d8-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="375d8-105">Die Zeitplanübersicht zeigt eine Ressourcenliste und deren Verfügbarkeit an.</span><span class="sxs-lookup"><span data-stu-id="375d8-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="375d8-106">Wählen Sie einen Anzeigemodus aus, um die Verfügbarkeiten nach **Stunden** , **Tag** , **Woche** und **Monat** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="375d8-106">Select a view mode to show availability by **Hours** , **Day** , **Week** , or **Month**.</span></span>  
  
<span data-ttu-id="375d8-107">Bevor Sie die Zeitplanübersicht verwenden, müssen Sie diese einrichten.</span><span class="sxs-lookup"><span data-stu-id="375d8-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="375d8-108">Weitere Informationen finden Sie unter [Konfigurieren der Zeitplanübersicht (Field Service oder Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="375d8-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="375d8-109">Wenn Sie eine ältere Version verwenden, lesen Sie für die Ressourcenverfügbarkeit [Ressourcenverfügbarkeit anzeigen (Project Service Automation)](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="375d8-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="375d8-110">Um die Zeitplanübersicht-Buchungsfunktion, Standorterfassung und Standortservices zu verwenden, müssen Sie Karten aktivieren.</span><span class="sxs-lookup"><span data-stu-id="375d8-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="375d8-111">Klicken Sie im Hauptmenü auf die Option für **Ressourcenplanung** > **Verwaltung**.</span><span class="sxs-lookup"><span data-stu-id="375d8-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="375d8-112">Klicken Sie auf **Planungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="375d8-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="375d8-113">Öffnen Sie den Datensatz und führen Sie einen Bildlauf nach unten zum **Resource Scheduling Optimization** Abschnitt durch.</span><span class="sxs-lookup"><span data-stu-id="375d8-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="375d8-114">Wählen Sie im Feld **Mit Karten verbinden** die Option **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="375d8-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="375d8-115">Akzeptieren Sie die Bedingungen und speichern Sie den Datensatz.</span><span class="sxs-lookup"><span data-stu-id="375d8-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="375d8-116">Klicken Sie im Hauptmenü auf **Project Service** > **Zeitplanübersicht**.</span><span class="sxs-lookup"><span data-stu-id="375d8-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="375d8-117">Es gibt unterschiedliche Arten eine Buchungsanforderung manuell zu planen.</span><span class="sxs-lookup"><span data-stu-id="375d8-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="375d8-118">Wählen Sie die Methode aus, die für Sie funktioniert.</span><span class="sxs-lookup"><span data-stu-id="375d8-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="375d8-119">Verfügbare Ressourcen finden</span><span class="sxs-lookup"><span data-stu-id="375d8-119">Find available resources</span></span>

1.  <span data-ttu-id="375d8-120">Rechtsklicken Sie in der Liste **Buchungsanforderung** auf eine ungeplante Buchung, und wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="375d8-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="375d8-121">Wählen Sie **Verfügbarkeit suchen – Aktuelle Ressourcen** , um verfügbaren Ressourcen in der Zeitplanübersicht zu suchen.</span><span class="sxs-lookup"><span data-stu-id="375d8-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="375d8-122">Wählen Sie **Verfügbarkeit suchen – Alle Ressourcen** , um verfügbare Ressourcen im System zu suchen.</span><span class="sxs-lookup"><span data-stu-id="375d8-122">Choose **Find availability - All Resources** , to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="375d8-123">Dabei werden die Filter die Optionen für die ausgewählte Buchungsanforderung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="375d8-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="375d8-124">Wenn Sie einen verfügbaren Zeitraum sehen, klicken Sie mit rechts in der Zeitplanübersicht auf den Zeitraum und wählen Sie **Hier buchen**.</span><span class="sxs-lookup"><span data-stu-id="375d8-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="375d8-125">Oder Ziehen Sie die Buchungsanforderungen auf einen Zeitraum und legen Sie diese dort ab.</span><span class="sxs-lookup"><span data-stu-id="375d8-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="375d8-126">Buchen einer Ressource mithilfe der täglichen Ansicht und nicht ausgebuchte Personen suchen</span><span class="sxs-lookup"><span data-stu-id="375d8-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="375d8-127">Auf der Zeitplanübersicht klicken Sie auf **Ansichtsmodus** , und wählen Sie **Tage** aus.</span><span class="sxs-lookup"><span data-stu-id="375d8-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="375d8-128">Dies zeigt eine Tabellenansicht der Anzahl der gebuchten Stunden einer Ressource pro Tag und die freien Tage an.</span><span class="sxs-lookup"><span data-stu-id="375d8-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="375d8-129">Klicken Sie auf den Namen der Ressource, die Sie buchen möchten, und klicken Sie dann auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="375d8-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="375d8-130">Wählen Sie im Dialogfeld **Ressourcenbuchung (erstellen)** das Projekt, für das Sie die Ressource buchen möchten sowie die Buchungsmethode und die Start- und Endzeiten.</span><span class="sxs-lookup"><span data-stu-id="375d8-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="375d8-131">Wählen Sie **Buchen** aus, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="375d8-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="375d8-132">Anzeigen der Zeitplanübersicht</span><span class="sxs-lookup"><span data-stu-id="375d8-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="375d8-133">Wählen Sie eine ungeplante Buchungsanforderung von der Liste unten aus.</span><span class="sxs-lookup"><span data-stu-id="375d8-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="375d8-134">Verschieben Sie die Buchungsanforderungen zu einer verfügbaren Ressource/einem verfügbaren Zeitfenster in der Zeitplanübersicht.</span><span class="sxs-lookup"><span data-stu-id="375d8-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="375d8-135">Wählen Sie **Buchen** aus, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="375d8-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="375d8-136">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="375d8-136">Additional resources</span></span>  
 [<span data-ttu-id="375d8-137">Ressourcenmanagerhandbuch</span><span class="sxs-lookup"><span data-stu-id="375d8-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
