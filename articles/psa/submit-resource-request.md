---
title: Übermitteln einer Ressourcenanforderung
description: Dieses Thema enthält Informationen zum Übermitteln einer Anforderung für eine Projektressource.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 173572be43149aea253bf7beddb993f8c50ab337
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149722"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="87d0b-103">Übermitteln einer Ressourcenanforderung</span><span class="sxs-lookup"><span data-stu-id="87d0b-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="87d0b-104">Sie können eine generierte Ressourcenanfrage als Ressourcenanforderung übermitteln.</span><span class="sxs-lookup"><span data-stu-id="87d0b-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="87d0b-105">Die Anforderung wird dann zur Erfüllung an einen Resource Manager gesendet.</span><span class="sxs-lookup"><span data-stu-id="87d0b-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="87d0b-106">Klicken Sie in Project Service Automation (PSA) auf der Seite **Projekte** auf die Registerkarte **Team**, um eine Liste der buchbaren Ressourcen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="87d0b-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="87d0b-107">Wählen Sie die allgemeine Ressource aus, die eine Ressourcenanfrage aus der Liste enthält, und klicken Sie dann auf **Anforderung übermitteln**.</span><span class="sxs-lookup"><span data-stu-id="87d0b-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Übermitteln einer Ressourcenanforderung](media/RM-how-to-18.png)

<span data-ttu-id="87d0b-109">Der Anforderungsstatus des allgemeinen Teammitglieds wird in **Übermittelt** geändert.</span><span class="sxs-lookup"><span data-stu-id="87d0b-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="87d0b-110">Nachdem die Anforderung vom Resource Manager erfüllt wurde, wird die allgemeine Ressource durch eine benannte Ressource ersetzt, falls der Resource Manager die Anforderung durch die Buchung einer benannten Ressource erfüllt.</span><span class="sxs-lookup"><span data-stu-id="87d0b-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="87d0b-111">Andernfalls verbleibt die allgemeine Ressource im Team und der Anforderungsstatus wird in **Prüfung erforderlich** geändert, falls der Resource Manager eine benannte Ressource vorschlägt.</span><span class="sxs-lookup"><span data-stu-id="87d0b-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
