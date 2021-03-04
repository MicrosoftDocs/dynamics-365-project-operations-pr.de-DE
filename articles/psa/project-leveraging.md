---
title: Vertriebsvorkalkulationen und Projekte
description: In diesem Thema finden Sie Informationen den Zeitplan und die Schätzungen im Vertriebsprozess zu Ihrem Vorteil nutzen.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 76e21f80e51e6f3092880dc629ba90b400805486
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148372"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="15a4f-103">Vertriebsvorkalkulationen und Projekte</span><span class="sxs-lookup"><span data-stu-id="15a4f-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="15a4f-104">Während des Vertriebsprozesses können Sie Vertriebsvorkalkulationen erstellen, indem Sie ein Projekt mit einem Vertriebsangebot verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="15a4f-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="15a4f-105">Dadurch kann es im Vertriebsprozess zu deterministischen Kalkulation kommen, um die Vorteile der Projektterminplanungs- und Kalkulationsfunktionen zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="15a4f-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="15a4f-106">Wird der Verkauf abgeschlossen, lässt sich der für die Vertriebsvorkalkulation verwendete Zeitplan als Basis für die weitere Verfeinerung des Projektplans nutzen.</span><span class="sxs-lookup"><span data-stu-id="15a4f-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="15a4f-107">Verknüpfung von Projekten mit Angebotspositionen</span><span class="sxs-lookup"><span data-stu-id="15a4f-107">Linking a project to a quote line</span></span>

<span data-ttu-id="15a4f-108">Wenn Sie eine projektbasierte Angebotsposition erstellen, können Sie ein neues Projekt erstellen oder ein bestehendes Projekt auf der Seite **Angebotsposition** zuordnen.</span><span class="sxs-lookup"><span data-stu-id="15a4f-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Formular für Angebotsposition](media/project-8.png)
 
<span data-ttu-id="15a4f-110">Wenn Sie ein neues Projekt aus Angebotspositionsdetails erstellen, können Sie Projektvorlagen nutzen.</span><span class="sxs-lookup"><span data-stu-id="15a4f-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="15a4f-111">Projektvorlagen sind für ein Unternehmen typische Musterprojekte, die Standardprojektpläne und finanzielle Vorkalkulationen darstellen.</span><span class="sxs-lookup"><span data-stu-id="15a4f-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="15a4f-112">Sie können außerdem Kopien von Projektplänen und Vorkalkulationen aus vergangenen Projekten darstellen.</span><span class="sxs-lookup"><span data-stu-id="15a4f-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Detailinformationen zur Angebotsposition](media/project-9.png)
  
<span data-ttu-id="15a4f-114">Wenn Sie das Projekt vom Angebot aus erstellen, ist das Projekt automatisch mit der Angebotszeile verbunden.</span><span class="sxs-lookup"><span data-stu-id="15a4f-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="15a4f-115">Komponenten von Vorkalkulationen in einem Projekt</span><span class="sxs-lookup"><span data-stu-id="15a4f-115">Components of estimates in a project</span></span>

<span data-ttu-id="15a4f-116">Ein Zeitplan ermöglicht die Aufgliederung von Arbeit in Aufgaben, die Beibehaltung einer Hierarchie von Aufgaben, die Festlegung der zur Ausführung einer Aufgabe erforderlichen Ressourcen und die Zuweisung einer Schätzung des Aufwands, den es erfordert, um eine Aufgabe abzuschließen</span><span class="sxs-lookup"><span data-stu-id="15a4f-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="15a4f-117">Sie können den Arbeitsaufwand definieren und Vorkalkulationen planen, indem Sie die Felder auf der Registerkarte **Zeitplan** der Seite **Projekt** verwenden.</span><span class="sxs-lookup"><span data-stu-id="15a4f-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="15a4f-118">Da dem Projekt eine Preisliste zugeordnet ist, werden finanzielle Vorkalkulationen anhand der in der Preisliste definierten Kosten und Verkaufspreise berechnet.</span><span class="sxs-lookup"><span data-stu-id="15a4f-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="15a4f-119">Importieren von Vorkalkulationen aus einem Projekt in ein Angebot</span><span class="sxs-lookup"><span data-stu-id="15a4f-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="15a4f-120">Nach der Definition von Projektvorkalkulationen können Sie diese in die Angebotszeile importieren.</span><span class="sxs-lookup"><span data-stu-id="15a4f-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="15a4f-121">Wählen Sie auf der Seite **Detailinformationen zur Angebotsposition** im Menüband die Schaltfläche **Aus Vorkalkulation importieren** aus, um Projektvorkalkulationen nach Transaktionstyp, Rolle oder Aufgabenebene zusammenzufassen.</span><span class="sxs-lookup"><span data-stu-id="15a4f-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
