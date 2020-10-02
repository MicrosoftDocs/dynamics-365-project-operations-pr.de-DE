---
title: Projektkalender definieren
description: Dieses Thema enthält Informationen zur Verwendung eines Projektkalenders zum Verfolgen des Projektzeitplans.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d44a2d0d8c13fb9e93b9a6da15fb3a7ce8d764c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897990"
---
# <a name="define-project-calendars"></a><span data-ttu-id="947a4-103">Projektkalender definieren</span><span class="sxs-lookup"><span data-stu-id="947a4-103">Define project calendars</span></span>

<span data-ttu-id="947a4-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="947a4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="947a4-105">Zur Erstellung eines Projektzeitplans erstellen Sie zuerst eine Projektkalendervorlage, in der die Anzahl der Arbeitsstunden pro Tag sowie etwaige Betriebsferien definiert werden.</span><span class="sxs-lookup"><span data-stu-id="947a4-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="947a4-106">Zur Erstellung einer Projektkalendervorlage weisen Sie dem Feld **Kalendervorlage** eine Arbeitsvorlage für das Projekt zu.</span><span class="sxs-lookup"><span data-stu-id="947a4-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="947a4-107">Führen Sie die folgenden Schritte aus, um eine Arbeitsvorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="947a4-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="947a4-108">Wählen Sie im Navigationsbereich die Option **Ressouren** aus.</span><span class="sxs-lookup"><span data-stu-id="947a4-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="947a4-109">Öffnen Sie auf der Listenseite **Ressourcen** einen Benutzerdatensatz und wählen Sie dann **Arbeitsstunden anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="947a4-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="947a4-110">Stellen Sie sicher, dass auf der Browserseite Popups zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="947a4-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="947a4-111">So können Sie die für die Ressource festgelegten Arbeitsstunden anzeigen.</span><span class="sxs-lookup"><span data-stu-id="947a4-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="947a4-112">Wählen Sie auf der Registerkarte **Monatliche Ansicht** **Einrichten** aus.</span><span class="sxs-lookup"><span data-stu-id="947a4-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="947a4-113">Eine Liste mit drei Optionen wird angezeigt:</span><span class="sxs-lookup"><span data-stu-id="947a4-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="947a4-114">Neuer wöchentlicher Zeitplan</span><span class="sxs-lookup"><span data-stu-id="947a4-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="947a4-115">Arbeitsplan für einen Tag</span><span class="sxs-lookup"><span data-stu-id="947a4-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="947a4-116">Arbeitsfreie Zeit</span><span class="sxs-lookup"><span data-stu-id="947a4-116">Time Off</span></span>

4. <span data-ttu-id="947a4-117">Wählen Sie **Neuer wöchentlicher Zeitplan** aus und legen Sie anschließend die Optionen für den Ressourcenzeitplan fest.</span><span class="sxs-lookup"><span data-stu-id="947a4-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="947a4-118">Sie können einen wöchentlichen Serienzeitplan, tägliche Stundenparameter, Betriebsferien und mehr festlegen.</span><span class="sxs-lookup"><span data-stu-id="947a4-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="947a4-119">Legen Sie den Datumsbereich fest, wählen Sie **Speichern** aus und wählen Sie dann **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="947a4-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="947a4-120">Kehren Sie zur Listenseite **Ressourcen** zurück und wählen Sie die Ressource aus, für die Sie die Arbeitsstunden festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="947a4-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="947a4-121">Wählen Sie **Kalender festlegen als** aus, um die Arbeitsvorlage festzulegen.</span><span class="sxs-lookup"><span data-stu-id="947a4-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="947a4-122">Geben Sie im Dialogfeld **Arbeitsvorlage** einen Namen für die Arbeitsvorlage ein und wählen Sie dann **Übernehmen** aus.</span><span class="sxs-lookup"><span data-stu-id="947a4-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="947a4-123">Sie können die Arbeitsvorlage jetzt einer Projektkalendervorlage zuordnen.</span><span class="sxs-lookup"><span data-stu-id="947a4-123">You can now associate the work template with a project calendar template.</span></span>
