---
title: Projektvorkalkulation (Festpreis) des Umsatzes
description: Dieses Thema enthält Informationen zum Festpreisumsatz in Projekten.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278912"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="956de-103">Projektvorkalkulation (Festpreis) des Umsatzes</span><span class="sxs-lookup"><span data-stu-id="956de-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="956de-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="956de-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="956de-105">Wenn Sie eine Projektvertragszeile mit den folgenden Attributen in Dynamics 365 Project Operations auf Microsoft Dataverse erstellen, erstellt das System automatisch ein Projekt zur Schätzung des Festpreisumsatzes.</span><span class="sxs-lookup"><span data-stu-id="956de-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="956de-106">Die Informationen in diesem Projekt basieren auf Folgendem:</span><span class="sxs-lookup"><span data-stu-id="956de-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="956de-107">Eine Abrechnungsmethode zum Festpreis.</span><span class="sxs-lookup"><span data-stu-id="956de-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="956de-108">Ein zugeordnetes Projekt.</span><span class="sxs-lookup"><span data-stu-id="956de-108">An associated project.</span></span>
  - <span data-ttu-id="956de-109">Mindestens ein Meilenstein, der auf der **Rechnungsplan**-Registerkarte auf der **Projektvertragszeile**-Seite definiert ist.</span><span class="sxs-lookup"><span data-stu-id="956de-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="956de-110">Projektvorkalkulationen (Festpreis) des Umsatzes überprüfen</span><span class="sxs-lookup"><span data-stu-id="956de-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="956de-111">Führen Sie die folgenden Schritte aus, um Projekte zur Schätzung von Festpreiseinnahmen zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="956de-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="956de-112">Gehen Sie in der Dynamics 365 Finance-Umgebung zu **Projektmanagement und Buchhaltung** > **Projekte** > **Projektvorkalkulation (Festpreis) des Umsatzes**.</span><span class="sxs-lookup"><span data-stu-id="956de-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="956de-113">Wählen Sie das Projekt aus, das Sie anzeigen möchten, und doppelklicken Sie auf **Projekt-ID schätzen**, um den Datensatz zu öffnen und die Details des Projekts zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="956de-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="956de-114">Erweitern Sie die **Projekt**-Registerkarte. Sie sehen ein Projekt im **Ausgewählte Projekte**-Raster.</span><span class="sxs-lookup"><span data-stu-id="956de-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="956de-115">Das System verwendet dies als Standardprojekt, da es sich um das Projekt handelt, das der Projektvertragszeile zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="956de-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="956de-116">Um die Zuordnung zu ändern, wählen Sie zusätzliche Projekte aus und fügen Sie sie dem **Ausgewählte Projekte**-Raster hinzu.</span><span class="sxs-lookup"><span data-stu-id="956de-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="956de-117">Wenn in diesem Raster mehrere Projekte ausgewählt sind, werden die prozentualen Projektabschluss- und Umsatzschätzungen für alle ausgewählten Projekte zusammen berechnet.</span><span class="sxs-lookup"><span data-stu-id="956de-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="956de-118">Projektkosten, Umsatzprofil, Kostenvorlage und der Periodencode können manuell festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="956de-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="956de-119">Wenn sie nicht manuell festgelegt werden, werden die Werte bei der ersten Schätzungsberechnung für das Projekt standardmäßig unter Verwendung der für Projektkosten- und Ertragsprofile konfigurierten Regeln verwendet.</span><span class="sxs-lookup"><span data-stu-id="956de-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]