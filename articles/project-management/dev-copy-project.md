---
title: Projektvorlagen mit Projekt kopieren erstellen
description: Dieses Thema enthält Informationen zum Erstellen von Projektvorlagen mithilfe der benutzerdefinierten Aktion „Projekt kopieren“.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642407"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="f5a4f-103">Projektvorlagen mit Projekt kopieren erstellen</span><span class="sxs-lookup"><span data-stu-id="f5a4f-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="f5a4f-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="f5a4f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f5a4f-105">Dynamics 365 Project Operations unterstützt die Möglichkeit, ein Projekt zu kopieren und alle Zuweisungen auf die allgemeinen Ressourcen zurückzusetzen, die die Rolle darstellen.</span><span class="sxs-lookup"><span data-stu-id="f5a4f-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="f5a4f-106">Kunden können diese Funktionalität verwenden, um grundlegende Projektvorlagen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f5a4f-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="f5a4f-107">Wenn Sie **Projekt kopieren** auswählen, wird der Status des Zielprojekts aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f5a4f-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="f5a4f-108">Verwenden Sie **Statusgrund**, um festzustellen, wann die Kopieraktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f5a4f-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="f5a4f-109">Durch Auswahl von **Projekt kopieren** wird auch das Startdatum des Projekts auf das aktuelle Startdatum aktualisiert, wenn in der Zielprojektentität kein Zieldatum erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="f5a4f-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="f5a4f-110">Benutzerdefinierte Aktion „Projekt kopieren“</span><span class="sxs-lookup"><span data-stu-id="f5a4f-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="f5a4f-111">Name des Dataflows</span><span class="sxs-lookup"><span data-stu-id="f5a4f-111">Name</span></span> 

<span data-ttu-id="f5a4f-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="f5a4f-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="f5a4f-113">Eingabeparameter</span><span class="sxs-lookup"><span data-stu-id="f5a4f-113">Input parameters</span></span>
<span data-ttu-id="f5a4f-114">Es gibt drei Eingabeparameter:</span><span class="sxs-lookup"><span data-stu-id="f5a4f-114">There are three input parameters:</span></span>

| <span data-ttu-id="f5a4f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5a4f-115">Parameter</span></span>          | <span data-ttu-id="f5a4f-116">Art</span><span class="sxs-lookup"><span data-stu-id="f5a4f-116">Type</span></span>   | <span data-ttu-id="f5a4f-117">Werte</span><span class="sxs-lookup"><span data-stu-id="f5a4f-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="f5a4f-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="f5a4f-118">ProjectCopyOption</span></span>  | <span data-ttu-id="f5a4f-119">String</span><span class="sxs-lookup"><span data-stu-id="f5a4f-119">String</span></span> | <span data-ttu-id="f5a4f-120">**{"removeNamedResources":true}** oder **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="f5a4f-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="f5a4f-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="f5a4f-121">SourceProject</span></span>      | <span data-ttu-id="f5a4f-122">Entitätsreferenz</span><span class="sxs-lookup"><span data-stu-id="f5a4f-122">Entity Reference</span></span> | <span data-ttu-id="f5a4f-123">Quellprojekt</span><span class="sxs-lookup"><span data-stu-id="f5a4f-123">Source Project</span></span> |
| <span data-ttu-id="f5a4f-124">Zielsprache</span><span class="sxs-lookup"><span data-stu-id="f5a4f-124">Target</span></span>             | <span data-ttu-id="f5a4f-125">Entitätsreferenz</span><span class="sxs-lookup"><span data-stu-id="f5a4f-125">Entity Reference</span></span> | <span data-ttu-id="f5a4f-126">Zielprojekt</span><span class="sxs-lookup"><span data-stu-id="f5a4f-126">Target Project</span></span> |


- <span data-ttu-id="f5a4f-127">**{"clearTeamsAndAssignments":true}**: Das Standardverhalten für Project für das Web. Dadurch werden alle Arbeitsaufträge und Teammitglieder entfernt.</span><span class="sxs-lookup"><span data-stu-id="f5a4f-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="f5a4f-128">**{"removeNamedResources":true}** Das Standardverhalten für Project Operations, bei dem Zuweisungen zu generischen Ressourcen zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="f5a4f-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="f5a4f-129">Weitere Standardinformationen über Aktionen finden Sie unter [Nutzen von Web-API-Aktionen](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions).</span><span class="sxs-lookup"><span data-stu-id="f5a4f-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="f5a4f-130">Zu kopierende Felder angeben</span><span class="sxs-lookup"><span data-stu-id="f5a4f-130">Specify fields to copy</span></span> 
<span data-ttu-id="f5a4f-131">Wenn die Aktion aufgerufen wird, wird mit **Projekt kopieren** die Ansicht **Projektspalten kopieren** betrachtet, um zu bestimmen, welche Felder kopiert werden sollen, wenn das Projekt kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="f5a4f-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
