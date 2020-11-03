---
title: Eine Projektvorkalkulation entfernen
description: Dieses Thema enthält Informationen zum Entfernen einer Projektkalkulation nach deren Abschluss.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076577"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="99945-103">Eine Projektvorkalkulation entfernen</span><span class="sxs-lookup"><span data-stu-id="99945-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99945-104">Projektvorkalkulationen stellen die Finanzansicht für die Arbeit bereit, die für ein Projekt geschätzt und geplant wird.</span><span class="sxs-lookup"><span data-stu-id="99945-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="99945-105">Um mit Vorkalkulationen für ein Projekt arbeiten zu können, müssen Sie das Projekt an ein Vorkalkulationsprojekt anhängen.</span><span class="sxs-lookup"><span data-stu-id="99945-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="99945-106">Ein Vorkalkulationsprojekt basiert immer auf einem vorhandenen Projekt. Mehrere Projekte können sich jedoch auf ein einzelnes Vorkalkulationsprojekt beziehen.</span><span class="sxs-lookup"><span data-stu-id="99945-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="99945-107">An Vorkalkulationsprojekte können nur Festpreis- und Investitionsprojekte angehängt werden, und diese Projekte müssen zur selben Projektgruppe gehören wie das Vorkalkulationsprojekt.</span><span class="sxs-lookup"><span data-stu-id="99945-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="99945-108">Um ein Vorkalkulationsprojekt zu löschen, muss es vollständig sein.</span><span class="sxs-lookup"><span data-stu-id="99945-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="99945-109">In den folgenden Schritten wird erläutert, wie Sie eine Vorkalkulation entfernen.</span><span class="sxs-lookup"><span data-stu-id="99945-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="99945-110">Navigieren Sie zu **Projektmanagement und -buchhaltung** > **All Projekte** , und öffnen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="99945-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="99945-111">Wählen Sie auf der Registerkarte **Verwalten** **Vorkalkulationen** und auf der Seite **Schätzung** die Option **Entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="99945-111">On the **Manage** tab, select **Estimates** , and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="99945-112">Legen Sie auf der Seite **Vorkalkulation löschen** auf der Registerkarte **Allgemein** die folgenden Optionen fest:</span><span class="sxs-lookup"><span data-stu-id="99945-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="99945-113">**Periodencode** : Wählen Sie den Periodencode aus, um die entsprechenden Vorkalkulationsprojekte auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="99945-113">**Period code** : Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="99945-114">**Vorkalkulationsdatum** : Wählen Sie das geeignete Vorkalkulationsdatum für das Entfernen aus.</span><span class="sxs-lookup"><span data-stu-id="99945-114">**Estimate date** : Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="99945-115">**Mit WIP-Warnungen löschen** : Aktivieren Sie diese Option, um eine Benachrichtigung bereitzustellen, wenn eine Vorkalkulation, die mit einem WIP (Work in Progress) verknüpft ist, entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="99945-115">**Eliminate with WIP warnings** : Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="99945-116">Wenn diese Option nicht aktiviert ist, kann das Entfernen nicht fortgesetzt werden, wenn nicht geschätzte Transaktionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="99945-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="99945-117">Diese Option ist nur verfügbar, wenn das Entfernen auf ein Vorkalkulationsprojekt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="99945-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="99945-118">Es ist nicht verfügbar, wenn Sie regelmäßige Buchungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="99945-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="99945-119">Diese Einstellung funktioniert mit den Einstellungen auf der Registerkarte **Schätzung** auf der Seite **Projektparameter** in der Feldgruppe **Löschung bei nicht vorkalkulierten Buchungen zulassen**.</span><span class="sxs-lookup"><span data-stu-id="99945-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="99945-120">**Phase als 'abgeschlossen' festlegen** : Aktivieren Sie diese Option, um die Phase des Vorkalkulationsprojekts als **Abgeschlossen** festzulegen, nachdem Sie das Entfernen ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="99945-120">**Set stage to Finished** : Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="99945-121">**Vorkalkulationsliste drucken** : Wählen Sie die Informationen aus, die beim Drucken der Vorkalkulationsliste berücksichtigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="99945-121">**Print estimate list** : Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="99945-122">**Infolog anzeigen** : Aktivieren Sie diese Option, um das Infolog anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="99945-122">**Show Infolog** : Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="99945-123">**Buchungsdatum** : Wählen Sie das Buchungsdatum der Finanzbuchhaltung für die Vorkalkulation ein.</span><span class="sxs-lookup"><span data-stu-id="99945-123">**Posting date** : Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="99945-124">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="99945-124">Select **OK**.</span></span>
5. <span data-ttu-id="99945-125">Nach Abschluss des Entfernungsprozesses wird das entfernte Vorkalkulationsprojekt mit einem negativen Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="99945-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="99945-126">Wenn das Entfernen der Vorkalkulation nicht beabsichtigt war, können Sie die entfernte Vorkalkulation und dann **Entfernen stornieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="99945-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
