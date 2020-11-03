---
title: Wichtige Konzepte für die Ressourcenverwaltung
description: Dieses Thema enthält Informationen zu den Funktionen für die Ressourcenverwaltung in Microsoft Dynamics Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 124d9bad5cc0c16955417a8213db047a2d8bae1d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076371"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="a738e-103">Wichtige Konzepte für die Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="a738e-103">Resource management key concepts</span></span>

<span data-ttu-id="a738e-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="a738e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a738e-105">Ressourcen sind die wichtigsten Anlagen einer dienstbasierten Organisation.</span><span class="sxs-lookup"><span data-stu-id="a738e-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="a738e-106">Die Möglichkeit, die richtigen Ressourcen zum richtigen Zeitpunkt zu finden, diese Ressourcen für Projekte zu buchen und die Ressourcen weiterhin zu nutzen, hilft der Organisation dabei, Umsatzziele und Kundenzufriedenheitsziele zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="a738e-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="a738e-107">Sie können die Ressourcenfunktion für Projekte in Dynamics 365 Project Operations verwenden, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="a738e-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="a738e-108">Bilden Sie Projektteams durch das Buchen verfügbarer und qualifizierter Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a738e-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="a738e-109">Erstellen Sie generische Teammitgliedsdatensätze und definieren Sie ihre Rollen und Ressourcenorganisationseinheit.</span><span class="sxs-lookup"><span data-stu-id="a738e-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="a738e-110">Generieren Sie Ressourcenanforderungen für generische Teammitglieder aus ihren Aufgabenzuweisungen.</span><span class="sxs-lookup"><span data-stu-id="a738e-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="a738e-111">Führen Sie einen Abgleich der Fähigkeiten durch, indem Sie die für die Ressourcennachfrage definierten Fähigkeiten mit den verfügbaren Ressourcenfähigkeiten vergleichen.</span><span class="sxs-lookup"><span data-stu-id="a738e-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="a738e-112">Ersetzen Sie Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a738e-112">Substitute resources.</span></span>
- <span data-ttu-id="a738e-113">Richten Sie Zuweisungen und Ressourcenbuchungen für den Projektzeitplan aus.</span><span class="sxs-lookup"><span data-stu-id="a738e-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="a738e-114">Stimmen Sie die Unterschiede zwischen Buchungen und Zuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="a738e-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="a738e-115">Ändern Sie die Ressourcenbuchungen als Reaktion auf den Abwesenheitsstatus.</span><span class="sxs-lookup"><span data-stu-id="a738e-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="a738e-116">Ermöglichen Sie das Zusammenarbeiten von Projektmanagern und Ressourcen-Managern.</span><span class="sxs-lookup"><span data-stu-id="a738e-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="a738e-117">Zeigen Sie den Verlauf für die Ressourcennutzung gegen ein Ziel an, einschließlich einer Aufschlüsselung zur Nutzung der Zeit der Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a738e-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="a738e-118">Pflegen Sie ein Repository für Fähigkeiten und Kompetenzen.</span><span class="sxs-lookup"><span data-stu-id="a738e-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="a738e-119">Sie können Ihr Projekt mit einem Team aus generischen oder benannten Ressourcen in Project Operations besetzen.</span><span class="sxs-lookup"><span data-stu-id="a738e-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="a738e-120">Sie können verschiedene Methoden verwenden, um Teammitglieder Hinzuzufügen und Zuzuweisen und ihre Buchungen und Zuweisungen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a738e-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 
