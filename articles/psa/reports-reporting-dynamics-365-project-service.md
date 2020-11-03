---
title: Homepage zur Berichterstellung
description: Dieses Thema enthält Informationen zur Berichterstellung in Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 30411818bdc1b370a71148cf79f743413167dab2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076751"
---
# <a name="reporting-home-page"></a><span data-ttu-id="6e818-103">Homepage zur Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="6e818-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6e818-104">Microsoft Dynamics 365 Project Service Automation ermöglicht projektbasierten Organisationen die effiziente Verwaltung ihrer Geschäftsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="6e818-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="6e818-105">Für jedes Projekt müssen Teammitglieder die Verkaufschance verwalten, die Arbeit veranschlagen und planen, die Projekte mit Ressource versehen, die Arbeit entsprechend dem Plan verwalten, die Arbeit in Rechnung stellen und dann die entsprechende Arbeit für den Abschluss des Projekts durchführen.</span><span class="sxs-lookup"><span data-stu-id="6e818-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="6e818-106">Die Möglichkeit der Berichterstellung zu Vorgängen ist zum Ermitteln der Integrität der Organisation und für das Ergreifen der erforderlichen korrektiven Maßnahmen unerlässlich.</span><span class="sxs-lookup"><span data-stu-id="6e818-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="6e818-107">PSA verwendet für die Berichterstellung die Methoden und Technologien von Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6e818-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="6e818-108">Weitere Informationen zu den Berichtsoptionen finden Sie unter [Schreibleitfaden für Bericht für Dynamics 365 Customer Engagement (on-premises), Versions 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="6e818-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="6e818-109">Berichts-Assistent</span><span class="sxs-lookup"><span data-stu-id="6e818-109">Report Wizard</span></span>

<span data-ttu-id="6e818-110">Mit dem Berichts-Assistenten können Nicht-Entwickler einfache Berichte erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e818-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="6e818-111">Da die App auf einer vorhandenen Plattform aufbaut, entspricht die Erfahrung derjenigen, die in [Erstellen oder Bearbeiten eines Berichts mit dem Berichts-Assistenten](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard) dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="6e818-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="6e818-112">Es werden jedoch die für Project Service Automation spezifischen Entitäten verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e818-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="6e818-113">Benutzerdefinierte SQL Server Reporting Services-Berichte</span><span class="sxs-lookup"><span data-stu-id="6e818-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="6e818-114">Falls Ihr Unternehmen einen bestimmten Bericht benötigt, der nicht mit dem Berichts-Assistenten erstellt werden kann, können Sie einen benutzerdefinierten Bericht erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e818-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="6e818-115">Hierfür muss Microsoft Visual Studio zusammen mit den entsprechenden Microsoft SQL Server Data Tools und Berichterstellungserweiterungen installiert sein.</span><span class="sxs-lookup"><span data-stu-id="6e818-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="6e818-116">Weitere Informationen zu Tools und Versionene finden Sie unter [Berichtverfassungsumgebung mit SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="6e818-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="6e818-117">Informationen zum erstellen eines benutzerdefinierten Berichts finden Sie unter [Erstellen eines neuen Berichts mithilfe von SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="6e818-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="6e818-118">Power BI Insights-Apps</span><span class="sxs-lookup"><span data-stu-id="6e818-118">Power BI insights apps</span></span>

<span data-ttu-id="6e818-119">In der Form von Insights-Apps bieten Ihnen Microsoft Power BI und Dynamics 365 eine leistungsstarke Möglichkeit, um mit Ihren Daten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6e818-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="6e818-120">Informationen zur Verfügbarkeit von Insights-Apps finden Sie auf der Seite [Power BI Insights-Apps](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="6e818-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="6e818-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6e818-121">Additional resources</span></span>
<span data-ttu-id="6e818-122">Weitere Informationen zur Berichterstellung in PSA finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="6e818-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="6e818-123">Arbeiten mit dem Project Service-Datenmodell</span><span class="sxs-lookup"><span data-stu-id="6e818-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="6e818-124">Dashboards</span><span class="sxs-lookup"><span data-stu-id="6e818-124">Dashboards</span></span>](reports-dashboards.md)

