---
title: Periodentypen
description: Dieses Thema enthält Informationen zum Einrichten von Periodentypen für Umsatzschätzungen.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013485"
---
# <a name="period-types"></a><span data-ttu-id="b85b0-103">Periodentypen</span><span class="sxs-lookup"><span data-stu-id="b85b0-103">Period types</span></span>

<span data-ttu-id="b85b0-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="b85b0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b85b0-105">Ein Periodentyp definiert, wie häufig die Einnahmen aus einem Projekt geschätzt werden.</span><span class="sxs-lookup"><span data-stu-id="b85b0-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="b85b0-106">Dieses Thema enthält Informationen zum Einrichten von Periodentypen für Umsatzschätzungen.</span><span class="sxs-lookup"><span data-stu-id="b85b0-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="b85b0-107">Erstellen und Arbeiten mit Periodentypen</span><span class="sxs-lookup"><span data-stu-id="b85b0-107">Create and work with period types</span></span>
<span data-ttu-id="b85b0-108">Führen Sie die folgenden Schritte aus, um Periodentypen zu erstellen und damit zu arbeiten:</span><span class="sxs-lookup"><span data-stu-id="b85b0-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="b85b0-109">Gehen Sie in der Dynamics 365 Finance-Umgebung zu **Projektmanagement und Buchhaltung** > **Einrichten** > **Schätzungen** > **Periodentypen**.</span><span class="sxs-lookup"><span data-stu-id="b85b0-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="b85b0-110">Wählen Sie **Neu** aus, um einen neuen Periodentyp zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b85b0-110">Select **New** to create new period type.</span></span> <span data-ttu-id="b85b0-111">Geben Sie einen Namen und eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="b85b0-111">Enter a name and description.</span></span>
3. <span data-ttu-id="b85b0-112">Wählen Sie einen Wert im **Häufigkeit** aus:</span><span class="sxs-lookup"><span data-stu-id="b85b0-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="b85b0-113">Wenn Sie **Woche**, **Zweiwöchentlich**, **Halbmonatlich**, **Monat**, **Tag**, **Quartal** oder **Jahr** auswählen, wird der Kalender verwendet, um die Perioden zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b85b0-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="b85b0-114">Wenn Sie **Hauptbuchzeitraum** auswählen, werden Sachkontoperioden aus der Hauptbuchkonfiguration zum Generieren von Perioden verwendet.</span><span class="sxs-lookup"><span data-stu-id="b85b0-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="b85b0-115">Wenn Sie **Unbegrenzt** auswählen, können Sie benutzerdefinierte Zeiträume angeben.</span><span class="sxs-lookup"><span data-stu-id="b85b0-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="b85b0-116">Wählen Sie den Periodentyp-Datensatz aus und dann **Perioden generieren**, um Perioden für den Periodentyp zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b85b0-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="b85b0-117">Basierend auf der von Ihnen ausgewählten Periodenhäufigkeit haben Sie möglicherweise die Möglichkeit, ein Startdatum oder die Anzahl der zu generierenden Perioden anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b85b0-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="b85b0-118">Wählen Sie **Perioden** aus, um generierte Perioden zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b85b0-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]