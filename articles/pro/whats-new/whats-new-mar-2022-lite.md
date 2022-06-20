---
title: Neuerungen im März 2022 – Bereitstellung von Project Operations Lite
description: Dieser Artikel informiert Sie über die Qualitätsupdates, die in der Lite-Bereitstellung von Project Operations im März 2022 verfügbar sind.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934227"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Neuerungen im März 2022 – Bereitstellung von Project Operations Lite

_Gilt für: Lite Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Version 4.30.0.99

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

- Unterauftragsvergabe: Erstellung von Kreditorenrechnungen und Abgleichserfahrungen

## <a name="quality-updates"></a>Qualitätsupdates

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Zeit und Ausgaben | 2388011 | Anzeigen von Ablehnungskommentaren für Einreicher von Zeiteinträgen während der Massengenehmigung. |
| Projektplanung und -nachverfolgung | 2495294 | Projektdetails dürfen auf der **Aufgabendetails**-Seite nicht editierbar sein. |
| Preise und Abrechnung | 2499605 | Vertragsmeilensteine, die aus Angebotsmeilensteinen erstellt werden, sind fälschlicherweise als schreibgeschützt gekennzeichnet. |
| Projektplanung und -nachverfolgung | 2506050 | Der Vorgangssatz bleibt eine Stunde lang ausstehend, wenn keine Änderung zu speichern ist. Der Satz wird dann fälschlicherweise als **Fehlgeschlagen** markiert, wobei er sofort abgeschlossen werden sollte. |
| Preise und Abrechnung | 2507401 | Standardvertragseinheiten werden aufgrund von falschem Zwischenspeichern in Projekten falsch eingegeben. |
| Preise und Abrechnung | 2541660 | **Validierung der Vertriebsauftragserstellung** beim dualen Schreiben sollten nur für projektbasierte Aufträge verwendet werden. |
| Preise und Abrechnung | 2552745 | Die Steuer wird nicht zwischen Kunden aufgeteilt, die Regeln für die getrennte Abrechnung eingerichtet haben. |
| Preise und Abrechnung | 2558859 | Verbesserte Fehlermeldungen beim Einrichten von Preisdimensionen. |
| Preise und Abrechnung | 2558933 | **Import aus Project Estimates** scheitert, wenn **msdyn\_project** als Preisdimension hinzugefügt wird. |
| Preise und Abrechnung | 2559101 | Das Löschen von Projektparametern wird nicht blockiert und verursacht Probleme. |
| Verkaufschancenmanagement | 2570390 | Das Plug-In für duales Schreiben erzwingt bei Angeboten, Aufträgen und Verkaufschancen den Kontotyp **Kunde**, auch wenn dieser Kontotyp nicht korrekt ist. |
| Preise und Abrechnung | 2586097 | Geteilte abgerechnete Kosten-Ist-Werte werden nicht storniert, wenn ein Projekt aus einer Projektvertragsposition entfernt wird. |
| Preise und Abrechnung | 2589619 | Die Steuer auf manuell eingetragenes Material wird auf die nicht fakturierten Verkaufs-Ist-Werte und die Rechnung übertragen. |
| Verkaufschancenmanagement | 2594015 | Ein Angebot kann für Kunden mit **Net60**-Zahlungsbedingungen nicht als gewonnen abgeschlossen werden. |
| Projektplanung und -nachverfolgung | 2595841 | In Project for the Web erhalten Benutzer eine Fehlermeldung zu einem fehlenden **msdyn\_actualstart**, wenn sie eine neue Ressourcenanforderung erstellen. |
| Zeit und Ausgaben | 2602511 | Das **Zurückgewiesen von**-Feld für Zeiteinträge zeigt als Ablehner **System** anstelle eines benannten Benutzers. |
| Zeit und Ausgaben | 2602528 | Ein Projektgenehmiger kann Zeit für Projekte genehmigen, in denen er nicht als Genehmiger aufgeführt ist. |
| Preise und Abrechnung | 2608550 | Eine Korrekturrechnung kann auch dann bestätigt werden, wenn gegenüber dem Original keine Änderungen vorgenommen wurden. |

## <a name="removed-and-deprecated-features"></a>Entfernte und veraltete Funktionen

Der Artikel [Entfernte oder veraltete Funktionen in Project Operations](../../whats-new/removed-depreciated-features-project.md) beschreibt Funktionen, die für Dynamics 365 Project Operations entfernt oder außer Betrieb genommen wurden.

- Eine entfernte Funktion ist im Produkt nicht mehr verfügbar.
- Eine veraltete Funktion wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Eine Ankündigung, dass Funktionen außer Betrieb genommen werden, wird im Artikel [Entfernte oder veraltete Funktionen in Project Operations](../../whats-new/removed-depreciated-features-project.md) erscheinen, 12 Monate bevor eine Funktion aus dem Produkt entfernt wird.
