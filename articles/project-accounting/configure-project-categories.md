---
title: Projektkategorien konfigurieren
description: Dieses Thema enthält Informationen zum Einrichten von Projektkategorien.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895965"
---
# <a name="configure-project-categories"></a><span data-ttu-id="cacf2-103">Projektkategorien konfigurieren</span><span class="sxs-lookup"><span data-stu-id="cacf2-103">Configure project categories</span></span>

<span data-ttu-id="cacf2-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="cacf2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cacf2-105">Project Operations bietet robuste Funktionen zum Kategorisieren von Einnahmen und Ausgaben für Projekte.</span><span class="sxs-lookup"><span data-stu-id="cacf2-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="cacf2-106">Kategorien bieten die Möglichkeit, über Projekttransaktionen zu berichten und diese zu analysieren und die Buchung in das Hauptbuch zu steuern.</span><span class="sxs-lookup"><span data-stu-id="cacf2-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="cacf2-107">Das folgende Diagramm zeigt die Korrelation zwischen Transaktionskategorien, gemeinsam genutzten Kategorien und Projektkategorien.</span><span class="sxs-lookup"><span data-stu-id="cacf2-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="cacf2-108">Transaktionskategorien sind die grundlegende Gruppierung für Projekttransaktionen.</span><span class="sxs-lookup"><span data-stu-id="cacf2-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="cacf2-109">Innerhalb dieser Gruppierung gibt es eine Reihe von gemeinsam genutzten Kategorien, die von Anwendungen und Modulen gemeinsam genutzt werden können.</span><span class="sxs-lookup"><span data-stu-id="cacf2-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="cacf2-110">Projektkategorien sind die detailliertesten Kategorien. So wird es noch spezifischer.</span><span class="sxs-lookup"><span data-stu-id="cacf2-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="cacf2-111">Projektkategorien sind spezifisch für juristische Personen, Module und Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="cacf2-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korrelation zwischen Transaktionskategorien, gemeinsam genutzten Kategorien und Projektkategorien](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="cacf2-113">Transaktionskategorien</span><span class="sxs-lookup"><span data-stu-id="cacf2-113">Transaction categories</span></span>

<span data-ttu-id="cacf2-114">Transaktionskategorien stellen die grundlegende Gruppierung für Projekttransaktionen dar und sind nicht unternehmens- oder transaktionsartspezifisch.</span><span class="sxs-lookup"><span data-stu-id="cacf2-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="cacf2-115">Beispielsweise verwendet Contoso Robotics die Kategorien Design, Travel, Installation und Service Transaction, um Projekttransaktionen zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="cacf2-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="cacf2-116">Transaktionskategorien werden im Project Operations-Modul definiert.</span><span class="sxs-lookup"><span data-stu-id="cacf2-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="cacf2-117">Wechseln Sie zu **Einstellungen** \> **Transaktionskategorien**, um das Formular zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cacf2-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="cacf2-118">Erstellen Sie eine neue Transaktionskategorie, indem Sie entweder **Neu** oder **Aus Excel importieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="cacf2-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="cacf2-119">Gemeinsame Kategorien</span><span class="sxs-lookup"><span data-stu-id="cacf2-119">Shared categories</span></span>

<span data-ttu-id="cacf2-120">Dynamics 365 verwendet das Konzept der gemeinsamen Kategorien, um Ausgaben in verschiedenen Anwendungen zu kategorisieren, z. B. Dynamics 365 Finance, Dynamics 365 Supply Chain und Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="cacf2-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="cacf2-121">Für jede erstellte Transaktionskategorie erstellt Project Operations automatisch vier verwandte gemeinsame Kategorien: Stunden, Kosten, Gebühren und Artikel.</span><span class="sxs-lookup"><span data-stu-id="cacf2-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="cacf2-122">Sie können die gemeinsamen Kategorien überprüfen und anpassen, indem Sie zu **Projektmanagement und Buchhaltung** \> **Einrichten** \> **Kategorien** \> **Gemeinsame Kategorien** wechseln.</span><span class="sxs-lookup"><span data-stu-id="cacf2-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="cacf2-123">Projektkategorien</span><span class="sxs-lookup"><span data-stu-id="cacf2-123">Project categories</span></span>

<span data-ttu-id="cacf2-124">Projektkategorien stellen die detaillierteste Ebene der Kategoriekonfiguration dar und müssen von einem Projektbuchhalter separat und für jedes Unternehmen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="cacf2-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="cacf2-125">Wechseln Sie zu **Projektmanagement und Buchhaltung** \> **Einrichtung** \> **Kategorien** \> **Projektkategorien**.</span><span class="sxs-lookup"><span data-stu-id="cacf2-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="cacf2-126">Wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="cacf2-126">Select **New**.</span></span>
3. <span data-ttu-id="cacf2-127">Wählen Sie die **Kategorie-ID** der gemeinsamen Kategorie aus, die Sie im vorherigen Abschnitt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="cacf2-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="cacf2-128">Mit Project Operations können nur die gemeinsame Kategorien verwendet werden, die Transaktionskategorien zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cacf2-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="cacf2-129">Wählen Sie eine Kategoriegruppe aus.</span><span class="sxs-lookup"><span data-stu-id="cacf2-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="cacf2-130">Kategoriegruppen</span><span class="sxs-lookup"><span data-stu-id="cacf2-130">Category groups</span></span>

<span data-ttu-id="cacf2-131">Kategoriegruppen werden verwendet, um Eigenschaften, hauptsächlich Buchungsprofile, zwischen verwandten Projektkategorien freizugeben.</span><span class="sxs-lookup"><span data-stu-id="cacf2-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="cacf2-132">Für jeden Transaktionstyp muss mindestens eine Kategoriegruppe vorhanden sein, und jeder Projektkategorie ist eine Gruppe zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cacf2-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="cacf2-133">Die Buchungsspezifikationen in Project Operations werden durch die Projektkosten- und Ertragsprofilregeln, Projektkategorien sowie Kategoriegruppen definiert.</span><span class="sxs-lookup"><span data-stu-id="cacf2-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="cacf2-134">Sie können Kategoriegruppen unter **Projektmanagement und Buchhaltung** \> **Einrichtung** \> **Kategorien** \> **Kategoriegruppen** einrichten.</span><span class="sxs-lookup"><span data-stu-id="cacf2-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
