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
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286382"
---
# <a name="update-a-project"></a><span data-ttu-id="be4ca-103">Ein Projekt aktualisieren</span><span class="sxs-lookup"><span data-stu-id="be4ca-103">Update a project</span></span>

<span data-ttu-id="be4ca-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="be4ca-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="be4ca-105">Im Folgenden finden Sie eine Zusammenfassung der Felder, die für ein Projekt aktualisiert werden können, nachdem es erstellt wurde, sowie alle anwendbaren Auswirkungen der Aktualisierungen.</span><span class="sxs-lookup"><span data-stu-id="be4ca-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="be4ca-106">Projektdetailfelder</span><span class="sxs-lookup"><span data-stu-id="be4ca-106">Project detail fields</span></span>

- <span data-ttu-id="be4ca-107">**Name**: Der Titel des Projekts</span><span class="sxs-lookup"><span data-stu-id="be4ca-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="be4ca-108">**Beschreibung**: Eine Übersicht über das Projekt</span><span class="sxs-lookup"><span data-stu-id="be4ca-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="be4ca-109">**Kunde**: Das Unternehmen, für das das Projekt bereitgestellt wird</span><span class="sxs-lookup"><span data-stu-id="be4ca-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="be4ca-110">**Kalendervorlage**: Die Arbeitszeiten des Projekts</span><span class="sxs-lookup"><span data-stu-id="be4ca-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="be4ca-111">Wenn das Feld geändert wird, wird der gesamte Zeitplan neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="be4ca-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="be4ca-112">**Währung**: Die Währung für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="be4ca-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="be4ca-113">Dieses Feld basiert standardmäßig auf der in der Vertragseinheit definierten Währung.</span><span class="sxs-lookup"><span data-stu-id="be4ca-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="be4ca-114">Wenn die Vertragseinheit aktualisiert wird, wird auch das Feld aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="be4ca-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="be4ca-115">**Vertragseinheit**: Die Organisationseinheit, die die Unternehmensgruppe oder den Geschäftsbereich darstellt, die bzw. der hauptsächlich für den Verkaufsabschluss und die Verwaltung der Bereitstellung von Arbeit und Services an den Kunden verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="be4ca-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="be4ca-116">**Projektmanager**: Das Projektteammitglied, das befugt ist, Zeiteinträge und Ausgaben zu überprüfen und zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="be4ca-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="be4ca-117">Felder schätzen</span><span class="sxs-lookup"><span data-stu-id="be4ca-117">Estimate fields</span></span>

- <span data-ttu-id="be4ca-118">**Geschätztes Startdatum** : Das Datum, an dem das Projekt beginnt</span><span class="sxs-lookup"><span data-stu-id="be4ca-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="be4ca-119">Wenn dieses Feld aktualisiert wird, werden alle Aufgaben im Projekt proportional zum Startdatum des neuen Startdatums verschoben.</span><span class="sxs-lookup"><span data-stu-id="be4ca-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="be4ca-120">**Enddatum**: Das Datum, an dem das Projekt enden soll</span><span class="sxs-lookup"><span data-stu-id="be4ca-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="be4ca-121">**Aufwand**: Der geschätzte Aufwand des Projekts</span><span class="sxs-lookup"><span data-stu-id="be4ca-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="be4ca-122">Wenn dem Projekt Aufgaben hinzugefügt werden, kann dieses Feld nicht mehr bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="be4ca-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="be4ca-123">**Geschätzte Arbeitskosten**: Die geschätzten Arbeitskosten des Projekts</span><span class="sxs-lookup"><span data-stu-id="be4ca-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="be4ca-124">Wenn dem Projekt Arbeitskosten hinzugefügt werden, kann dieses Feld nicht mehr bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="be4ca-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="be4ca-125">**Geschätzte Kosten**: Die geschätzten Kosten des Projekts</span><span class="sxs-lookup"><span data-stu-id="be4ca-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="be4ca-126">Wenn dem Projekt Ausgaben hinzugefügt werden, kann dieses Feld nicht mehr bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="be4ca-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="be4ca-127">Aktuelle Felder des Projekts</span><span class="sxs-lookup"><span data-stu-id="be4ca-127">Project actual fields</span></span>
- <span data-ttu-id="be4ca-128">**Tatsächlicher Start**: Das Datum, an dem das Projekt gestartet wurde</span><span class="sxs-lookup"><span data-stu-id="be4ca-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="be4ca-129">**Tatsächliches Ende**: Wird aktualisiert, wenn ein Projekt abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="be4ca-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="be4ca-130">Felder für den Projektstatus</span><span class="sxs-lookup"><span data-stu-id="be4ca-130">Project status fields</span></span>

- <span data-ttu-id="be4ca-131">**Gesamtprojektstatus**: Der vom Projektmanager bereitgestellte Gesamtzustand des Projekts</span><span class="sxs-lookup"><span data-stu-id="be4ca-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="be4ca-132">**Kommentare**: Eine vom Projektmanager bereitgestellte Darstellung des aktuellen Zustands des Projekts</span><span class="sxs-lookup"><span data-stu-id="be4ca-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]