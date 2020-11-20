---
title: Ein Projekt aktualisieren
description: Dieses Thema bietet Informationen zur Aktualisierung von Projekten in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131432"
---
# <a name="update-a-project"></a><span data-ttu-id="1efad-103">Ein Projekt aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1efad-103">Update a project</span></span>

<span data-ttu-id="1efad-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="1efad-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1efad-105">Im Folgenden finden Sie eine Zusammenfassung der Felder, die für ein Projekt aktualisiert werden können, nachdem es erstellt wurde, sowie alle anwendbaren Auswirkungen der Aktualisierungen.</span><span class="sxs-lookup"><span data-stu-id="1efad-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="1efad-106">Projektdetailfelder</span><span class="sxs-lookup"><span data-stu-id="1efad-106">Project detail fields</span></span>

- <span data-ttu-id="1efad-107">**Name**: Der Titel des Projekts</span><span class="sxs-lookup"><span data-stu-id="1efad-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="1efad-108">**Beschreibung**: Eine Übersicht über das Projekt</span><span class="sxs-lookup"><span data-stu-id="1efad-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="1efad-109">**Kunde**: Das Unternehmen, für das das Projekt bereitgestellt wird</span><span class="sxs-lookup"><span data-stu-id="1efad-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="1efad-110">**Kalendervorlage**: Die Arbeitszeiten des Projekts</span><span class="sxs-lookup"><span data-stu-id="1efad-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="1efad-111">Wenn das Feld geändert wird, wird der gesamte Zeitplan neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="1efad-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="1efad-112">**Währung**: Die Währung für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="1efad-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="1efad-113">Dieses Feld basiert standardmäßig auf der in der Vertragseinheit definierten Währung.</span><span class="sxs-lookup"><span data-stu-id="1efad-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="1efad-114">Wenn die Vertragseinheit aktualisiert wird, wird auch das Feld aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1efad-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="1efad-115">**Vertragseinheit**: Die Organisationseinheit, die die Unternehmensgruppe oder den Geschäftsbereich darstellt, die bzw. der hauptsächlich für den Verkaufsabschluss und die Verwaltung der Bereitstellung von Arbeit und Services an den Kunden verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="1efad-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="1efad-116">**Projektmanager**: Das Projektteammitglied, das befugt ist, Zeiteinträge und Ausgaben zu überprüfen und zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="1efad-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="1efad-117">Felder schätzen</span><span class="sxs-lookup"><span data-stu-id="1efad-117">Estimate fields</span></span>

- <span data-ttu-id="1efad-118">**Geschätztes Startdatum** : Das Datum, an dem das Projekt beginnt</span><span class="sxs-lookup"><span data-stu-id="1efad-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="1efad-119">Wenn dieses Feld aktualisiert wird, werden alle Aufgaben im Projekt proportional zum Startdatum des neuen Startdatums verschoben.</span><span class="sxs-lookup"><span data-stu-id="1efad-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="1efad-120">**Enddatum**: Das Datum, an dem das Projekt enden soll</span><span class="sxs-lookup"><span data-stu-id="1efad-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="1efad-121">**Aufwand**: Der geschätzte Aufwand des Projekts</span><span class="sxs-lookup"><span data-stu-id="1efad-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="1efad-122">Wenn dem Projekt Aufgaben hinzugefügt werden, kann dieses Feld nicht mehr bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1efad-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="1efad-123">**Geschätzte Arbeitskosten**: Die geschätzten Arbeitskosten des Projekts</span><span class="sxs-lookup"><span data-stu-id="1efad-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="1efad-124">Wenn dem Projekt Arbeitskosten hinzugefügt werden, kann dieses Feld nicht mehr bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1efad-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="1efad-125">**Geschätzte Kosten**: Die geschätzten Kosten des Projekts</span><span class="sxs-lookup"><span data-stu-id="1efad-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="1efad-126">Wenn dem Projekt Ausgaben hinzugefügt werden, kann dieses Feld nicht mehr bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1efad-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="1efad-127">Aktuelle Felder des Projekts</span><span class="sxs-lookup"><span data-stu-id="1efad-127">Project actual fields</span></span>
- <span data-ttu-id="1efad-128">**Tatsächlicher Start**: Das Datum, an dem das Projekt gestartet wurde</span><span class="sxs-lookup"><span data-stu-id="1efad-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="1efad-129">**Tatsächliches Ende**: Wird aktualisiert, wenn ein Projekt abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="1efad-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="1efad-130">Felder für den Projektstatus</span><span class="sxs-lookup"><span data-stu-id="1efad-130">Project status fields</span></span>

- <span data-ttu-id="1efad-131">**Gesamtprojektstatus**: Der vom Projektmanager bereitgestellte Gesamtzustand des Projekts</span><span class="sxs-lookup"><span data-stu-id="1efad-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="1efad-132">**Kommentare**: Eine vom Projektmanager bereitgestellte Darstellung des aktuellen Zustands des Projekts</span><span class="sxs-lookup"><span data-stu-id="1efad-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>

