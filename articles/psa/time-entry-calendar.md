---
title: Zeiteintragskalender
description: Dieses Thema bietet Informationen zur Verwendung des Zeiteintragskalenders.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: afc31609c51f48db61ce359c18707b5a92211082
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076614"
---
# <a name="time-entry-calendar"></a><span data-ttu-id="b6a45-103">Zeiteintragskalender</span><span class="sxs-lookup"><span data-stu-id="b6a45-103">Time entry calendar</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b6a45-104">Auf der Seite **Zeiteinträge** können Sie die Zeiteintragungen im Kalender anzeigen, indem Sie **Anzeigen als** \> **Kalender-Steuerelement** auswählen.</span><span class="sxs-lookup"><span data-stu-id="b6a45-104">On the **Time Entries** page, you can view the time entries on the calendar by selecting **Show as** \> **Calendar Control**.</span></span>

## <a name="updated-calendar-control"></a><span data-ttu-id="b6a45-105">Aktualisiertes Kalender-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b6a45-105">Updated calendar control</span></span>

<span data-ttu-id="b6a45-106">Dynamics 365 Project Service Automation bietet eine neue und erweiterbare Zeiteintragumgebung.</span><span class="sxs-lookup"><span data-stu-id="b6a45-106">Dynamics 365 Project Service Automation offers a new and extensible time entry experience.</span></span> <span data-ttu-id="b6a45-107">Diese neue Umgebung ersetzt das Benutzerdefinierte Kalender-Steuerelement, das in früheren Versionen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b6a45-107">This new experience replaces the Custom Calendar Control that was used in earlier versions.</span></span> <span data-ttu-id="b6a45-108">Sie können jedoch immer noch Zeiteinträge über ein schreibgeschütztes Kalender-Steuerelement anzeigen, das das Framework der einheitlichen Oberfläche für tägliche, wöchentliche oder monatliche Ansichten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b6a45-108">However, you can still view time entries through a read-only calendar control that the Unified Interface Framework provides for daily, weekly, or monthly views.</span></span>

<span data-ttu-id="b6a45-109">Der Kalender unterstützt keine Aktionen für einzelne Kalenderelemente, und Sie können nicht mindestens ein Kalenderelement zur Übermittlung oder Löschung auswählen.</span><span class="sxs-lookup"><span data-stu-id="b6a45-109">The calendar doesn't support actions on individual calendar items, and you can't select one or more calendar items for submission or deletion.</span></span> <span data-ttu-id="b6a45-110">Stattdessen wählen Sie ein Kalenderelement aus, um die Entitätsseite **Zeiteintrag** zu öffnen, auf der Sie die erforderlichen Aktionen abschließen können.</span><span class="sxs-lookup"><span data-stu-id="b6a45-110">Instead, select a calendar item to open the **Time Entry** entity page, where you can complete the required actions.</span></span>

## <a name="extensibility"></a><span data-ttu-id="b6a45-111">-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="b6a45-111">Extensibility</span></span>

<span data-ttu-id="b6a45-112">Auf der Seite **Zeiteinträge** , die das Zeiteintragraster enthält, können Sie benutzerdefinierte Felder hinzufügen, Suchfelder einrichten und benutzerdefinierte Ansichten erstellen.</span><span class="sxs-lookup"><span data-stu-id="b6a45-112">On the **Time Entries** page that has the time entry grid, you can add custom fields, set up lookup fields, and create custom views.</span></span> <span data-ttu-id="b6a45-113">Sie können auch eine benutzerdefinierte Geschäftslogik einrichten, die auf Werten basiert, die ausgewählt sind oder in benutzerdefinierten Feldern eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b6a45-113">You can also set up custom business logic that is based on the values that are selected or entered in custom fields.</span></span>