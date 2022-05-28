---
title: Neuigkeiten für Februar 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version von Project Operations vom Februar 2021 für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen verfügbar sind.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cb6ab1337652d18a30fba56560ffe50f78dd4eb4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589011"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten für Februar 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:

- Project Operations für Dataverse Umgebung 4.7.0.95
- Projektmanagement und -buchhaltung in Dynamics 365 Finance-Umgebungsversion 10.0.16 

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| **Preise und Abrechnung** | 2053736 | Details zur Rechnungsposition können jetzt unter **Rechnung** > **Verwandte Informationen** abgerufen werden. |
| **Preise und Abrechnung** | 2122613 | Die Aktionen **Aktivieren** und **Deaktivieren** wurden aus den zugeordneten Entitäten **Preisliste** entfernt. |
| **Preise und Abrechnung** | 2128606 | Problem mit dem Plug-In **ullReferenceException** in dem **GetEstimatesForProject** behoben. |
| **Bereitstellung und Konfiguration** | 2139346 | Das Problem mit dem nicht verwalteten Import in der **Dynamics365ProjectOperationsDualWrite** Lösung wurde behoben. |
| **Bereitstellung und Konfiguration** | 2140569 | Die Projektlösung muss in den Dataverse Teams Umgebungen nicht installiert sein. |
| **Bereitstellung und Konfiguration** | 2086991 | Eingeschränkte Anpassung der Lokalisierung von Webressourcen. |
| **Verkaufschancenmanagement** | 2136794 | Zeigen Sie die richtige Fehlermeldung an, wenn der Prozess **Rechnung bestätigen** oder **Rechnung als bezahlt markieren** fehl schlägt. |
| **Verkaufschancenmanagement** | 2139330 | Durch Ändern des Projektmanagers für ein Projekt darf die besitzende Firma nicht auf den Standardwert zurückgesetzt werden. |
| **Verkaufschancenmanagement** | 2146376 | Der korrigierte Steuerbetrag in einem nicht steuerpflichtigen Ist wird aus der Rechnungsbestätigung erstellt. |
| **Projektplanung und -nachverfolgung** | 2099879 | Die Dataverse Umgebungsbereitstellung muss eine Standardtransaktionskategorie mit einer statischen ID erstellen und darf nicht zufällig eine pro Umgebung generieren. |
| **Projektplanung und -nachverfolgung** | 2128577 | Die Benutzerrechte von Project Service zum Aktualisieren der Transaktionskategorie für eine Ressourcenzuweisung wurden behoben. |
| **Projektplanung und -nachverfolgung** | 2164035 | Probleme mit der Funktion **Projekt kopieren** behoben. |
| **Zeiteintrag** | 2129161 | Es werden strengere Einschränkungen angewendet, um sicherzustellen, dass Benutzer einen eingereichten oder genehmigten Zeiteintrag nicht ändern und aktualisieren können. |
| **Zeiteintrag** | 2103572 | Die Zeitgenehmigung für Zeiteinträge außerhalb des Projekts darf nicht nach einer Projektgenehmigungsrolle suchen. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmanagement und -buchhaltung in Dynamics 365 Finance 

Weitere Informationen zu Projektmanagement und -buchhaltung in Dynamics 365 Finance finden Sie unter [Was ist neu im Januar 2021 – Project Operations für ressourcen-/nicht lagerbasierte Szenarien](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Aktualisierungen der Vorschriften

Informationen zu regulatorischen Aktualisierungen für Finanz- und Betriebs-Apps finden Sie unter [Regulatorische Aktualisierungen](/dynamics365/finance/localizations/regulatory-updates). Eine weitere Möglichkeit, Informationen zu behördlichen Aktualisierungen zu erhalten, besteht darin, sich bei Lifecycle Services (LCS) anzumelden und die geplanten behördlichen Aktualisierungen mithilfe des Problemsuchwerkzeugs anzuzeigen. Mit der Problemsuche können Sie nach Land, Art der Funktion und Version suchen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]