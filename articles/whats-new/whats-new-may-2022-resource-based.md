---
title: Neuigkeiten Mai 2022 – Project Operations für Ressourcen basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieser Artikel enthält Informationen über die Qualitätsupdates, die in der Version von Microsoft Dynamics 365 Project Operations vom Mai 2022 für Szenarien mit und ohne Ressourcenvorrat verfügbar sind.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921393"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten Mai 2022 – Project Operations für Ressourcen basierend auf vorrätigen/nicht-vorrätigen Ressourcen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Version 4.42.0.70
- Projektmanagement und -buchhaltung in einer Dynamics 365 Finance-Umgebungsversion 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Es gibt keine Updates für Project Operations Dual-Write Zuordnungen in dieser Version. Eine aktuelle Liste und Versionen von Project Operations dual-write Zuordnungen finden Sie unter [Versionen von Project Operations dual-write Zuordnungen](../environment/resource-dual-write-maps.md).

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Einige Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Sie können die aktive Version der Zuordnung in der Spalte **Version** auf der Seite **Dual-Write** anzeigen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine vorkonfigurierte Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen im Abschnitt [Problem mit fehlenden Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) des Handbuchs zur Fehlerbehebung für duales Schreiben.

## <a name="quality-updates"></a>Qualitätsupdates
### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Ressourcenverwaltung | 2634019 | Verbesserte Fehlermeldungen für Geschäftsvalidierungen beim Hinzufügen generischer Teammitglieder als Ressourcen. |
| Projektplanung und -nachverfolgung | 2648515 | Eingeschränkte Updates von **ownerid**, **Zustand** und **Status** in Planungsentitäten. |
| Preise und Abrechnung | 2653167 | Das Dezimaltrennzeichen für das **Schätzungen**-Raster muss den Formateinstellungen in **Persönliche Optionen** folgen. |
| Preise und Abrechnung| 2662251 | Werte in den Feldern **Korrigierte Einheit** und **Einheitsgruppe** nehmen beim Erstellen von Datensätzen in Materialvoranschlägen den Standardwert an. |
| Preise und Abrechnung| 2571408 | Nicht fakturierte Verkaufs-Ist-Werte werden beim Erstellen eines Rechnungsentwurfs mit einer Proforma-Rechnungs-ID gestempelt. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmanagement und -buchhaltung in Dynamics 365 Finance

Melden Sie sich bei Microsoft Dynamics Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) an.
