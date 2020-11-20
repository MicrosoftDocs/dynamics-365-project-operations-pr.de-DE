---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 24, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 24, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3a37e71be2cce259d8aed0621d13393b6bbe4199
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126572"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation Update Release 24, V3

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 24 aufgeführt. Diese Version hat eine Build-Nummer von V 3.10.42.43 und ist durch ein Selbst-Update im Oktober 2020 allgemein verfügbar.

## <a name="update-release-24"></a>Update Release 24

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Vertrieb**

Die folgenden Probleme wurden behoben:

- Problem beim Festlegen der Standardpreisliste der Produkte.
- Die Leistung des Angebotsgewinns ist aufgrund der eingebetteten Preisliste und der Kopie der Rollenpreisdatensätze langsam.
- **Projektvertrag/Vertriebs-Hub** > **Produktposition/Bestellpositionsmenge** wird automatisch auf die nächste ganze Zahl gerundet.
- Erhöhen Sie die Systemberechtigungen beim Lesen von Preislisten.
- Kopieren Sie die Kundenadressfelder **address1_freighttermscode** und **address1_shippingmethodcode** nach Angebot/Auftrag. 


**Zeit und Ausgaben**

Die folgenden Probleme wurden behoben:

- Das **Zeiterfassungsraster** unterstützt kein **Nur Datum**-Zeitverhalten.
- **Zeiteintrag** wird nicht automatisch aktualisiert. Eine manuelle Aktualisierung ist erforderlich.
- Die Zeiteinträge können nicht aus einer Zuweisung importiert werden, wenn die Zuweisungen einer Ressource unterbrochen sind (0 Stunden).
- Stellen Sie beim Erstellen eines Zeiteintrags den Start auf den gleichen Wert ein wie **msdyn_date**.
- Aktivieren Sie die Massenbearbeitung für die Zeiteingabe erneut.

**Ressourcenverwaltung**

Die folgenden Probleme wurden behoben:

- Wenn Sie versuchen, den Status einer Buchung zwischen zwei Tagen ohne Anforderung zu aktualisieren, wird eine null-ref-Ausnahme ausgelöst.
- Fehler beim Laden der **Abstimmungsansicht**.


**Projektmanagement**

Die folgenden Probleme wurden behoben:

- Die automatische Speicherung wird im **Projektplan** beim Wechsel von **Manuell** zu **Automatisch** nicht abgeschlossen.
- Aufwandskosten sollten nicht zur Abweichung auf dem **Projektverfolgungsraster** berechnet werden.
- Inkonsistentes Verhalten für **Schätzungs-Tag**-Spalten während des Ladens versus Änderungen vom Typ **Zeitphase**.
- Die tatsächlichen Kosten eines Projekts spiegeln möglicherweise nicht die Gesamtsummen von **Tatsächliche Transaktionen** wider.
- Das **geschätzte Enddatum** auf der Registerkarte **Zusammenfassung** stimmt nicht mit dem **PSP-Zeitplan** überein.
- **Aktuelle Stunden aktualisieren** beim Ausrücken funktioniert nicht richtig.
- Ein Projektmanager außerhalb des **Unternehmenseinheit**-Stamms kann kein Projekt erstellen.
- Änderungen an der Aufgabe oder Kategorie unter **Ausgabenschätzungen** werden nicht beibehalten.
- **Kopie des Vertrags** kopiert die Rechnungspläne und den Ausführungsstatus.
- Die Schaltfläche **Tatsächliche Transaktionen aktualisieren** berechnet Zusammenfassungsaufgaben falsch.
- Microsoft Project-Add-In: Behebung eines Nullreferenzfehlers, wenn ein Teammitglied eine leere Ressourceneinheit hat.

