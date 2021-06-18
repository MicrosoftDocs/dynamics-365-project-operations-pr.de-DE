---
title: Eine Arbeitsstundenvorlage erstellen
description: In diesem Thema wird beschrieben, wie Sie eine Arbeitszeitvorlage in Project Service erstellen.
author: ruhercul
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997195"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="ec24f-103">Erstellen Sie eine Arbeitszeitvorlage (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ec24f-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ec24f-104">Um ein Projekt zu erstellen und zu verwalten, müssen Sie eine Kalendervorlage auf das Projekt anwenden.</span><span class="sxs-lookup"><span data-stu-id="ec24f-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="ec24f-105">Die Kalendervorlage definiert die folgenden Projektattribute:</span><span class="sxs-lookup"><span data-stu-id="ec24f-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="ec24f-106">Arbeitszeit einschließlich Start- und Endzeit</span><span class="sxs-lookup"><span data-stu-id="ec24f-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="ec24f-107">Werktags</span><span class="sxs-lookup"><span data-stu-id="ec24f-107">Working days</span></span>
- <span data-ttu-id="ec24f-108">Kalenderausnahmen wie arbeitsfreie Tage</span><span class="sxs-lookup"><span data-stu-id="ec24f-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="ec24f-109">Die Kalendervorlage, die auf ein Projekt angewendet wird, ist eine Kopie der Kalendervorlage, die in den Einstellungen Ihrer Organisation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ec24f-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="ec24f-110">Wenn Sie die Kalendervorlage ändern, werden diese Änderungen nicht auf die Arbeitszeiten des Projekts übertragen.</span><span class="sxs-lookup"><span data-stu-id="ec24f-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="ec24f-111">Um die Arbeitszeiten des Projekts zu ändern, muss eine neue Vorlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec24f-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="ec24f-112">Um eine Kalendervorlage für Ihre Organisation zu erstellen, gibt es zwei Hauptanforderungen:</span><span class="sxs-lookup"><span data-stu-id="ec24f-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="ec24f-113">Definieren Sie die gewünschten Arbeitszeiten der Vorlage mithilfe einer neuen oder vorhandenen buchbaren Ressource.</span><span class="sxs-lookup"><span data-stu-id="ec24f-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="ec24f-114">Erstellen Sie eine neue Kalendervorlage und ordnen Sie die Vorlage der buchbaren Ressource zu.</span><span class="sxs-lookup"><span data-stu-id="ec24f-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="ec24f-115">**Arbeitsstunden der Vorlage definieren**</span><span class="sxs-lookup"><span data-stu-id="ec24f-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="ec24f-116">Navigieren Sie zu **Ressourcen** \> **Ressourcen**.</span><span class="sxs-lookup"><span data-stu-id="ec24f-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="ec24f-117">Erstellen Sie eine neue Ressource, auf die in der Kalendervorlage verwiesen werden soll, oder wählen Sie eine vorhandene Ressource aus.</span><span class="sxs-lookup"><span data-stu-id="ec24f-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="ec24f-118">Wählen Sie die Registerkarte **Arbeitsstunden** der Ressource und vervollständigen Sie die Anweisungen in [Arbeitszeiten für eine Ressource festlegen](/dynamics365/field-service/set-work-hours-resource.md) um die Kalenderregeln zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ec24f-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="ec24f-119">**Erstellen einer neuen Kalendervorlage.**</span><span class="sxs-lookup"><span data-stu-id="ec24f-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="ec24f-120">Wechseln Sie zu **Einstellungen** \> **Kalendervorlage**.</span><span class="sxs-lookup"><span data-stu-id="ec24f-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="ec24f-121">Wählen Sie **Neu** und geben Sie einen Namen, eine Beschreibung und eine Vorlagenressource ein.</span><span class="sxs-lookup"><span data-stu-id="ec24f-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="ec24f-122">Wenn in einer Kalendervorlage auf eine Ressource verwiesen wird, wird der Kalendervorlage eine Kopie des Kalenders der Ressource zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ec24f-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="ec24f-123">Wenn die Arbeitszeiten der kopierten Vorlage sich ändern, werden diese Änderungen nicht auf die Kalendervoralge übertragen.</span><span class="sxs-lookup"><span data-stu-id="ec24f-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="ec24f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec24f-124">See Also</span></span>  
 [<span data-ttu-id="ec24f-125">Ressourcen einrichten</span><span class="sxs-lookup"><span data-stu-id="ec24f-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
