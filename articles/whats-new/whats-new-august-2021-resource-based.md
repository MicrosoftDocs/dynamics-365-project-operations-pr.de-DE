---
title: Was ist neu August 2021 - Project Operations für ressourcenbasierte/nicht vorrätige Szenarien
description: Dieses Thema enthält Informationen zu den Qualitätsaktualisierungen, die in der Version August 2021 von Project Operations für ressourcen-/nicht vorratsbasierte Szenarien verfügbar sind.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cd5a7e74fc90c6138cd672ff6109b59a8d2ae916
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323460"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Was ist neu August 2021 - Project Operations für ressourcenbasierte/nicht vorrätige Szenarien

*Gilt für: Project Operations für ressourcen-/nicht vorratsbasierte Szenarien*

Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:

   - Project Operations in der Microsoft Dataverse-Umgebung Version 4.13.0.152.
   - Projektmanagement und -buchhaltung in der Dynamics 365 Finance-Umgebung Version 10.0.20.

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

Die folgenden Funktionen sind in dieser Version enthalten:

- **Zulassungssätze**: Genehmigungssets gruppieren Genehmigungsanfragen für Zeit, Ausgaben oder Materialverbrauch in kleinere Vorgangsteilmengen. Diese Gruppierung ermöglicht die Bearbeitung von Genehmigungen nach Projekt in einer bestimmten Reihenfolge und ermöglicht Wiederholungsversuche und Sequenzierung. Das Gruppieren der Anfragen verbessert die Zuverlässigkeit und Nachvollziehbarkeit der Genehmigungsverarbeitung bei großen Genehmigungsmengen. Weitere Informationen finden Sie unter [Genehmigungssätze](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Es gibt keine Updates für Project Operations Dual-Write Zuordnungen in dieser Version. 

Eine aktuelle Liste und Versionen von Project Operations dual-write Zuordnungen finden Sie unter [Versionen von Project Operations dual-write Zuordnungen](../environment/resource-dual-write-maps.md).

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Bestimmte Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Die aktive Version der Zuordnung können Sie auf der Seite **Dual-write** in der Spalte **Version** sehen. Aktivieren Sie eine neue Version der Zuordnung, indem Sie **Kartenversionen zuordnen** wählen, die neueste Version auswählen und dann die ausgewählte Version speichern. Wenn Sie eine sofort einsatzbereite Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn ein Problem beim Starten der Zuordnung auftritt, befolgen Sie die Anweisungen im Abschnitt [Fehlende Tabellenspalten bei Zuordnungen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) in der Anleitung zur Fehlerbehebung für Dual-Write.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| Preise und Abrechnung | 2295625 | Der Meilensteinname muss aus dem Rechnungsplan in das Rechnungspostendetail kopiert werden. |
| Preise und Abrechnung | 2316323 | Der Rabatt sollte auf einer Proforma-Rechnung in Project Operations für ressourcenbasierte Szenarien nicht bearbeitet werden können. |
| Verkaufschancenmanagement | 2338619 | Die Geschäftsregeln **Verkaufschance** und **Angebot** dürfen nur auf Seiten aufgerufen werden. |
| Ressourcenverwaltung | 2316523 | Das Verwenden von **Anfrage senden** aus einer Ressourcenanforderung, der eine Rolle zugeordnet ist, sollte keinen Fehler anzeigen. |
| Ressourcenverwaltung | 2326885 | Beim Erstellen einer Ressourcenanforderung mittels eines Projekts sollte kein Fehler angezeigt werden. |
| Zeit und Ausgaben | 2335584 | Veraltete Aufgabenflüsse in der Zeiterfassung. |
| Zeit und Ausgaben | 2336884 | Die Zeiteingabeschaltfläche **Woche kopieren** muss für mehr als nur für den aktuellen Benutzer funktionieren. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmanagement und -buchhaltung in Dynamics 365 Finance

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Reisen und Spesen | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Falsche Kreditorentransaktions- und Mehrwertsteuertransaktionsbeträge werden gebucht, wenn eine Ausgabe aus einer Kreditkartentransaktion erstellt wird. |
| Reisen und Spesen | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Die falsche Abrechnung sind Zeilen, die beim Generieren des Zahlungsjournals erstellt werden. |
| Reisen und Spesen | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Falsche Mehrwertsteuertransaktionsbeträge werden gebucht, wenn eine Ausgabe aus einer Kreditkartentransaktion erstellt wird. |
| Reisen und Spesen | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Das Löschen einer Ausgabenzeile kann lange dauern. |
| Projektbuchhaltung | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Das System unterstützt die Einrichtung der fortlaufenden Nummernreihenfolge nicht, wenn Sie nach der Anwendung von KB 4619395 einen Kostenvoranschlag buchen. |
| Projektbuchhaltung | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Die Buchung der Kreditorenrechnung schlägt möglicherweise mit folgender Fehlermeldung fehl: „Die Buchungen auf dem Beleg sind am 17.05.2021 nicht ausgeglichen. (Abrechnungswährung: 0,00 – Berichtswährung: 0,01)“ |
