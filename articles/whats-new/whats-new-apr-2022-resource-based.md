---
title: Neuigkeiten April 2022 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieser Artikel enthält Informationen zu den Qualitätsupdates, die in der Version vom April 2022 von Microsoft Dynamics 365 Project Operations für ressourcenbasierte/nicht vorratsbasierte Szenarien zur Verfügung stehen.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ea1c96d64309990962f431b1c72ae47bf445bfa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912377"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten April 2022 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Version 4.41.0.45
- Projektmanagement und -buchhaltung in einer Dynamics 365 Finance-Umgebungsversion 10.0.26

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

Beschaffungskategorien können in Projektbestellungen und ausstehenden Kreditorenrechnungen verwendet werden. Weitere Informationenen finden Sie unter [Beschaffungskategorien mit Projektbestellungen und ausstehenden Kreditorenrechnungen verwenden](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Die folgende Tabelle zeigt die Zuordnungen für duales Schreiben, die in der Version vom März 2022 von Project Operations geändert oder hinzugefügt wurden.

| Entitätszuordnung | Aktualisierte Version | Anmerkungen |
| -------------- | ------------------- | ------------|
| Project Operations-Integrationsprojektanbieter-Rechnungszeilenexportentität msdyn\_projectvendorinvoicelines | 1.0.0.4 | Diese Zuordnung unterstützt die Verwendung von Beschaffungskategorien mit Bestellungen und ausstehenden Kreditorenrechnungen. |

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Einige Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Sie können die aktive Version der Zuordnung in der Spalte **Version** auf der Seite **Dual-Write** anzeigen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine vorkonfigurierte Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen im Abschnitt [Problem mit fehlenden Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) des Handbuchs zur Fehlerbehebung für duales Schreiben.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| ------------ | ---------------- | -------------- |
| Zeit und Ausgaben | 2573900 | Die **Moderne Genehmigung**-Funktion muss standardmäßig aktiviert sein. |
| Preise und Abrechnung | 2603313 | Es wurde ein doppelter Datensatzfehler behoben, der verhinderte, dass Angebots- und Vertragspositionen mit einem Produkt hinzugefügt wurden. |
| Bereitstellung und Konfiguration | 2611368 | Kunden müssen der Lösung mithilfe des modernen App-Designers bis zu fünf benutzerdefinierte Entitäten hinzufügen können. |
| Zeit und Ausgaben | 2628285 | Es wurde ein Problem behoben, das die Möglichkeit beeinträchtigte, während des Imports von Zeiteinträgen die richtige Ressourcenkategorie festzulegen. |
| Verkaufschancenmanagement| 2628815 | Aktualisieren Sie die Zeichenbeschränkung der Detailbeschreibung der Angebotszeile, sodass sie mit der Zeichenbeschränkung des Aufgabenbetreffs übereinstimmt, damit der Import für Aufgaben, deren Betreff länger als 100 Zeichen ist, erfolgreich ist. |
| Zeit und Ausgaben| 2629547 | Das **Eingereicht von**-Feld der Projektgenehmigungen muss auf den Benutzer verweisen, der den Datensatz eingereicht hat. |
| Zeit und Ausgaben| 2629865 | Das **Kategorie kopieren**-Feld für Aufgaben, wenn Projekte kopiert werden. |
| Zeit und Ausgaben| 2636463 | Die Filter für Genehmigungen in modernen Genehmigungsformularen wurden korrigiert. |
| Projektplanung und -nachverfolgung | 2648300 | Es wurde ein Problem behoben, das verhindert, dass der Projektbesitzer geändert wird. |
| Preise und Abrechnung | 2563000 | Erfassungspositionen für einen nicht fakturierten Verkauf, bei denen die Währung von der Vertragswährung abweicht, dürfen nicht zulässig sein. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmanagement und -buchhaltung in Dynamics 365 Finance

Melden Sie sich bei Microsoft Dynamics Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) an.
