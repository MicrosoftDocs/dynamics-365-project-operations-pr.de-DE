---
title: Neuigkeiten für Mai 2021 – Project Operations – Lite-Bereitstellung
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version von Project Operations – Lite-Bereitstellung vom Mai 2021 verfügbar sind.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6fb1955e2adb8562ac00a90880bf8e147bf5ed6a
ms.sourcegitcommit: 18bb56676999dbde1cf880239847ee9c2b216fe4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6060432"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Neuigkeiten für Mai 2021 – Project Operations – Lite-Bereitstellung

_Gilt für: Lite Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:

   - Project Operations in Dataverse Umgebungsversion 4.10.0.186.

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

Die folgenden Funktionen sind in dieser Version enthalten:

- [Planungsmodi](../../project-management/scheduling-modes.md): Projektmanager können jetzt definieren, ob ein Projekt mit einer festen Dauer, einer festen Arbeit oder einem Planungsmodus mit festen Einheiten verwaltet werden soll.

## <a name="quality-updates"></a>Qualitätsupdates

| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| Preise und Abrechnung | 2224568 | Logik hinzugefügt, um Anpassungen zu ermöglichen, bei denen das Rechnungsbestätigungs-Plug-In aufgerufen wird. |
| Preise und Abrechnung | 2101098 | Die Logik der Standardfelder für die Proforma-Rechnung wurde verbessert. Zu diesen Feldern gehören **Rechnungsanschrift**, **Rechnungsname** und **Zahlungsbedingungen**. Die Felder werden jetzt standardmäßig aus dem entsprechenden Projektvertragskundendatensatz verwendet. |
| Preise und Abrechnung | 2021413 | Die Felder **Tatsächliche Kosten** und **Vertrieb** in der Entität **Aufgabe** wurden aktualisiert, um Verkaufswerte aus nicht in Rechnung gestellten und in Rechnung gestellten Ausgaben für Aufgaben einzubeziehen. |
| Preise und Abrechnung | 2182110 | Beim Kopieren eines Projektvertrags wird die Vertragszeilen-ID im Zielprojektvertrag neu generiert, um sicherzustellen, dass sie eindeutig ist. |
| Verkaufschancenmanagement | 2186741 | Es wurden Validierungen hinzugefügt, um sicherzustellen, dass das Feld **Ursprung** und Transaktionstyp nicht auf vorhandenen Angebotszeilendetails aktualisiert werden kann. |
| Verkaufschancenmanagement | 2191353 | Meilensteinerstellung dürfen nicht auf einer zeitlichen und materiellen Vertragszeile erstellt werden. |
| Verkaufschancenmanagement | 2216956 | Probleme mit **Preise aktualisieren** behoben. |
| Planung und Nachverfolgung | 2182979 | Die Projektkopierfunktion wurde verbessert, um sicherzustellen, dass Ausgabenschätzungszeilen aus dem ursprünglichen Projekt kopiert werden. |
| Planung und Nachverfolgung | 2184144 | Die Projektkopierfunktion wurde verbessert, um sicherzustellen, dass der Ressourcenpositionsname aus dem ursprünglichen Projekt kopiert wird. |
| Planung und Nachverfolgung | 2184799 | Das Steuerelement beim Kopieren eines Projekts ist nun strenger, um sicherzustellen, dass das geschätzte Startdatum während des Kopiervorgangs nicht geändert werden kann. |
| Planung und Nachverfolgung | 2185134 | Während dem Kopieren eines Projekts wird das geschätzte Startdatum des Zielprojekts auf das heutige Datum festgelegt. |
| Planung und Nachverfolgung | 2196373 | Stellen Sie sicher, dass die Datensätze des Projektmanagers und der Teammitglieder nicht im Projektteam dupliziert werden, wenn Sie ein Projekt kopieren. |
| Planung und Nachverfolgung | 2211833 | Ressourcenzuweisungen werden von der Quellprojektaufgabe in das Zielprojekt kopiert. |
| Planung und Nachverfolgung | 2186541 | Probleme im Raster **Schätzungen** bei der Gruppierung nach **Ressourcen** wurde behoben. |
| Planung und Nachverfolgung | 2166906 | Die Transaktionskategorie einer Aufgabe muss in die Entität **Ressourcenzuweisung** kopiert werden. |
| Ressourcenverwaltung | 2125362 | Probleme beim Erstellen eines generischen Teammitglieds mithilfe der stundenbasierten Zuordnungsmethode wurde behoben. |
| Zeit und Ausgaben | 2113603 | Das Anpassungsproblem beim Entfernen von Attributen von der Seite **Zeiteintrag** wurde behoben. Das System prüft nun mithilfe eines Skripts, ob das Attribut auf der Seite vorhanden ist, bevor es auf das Attribut zugreift. |
| Zeit und Ausgaben | 2204377 | Kopierte Arbeitszeittabellen müssen bei der Auswahl von **Woche kopieren** automatisch angezeigt werden. |
| Zeit und Ausgaben | 2209059 | Der **Status** Feld kann für Dynamics 365 Field Service-Zeiteinträge bearbeitet werden. |
