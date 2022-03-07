---
title: Neuerungen im März 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der März 2021-Veröffentlichung von Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen verfügbar sind.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b11a57ae152be154fd6a7d330c8520f3b295ce3ef5cc7051ac9b343e3bcdbe12
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006335"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuerungen im März 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:

- Project Operations in Dataverse, Umgebungsversion 4.8.0.91 
- Projektmanagement und Buchhaltung in Dynamics 365 Finance, Umgebungsversion 10.0.16 

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse


| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| Preise und Abrechnung | 2133873 | Das Problem bei der Anzeige des Währungssymbols für **Verkaufspreis pro Einheit** im Raster **Kostenschätzungen** wurde behoben. |
| Preise und Abrechnung | 2174616 | Erhält ein Angebot den Zuschlag, wird auf die benutzerdefinierte Preisliste des Vertrags in den Detaisl der Vertragszeilen verwiesen, die aus dem Angebot übernommen werden. |
| Verkaufschancenmanagement | 2167475 | Fester Steuerbetrag in der Korrekturrechnung, aus dem ein nicht abgerechneter tatsächlicher Eintrag hervorgegangen ist. |
| Verkaufschancenmanagement | 2176285 | Der Steuerbetrag darf nicht aus den Details des Kaufvertrags/der Angebotszeile in die Details des Kostenvertrags/der Angebotszeile übernommen werden. |
| Verkaufschancenmanagement | 2188079 | Für Verträge, die nicht arbeitsbezogen sind, darf keine geteilte Abrechnungsregel erstellt werden. |
| Planung und Nachverfolgung | 2125274 | **Zuordnung für Duales Schreiben**-Attribut für **Zuordnen des Projektstartdatums** von **msdyn\_taskearlieststart** auf **msdyn\_actualstart** aktualisiert. |
| Planung und Nachverfolgung | 2138853 | Die Projektkopierfunktion wurde aktualisiert, um sicherzustellen, dass Kostenschätzungspositionen, die auf Aufgaben verweisen, in das Zielprojekt übernommen werden. |
| Planung und Nachverfolgung | 2154306 | Probleme beim Löschen von Kostenschätzungen in Project Operations für ressourcenbasierte Szenarien wurden behoben. |
| Planung und Nachverfolgung | 2173259 | Die Projektkopierfunktion wurde aktualisiert, um sicherzustellen, dass in bestimmten Szenarien nicht die Fehlermeldung **PSP wird kopiert** erscheint. |
| Zeit und Ausgaben | 2148910 | Anzeigeproblem der Seite **Eintrag bearbeiten** im Raster **Zeiteintrag** wurde behoben. |
| Zeit und Ausgaben | 2159798 | Engere Steuerung, um sicherzustellen, dass genehmigte Ausgabeneinträge nicht bearbeitet werden können. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmanagement und -buchhaltung in Dynamics 365 Finance

Weitere Informationen siehe [Neuigkeiten für Januar 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Aktualisierungen der Vorschriften

Informationen zu behördlichen Aktualisierungen für Finance and Operations-Apps, siehe [Aktualisierungen der Vorschriften](/dynamics365/finance/localizations/regulatory-updates). Eine weitere Möglichkeit, Informationen zu behördlichen Aktualisierungen zu erhalten, besteht darin, sich bei LCS anzumelden und die geplanten behördlichen Aktualisierungen mithilfe des Problemsuchwerkzeugs anzuzeigen. Mit der Problemsuche können Sie nach Land, Art der Funktion und Version suchen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]