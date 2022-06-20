---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 21, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in Project Service Automation Updateversion 21, V3, zur Verfügung stehen.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 7d7c098a4572aa4f5730ffdbdab77b2897cdfeff
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918817"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation Update Release 21, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die für Project Service Automation V3, Updateversion 21, neu sind oder geändert wurden. Diese Version hat die Build-Nummer V 3.10.32.50 und ist allgemein über ein Selbstupdate im Juni 2020 verfügbar.

## <a name="update-release-21"></a>Update Release 21

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Zeit und Ausgaben**

Die folgenden Probleme wurden behoben:

- Beim Hosting des **Zeiteintragsraster-Steuerelements** in Dashboards nutzt das Raster nicht die gesamte Breite des Dashboardrastercontainers.
- Für bestimmte Zeitzonen zeigt das Rastersteuerelement **Zeiteintrag** keine Datensätze an.
- Zeiteinträge, die nach 21:00 Uhr liegen, werden am falschen Tag angezeigt.
- Benutzer können keine Ausgaben übermitteln, wenn die Ausgabenkategorie **Ausgabenbeleg erforderlich** keinen Wert aufweist.

**Ressourcenverwaltung**

Die folgenden Probleme wurden behoben:

- Inaktive Buchungen werden in der Ansicht **Abstimmung** angezeigt.
- Bei der generischen Ressourcenerfüllung fehlte die Prüfung, um sicherzustellen, dass ein gültiger Buchungsstatus vorliegt.

**Projektmanagement**

Die folgenden Probleme wurden behoben:

- Die Formularraster **Projekt** (Ansicht **Ressourcenzuweisung**, **Aufgabe**, **Abstimmung**, **Ausgabenvorkalkulationen**) bleiben bearbeitbar, selbst wenn ein Projekt nicht aktiv ist.
- Doppelte Kunden können nicht mit Kunden zusammengeführt werden, die mit bestätigten Projektverträgen verknüpft sind.
- Wenn eine Ressource hinzugefügt wird, die keinen gültigen Kalender hat, gibt das System keine benutzerfreundliche Fehlermeldung zurück.
- Die Schaltfläche **Aufgabe hinzufügen** im Aufgabenraster ist aktiviert, wenn das Projekt mit **Microsoft Project-Add-In** verknüpft ist.
- Der Aufwand wächst unkontrolliert, wenn eine Aufgabe mit einer Kategorie einer Ressource mit einer Rolle zugewiesen wird, für die ein Einstandspreis definiert ist.

**Vertrieb**

Die folgenden Verbesserungen wurden vorgenommen:

- **Rechnungsintervall** und **Abrechnungsstart** wurden in die Registerkarte **Rechnungszeitplan** verschoben.

Die folgenden Probleme wurden behoben:

- **Gesamtverkaufspreis** ist null (0) für **Kategorie**, obwohl **Rolle** einen Gesamtverkaufspreis hat, der nicht Null ist.
- Kunden können den Wert des Felds **Rechnungsstatus** nicht in **Bereit zur Rechnungsstellung** ändern, wenn ein anderer angepasster Prozess ein zusätzliches Feld aktualisiert.
- Die Schaltfläche **Rechnungspositionen aktualisieren** kann mehrere doppelte Positionen erstellen, wenn sie wiederholt ausgewählt wird.
- Die **Preise aktualisieren**-Schaltfläche funktioniert nicht im **Rollenpreise**-Unterraster im Formular **Schnellansicht**.
- Die Logik **Verkaufspreislisten-Lösung** behandelt Zeitzonen nicht ordnungsgemäß, was zu einer falschen Auswahl von Preislisten führt.
- Die **Gesamten Istkosten** eines Projekts können um einen Bruchteil des Betrags abweichen, nachdem ein einmaliger Eintrag genehmigt wurde.
- Die Logik **Preislösung** liefert keine benutzerfreundliche Fehlermeldung, wenn **Abgerufener RolePrice** keine Werte in den Feldern **Primäre Einheit** und **Preis in primärer Einheit** hat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
