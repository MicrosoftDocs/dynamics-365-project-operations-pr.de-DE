---
title: Dual-Write-Integration für Project Operations
description: Dieses Thema bietet einen Überblick über die Dual-Write-Integration von Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998680"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="5fdd7-103">Dual-Write-Integration für Project Operations – Überblick</span><span class="sxs-lookup"><span data-stu-id="5fdd7-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="5fdd7-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="5fdd7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5fdd7-105">Project Operations verwendet [Dual-Write-Funktionen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), um Daten in Microsoft Dataverse und Dynamics 365 Finance zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="5fdd7-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="5fdd7-106">Die folgende Abbildung zeigt, wie Daten im Rahmen dieser Integration zwischen Dataverse und Finance synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5fdd7-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Übersicht über die Project Operations-Dataflows](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="5fdd7-108">Project Operations in Dataverse bietet eine moderne Benutzeroberfläche und eine einfache Erweiterbarkeit ohne Code/Low-Code mit Power Platform Fähigkeiten.</span><span class="sxs-lookup"><span data-stu-id="5fdd7-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="5fdd7-109">Projektmanager, Ressourcenmanager, Mitglieder des Projektteams und andere Front-Office-Mitarbeiter führen ihre Aktivitäten in Project Operations in Dataverse aus.</span><span class="sxs-lookup"><span data-stu-id="5fdd7-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="5fdd7-110">Project Operations in Finance bietet Unterstützung bei der Projektbuchhaltung und Umsatzrealisierung.</span><span class="sxs-lookup"><span data-stu-id="5fdd7-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="5fdd7-111">Project Operations fügt sich in den Finanzrahmen von Finance ein, um Umsatzsteuerberechnungen, Wechselkurse, Finanzdimensionsberichte und mehr zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5fdd7-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="5fdd7-112">Die Erfahrungen der Projektbuchhalter befinden sich hauptsächlich in Finance.</span><span class="sxs-lookup"><span data-stu-id="5fdd7-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="5fdd7-113">Die Project Operations-Integration besteht aus der folgenden Komponentenintegration:</span><span class="sxs-lookup"><span data-stu-id="5fdd7-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="5fdd7-114">Project Operations-Einrichtung und Konfigurationsdatenintegration</span><span class="sxs-lookup"><span data-stu-id="5fdd7-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="5fdd7-115">Projekt-Schätz- und Ist-Werte</span><span class="sxs-lookup"><span data-stu-id="5fdd7-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="5fdd7-116">Projektrechnungen</span><span class="sxs-lookup"><span data-stu-id="5fdd7-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="5fdd7-117">Ausgabenverwaltung</span><span class="sxs-lookup"><span data-stu-id="5fdd7-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="5fdd7-118">Kreditorenrechnung</span><span class="sxs-lookup"><span data-stu-id="5fdd7-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
