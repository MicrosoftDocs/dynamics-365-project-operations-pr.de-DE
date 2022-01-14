---
title: Neuigkeiten Dezember 2021 – Project Operations Lite-Bereitstellung
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version vom Dezember 2021 der Project Operations Lite-Bereitstellung verfügbar sind.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942976"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Neuigkeiten Dezember 2021 – Project Operations Lite-Bereitstellung

_Gilt für: Lite Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieses Thema gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Versionen 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

### <a name="subcontract-management"></a>Fremdarbeitsverwaltung 

- [Fremdarbeitsprojektteammitglieder](../subcontracting/subcontracting-project-team-members.md): Ein Projektmanager kann benannte oder generische Teammitglieder mit Fremdarbeiten und Fremdarbeitspositionen erstellen, um die Personalausstattung und Schätzung zu beeinflussen.
- [Fremdarbeitsoptionen für Projektteammitglieder](../subcontracting/subcon-options.md): Bei der Personalauswahl für benannte oder generische Projektteammitglieder kann der Projektmanager bestehende Fremdarbeiten überprüfen oder neue Fremdarbeiten für ein oder mehrere Projektteammitglieder erstellen. 
- [Kostenschätzung von Fremdarbeitsressourcenzuweisungen](../subcontracting/costing-subcon-ra.md): Die Projektkostenschätzung berücksichtigt die Fremdarbeitsressourcenzuweisungen und berechnet diese anhand der Einkaufspreislisten, die mit Fremdarbeiten verbunden sind. 
- [Zeitplanübersicht konfigurieren für die Anzeige von Vertragsmitarbeitern und Fremdarbeitskapazität](../subcontracting/configure-sb-subcon.md): Die Zeitplanübersicht in Project Operations kann jetzt so konfiguriert werden, dass sie nach buchbaren Ressourcen des Typs Vertragsarbeiter und Fremdarbeitskapazität zusammen mit Mitarbeitern sucht und diese vorschlägt. Diese Konfiguration kann bei der Suche nach Ressourcen im Rahmen der Personalbesetzung für eine bestimmte Projektanforderung oder bei der Suche außerhalb des Kontexts einer Projektanforderung angewendet werden.
- [Besetzung eines Projekts mit Vertragsmitarbeitern und Fremdarbeitskapazität](../subcontracting/staffing-cw.md): Vertragsarbeiter können jetzt für Projekte gebucht werden, die die Zeitplanübersichtserfahrungen nutzen.
- [Erfassung von Zeit, Ausgaben und Materialverbrauch für Projekte aus Fremdarbeitskomponenten](../subcontracting/recording-subcon-actuals.md): Vertragsarbeiter können Zeit und Ausgaben aufzeichnen, und Projektteammitglieder können auch die Verwendung von Materialien aufzeichnen, die über eine Fremdarbeit in einem Projekt gekauft wurden. Dies führt dazu, dass die Kosten für Projekte, die gekaufte Kapazitäten oder Materialien verwenden, genau erfasst werden.
- [Statusübergänge bei Fremdarbeit](../subcontracting/subcon-states.md): Fremdarbeiten können bestätigt werden, um die Verhandlungen mit dem Verkäufer abzuschließen, geschlossen werden, um den Abschluss der Lieferung anzuzeigen, oder storniert werden, um die Beendigung des Vertrags mit dem Verkäufer vor Abschluss der Lieferung anzuzeigen.

### <a name="task-planning"></a>Aufgabenplanung
- Verbesserte Fehlerbehebung für Systemadministratoren. Wenn ein Benutzer ein Projekt nicht öffnen kann, kann der Administrator nicht-lizenzbezogene Fehler überprüfen, die von Project for the Web in den [Projektplanungsprotokollen](../../project-management/schedule-api-logs.md) erzeugt wurden.
- [Verwenden von Aufgabenchecklisten in Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). In Microsoft Project for the Web können Sie einer Aufgabe eine Prüfliste hinzufügen, um bestimmte Elemente zu verfolgen.

## <a name="quality-updates"></a>Qualitätsupdates

| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| Planung und Nachverfolgung | 2392596 | Zeitplan-APIs ermöglichen jetzt Aktualisierungen der Felder **Aufwand verbleibend**, **Aufwand abgeschlossen** und **% abgeschlossen**. |
| Planung und Nachverfolgung | 2478497 | Die Felder **Aktivitätsnummer** und **Aufgaben-ID** der Zeitplan-APIs können bei der Eingabe leer sein, da das System sie mit automatischer Nummerierung auffüllt.|
| Zeit und Ausgaben | 2468135 | Die Zahl der Zulassungsversuche wird von fünf auf drei reduziert. |
| Zeit und Ausgaben | 2468188 | Es wurde ein Problem behoben, bei dem der Protokolltext die maximale Länge im **Notiztext**-Attribut der **Anmerkung**-Entität überschritten hat. |
