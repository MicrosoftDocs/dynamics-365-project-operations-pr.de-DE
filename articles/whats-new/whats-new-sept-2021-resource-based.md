---
title: Neuigkeiten September 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version vom September 2021 der Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 06f23630ef0205394f376e5bb93a29ae8a9eab15
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582893"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten September 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

*Gilt für: Project Operations für ressourcen-/nicht vorratsbasierte Szenarien*

Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:

   - Project Operations in der Microsoft Dataverse-Umgebung Version 4.14.0.99.
   - Projektmanagement und -buchhaltung in Dynamics 365 Finance-Umgebungsversion 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Es gibt keine Updates für Project Operations Dual-Write Zuordnungen in dieser Version. Eine aktuelle Liste und Versionen von Project Operations dual-write Zuordnungen finden Sie unter [Versionen von Project Operations dual-write Zuordnungen](../environment/resource-dual-write-maps.md).

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Bestimmte Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Die aktive Version der Zuordnung können Sie auf der Seite **Dual-write** in der Spalte **Version** sehen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine sofort einsatzbereite Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen im Abschnitt [Problem mit fehlenden Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) des Handbuchs zur Fehlerbehebung für duales Schreiben.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| Zeit und Ausgaben | 1811407 | Der Projektgenehmiger-Sicherheitsrolle für die Genehmigung von Ausgabeneinträgen wurde angepasst. |
| Zeit und Ausgaben | 1811438 | Der Projektgenehmiger-Sicherheitsrolle für die Genehmigungsstornierung von Zeiteinträgen wurde angepasst. |
| Zeit und Ausgaben | 2370126 | Aktualisierte Symbole für **Projektaufgabe** und **Rolle** in der Entität **Zeiteingabe**. |
| Zeit und Ausgaben | 2379879 | Korrigierte Funktion **Woche kopieren** in der Zeiteingabe bei Verwendung von Dynamics 365 für Telefon. |
| Preise und Abrechnung | 2371906 | Der Gesamtbetrag der Proforma-Rechnung darf in Project Operations für ressourcenbasierte Bereitstellungen nicht angepasst werden. |
| Preise und Abrechnung | 2385802 | Der Fehler, der bei negativen Ist-Stunden auftritt, wenn Projektsummen aktualisiert werden, wurde behoben. |
| Preise und Abrechnung | 2389675 | Verbessertes Verhalten bei der Bestätigung von Proforma-Rechnungen. Die Entität für lang laufende Jobs muss die Aktivität berücksichtigen, die zum Schreiben von Bestätigungsergebnissen für die Buchhaltung erforderlich ist. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmanagement und -buchhaltung in Dynamics 365 Finance

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Reisen und Spesen | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Die Beträge für Kreditoren- und Mehrwertsteuertransaktionen, die aus einer Ausgabe gebucht werden, die aus einer Kreditkartentransaktion erstellt wurde, sind falsch. |
| Reisen und Spesen | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Beim Generieren des Zahlungsjournals werden die falschen Abrechnungszeilen erstellt. |
| Reisen und Spesen | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Die Beträge für Mehrwertsteuertransaktionen, die aus einer Ausgabe gebucht werden, die aus einer Kreditkartentransaktion erstellt wurde, sind falsch. |
| Reisen und Spesen | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Das Löschen einer Ausgabenzeile kann lange dauern. |
| Projektbuchhaltung | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Nachdem Sie KB 4619395 angewendet haben, wird das Ändern der Zahlenfolge in **Kontinuierlich** nicht unterstützt und wenn Sie einen Kostenvoranschlag veröffentlichen, tritt der folgende Fehler auf: „Das System unterstützt die Einrichtung 'kontinuierlich' des Nummernkreises Proj_X nicht.“ |
| Projektbuchhaltung | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Das Buchen einer Kreditorenrechnung schlägt möglicherweise mit der folgenden Fehlermeldung fehl: „Die Buchungen auf dem Beleg sind am 17.05.2021 nicht ausgeglichen. (Abrechnungswährung: 0,00 – Berichtswährung: 0,01).“ |
