---
title: Homepage für die Berichterstellung
description: Dieser Artikel enthält Informationen über die Berichterstattung in Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
- intro-internal
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
ms.reviewer: johnmichalak
ms.openlocfilehash: cf55495cc435d929bd305c9fea270aeb2d62a3da
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921669"
---
# <a name="reporting-home-page"></a>Homepage für die Berichterstellung

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 Project Service Automation ermöglicht projektbasierten Organisationen die effiziente Verwaltung ihrer Geschäftsvorgänge. Für jedes Projekt müssen Teammitglieder die Verkaufschance verwalten, die Arbeit veranschlagen und planen, die Projekte mit Ressource versehen, die Arbeit entsprechend dem Plan verwalten, die Arbeit in Rechnung stellen und dann die entsprechende Arbeit für den Abschluss des Projekts durchführen. Die Möglichkeit der Berichterstellung zu Vorgängen ist zum Ermitteln der Integrität der Organisation und für das Ergreifen der erforderlichen korrektiven Maßnahmen unerlässlich. PSA verwendet für die Berichterstellung die Methoden und Technologien von Microsoft Dynamics 365. Weitere Informationen zu den Berichtsoptionen finden Sie unter [Schreibleitfaden für Bericht für Dynamics 365 Customer Engagement (on-premises), Versions 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).

## <a name="report-wizard"></a>Berichts-Assistent

Mit dem Berichts-Assistenten können Nicht-Entwickler einfache Berichte erstellen. Da die App auf einer vorhandenen Plattform aufbaut, entspricht die Erfahrung derjenigen, die in [Erstellen oder Bearbeiten eines Berichts mit dem Berichts-Assistenten](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard) dokumentiert ist. Es werden jedoch die für Project Service Automation spezifischen Entitäten verwendet.

## <a name="custom-sql-server-reporting-services-reports"></a>Benutzerdefinierte SQL Server Reporting Services-Berichte

Falls Ihr Unternehmen einen bestimmten Bericht benötigt, der nicht mit dem Berichts-Assistenten erstellt werden kann, können Sie einen benutzerdefinierten Bericht erstellen. Hierfür muss Microsoft Visual Studio zusammen mit den entsprechenden Microsoft SQL Server Data Tools und Berichterstellungserweiterungen installiert sein. Weitere Informationen zu Tools und Versionene finden Sie unter [Berichtverfassungsumgebung mit SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools). Informationen zum erstellen eines benutzerdefinierten Berichts finden Sie unter [Erstellen eines neuen Berichts mithilfe von SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).

## <a name="power-bi-insights-apps"></a>Power BI Insights-Apps

Microsoft Power BI und Dynamics 365 bieten Ihnen in Form von Insights-Apps eine leistungsstarke Möglichkeit, um mit Ihren Daten zu arbeiten. Informationen zur Verfügbarkeit von Insights-Apps finden Sie auf der Seite [Power BI Insights-Apps](https://powerbi.microsoft.com/power-bi-insights-apps/).


## <a name="additional-resources"></a>Zusätzliche Ressourcen
Weitere Informationen über die Berichterstattung in PSA finden Sie in den folgenden Artikeln:

- [Arbeiten mit dem Project Service-Datenmodell](reports-working-project-service-data-model.md)
- [Dashboards](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
