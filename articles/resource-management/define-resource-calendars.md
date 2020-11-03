---
title: Ressourcenkalender definieren
description: Dieses Thema enthält Informationen zum Definieren der Arbeitsstundenkalender für Ressourcen in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076372"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="fda76-103">Ressourcenkalender definieren</span><span class="sxs-lookup"><span data-stu-id="fda76-103">Define resource calendars</span></span>

<span data-ttu-id="fda76-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="fda76-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fda76-105">Jede buchbare Ressource, die an einem Projekt arbeitet, muss über einen Arbeitszeitkalender verfügen, um ihre Verfügbarkeit zu definieren.</span><span class="sxs-lookup"><span data-stu-id="fda76-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="fda76-106">Die Arbeitszeiten für eine Ressource können auf zwei Arten definiert werden:</span><span class="sxs-lookup"><span data-stu-id="fda76-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="fda76-107">Definieren individueller Kalenderregeln für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="fda76-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="fda76-108">Anwenden einer vorhandene Kalendervorlage für die Ressource</span><span class="sxs-lookup"><span data-stu-id="fda76-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="fda76-109">Definieren der Arbeitsstunden einer Ressource</span><span class="sxs-lookup"><span data-stu-id="fda76-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="fda76-110">Wählen Sie im **Ressourcen** -Menü **Ressourcen** aus.</span><span class="sxs-lookup"><span data-stu-id="fda76-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="fda76-111">Wählen Sie in der Rasteransicht die entsprechende **Buchbare Ressource** aus.</span><span class="sxs-lookup"><span data-stu-id="fda76-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="fda76-112">Wählen Sie auf der **Ressourcendetails** -Seite die **Arbeitszeit** -Registerkarte aus. Standardmäßig werden im buchbaren Ressourcenkalender die Arbeitszeiten der Standardarbeitsstundenvorlage verwendet, die für die Organisation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="fda76-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="fda76-113">Um die Arbeitszeiten zu aktualisieren, klicken Sie mit der rechten Maustaste auf das Startdatum der vorgeschlagenen zu definierenden Kalenderregel.</span><span class="sxs-lookup"><span data-stu-id="fda76-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="fda76-114">Verwenden Sie das Kalenderregelmenü, um eine Kalenderregel für einen bestimmten Tag, den Rest der Serie oder den gesamten Kalender zu definieren.</span><span class="sxs-lookup"><span data-stu-id="fda76-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="fda76-115">Nachdem die Option ausgewählt wurde, können Sie Folgendes definieren:</span><span class="sxs-lookup"><span data-stu-id="fda76-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="fda76-116">Den Wochentag, an dem die Arbeitszeit gilt.</span><span class="sxs-lookup"><span data-stu-id="fda76-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="fda76-117">Die Arbeitszeiten innerhalb jeden Tages.</span><span class="sxs-lookup"><span data-stu-id="fda76-117">The working times within each day.</span></span>
    - <span data-ttu-id="fda76-118">Die Zeitzone für die Kalenderregel.</span><span class="sxs-lookup"><span data-stu-id="fda76-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="fda76-119">Falls zutreffend, kann für die Regel auch eine arbeitsfreie Zeit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fda76-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="fda76-120">Anwenden einer Kalendervorlagen auf eine Ressource</span><span class="sxs-lookup"><span data-stu-id="fda76-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="fda76-121">Wählen Sie im **Ressourcen** -Menü **Ressourcen** aus.</span><span class="sxs-lookup"><span data-stu-id="fda76-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="fda76-122">Wählen Sie in der Rasteransicht bis zu 25 **Buchbare Ressourcen** zum Aktualisieren aus.</span><span class="sxs-lookup"><span data-stu-id="fda76-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="fda76-123">Wählen Sie **Kalender einstellen** aus. Ein Dialogfeld zeigt einer Liste der verfügbaren Arbeitsstundenvorlagen an.</span><span class="sxs-lookup"><span data-stu-id="fda76-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="fda76-124">Wählen Sie die zu verwendende Vorlage aus und wählen Sie dann **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="fda76-124">Select the template you want to use, and then select **Apply**.</span></span>
