---
title: Eine Arbeitsstundenvorlage erstellen
description: In diesem Thema wird beschrieben, wie Sie eine Arbeitszeitvorlage in Project Service erstellen.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981254"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="fcb70-103">Erstellen Sie eine Arbeitszeitvorlage (Project Service)</span><span class="sxs-lookup"><span data-stu-id="fcb70-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fcb70-104">Um ein Projekt zu erstellen und zu verwalten, müssen Sie eine Kalendervorlage auf das Projekt anwenden.</span><span class="sxs-lookup"><span data-stu-id="fcb70-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="fcb70-105">Die Kalendervorlage definiert die folgenden Projektattribute:</span><span class="sxs-lookup"><span data-stu-id="fcb70-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="fcb70-106">Arbeitszeit einschließlich Start- und Endzeit</span><span class="sxs-lookup"><span data-stu-id="fcb70-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="fcb70-107">Werktags</span><span class="sxs-lookup"><span data-stu-id="fcb70-107">Working days</span></span>
- <span data-ttu-id="fcb70-108">Kalenderausnahmen wie arbeitsfreie Tage</span><span class="sxs-lookup"><span data-stu-id="fcb70-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="fcb70-109">Die Kalendervorlage, die auf ein Projekt angewendet wird, ist eine Kopie der Kalendervorlage, die in den Einstellungen Ihrer Organisation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="fcb70-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="fcb70-110">Wenn Sie die Kalendervorlage ändern, werden diese Änderungen nicht auf die Arbeitszeiten des Projekts übertragen.</span><span class="sxs-lookup"><span data-stu-id="fcb70-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="fcb70-111">Um die Arbeitszeiten des Projekts zu ändern, muss eine neue Vorlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcb70-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="fcb70-112">Um eine Kalendervorlage für Ihre Organisation zu erstellen, gibt es zwei Hauptanforderungen:</span><span class="sxs-lookup"><span data-stu-id="fcb70-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="fcb70-113">Definieren Sie die gewünschten Arbeitszeiten der Vorlage mithilfe einer neuen oder vorhandenen buchbaren Ressource.</span><span class="sxs-lookup"><span data-stu-id="fcb70-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="fcb70-114">Erstellen Sie eine neue Kalendervorlage und ordnen Sie die Vorlage der buchbaren Ressource zu.</span><span class="sxs-lookup"><span data-stu-id="fcb70-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="fcb70-115">**Arbeitsstunden der Vorlage definieren**</span><span class="sxs-lookup"><span data-stu-id="fcb70-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="fcb70-116">Navigieren Sie zu **Ressourcen** \> **Ressourcen**.</span><span class="sxs-lookup"><span data-stu-id="fcb70-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="fcb70-117">Erstellen Sie eine neue Ressource, auf die in der Kalendervorlage verwiesen werden soll, oder wählen Sie eine vorhandene Ressource aus.</span><span class="sxs-lookup"><span data-stu-id="fcb70-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="fcb70-118">Wählen Sie die Registerkarte **Arbeitsstunden** der Ressource und vervollständigen Sie die Anweisungen in [Arbeitszeiten für eine Ressource festlegen](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) um die Kalenderregeln zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fcb70-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="fcb70-119">**Erstellen einer neuen Kalendervorlage.**</span><span class="sxs-lookup"><span data-stu-id="fcb70-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="fcb70-120">Wechseln Sie zu **Einstellungen** \> **Kalendervorlage**.</span><span class="sxs-lookup"><span data-stu-id="fcb70-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="fcb70-121">Wählen Sie **Neu** und geben Sie einen Namen, eine Beschreibung und eine Vorlagenressource ein.</span><span class="sxs-lookup"><span data-stu-id="fcb70-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="fcb70-122">Wenn in einer Kalendervorlage auf eine Ressource verwiesen wird, wird der Kalendervorlage eine Kopie des Kalenders der Ressource zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="fcb70-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="fcb70-123">Wenn die Arbeitszeiten der kopierten Vorlage sich ändern, werden diese Änderungen nicht auf die Kalendervoralge übertragen.</span><span class="sxs-lookup"><span data-stu-id="fcb70-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="fcb70-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fcb70-124">See Also</span></span>  
 [<span data-ttu-id="fcb70-125">Ressourcen einrichten</span><span class="sxs-lookup"><span data-stu-id="fcb70-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
