---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 26, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 26, V3, zur Verfügung stehen.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 11f722c1f31c0e8aa08192cc955aabbe97018225
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928799"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation Update Release 26, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die in Project Service Automation Updateversion 26, V3, neu sind oder geändert wurden. Diese Version hat die Build-Nummer V3.10.44.59 und ist im Allgemeinen über ein Selbstupdate im Dezember 2020 verfügbar.

## <a name="update-release-26"></a>Update Release 26

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Zeit und Ausgaben**

Die folgenden Probleme wurden behoben:

- Benutzer können die Aufgabe für einen Zeiteintrag ändern, der genehmigt/übermittelt wurde.
- Fehler „Objektreferenz nicht gesetzt“ beim Speichern der Zeiteingabe.
- Der Zeiteintragsimport aus Ressourcenzuweisungen erstellt Zeiteinträge mit den falschen DateTime-Werten.
- Wenn Project Service Automation und die Field Service-App installiert sind, wird die **Neu**-Schaltfläche zweimal in der Befehlsleiste für Zeiteinträge in der Field Service-App angezeigt.
- Zellenaktualisierungen von **Einheit zulassen** und **Einheitengruppe** funktionieren jetzt im Raster **Kostenschätzungen**.
- **Zeiteintragsbearbeitung aktualisieren**-Formular enthält **Zeitleiste**.
- Die Zeitgenehmigung für Zeiteinträge außerhalb des Projekts blockiert das System bei der Suche nach einer Projektgenehmigungsrolle.

**Ressourcenverwaltung**

Die folgenden Probleme wurden behoben:

- Validierung im **PostProjectCreate**-Plug-In hinzugefügt, um vor dem Erstellen einer primären Anforderung nach einer primären Anforderung zu suchen.
- **Mitglied des Projektteams**-Formular für Schnellerfassung löst eine Nullreferenzausnahme aus, wenn Felder aus dem Formular entfernt werden.
- Das Generieren von Anforderungen für 12 Stunden über 1 Jahr schlägt fehl.
- Verbesserte Nullreferenzausnahme für Fehlermeldungen während der Erstellung der Ressourcenanforderungen.

**Projektmanagement**

Die folgenden Probleme wurden behoben:

- Verbesserte Validierung zur Behebung der Nullreferenzausnahme im **PreProjectUpdate** Plug-In.
- Vom Microsoft Project-Desktop-Add-In veröffentlichte Projekte löschen nicht zugewiesene Zuweisungen.
- Neue Validierung hinzugefügt, wenn die Projektreferenz einer Aufgabe aufgrund einer Nullreferenzausnahme im **PreValidateProjectTaskUpdate**-Plug-In ungültig ist.
- Das Teammitgliedsraster zeigt keine eindeutigen Zuordnungen im Teammitgliedsdatensatz an.
- Neue Validierungs- und Fehlermeldungen aufgrund einer Nullreferenzausnahme im **PreProjectTaskDelete**-Plug-In hinzugefügt.

**Vertrieb**

Die folgenden Probleme wurden behoben:

- Bei der Auswahl einer projektbasierten Zeile im Angebot oder Vertrag sollte die **Vorschlag**-Schaltfläche nur sichtbar sein, wenn Sie eine produktbasierte Position auswählen, die einem vorhandenen Produkt zugeordnet ist.
- **Create_Product**-Berechtigung wurde von **Create_ProjectContract**-Berechtigung abgetrennt.
- Das Löschen einer Rechnungsposition führt zu einem Nullreferenzfehler **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
