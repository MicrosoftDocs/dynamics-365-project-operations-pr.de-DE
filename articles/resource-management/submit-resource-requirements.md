---
title: Eine Ressourcenanforderung übermitteln
description: Sie können eine generierte Ressourcenanfrage als Ressourcenanforderung übermitteln. Die Anforderung wird dann zur Erfüllung an einen Resource Manager gesendet.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279137"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="37dd9-104">Eine Ressourcenanforderung übermitteln</span><span class="sxs-lookup"><span data-stu-id="37dd9-104">Submit a resource request</span></span>

<span data-ttu-id="37dd9-105">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="37dd9-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="37dd9-106">Sie können eine generierte Ressourcenanfrage als Ressourcenanforderung übermitteln.</span><span class="sxs-lookup"><span data-stu-id="37dd9-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="37dd9-107">Die Anfrage wird dann zur Erfüllung an einen Ressourcenmanager gesendet.</span><span class="sxs-lookup"><span data-stu-id="37dd9-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="37dd9-108">Wählen Sie in Dynamics 365 Project Operations auf der Seite **Projekte** die Registerkarte **Team** aus, um eine Liste der buchbaren Ressourcen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="37dd9-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="37dd9-109">Wählen Sie die allgemeine Ressource aus, die eine Ressourcenanforderung aus der Liste enthält, und klicken Sie dann auf **Anforderung einreichen**.</span><span class="sxs-lookup"><span data-stu-id="37dd9-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="37dd9-110">Der Anforderungsstatus des allgemeinen Teammitglieds wird in **Übermittelt** geändert.</span><span class="sxs-lookup"><span data-stu-id="37dd9-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="37dd9-111">Nachdem die Anforderung erfüllt ist, wird die generische Ressource durch eine benannte Ressource ersetzt, wenn der Ressourcenmanager die Anforderung durch die Buchung einer benannten Ressource erfüllt.</span><span class="sxs-lookup"><span data-stu-id="37dd9-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="37dd9-112">Wenn der Resource Manager andernfalls einen benannte Ressource vorschlägt, verbleibt die allgemeine Ressource im Team, und der Anforderungsstatus wird in **Prüfung erforderlich** geändert.</span><span class="sxs-lookup"><span data-stu-id="37dd9-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]