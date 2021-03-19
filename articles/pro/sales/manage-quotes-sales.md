---
title: Projektangebote verwalten
description: Dieses Thema enthält Informationen zu Projektangeboten.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87921221ea210e67a3ddc53bd124f292de80de99
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272927"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="24b7d-103">Projektangebote verwalten</span><span class="sxs-lookup"><span data-stu-id="24b7d-103">Manage project quotes</span></span>

<span data-ttu-id="24b7d-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="24b7d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="24b7d-105">In Dynamics 365 Project Operations sollen Projektangebote dazu beitragen, Vorschläge für die Projektarbeit zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="24b7d-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="24b7d-106">Die Struktur eines Projektangebots in Project Operations ist für Projektvorschläge mit den folgenden Komponenten strukturiert:</span><span class="sxs-lookup"><span data-stu-id="24b7d-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="24b7d-107">Angebotszeilen, die die diskreten Komponenten der Arbeit identifizieren, die als übergeordnete Komponenten dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="24b7d-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="24b7d-108">Angebotszeilendetails, die die Arbeit für jede übergeordnete Komponente oder Angebotszeile identifizieren und schätzen.</span><span class="sxs-lookup"><span data-stu-id="24b7d-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="24b7d-109">Zeitplan‑ oder Datumsschätzungen und die finanziellen Aspekte der Arbeit sind an diese Angebotszeile gebunden.</span><span class="sxs-lookup"><span data-stu-id="24b7d-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="24b7d-110">Für jede Angebotszeile werden Vertragsmodelle und kostenpflichtige Komponenten eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="24b7d-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="24b7d-111">Diese Einrichtung hilft bei der Schätzung der Verteilung von Einnahmen, Ausgaben und Rentabilität für jede Angebotszeile und das Gesamtangebot.</span><span class="sxs-lookup"><span data-stu-id="24b7d-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="24b7d-112">Alle projektbasierten Angebote anzeigen</span><span class="sxs-lookup"><span data-stu-id="24b7d-112">View all project-based quotes</span></span>

<span data-ttu-id="24b7d-113">Eine Liste aller Projektangebote finden Sie auf der **Angebote**-Listenseite.</span><span class="sxs-lookup"><span data-stu-id="24b7d-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="24b7d-114">Gehen Sie zu **Vertrieb** > **Angebote**.</span><span class="sxs-lookup"><span data-stu-id="24b7d-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="24b7d-115">Eine Liste aller Ihrer Projektangebote im System wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="24b7d-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="24b7d-116">Verwenden Sie **Ansicht wechseln**, um andere gefilterte Ansichten der Angebote auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="24b7d-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="24b7d-117">Mithilfe benutzerdefinierter Filterkriterien können Sie Ihre eigenen Ansichten und Navigationsoptionen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="24b7d-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="24b7d-118">Auf dieser Listenseite oder auf den Detailseiten können Angebote erstellt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="24b7d-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]