---
title: Eine Ressourcenanforderung übermitteln
description: Sie können eine generierte Ressourcenanfrage als Ressourcenanforderung übermitteln. Die Anforderung wird dann zur Erfüllung an einen Resource Manager gesendet.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076418"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="4846b-104">Eine Ressourcenanforderung übermitteln</span><span class="sxs-lookup"><span data-stu-id="4846b-104">Submit a resource request</span></span>

<span data-ttu-id="4846b-105">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="4846b-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4846b-106">Sie können eine generierte Ressourcenanfrage als Ressourcenanforderung übermitteln.</span><span class="sxs-lookup"><span data-stu-id="4846b-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="4846b-107">Die Anforderung wird dann zur Erfüllung an einen Resource Manager gesendet.</span><span class="sxs-lookup"><span data-stu-id="4846b-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="4846b-108">Wählen Sie in Dynamics 365 Project Operations auf der Seite **Projekte** die Registerkarte **Team** aus, um eine Liste der buchbaren Ressourcen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4846b-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="4846b-109">Wählen Sie die allgemeine Ressource aus, die eine Ressourcenanforderung aus der Liste enthält, und klicken Sie dann auf **Anforderung einreichen**.</span><span class="sxs-lookup"><span data-stu-id="4846b-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="4846b-110">Der Anforderungsstatus des allgemeinen Teammitglieds wird in **Übermittelt** geändert.</span><span class="sxs-lookup"><span data-stu-id="4846b-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="4846b-111">Nachdem die Anforderung vom Resource Manager erfüllt wurde, wird die allgemeine Ressource durch eine benannte Ressource ersetzt, falls der Resource Manager die Anforderung durch die Buchung einer benannten Ressource erfüllt.</span><span class="sxs-lookup"><span data-stu-id="4846b-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="4846b-112">Wenn der Resource Manager andernfalls einen benannte Ressource vorschlägt, verbleibt die allgemeine Ressource im Team, und der Anforderungsstatus wird in **Prüfung erforderlich** geändert.</span><span class="sxs-lookup"><span data-stu-id="4846b-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
