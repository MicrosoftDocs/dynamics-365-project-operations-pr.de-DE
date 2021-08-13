---
title: Neuigkeiten für Februar 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version von Project Operations vom Februar 2021 für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen verfügbar sind.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 41d7d7133652069ca3899db7f12e67e9ba531bcd3e36d67c3686a6b637b077d3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986805"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten für Februar 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:

- Project Operations für Dataverse Umgebung 4.7.0.95
- Projektmanagement und Buchhaltung in Dynamics 365 Finance, Umgebungsversion 10.0.16 

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

Weitere Informationen zum Projektmanagement und zur Buchhaltung finden Sie unter Dynamics 365 Finance [Was ist neu Januar 2021 – Project Operations für Ressourcen/nicht vorrätige Szenarien](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Aktualisierungen der Vorschriften

Informationen zu behördlichen Aktualisierungen für Finance and Operations-Apps, siehe [Aktualisierungen der Vorschriften](/dynamics365/finance/localizations/regulatory-updates). Eine weitere Möglichkeit, Informationen zu behördlichen Aktualisierungen zu erhalten, besteht darin, sich bei Lifecycle Services (LCS) anzumelden und die geplanten behördlichen Aktualisierungen mithilfe des Problemsuchwerkzeugs anzuzeigen. Mit der Problemsuche können Sie nach Land, Art der Funktion und Version suchen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]