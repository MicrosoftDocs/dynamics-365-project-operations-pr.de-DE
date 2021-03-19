---
title: Projektteammitglieder
description: Dieses Thema enthält Informationen zum Arbeiten mit Informationen, Attributen und der Planung von Mitgliedern des Projektteams.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3526c5e2c968bdaa4d957592aed8d1b21c64b799
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286652"
---
# <a name="project-team-members"></a>Projektteammitglieder

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Mitglieder des Projektteams sind die Projektteilnehmer, die die Arbeit an einem Projekt abschließen. Das Ziel des Teammitgliedsrasters besteht darin, eine Liste der benannten Ressourcen bereitzustellen, die für das Projekt verpflichtet sind, sowie allgemeine Teammitglieder, die Platzhalterressourcen sind und später mit Personal besetzt werden.

Aus dem Teammitgliedsraster können der Projektmanager und die anderen Projektteilnehmer sehen, wer sich für das Projekt verpflichtet hat. Sie können auch eine Zusammenfassung ihrer Buchungen, des geplanten Aufwands und der einzelnen Ressourcenzuweisungen anzeigen. Über das Teammitgliedsraster können Projektmanager Ressourcenanforderungen für allgemeine Teammitglieder definieren und die Buchungen vorhandener Teammitglieder verwalten.

In der folgenden Tabelle sind die wichtigsten Attribute eines Projektteammitglieds aufgeführt.

| Feldname          | Beschreibung des Dataflows                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zuordnungsmethode        | Die Zuordnungsmethode zum Buchen von Ressourcen für das Projekt.                                                                         |
| Fakturierungstyp             | Wählen Sie aus, ob das Teammitglied als fakturierbar klassifiziert ist.                                                                                                                                       |
| Buchbare Ressource        | Die buchbare Ressource, die zum Ersetzen der generischen Ressource ausgewählt wurde.                                                                                                                   |
| Löschstatus            | Der Löschstatus des Teammitglieds, um nachzuverfolgen, ob eine Löschanforderung an PSS gesendet wurde und ob PSS die Antwort erfolgreich und innerhalb des erwarteten Zeitfensters zurücksendet |
| Gesamtaufwand (Stunden)     | Die Aufwandssumme des Teammitglieds bei den Zuweisungen.                                                                                                                         |
| Aufwand abgeschlossen (Stunden) | Eine Verfolgung des Aufwands, den das Teammitglied für seine Zuweisungen erzielt hat                                                                                           |
| Aufwand verbleibend (Stunden) | Eine Verfolgung des noch nicht abgeschlossenen Aufwands, den das Teammitglied für seine Zuweisungen erzielt hat                                                                                    |
| Fertigstellen                   | Das Abschlussdatum der Ressourcenteammitgliedschaft.                                                                                                                                            |
| Verbindlich gebuchte Stunden        | Die verbindlich gebuchten Stunden des Teammitglieds                                                                                                                                                                |
| Positionsname            | Der Name, der zur Identifizierung der generischen Ressource verwendet wird.                                                                                                                                   |
| Ressourcenzuordnungseinheit          | Die Organisationseinheit der Ressource, die die Arbeit ausführt.                                                                                                                      |
| Projektgenehmiger         | Wählen Sie aus, ob das Teammitglied Zeit und Ausgaben genehmigen darf.                                                                                                                     |
| Erforderliche Stunden           | Die erforderlichen Stunden des Teammitglieds für die Teammitgliedsanforderung.                                                                                                                       |
| Rolle                     | Die Rolle, die das Teammitglied in diesem Team ausfüllt                                                                                                                                |
| Positionsbeschreibung     | Geben Sie eine Beschreibung der Rolle für dieses Teammitglied ein.                                                                                                                             |
| Unverbindlich gebuchte Stunden        | Die unverbindlich gebuchten Stunden des Teammitglieds                                                                                                                                                                 |
| Anfang                    | Das Startdatum der Ressourcenteammitgliedschaft.                                                                                                                                          |

Im Raster der Teammitglieder können die folgenden Aktionen ausgeführt werden:

- **Buchen**: Für Organisationen, die die hybride Buchungsmethode nutzen, können Benutzer mit der Buchaktion eine benannte Ressource basierend auf den vom allgemeinen Teammitglied generierten Anforderungen buchen
- **Anforderung generieren**: Diese Aktion generiert die Anforderung.
- **Muster angeben**: Ermöglicht Projektmanagern, die Konturen des Ressourcenbedarfs auf granularer Ebene anzupassen Projektmanager können sich an die spezifischen Anforderungen des Projekts anpassen, wenn die Standardverteilung nicht passt.
- **Anfrage einreichen**: Für Organisationen, die die zentrale Buchungsmethode verwenden
- **Bearbeiten**: Teammitgliedsattribute können bearbeitet werden, einschließlich Organisationseinheit, Rolle und Positionsname
- **Buchungen verwalten**: Wenn Ressourcenbuchungen aktualisiert werden müssen, kann der Projektmanager durch Verwalten von Buchungen Folgendes anpassen:

    - Anfang
    - Beenden
    - Zuteilung des Gesamtaufwands

- **Neu**: Zusätzlich zum Hinzufügen von Ressourcen direkt aus dem Zeitplan können Projektmanager neue benannte oder allgemeine Teammitglieder aus dem Teammitgliedsraster hinzufügen.
- **Löschen**: Durch Auswahl eines oder mehrerer Teammitglieder kann der Projektmanager Ressourcen löschen, die nicht mehr am Projekt teilnehmen werden. Durch das Löschen eines Teammitglieds werden auch alle zugehörigen Ressourcenzuweisungen gelöscht und alle vorhandenen Buchungen storniert.


[!INCLUDE[footer-include](../includes/footer-banner.md)]