---
title: Stellen Sie Arbeitsschätzungen für ein Projekt während des Verkaufsprozesses zur Verfügung
description: Stellen Sie Arbeitsschätzungen für ein Projekt während des Verkaufsprozesses zur Verfügung (Project Service)
author: ruhercul
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
ms.openlocfilehash: ddb7f8c0ff8c7fd7e51edb42f9d227f2b91a811b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076574"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="4ec33-103">Stellen Sie Arbeitsschätzungen für ein Projekt während des Verkaufsprozesses zur Verfügung (Project Service)</span><span class="sxs-lookup"><span data-stu-id="4ec33-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4ec33-104">Während der Verkäufe Prozess, können Sie Umsatzschätzungen mit Angebotszeilen von Grund auf ausarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4ec33-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]<span data-ttu-id="4ec33-105">-Funktionen in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] bieten eine wissenschaftlichere und deterministischere Weise des Erhaltens von Umsatzschätzungen, indem Arbeitseinzelteile aufgegliedert und relevante Attribute verbunden werden, die zu den Schätzungen für das Projekt im Projektstrukturplan beitragen.</span><span class="sxs-lookup"><span data-stu-id="4ec33-105">capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="4ec33-106">Sobald Sie den Verkauf gewinnen, können Sie den verbundenen Projektstrukturplan in Ihrem Projektplan benutzen und ihn falls erforderlich weiter entwickeln für erfolgreiche Fertigstellung Ihres Projektes.</span><span class="sxs-lookup"><span data-stu-id="4ec33-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="4ec33-107">Verbinden Sie ein Projekt mit einer Angebotszeile</span><span class="sxs-lookup"><span data-stu-id="4ec33-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="4ec33-108">Wenn Sie eine projektbasierte Angebotszeile schaffen, können Sie ein neues Projekt von der Angebotszeile erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ec33-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="4ec33-109">Sie können Projektvorlagen, die entweder vorkonfigurierte Standardprojektpläne und Finanzschätzungen, die für Ihre Organisation allgemein sind sind, oder eine Kopie eines Projektplanes und -schätzungen von einem vorangehenden Projekt dann benutzen.</span><span class="sxs-lookup"><span data-stu-id="4ec33-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="4ec33-110">Wenn Sie ein Projekt schaffen, bietet das Wählen einer Projektvorlage eine Basis, um den Projektplan, die Schätzungen und die Rollenanforderungen weiter zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="4ec33-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="4ec33-111">Wenn Sie Ihr Projekt vom Angebot aus erstellen, ist das Projekt automatisch mit der Angebotszeile verbunden.</span><span class="sxs-lookup"><span data-stu-id="4ec33-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="4ec33-112">Projektschätzungskomponenten</span><span class="sxs-lookup"><span data-stu-id="4ec33-112">Project estimate components</span></span>  
 <span data-ttu-id="4ec33-113">Der Projektstrukturplan in einem Projekt liefert eine Weise, Arbeit in Aufgaben aufzugliedern, eine Hierarchie von Aufgaben beizubehalten, und eine Schätzung der Bemühung zuzuweisen, die es erfordert, um jede Aufgabe abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4ec33-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="4ec33-114">Sie können auch Rollen zu einer Aufgabe verbinden, um eine Schätzung der Art der Ressource anzuzeigen, die erforderlich ist, um eine Aufgabe und einen Zeitplan abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="4ec33-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="4ec33-115">Der Projektstrukturplan hilft Ihnen, Arbeitseinsatz- und Zeitplanschätzungen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="4ec33-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="4ec33-116">Standardmäßig nutzt das Projekt Preislisten, die Sie früher definierten.</span><span class="sxs-lookup"><span data-stu-id="4ec33-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="4ec33-117">Die Kosten und die Verkaufspreise, die in den Preislisten definiert werden, helfen, Haushaltsvoranschläge für den Projektstrukturplan zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="4ec33-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="4ec33-118">Wenn Ihr Projekt mit einem Angebot verbunden ist und das Angebot eine andere Preisliste als die Standardliste hat, wird die Preisliste des Angebots für Finanzschätzungen benutzt.</span><span class="sxs-lookup"><span data-stu-id="4ec33-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="4ec33-119">Import von Schätzungen von einem Projekt in ein Angebot</span><span class="sxs-lookup"><span data-stu-id="4ec33-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="4ec33-120">Sobald Sie Projektschätzungen im Projekt haben, können Sie diese Schätzungen in die Angebotszeile importieren.</span><span class="sxs-lookup"><span data-stu-id="4ec33-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="4ec33-121">In **Detailinformationen zur Angebotsposition** klicken Sie auf **Import aus Schätzungen**.</span><span class="sxs-lookup"><span data-stu-id="4ec33-121">In **Quote Line Details** , click **Import from estimates**.</span></span> 

-   <span data-ttu-id="4ec33-122">Wählen Sie aus, ob man die Projektschätzungen importiert, die durch Transaktionstyp, Rolle oder Knotenebene des Projektstrukturplans zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="4ec33-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4ec33-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ec33-123">See Also</span></span>  
 [<span data-ttu-id="4ec33-124">Handbuch des Projektmanagers</span><span class="sxs-lookup"><span data-stu-id="4ec33-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
