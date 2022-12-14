---
title: Neuigkeiten Oktober 2022 – Project Operations lite-Bereitstellung
description: Dieser Artikel enthält Informationen über die Qualitätsupdates, die in der Lite-Bereitstellung von Microsoft Dynamics 365 Project Operations im Oktober 2022 zur Verfügung stehen.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806613"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Neuigkeiten Oktober 2022 – Project Operations lite-Bereitstellung

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Version 4.57.0.176

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

| Funktionsbereich | Funktionsname | Weitere Informationen |
| --- | --- | --- |
| Projektplanung und -nachverfolgung | **Project Operations externe Planung**<br>Mit der externen Zeitplanung können Kunden Entitäten, die sich auf Projektstrukturpläne (WBS) beziehen, durch die Verwendung der nativen Dataverse APIs nativ erstellen, aktualisieren und löschen, jedoch ohne die aktuellen Einschränkungen, die von Microsoft Project for the Web erzwungen werden. | [Externe Zeitplanung](/dynamics365/project-operations/project-management/external-scheduling) |
| Bereitstellung und Konfiguration | <p>**Erlauben Sie Kunden, den Bereitstellungstyp auszuwählen**<br>Produktgesteuerte Updates (PDUs) von Project Operations werden verwendet, um die Dual-Write-Lösung von Project Operations automatisch zu installieren, wenn Dual-Write-Kern- und -Orchestrierungslösungen in der Umgebung installiert sind.</p><p>Diese Funktion führt einen neuen **Lösungs-Upgrade-Verhalten** Parameter in den Projektparametern ein. Wenn dieser Parameter auf **Nur Lite** eingestellt ist, werden PUDs nicht mehr verwendet, um die Dual-Write-Lösung von Project Operations automatisch zu installieren, selbst wenn Dual-Write-Kern- und -Orchestrierungslösungen in der Umgebung installiert sind. Dieses Verhalten kommt Kunden zugute, die Dual-Write-Lösungen verwenden möchten, um Verkaufsaufträge in Finanz- und Betriebs-Apps zu integrieren, Project Operations jedoch in einem Lite-Modus verwenden möchten (d. h. ohne Integration in Finanz- und Betriebs-Apps).</p> | |

## <a name="quality-updates"></a>Qualitätsupdates

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Preise und Abrechnung | 2316317 | Das System ermöglicht die Erstellung von Rechnungen ohne fakturierbare Transaktionen. |
| Preise und Abrechnung | 2737300 | Überprüfen Sie die Verfügbarkeit des Kundenfelds, bevor auf das Formular zugegriffen wird. |
| Preise und Abrechnung | 2744948 | Fügen Sie eine Nullprüfung für die Abrechnungsmethode hinzu. |
| Preise und Abrechnung | 2763515 | Null-Referenz-Fehlerbehandlung, wenn der Kaufvertrag der Rechnung fehlt. |
| Preise und Abrechnung | 2844301 | Die Batch-Rechnungserstellung schlägt aufgrund eines Fehlers fehl. |
| Preise und Abrechnung | 2845869 | Falsche Speicherung des Organisationsdienstes. |
| Preise und Abrechnung | 2853729 | Rollen- und Preisdetails werden aktualisiert, wenn der Abrechnungstyp geändert wird. |
| Preise und Abrechnung | 2940350 | Bei der Bepreisung von Istwerten sollten nur aktive Preislisten automatisch eingetragen werden. |
| Bereitstellung und Konfiguration | 3001206 | Die Entität msdyn\_replaylogheader verhindert Upgrades von Kundenorganisationen. |
| Verkaufschancenmanagement | 2755582 | Behandlung von Ausnahmen für Nullreferenzen im Helfer für geteilte Abrechnungsregeln. |
| Verkaufschancenmanagement | 2761477 | Wenn geteilte Abrechnung verwendet wird, hinterlässt das Löschen eines Meilensteins (Kopfzeile) verwaiste Meilensteine. |
| Verkaufschancenmanagement | 2767595 | Wenn ein Materialnutzungsdatensatz im Hauptformular geöffnet wird, wird die buchbare Ressource für den Datensatz auf den aktuell angemeldeten Benutzer geändert. |
| Projektplanung und -nachverfolgung | 2790384 | Das Timeout Pending OperationSet ist zu kurz. |
| Ressourcenverwaltung | 2751560 | Inkonsistente bevorzugte Organisationseinheiten im Ressourcenbedarf. |
| Fremdarbeit | 2907231 | Die Prozessphase von Kreditorenrechnungen kann nicht fortschreiten. |
| Zeit und Ausgaben | 2867363 | Datensätze fallen nicht aus der Ansicht Abwesenheiten/Urlaub zur Genehmigung heraus, wenn sie zur Genehmigung in die Warteschlange gestellt werden. |
| Zeit und Ausgaben | 2894405 | TESA: Das ungenutzte POC-Verzeichnis verursacht Compliance-Probleme. |
