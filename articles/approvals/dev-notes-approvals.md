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
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290268"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="bb2de-103">Entwickleranmerkungen für Genehmigungen</span><span class="sxs-lookup"><span data-stu-id="bb2de-103">Developer notes for Approvals</span></span>

<span data-ttu-id="bb2de-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="bb2de-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bb2de-105">Dynamics 365 Project Operations enthält eine Validierungslogik, die anhand der Genehmigungsphasen einen korrekten Datensatzübergang gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="bb2de-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="bb2de-106">Richtige Datensatzübergänge stellen sicher:</span><span class="sxs-lookup"><span data-stu-id="bb2de-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="bb2de-107">Alle unterstützenden Zeilen werden in verwandten Tabellen wie Journalen und Istdaten erstellt.</span><span class="sxs-lookup"><span data-stu-id="bb2de-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="bb2de-108">Die genehmigende Person wird als **Projektgenehmiger** im Projekt gekennzeichnet, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="bb2de-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]