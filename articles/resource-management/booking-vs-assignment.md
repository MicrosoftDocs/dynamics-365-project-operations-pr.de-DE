---
title: Buchungen gegenüber Arbeitsaufträge
description: Dieses Thema enthält Informationen zu den Unterschieden zwischen Ressourcenbuchungen und Ressourcenarbeitsaufträgen.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130217"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="63ca7-103">Buchungen gegenüber Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="63ca7-103">Bookings vs assignments</span></span>

<span data-ttu-id="63ca7-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="63ca7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="63ca7-105">Buchungen betreffen die verbindliche oder unverbindliche Zuweisung von Ressourcen zu einem Projekt.</span><span class="sxs-lookup"><span data-stu-id="63ca7-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="63ca7-106">Verbindliche Buchungen verbrauchen die Kapazität einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="63ca7-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="63ca7-107">Buchungen stellen Organisationskonzepte für Teams dar, damit sie verstehen, wie Ressourcen in verschiedenen Projekten eingesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="63ca7-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="63ca7-108">Dynamics 365 Project Operations betrachtet Buchungen als Konzept auf Projektebene.</span><span class="sxs-lookup"><span data-stu-id="63ca7-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="63ca7-109">Im Gegensatz zu Buchungen, betreffen Zuweisungen den Einsatz von Ressourcen zu Projektaufgaben im Projektzeitplan.</span><span class="sxs-lookup"><span data-stu-id="63ca7-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="63ca7-110">Die Ressourcen können benannt oder generisch sein.</span><span class="sxs-lookup"><span data-stu-id="63ca7-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="63ca7-111">In der Regel entspricht die Summe der Buchungen für eine Ressource der Summe der Zuweisungen der Ressource für eine oder mehrere Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="63ca7-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="63ca7-112">Project Operations erzwingt diese Vereinbarung jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="63ca7-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="63ca7-113">Die **Abstimmungsansicht** zeigt einem Projektmanager an, wo die Buchungen und Zuweisungen einer Ressource nicht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="63ca7-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
