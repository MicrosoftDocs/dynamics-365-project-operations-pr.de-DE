---
title: Project Service Automation konfigurieren
description: Schritte zum Konfigurieren von Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
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
ms.openlocfilehash: fd02611b5b3133e097b2818a725b6c5d667e5ac0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076633"
---
# <a name="configure-project-service"></a><span data-ttu-id="90416-103">Project Service konfigurieren</span><span class="sxs-lookup"><span data-stu-id="90416-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="90416-104">Bevor Sie die [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-Automatisierungsfunktionen in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] verwenden können, um Ihre Konten, Projekte und Ressourcen zu verwalten, müssen Sie einige Konfigurationsschritte abschließen, um sicherzustellen, dass die [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] -Lösung dem Bedarf Ihrer Organisation entspricht.</span><span class="sxs-lookup"><span data-stu-id="90416-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="90416-105">Hier die Schritte im Einzelnen:</span><span class="sxs-lookup"><span data-stu-id="90416-105">These steps include:</span></span>  
  
-   <span data-ttu-id="90416-106">[Einrichten von Zeiteinheiten](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="90416-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="90416-107">Konfigurieren Sie die Zeiteinheiten im Produktkatalog, den Sie als Basis für die Terminplanung und das Berechnen Ihrer Projekte benutzen.</span><span class="sxs-lookup"><span data-stu-id="90416-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="90416-108">[Währungen und Wechselkurse einrichten](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="90416-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="90416-109">Richten Sie die Währungen ein, die Sie für Ihre Projekte verwenden wollen.</span><span class="sxs-lookup"><span data-stu-id="90416-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="90416-110">[Organisationseinheiten erstellen](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="90416-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="90416-111">Richten Sie die Gruppen ein, die Ihr Unternehmen nutzt, um die Geschäftstätigkeiten aufzugliedern, ob nun nach Standort, Unternehmensfunktion oder andere logische Aufteilung.</span><span class="sxs-lookup"><span data-stu-id="90416-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="90416-112">[Rechnungshäufigkeiten einrichten](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="90416-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="90416-113">Richten Sie Zeiträume ein, die Sie für das Berechnen Ihrer Kunden verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="90416-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="90416-114">[Transaktionskategorien konfigurieren](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="90416-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="90416-115">Richten Sie Transaktionskategorien ein, für die Ihre Berater ihre fakturierbaren und nicht fakturierbaren Ausgaben in Rechnung stellen können.</span><span class="sxs-lookup"><span data-stu-id="90416-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="90416-116">[Ausgabenkategorien konfigurieren](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="90416-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="90416-117">Richten Sie die Kategorien ein, für die Ihre Berater ihre fakturierbaren und nicht fakturierbaren Ausgaben in Rechnung stellen können.</span><span class="sxs-lookup"><span data-stu-id="90416-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="90416-118">[Erstellen der Produktkatalogartikel](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="90416-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="90416-119">Fügen Sie die Produkte, die Sie verkaufen, wie Software-Lizenzen, dem Produktkatalog hinzu.</span><span class="sxs-lookup"><span data-stu-id="90416-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="90416-120">[Erstellen einer Preisliste](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="90416-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="90416-121">Konfigurieren Sie verschiedene Preislisten, abhängig von, wie viel Sie Ihren Kunden für jede Rolle in Rechnung stellen wollen, die ihr Projekt erfordert.</span><span class="sxs-lookup"><span data-stu-id="90416-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="90416-122">[Ressourcen einrichten](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="90416-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="90416-123">Fügen Sie die Fähigkeiten, die Leistungsfähigkeiten, die Ressourcenrollen und andere Ressourceninformationen hinzu, die Sie für Ihre Projekte benötigen.</span><span class="sxs-lookup"><span data-stu-id="90416-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="90416-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90416-124">See Also</span></span>  
 <span data-ttu-id="90416-125">[Übersicht über Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="90416-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="90416-126">[Project Service Automation konfigurieren](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="90416-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="90416-127">[Konto-Manager Handbuch](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="90416-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="90416-128">[Handbuch des Projektmanagers](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="90416-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="90416-129">[Handbuch Resource Manager](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="90416-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="90416-130">Handbuch Zeit, Ausgaben und Zusammenarbeit</span><span class="sxs-lookup"><span data-stu-id="90416-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)