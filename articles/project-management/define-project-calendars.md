---
title: Projektkalender definieren
description: Dieses Thema enthält Informationen zum Anwenden einer Kalendervorlage auf ein Projekt, um den Projektplan zu verfolgen.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981299"
---
# <a name="define-project-calendars"></a><span data-ttu-id="8b122-103">Projektkalender definieren</span><span class="sxs-lookup"><span data-stu-id="8b122-103">Define project calendars</span></span>

<span data-ttu-id="8b122-104">_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="8b122-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8b122-105">Um ein Projekt zu erstellen und zu verwalten, müssen Sie eine Kalendervorlage auf das Projekt anwenden.</span><span class="sxs-lookup"><span data-stu-id="8b122-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="8b122-106">Die Kalendervorlage definiert die folgenden Projektattribute:</span><span class="sxs-lookup"><span data-stu-id="8b122-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="8b122-107">Arbeitszeit einschließlich Start- und Endzeit</span><span class="sxs-lookup"><span data-stu-id="8b122-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="8b122-108">Arbeitstage</span><span class="sxs-lookup"><span data-stu-id="8b122-108">Working days</span></span>
- <span data-ttu-id="8b122-109">Kalenderausnahmen wie arbeitsfreie Tage</span><span class="sxs-lookup"><span data-stu-id="8b122-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="8b122-110">Die Kalendervorlage, die auf ein Projekt angewendet wird, ist eine Kopie der Kalendervorlage, die in den Einstellungen Ihrer Organisation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8b122-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="8b122-111">Wenn Sie die Kalendervorlage ändern, werden diese Änderungen nicht auf die Arbeitszeiten des Projekts übertragen.</span><span class="sxs-lookup"><span data-stu-id="8b122-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="8b122-112">Um die Arbeitszeiten des Projekts zu ändern, muss eine neue Vorlage angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b122-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="8b122-113">Um eine Kalendervorlage für Ihre Organisation zu erstellen, gibt es zwei Hauptanforderungen:</span><span class="sxs-lookup"><span data-stu-id="8b122-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="8b122-114">Definieren Sie die gewünschten Arbeitszeiten der Vorlage mithilfe einer neuen oder vorhandenen buchbaren Ressource.</span><span class="sxs-lookup"><span data-stu-id="8b122-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="8b122-115">Erstellen Sie eine neue Kalendervorlage und ordnen Sie die Vorlage der buchbaren Ressource zu.</span><span class="sxs-lookup"><span data-stu-id="8b122-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="8b122-116">**Arbeitsstunden der Vorlage definieren**</span><span class="sxs-lookup"><span data-stu-id="8b122-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="8b122-117">Navigieren Sie zu **Ressourcen** \> **Ressourcen**.</span><span class="sxs-lookup"><span data-stu-id="8b122-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="8b122-118">Erstellen Sie eine neue Ressource, auf die in der Kalendervorlage verwiesen werden soll, oder wählen Sie eine vorhandene Ressource aus.</span><span class="sxs-lookup"><span data-stu-id="8b122-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="8b122-119">Wählen Sie die Registerkarte **Arbeitsstunden** der Ressource und vervollständigen Sie die Anweisungen in [Arbeitszeiten für eine Ressource festlegen](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) um die Kalenderregeln zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8b122-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="8b122-120">**Erstellen einer neuen Kalendervorlage.**</span><span class="sxs-lookup"><span data-stu-id="8b122-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="8b122-121">Wechseln Sie zu **Einstellungen** \> **Kalendervorlage**.</span><span class="sxs-lookup"><span data-stu-id="8b122-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="8b122-122">Wählen Sie **Neu** und geben Sie einen Namen, eine Beschreibung und eine Vorlagenressource ein.</span><span class="sxs-lookup"><span data-stu-id="8b122-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="8b122-123">Wenn in einer Kalendervorlage auf eine Ressource verwiesen wird, wird der Kalendervorlage eine Kopie des Kalenders der Ressource zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8b122-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="8b122-124">Wenn die Arbeitszeiten der kopierten Vorlage sich ändern, werden diese Änderungen nicht auf die Kalendervoralge übertragen.</span><span class="sxs-lookup"><span data-stu-id="8b122-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="8b122-125">Sie können die Arbeitsvorlage jetzt einer Projektkalendervorlage zuordnen.</span><span class="sxs-lookup"><span data-stu-id="8b122-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

