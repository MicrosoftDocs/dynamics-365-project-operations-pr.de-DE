---
title: Projektkalender definieren
description: Dieses Thema enthält Informationen zum Anwenden einer Kalendervorlage auf ein Projekt, um den Projektplan zu verfolgen.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998995"
---
# <a name="define-project-calendars"></a><span data-ttu-id="21079-103">Projektkalender definieren</span><span class="sxs-lookup"><span data-stu-id="21079-103">Define project calendars</span></span>

<span data-ttu-id="21079-104">_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="21079-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="21079-105">Um ein Projekt zu erstellen und zu verwalten, müssen Sie eine Kalendervorlage auf das Projekt anwenden.</span><span class="sxs-lookup"><span data-stu-id="21079-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="21079-106">Die Kalendervorlage definiert die folgenden Projektattribute:</span><span class="sxs-lookup"><span data-stu-id="21079-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="21079-107">Arbeitszeit einschließlich Start- und Endzeit</span><span class="sxs-lookup"><span data-stu-id="21079-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="21079-108">Werktags</span><span class="sxs-lookup"><span data-stu-id="21079-108">Working days</span></span>
- <span data-ttu-id="21079-109">Kalenderausnahmen wie arbeitsfreie Tage</span><span class="sxs-lookup"><span data-stu-id="21079-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="21079-110">Die Kalendervorlage, die auf ein Projekt angewendet wird, ist eine Kopie der Kalendervorlage, die in den Einstellungen Ihrer Organisation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="21079-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="21079-111">Wenn Sie die Kalendervorlage ändern, werden diese Änderungen nicht auf die Arbeitszeiten des Projekts übertragen.</span><span class="sxs-lookup"><span data-stu-id="21079-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="21079-112">Um die Arbeitszeiten des Projekts zu ändern, muss eine neue Vorlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="21079-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="21079-113">Um eine Kalendervorlage für Ihre Organisation zu erstellen, gibt es zwei Hauptanforderungen:</span><span class="sxs-lookup"><span data-stu-id="21079-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="21079-114">Definieren Sie die gewünschten Arbeitszeiten der Vorlage mithilfe einer neuen oder vorhandenen buchbaren Ressource.</span><span class="sxs-lookup"><span data-stu-id="21079-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="21079-115">Erstellen Sie eine neue Kalendervorlage und ordnen Sie die Vorlage der buchbaren Ressource zu.</span><span class="sxs-lookup"><span data-stu-id="21079-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="21079-116">**Arbeitsstunden der Vorlage definieren**</span><span class="sxs-lookup"><span data-stu-id="21079-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="21079-117">Navigieren Sie zu **Ressourcen** \> **Ressourcen**.</span><span class="sxs-lookup"><span data-stu-id="21079-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="21079-118">Erstellen Sie eine neue Ressource, auf die in der Kalendervorlage verwiesen werden soll, oder wählen Sie eine vorhandene Ressource aus.</span><span class="sxs-lookup"><span data-stu-id="21079-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="21079-119">Wählen Sie die Registerkarte **Arbeitsstunden** der Ressource und vervollständigen Sie die Anweisungen in [Arbeitszeiten für eine Ressource festlegen](/dynamics365/field-service/set-work-hours-resource.md) um die Kalenderregeln zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="21079-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="21079-120">**Erstellen einer neuen Kalendervorlage.**</span><span class="sxs-lookup"><span data-stu-id="21079-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="21079-121">Wechseln Sie zu **Einstellungen** \> **Kalendervorlage**.</span><span class="sxs-lookup"><span data-stu-id="21079-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="21079-122">Wählen Sie **Neu** und geben Sie einen Namen, eine Beschreibung und eine Vorlagenressource ein.</span><span class="sxs-lookup"><span data-stu-id="21079-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="21079-123">Wenn in einer Kalendervorlage auf eine Ressource verwiesen wird, wird der Kalendervorlage eine Kopie des Kalenders der Ressource zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="21079-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="21079-124">Wenn die Arbeitszeiten der kopierten Vorlage sich ändern, werden diese Änderungen nicht auf die Kalendervoralge übertragen.</span><span class="sxs-lookup"><span data-stu-id="21079-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="21079-125">Sie können die Arbeitsvorlage jetzt einer Projektkalendervorlage zuordnen.</span><span class="sxs-lookup"><span data-stu-id="21079-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

