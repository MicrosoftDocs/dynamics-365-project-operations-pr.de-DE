---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 32, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 32, V3 aufgeführt.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 023e51e834060a35d2d7e3469d34297192e38ba11c12a2c4f57424213aba44ba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994860"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 32, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 32 aufgeführt. Diese Version hat die Build-Nummer V3.10.53.108 und ist im Juni 2021 durch eine Selbst-Aktualisierung allgemein verfügbar.

## <a name="update-release-32"></a>Update Release 32

### <a name="bug-fixes"></a>Fehlerkorrekturen

#### <a name="general"></a>Allgemein

- Wenn eine größere Aktualisierung fehlschlägt, sollten nur die Hauptanwendungseintrittspunkte blockiert werden, um sicherzustellen, dass auf gemeinsam genutzte Entitäten weiterhin zugegriffen werden kann.

#### <a name="time-and-expense"></a>Zeit und Ausgaben

Die folgenden Probleme wurden behoben:

- **TimeEntriesImportFromResourceAssignment** behält die Start- und Endzeiten des Konturabschnitts der Ressourcenzuweisung nicht bei.
- Wenn Sie **Eintrag öffnen** im Raster **Zeiteingabe** auswählen, werden Sie möglicherweise daran gehindert, andere Formulare auszuwählen.
- Beim Importieren von Zuweisungen zu Zeiteinträgen kann die Clientcode-Abfrage eine lange URL generieren, die dafür sorgt, dass die Abfrage fehlschlägt.
- In dem Raster **Zeiteingabe** bleibt der Fokus nicht im Raster, nachdem ein Wert aus einer Zelle gelöscht wurde.
- Die Schaltfläche **Ablehnen** wurde aus der Ansicht **Verarbeitungsgenehmigungen** für moderne Genehmigungen entfernt.
- Die Stabilität und Leistung der Zeiterfassungs-Massengenehmigung wird durch Deadlocks und eine nicht ordnungsgemäße Handhabung von Anpassungen im Zusammenhang mit der Entität **Zeiteingabe** beeinflusst.

#### <a name="project-planning"></a>Projektplanung

- Eine Nullverweisausnahme wird generiert, wenn Sie ein Projekt aktualisieren, das einen Nullwert im Feld **Vertragseinheit** hat.
- **Projektsummen aktualisieren** berechnet die verbleibenden Kosten und den verbleibenden Umsatz eines Projekts falsch.
- Redundante Preisberechnungen wirken sich auf die Leistung aus, die sich auf Aktualisierungen von Ressourcenzuweisungskonturen bezieht.

#### <a name="resource-management"></a>Ressourcenverwaltung

Das folgende Problem wurde behoben:

- Wenn die Kalenderkapazität einer buchbaren Ressource mehr als 1 beträgt, erkennt Project Service Automation die Kapazität fälschlicherweise als 0 (null). Daher tritt in der Zeitplanansicht eine Endlosschleife auf.

#### <a name="sales"></a>Vertrieb

Die folgenden Probleme wurden behoben:

- Wenn eine Journalzeile mit einem benutzerdefinierten Transaktionstyp erstellt wird, tritt die folgende Nullreferenzausnahme auf: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Rollen und Kategorien, die vor dem Kopieren eines Angebots deaktiviert werden, sollten nicht zu kostenpflichtigen Rollen und Kategorien des neu kopierten Angebots hinzugefügt werden.
- Das Dokumentdatum und das Abrechnungsdatum stimmen nicht mit dem Startdatum überein, das in einem Rechnungspostendetail angegeben ist, das direkt auf einem Rechnungsentwurf erstellt wird.
- Null-Referenz-Ausnahmen werden in Szenarien generiert, die sich auf die Inaktivierung von Rollen und Kategorien vor dem Kopieren eines Angebots beziehen.
- Die Aktion **Preise aktualisieren** auf der Seite **Projekte** aktualisiert keine Ausgabenschätzungen und Materialschätzungen.
