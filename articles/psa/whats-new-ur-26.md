---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 26, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643262"
---
<a name="project-service-automation-update-release-26-v3"></a>Project Service Automation Update Release 26, V3
================================================

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 26 aufgeführt. Diese Version hat die Build-Nummer V3.10.44.59 und ist im Allgemeinen über ein Selbstupdate im Dezember 2020 verfügbar.

<a name="update-release-26"></a>Update Release 26
-----------------

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Zeit und Ausgaben**

Die folgenden Probleme wurden behoben:

-   Benutzer können die Aufgabe für einen Zeiteintrag ändern, der genehmigt/übermittelt wurde.

-   Fehler „Objektreferenz nicht gesetzt“ beim Speichern der Zeiteingabe.

-   Der Zeiteintragsimport aus Ressourcenzuweisungen erstellt Zeiteinträge mit den falschen DateTime-Werten.

-   Wenn Project Service Automation und die Field Service-App installiert sind, wird die **Neu**-Schaltfläche zweimal in der Befehlsleiste für Zeiteinträge in der Field Service-App angezeigt.

-   Zellenaktualisierungen von **Einheit zulassen** und **Einheitengruppe** funktionieren jetzt im Raster **Kostenschätzungen**.

-   **Zeiteintragsbearbeitung aktualisieren**-Formular enthält **Zeitleiste**.

-   Die Zeitgenehmigung für Zeiteinträge außerhalb des Projekts blockiert das System bei der Suche nach einer Projektgenehmigungsrolle.

**Ressourcenverwaltung**

Die folgenden Probleme wurden behoben:

-   Validierung im **PostProjectCreate**-Plug-In hinzugefügt, um vor dem Erstellen einer primären Anforderung nach einer primären Anforderung zu suchen.

-   **Mitglied des Projektteams**-Formular für Schnellerfassung löst eine Nullreferenzausnahme aus, wenn Felder aus dem Formular entfernt werden.

-   Das Generieren von Anforderungen für 12 Stunden über 1 Jahr schlägt fehl.

-   Verbesserte Nullreferenzausnahme für Fehlermeldungen während der Erstellung der Ressourcenanforderungen.

**Projektmanagement**

Die folgenden Probleme wurden behoben:

-   Verbesserte Validierung zur Behebung der Nullreferenzausnahme im **PreProjectUpdate** Plug-In.

-   Vom Microsoft Project-Desktop-Add-In veröffentlichte Projekte löschen nicht zugewiesene Zuweisungen.

-   Neue Validierung hinzugefügt, wenn die Projektreferenz einer Aufgabe aufgrund einer Nullreferenzausnahme im **PreValidateProjectTaskUpdate**-Plug-In ungültig ist.

-   Das Teammitgliedsraster zeigt keine eindeutigen Zuordnungen im Teammitgliedsdatensatz an.

-   Neue Validierungs- und Fehlermeldungen aufgrund einer Nullreferenzausnahme im **PreProjectTaskDelete**-Plug-In hinzugefügt.

**Vertrieb**

Die folgenden Probleme wurden behoben:

-   Bei der Auswahl einer projektbasierten Zeile im Angebot oder Vertrag sollte die **Vorschlag**-Schaltfläche nur sichtbar sein, wenn Sie eine produktbasierte Position auswählen, die einem vorhandenen Produkt zugeordnet ist.

-   **Create_Product**-Berechtigung wurde von **Create_ProjectContract**-Berechtigung abgetrennt.

-   Das Löschen einer Rechnungsposition führt zu einem Nullreferenzfehler **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.
