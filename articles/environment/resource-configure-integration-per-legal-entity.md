---
title: Project Operations-Integration pro juristische Person konfigurieren
description: Dieses Thema enthält Informationen zum Einrichten einer Integration durch eine juristische Person in Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122882"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="4a8b8-103">Project Operations-Integration pro juristische Person konfigurieren</span><span class="sxs-lookup"><span data-stu-id="4a8b8-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="4a8b8-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="4a8b8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4a8b8-105">Dieses Thema führt Sie durch die Schritte, die zum Konfigurieren von Dynamics 365 Project Operations pro juristischer Person erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="4a8b8-106">Wichtige Funktionen in Dynamics 365 Finance aktivieren</span><span class="sxs-lookup"><span data-stu-id="4a8b8-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="4a8b8-107">Führen Sie die folgenden Schritte aus, um die erforderlichen Funktionen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="4a8b8-108">Navigieren Sie in Dynamics 365 Finance zum Arbeitsbereich **Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="4a8b8-109">Finden Sie in der **Funktionsliste** die folgenden Funktionen und aktivieren Sie diese:</span><span class="sxs-lookup"><span data-stu-id="4a8b8-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="4a8b8-110">**Mehrere Vertragszeilen für ein Projekt aktivieren**</span><span class="sxs-lookup"><span data-stu-id="4a8b8-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="4a8b8-111">**Project Operations in Dynamics 365 Customer Engagement** aktivieren</span><span class="sxs-lookup"><span data-stu-id="4a8b8-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="4a8b8-112">Wenn **Funktionsschlüssel** nicht aufgeführt ist, prüfen Sie, dass Ihre Finance-Version die Mindestanforderungen der Version erfüllt (Anwendungsversion 10.0.13 mit allen angewendeten Qualitätsupdates oder höher).</span><span class="sxs-lookup"><span data-stu-id="4a8b8-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="4a8b8-113">Wählen Sie **Auf Updates prüfen** aus, um die Funktionsliste zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="4a8b8-114">Das Project Operations-Bereitstellungsszenario für eine juristische Person definieren</span><span class="sxs-lookup"><span data-stu-id="4a8b8-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="4a8b8-115">Sie können Project Operations in Dynamics 365 Customer Engagement auf Ebene einer juristischen Person aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="4a8b8-116">Sie können eine juristische Person haben, die Project Operations in Dynamics 365 Customer Engagement für ressourcenbasierte/nicht ressourcenbasierte Szenarien verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="4a8b8-117">In derselben Umgebung können Sie eine andere juristische Person haben, die Project Operations für Lager-/Produktionsauftragsszenarien verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="4a8b8-118">Navigieren Sie in Dynamics 365 Finance zu **Projektmanagement und -buchhaltung** > **Einrichtung** > **Globale Projektmanagement und -Buchhaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="4a8b8-119">Wählen Sie in der Liste der verfügbaren juristischen Personen Entitäten aus, für die mehrere Vertragszeilen und Projektvorgänge in Dynamics 365 Customer Engagement-Funktionen aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="4a8b8-120">Wählen Sie juristische Personen, die Project Operations für Lager-/Fertigungsauftragsszenarien verwenden, weiterhin nicht aus.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="4a8b8-121">Eine juristische Person kann nur ausgewählt werden, wenn keine Projekte vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="4a8b8-122">Projektmanagement und -buchhaltungsparameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="4a8b8-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="4a8b8-123">Jede juristische Person, die Project Operations in Dynamics 365 Customer Engagement verwendet, benötigt eine Reihe von Standardparametern.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="4a8b8-124">Diese Parameter werden auf der Registerkarte **Project Operations** auf der Seite **Projektmanagement und -buchhaltungsparameter** konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="4a8b8-125">Die Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4a8b8-125">The parameters are:</span></span>

  - <span data-ttu-id="4a8b8-126">**Standards Fakturierungstyp**: Project Operations verwendet einen festen Satz von Standardeinstellungen für Fakturierungstypen, die den Zeileneigenschaften in Finance zugeordnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="4a8b8-127">Erstellen Sie für jeden Fakturierungstyp einen Datensatz: **Unbestimmt**, **Fakturierbar**, **Nicht fakturierbar**, **Kostenlos** und **Nicht verfügbar**.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="4a8b8-128">**Standardeinstellungen für Projektkategorien** : Wählen Sie die Standardprojektkategorien aus, die für jeden Transaktionstyp verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="4a8b8-129">Diese Standardeinstellungen werden in **Project Operations-Integrationsjournal** und in Vorkalkulationen, in denen keine Transaktionskategorie für die Istwerte des Projekts angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="4a8b8-130">**Prognosen**: Wählen Sie das Prognosemodell aus, das für Zeit- und Ausgabenvorkalkulationen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a8b8-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>
