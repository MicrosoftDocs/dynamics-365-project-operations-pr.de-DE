---
title: Periodentypen
description: Dieses Thema enthält Informationen zum Einrichten von Periodentypen für Umsatzschätzungen.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531431"
---
# <a name="period-types"></a><span data-ttu-id="7746d-103">Periodentypen</span><span class="sxs-lookup"><span data-stu-id="7746d-103">Period types</span></span>

<span data-ttu-id="7746d-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="7746d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7746d-105">Ein Periodentyp definiert, wie häufig die Einnahmen aus einem Projekt geschätzt werden.</span><span class="sxs-lookup"><span data-stu-id="7746d-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="7746d-106">Dieses Thema enthält Informationen zum Einrichten von Periodentypen für Umsatzschätzungen.</span><span class="sxs-lookup"><span data-stu-id="7746d-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="7746d-107">Erstellen und Arbeiten mit Periodentypen</span><span class="sxs-lookup"><span data-stu-id="7746d-107">Create and work with period types</span></span>
<span data-ttu-id="7746d-108">Führen Sie die folgenden Schritte aus, um Periodentypen zu erstellen und damit zu arbeiten:</span><span class="sxs-lookup"><span data-stu-id="7746d-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="7746d-109">Gehen Sie in der Dynamics 365 Finance-Umgebung zu **Projektmanagement und Buchhaltung** > **Einrichten** > **Schätzungen** > **Periodentypen**.</span><span class="sxs-lookup"><span data-stu-id="7746d-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="7746d-110">Wählen Sie **Neu** aus, um einen neuen Periodentyp zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7746d-110">Select **New** to create new period type.</span></span> <span data-ttu-id="7746d-111">Geben Sie einen Namen und eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="7746d-111">Enter a name and description.</span></span>
3. <span data-ttu-id="7746d-112">Wählen Sie einen Wert im **Häufigkeit** aus:</span><span class="sxs-lookup"><span data-stu-id="7746d-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="7746d-113">Wenn Sie **Woche**, **Zweiwöchentlich**, **Halbmonatlich**, **Monat**, **Tag**, **Quartal** oder **Jahr** auswählen, wird der Kalender verwendet, um die Perioden zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7746d-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="7746d-114">Wenn Sie **Hauptbuchzeitraum** auswählen, werden Sachkontoperioden aus der Hauptbuchkonfiguration zum Generieren von Perioden verwendet.</span><span class="sxs-lookup"><span data-stu-id="7746d-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="7746d-115">Wenn Sie **Unbegrenzt** auswählen, können Sie benutzerdefinierte Zeiträume angeben.</span><span class="sxs-lookup"><span data-stu-id="7746d-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="7746d-116">Wählen Sie den Periodentyp-Datensatz aus und dann **Perioden generieren**, um Perioden für den Periodentyp zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7746d-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="7746d-117">Basierend auf der von Ihnen ausgewählten Periodenhäufigkeit haben Sie möglicherweise die Möglichkeit, ein Startdatum oder die Anzahl der zu generierenden Perioden anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7746d-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="7746d-118">Wählen Sie **Perioden** aus, um generierte Perioden zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7746d-118">Select **Periods** to review generated periods.</span></span>

