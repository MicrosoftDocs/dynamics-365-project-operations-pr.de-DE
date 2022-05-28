---
title: Neuerungen im März 2022 – Bereitstellung von Project Operations Lite
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version vom März 2022 der Project Operations Lite-Bereitstellung verfügbar sind.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583749"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Neuerungen im März 2022 – Bereitstellung von Project Operations Lite

_Gilt für: Lite Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieses Thema gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

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

Das Thema [Entfernte oder veraltete Funktionen in Project Operations](../../whats-new/removed-depreciated-features-project.md) beschreibt Funktionen, die aus Dynamics 365 Project Operations entfernt wurden oder veraltet sind.

- Eine entfernte Funktion ist im Produkt nicht mehr verfügbar.
- Eine veraltete Funktion wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

12 Monate vor dem Entfernen wird im Thema [Entfernte oder veraltete Funktionen in Project Operations](../../whats-new/removed-depreciated-features-project.md) ein Verfallshinweis angezeigt.
