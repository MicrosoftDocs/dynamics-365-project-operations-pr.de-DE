---
title: Entwickleranmerkungen für Genehmigungen
description: Dieses Thema enthält zusätzliche Informationen für Entwickler zur Arbeit mit Genehmigungen.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483947"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="15af0-103">Entwickleranmerkungen für Genehmigungen</span><span class="sxs-lookup"><span data-stu-id="15af0-103">Developer notes for Approvals</span></span>

<span data-ttu-id="15af0-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="15af0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="15af0-105">Dynamics 365 Project Operations enthält eine Validierungslogik, die einen korrekten Datensatzübergang durch die Genehmigungsphasen gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="15af0-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="15af0-106">Richtige Datensatzübergänge stellen sicher:</span><span class="sxs-lookup"><span data-stu-id="15af0-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="15af0-107">Alle unterstützenden Zeilen werden in verwandten Tabellen wie Journalen und Istdaten erstellt.</span><span class="sxs-lookup"><span data-stu-id="15af0-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="15af0-108">Die genehmigende Person wird als **Projektgenehmiger** im Projekt gekennzeichnet, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="15af0-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
