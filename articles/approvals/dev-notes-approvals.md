---
title: Entwickleranmerkungen für Genehmigungen
description: Dieses Thema enthält zusätzliche Informationen für Entwickler zur Arbeit mit Genehmigungen.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996790"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="016d8-103">Entwickleranmerkungen für Genehmigungen</span><span class="sxs-lookup"><span data-stu-id="016d8-103">Developer notes for Approvals</span></span>

<span data-ttu-id="016d8-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="016d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="016d8-105">Dynamics 365 Project Operations enthält eine Validierungslogik, die anhand der Genehmigungsphasen einen korrekten Datensatzübergang gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="016d8-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="016d8-106">Richtige Datensatzübergänge stellen sicher:</span><span class="sxs-lookup"><span data-stu-id="016d8-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="016d8-107">Alle unterstützenden Zeilen werden in verwandten Tabellen wie Journalen und Istdaten erstellt.</span><span class="sxs-lookup"><span data-stu-id="016d8-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="016d8-108">Die genehmigende Person wird als **Projektgenehmiger** im Projekt gekennzeichnet, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="016d8-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]