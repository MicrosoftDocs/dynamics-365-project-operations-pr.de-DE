---
title: Projektstatus verstehen
description: Dieses Thema enthält Informationen zum Status, der Projekten in Dynamics 365 Project Operations zugewiesen ist.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076396"
---
# <a name="understand-project-status"></a><span data-ttu-id="49015-103">Projektstatus verstehen</span><span class="sxs-lookup"><span data-stu-id="49015-103">Understand project status</span></span>

<span data-ttu-id="49015-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="49015-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="49015-105">Der Abschnitt **Status** auf der Seite **Projektentität** bietet eine Zusammenfassung des Projektzustands basierend auf Kosten und Aufwand.</span><span class="sxs-lookup"><span data-stu-id="49015-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="49015-106">Felder der Statuszusammenfassung</span><span class="sxs-lookup"><span data-stu-id="49015-106">Status summary fields</span></span>

- <span data-ttu-id="49015-107">Das Feld **Gesamtprojektstatus** kann bearbeitet werden und zeigt den Gesamtstatus für das Projekt an.</span><span class="sxs-lookup"><span data-stu-id="49015-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="49015-108">Dieses Feld verwendet Farben (z. B. Grün, Gelb und Rot), um ein zunehmendes Risiko anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="49015-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="49015-109">Im Feld **Kommentare** kann der Projektmanager bestimmte Kommentare zum Status eingeben.</span><span class="sxs-lookup"><span data-stu-id="49015-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="49015-110">Das Feld **Status aktualisiert am** kann nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="49015-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="49015-111">Der Wert in diesem Feld ist ein Zeitstempel, der angibt, wann der Status zuletzt aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="49015-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="49015-112">Die Felder **Zeitplanleistung** und **Kostenleistung** werden über das Verfolgungsraster festgelegt.</span><span class="sxs-lookup"><span data-stu-id="49015-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="49015-113">Wenn die Zeitplan- und Kostenabweichung für den Stammknoten in der Ansicht **Aufwandsverfolgung** positiv sind, können Sie diese Felder auf **Vorsprung** festlegen.</span><span class="sxs-lookup"><span data-stu-id="49015-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="49015-114">Wenn die Zeitplan- und Kostenabweichung für den Stammknoten negativ sind, können Sie diese Felder auf **Rückstand** festlegen.</span><span class="sxs-lookup"><span data-stu-id="49015-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
