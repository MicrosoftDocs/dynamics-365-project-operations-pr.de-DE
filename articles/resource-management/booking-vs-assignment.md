---
title: Buchungen gegenüber Arbeitsaufträge
description: Dieses Thema enthält Informationen zu den Unterschieden zwischen Ressourcenbuchungen und Ressourcenarbeitsaufträgen.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279902"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="75bfa-103">Buchungen gegenüber Arbeitsaufträge</span><span class="sxs-lookup"><span data-stu-id="75bfa-103">Bookings vs assignments</span></span>

<span data-ttu-id="75bfa-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="75bfa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="75bfa-105">Buchungen betreffen die verbindliche oder unverbindliche Zuweisung von Ressourcen zu einem Projekt.</span><span class="sxs-lookup"><span data-stu-id="75bfa-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="75bfa-106">Verbindliche Buchungen verbrauchen die Kapazität einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="75bfa-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="75bfa-107">Buchungen stellen Organisationskonzepte für Teams dar, damit diese verstehen können, wie die Ressourcen projektübergreifend eingesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="75bfa-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="75bfa-108">Dynamics 365 Project Operations betrachtet Buchungen als ein Konzept auf Projektebene.</span><span class="sxs-lookup"><span data-stu-id="75bfa-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="75bfa-109">Im Gegensatz zu Buchungen sind Zuweisungen die Bindung von Ressourcen an Projektaufgaben im Projektplan.</span><span class="sxs-lookup"><span data-stu-id="75bfa-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="75bfa-110">Die Ressourcen können benannt oder generisch sein.</span><span class="sxs-lookup"><span data-stu-id="75bfa-110">The resources can be named or generic.</span></span>  <span data-ttu-id="75bfa-111">Wenn eine Ressourcenanforderung aus den Projektaufgabenzuweisungen abgeleitet wird, verwendet Project Operations die Aufwandskonturen der Ressourcenzuweisung, um die Konturen der Ressourcenanforderungsdetails zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="75bfa-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="75bfa-112">Eine Bezugnahme auf die Ressourcenzuweisungen wird jedoch nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="75bfa-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="75bfa-113">Aktualisierungen der Buchungen, die aus der Ressourcenanforderung abgeleitet wurden, aktualisieren keine Ressourcenzuweisungen.</span><span class="sxs-lookup"><span data-stu-id="75bfa-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="75bfa-114">Normalerweise entspricht die Summe der Buchungen für eine Ressource der Summe der Zuweisungen der Ressource für eine oder mehrere Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="75bfa-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="75bfa-115">Project Operations erzwingt diese Vereinbarung jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="75bfa-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="75bfa-116">Die **Abstimmungsansicht** zeigt einem Projektmanager an, wo die Buchungen und Zuweisungen einer Ressource nicht übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="75bfa-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]