---
title: Eine Ressourcenanforderung übermitteln
description: Sie können eine generierte Ressourcenanfrage als Ressourcenanforderung übermitteln. Die Anforderung wird dann zur Erfüllung an einen Resource Manager gesendet.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014025"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="9a82e-104">Eine Ressourcenanforderung übermitteln</span><span class="sxs-lookup"><span data-stu-id="9a82e-104">Submit a resource request</span></span>

<span data-ttu-id="9a82e-105">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="9a82e-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9a82e-106">Sie können eine generierte Ressourcenanfrage als Ressourcenanforderung übermitteln.</span><span class="sxs-lookup"><span data-stu-id="9a82e-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="9a82e-107">Die Anfrage wird dann zur Erfüllung an einen Ressourcenmanager gesendet.</span><span class="sxs-lookup"><span data-stu-id="9a82e-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="9a82e-108">Wählen Sie in Dynamics 365 Project Operations auf der Seite **Projekte** die Registerkarte **Team** aus, um eine Liste der buchbaren Ressourcen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9a82e-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="9a82e-109">Wählen Sie die allgemeine Ressource aus, die eine Ressourcenanforderung aus der Liste enthält, und klicken Sie dann auf **Anforderung einreichen**.</span><span class="sxs-lookup"><span data-stu-id="9a82e-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="9a82e-110">Der Anforderungsstatus des allgemeinen Teammitglieds wird in **Übermittelt** geändert.</span><span class="sxs-lookup"><span data-stu-id="9a82e-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="9a82e-111">Nachdem die Anforderung erfüllt ist, wird die generische Ressource durch eine benannte Ressource ersetzt, wenn der Ressourcenmanager die Anforderung durch die Buchung einer benannten Ressource erfüllt.</span><span class="sxs-lookup"><span data-stu-id="9a82e-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="9a82e-112">Wenn der Resource Manager andernfalls einen benannte Ressource vorschlägt, verbleibt die allgemeine Ressource im Team, und der Anforderungsstatus wird in **Prüfung erforderlich** geändert.</span><span class="sxs-lookup"><span data-stu-id="9a82e-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]