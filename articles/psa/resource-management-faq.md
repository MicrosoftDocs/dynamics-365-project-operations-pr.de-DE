---
title: FAQ zur Ressourcenverwaltung
description: Dieses Thema liefert Antworten auf häufig gestellte Fragen zur Ressourcenverwaltung.
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
ms.openlocfilehash: 38d9509768323a5a1d78683a2e65ade241adc65f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120137"
---
# <a name="resource-management-faq"></a><span data-ttu-id="4cb26-103">FAQ zur Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="4cb26-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="4cb26-104">Was ist der Unterschied zwischen einem Teammitglied und einer Ressourcenanforderung?</span><span class="sxs-lookup"><span data-stu-id="4cb26-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="4cb26-105">Ein Projektteammitglied kann Aufgaben zugewiesen, gebucht oder überbucht sowie als genehmigende Person festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4cb26-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="4cb26-106">Eine Ressourcenanforderung kann ohne ein Projektteammitglied existieren, als Entwurfsnotiz der Nachfrage.</span><span class="sxs-lookup"><span data-stu-id="4cb26-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="4cb26-107">Was ist der Unterschied zwischen vorgeschlagenen und unverbindlich gebuchten Stunden?</span><span class="sxs-lookup"><span data-stu-id="4cb26-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="4cb26-108">Vorgeschlagene Stunden und unverbindlich gebuchte Stunden unterscheiden sich hinsichtlich der Sichtbarkeit.</span><span class="sxs-lookup"><span data-stu-id="4cb26-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="4cb26-109">Vorgeschlagene Stunden sind nur für die Ressourcenmanager und den Projektmanager sichtbar, die die Nachfrage mithilfe einer Ressourcenanfrage initiiert haben.</span><span class="sxs-lookup"><span data-stu-id="4cb26-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="4cb26-110">Unverbindlich gebuchte Stunden sind für alle Personen sichtbar, die Zugriff auf die Zeitplanübersicht haben.</span><span class="sxs-lookup"><span data-stu-id="4cb26-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="4cb26-111">Wie können die unverbindlich gebuchten Stunden für Ressourcen in einem Team anzeigen?</span><span class="sxs-lookup"><span data-stu-id="4cb26-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="4cb26-112">Unverbindliche Buchungen können beim Buchen einer Ressourcenanforderung vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="4cb26-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="4cb26-113">Ressourcen, die für ein Projektteam unverbindlich gebucht werden, werden als Teammitglieder mit unverbindlich gebuchten Stunden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4cb26-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="4cb26-114">Sie werden auch in der Zeitplanübersicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4cb26-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="4cb26-115">Wie ändere ich die erforderlichen Stunden sowie das Start- und Enddatum für eine von mir gebuchte Ressource (generisch oder benannt)?</span><span class="sxs-lookup"><span data-stu-id="4cb26-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="4cb26-116">Wählen Sie nach dem Buchen von Ressourcen **Buchungen verwalten** aus, um erforderliche Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="4cb26-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="4cb26-117">Welche Ressourcentypen werden von Project Service Automation unterstützt?</span><span class="sxs-lookup"><span data-stu-id="4cb26-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="4cb26-118">**Benutzer** und **Kontakt** sind die einzigen Ressourcentypen, die in Dynamics 365 Project Service Automation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4cb26-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="4cb26-119">Obwohl Sie andere Ressourcentypen erstellen können (z. B. **Arbeitsgerät** und **Gruppe**), wird für sie kein End-to-End-Anwendungsfall unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4cb26-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="4cb26-120">Was ist der Unterschied zwischen einer Zuweisung und einer Buchung?</span><span class="sxs-lookup"><span data-stu-id="4cb26-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="4cb26-121">Zuweisungen betreffen die Zuweisung von Ressourcen zu Projektaufgaben im Projektzeitplan.</span><span class="sxs-lookup"><span data-stu-id="4cb26-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="4cb26-122">Bei den Ressourcen kann es sich entweder um reale oder um generische Ressourcen handeln.</span><span class="sxs-lookup"><span data-stu-id="4cb26-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="4cb26-123">Buchungen betreffen die verbindliche oder unverbindliche Zuweisung von Ressourcen zu einem Projekt.</span><span class="sxs-lookup"><span data-stu-id="4cb26-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="4cb26-124">Verbindliche Buchungen verbrauchen die Kapazität einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="4cb26-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="4cb26-125">Idealerweise sollten die Buchungen und Zuweisungen für reale Buchungen übereinstimmen, da sie sich nicht unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="4cb26-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="4cb26-126">Diese Vereinbarung wird von PSA jedoch nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="4cb26-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="4cb26-127">Die Abstimmungsansicht zeigt einem Projektmanager an, wo die Buchungen und Zuweisungen einer Ressource nicht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="4cb26-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
