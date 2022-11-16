---
title: Externe Zeitplanung
description: Dieser Artikel enthält Informationen über externe Zeitplanung.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736962"
---
# <a name="external-scheduling"></a>Externe Zeitplanung

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Mit der externen Zeitplanung können Sie Entitäten, die sich auf Projektstrukturpläne (PSPs) beziehen, nativ erstellen, aktualisieren und löschen, jedoch ohne die aktuellen Einschränkungen, die von Microsoft Project for the Web erzwungen werden. Es bietet auch eine begrenzte Validierung. Dieser Modus sollte nur von folgenden Kunden verwendet werden:

- Kunden, die über die Tools verfügen, die zum Definieren eines PSP außerhalb der von Project Operations bereitgestellten Planungslogik erforderlich sind
- Kunden, die Zeitplanhierarchie, Abhängigkeiten oder Aufgabendauer verwalten müssen

> [!IMPORTANT]
> Daten, die nicht korrekt in die PSP-bezogenen Entitäten eingegeben wurden, werden möglicherweise nicht im Ressourcenabstimmungsraster, Schätzungsraster, Nachverfolgungsraster oder Ressourcenzuweisungsraster gerendert.

## <a name="configuration"></a>Configuration

Diese Funktion ist standardmäßig aktiviert. Auf der standardmäßigen Hauptseite für Projekte ist das zugehörige Feld jedoch standardmäßig nicht sichtbar. Um das Feld zu aktivieren, öffnen Sie im Maker Portal die Hauptseite für die Projektentität, wählen Sie das Feld **Zeitplanungs-Engine** und ändern Sie dann das Feld zu **Standardmäßig sichtbar**. Wenn Sie die standardmäßige Projekthauptseite nicht verwenden, bearbeiten Sie Ihre vorhandene Seite und fügen Sie das Feld **Zeitplanungs-Engine** hinzu.

## <a name="settings"></a>Einstellungen

Um den externen Zeitplanungsmodus zu verwenden, müssen Sie zuerst ein neues Projekt erstellen und die **Extern geplante** Zeitplanungs Engine in der Dropdown-Liste auf der Projekt-Hauptseite erstellen. Nachdem dieser Modus für ein Projekt eingerichtet wurde, kann er nicht mehr geändert werden.

## <a name="viewing-the-wbs"></a>Anzeigen des WBS

Wenn ein Projekt extern geplant wird, ist der Zugriff auf Project for the Web dieses Projekt eingeschränkt. Um den PSP anzuzeigen, müssen Sie zum Verfolgungsraster gehen, wo der vollständige PSP angezeigt wird.

## <a name="creating-and-editing-the-wbs"></a>Erstellen und Bearbeiten des WBS

Wenn die externe Planung für ein Projekt aktiviert ist, müssen Sie die Daten für alle PSP-bezogenen Entitäten definieren, einschließlich Aufgaben, Teammitglieder, Ressourcenzuweisungen und Abhängigkeiten.

Die folgende Abbildung zeigt das Datenmodell für die Projektplanung.

![Datenmodell der Projektplanung.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Funktionale Einschränkungen

Die folgenden Vorgänge sind für extern geplante Projekte nicht zulässig.

### <a name="project-planning"></a>Projektplanung

- **Projekt kopieren** – Dieser Vorgang wird für extern geplante Projekte nicht unterstützt.
- **Projekt verschieben** – Änderungen am Startdatum eines Projekts verschieben nicht den Beginn von Vorgängen oder Ressourcenzuweisungen im PSP.
- **Aktualisieren des Projektmanagers** – Änderungen am Projektmanager auf der Projektstartseite erzeugen erst nach der Umstellung des Projekts automatisch ein neues Projektteammitglied.
- **Aktualisieren der Arbeitsstundenvorlage des Projekts** – Änderungen an der Arbeitsstundenvorlage des Projekts führen nicht zu einer Neuberechnung des Zeitplans des Projekts.
- **Ressourcenzuweisungskonturen** – Die Erstellung von Ressourcenzuweisungen aktualisiert das Feld **mdyn\_PlannedWork** nicht automatisch. Dieses Feld wird verwendet, um Konturen für den Ressourcenzuweisungsaufwand zu speichern. Wenn Sie den Zeitphasenaufwand im Ressourcenzuweisungsraster oder im Ressourcenabgleichsraster anzeigen, müssen Sie gültige Ressourcenzuweisungskonturen definieren. Diese Konturen müssen korrekt formatiert sein, damit sie die Berechnung sowohl der Kostenkonturen als auch der Verkaufspreiskonturen auslösen. Wir empfehlen, dass Sie ein Testprojekt erstellen, das von Project for the Web geplant wird, und dann die zugehörigen Daten überprüfen, um die Anforderungen und die Formatierung zu bestätigen.

### <a name="resource-management"></a>Ressourcenverwaltung

- **Generische Ressourcenerfüllung** – Generische Ressourcenerfüllung wird für extern geplante Projekte nicht unterstützt. Versuche, aktive offene Anforderungen zu erfüllen, werden neue Projektteammitglieder erstellen, aber das generische Teammitglied wird nicht gelöscht oder das generische Teammitglied bei vorhandenen Ressourcenzuweisungen ersetzt.
- **Teammitglied löschen** – Das Löschen eines Teammitglieds löscht nicht automatisch Ressourcenzuweisungen.

### <a name="quoting-and-contracting"></a>Angebotserstellung und Vertragsabschluss

- **Importieren von Angebotspositions- und Vertragspositionsdetails** – Wenn Angebots- oder Vertragspositionsdetails aus einem Projekt importiert werden, wurde die Anwendung getestet, um nur maximal 500 Aufgaben in der WBA zu unterstützen, basierend auf einer Grenze von 20 Zuweisungen pro Aufgabe.

### <a name="actuals-and-invoicing"></a>Ist- und Rechnungsstellung

- Obwohl es keine Änderungen an bestehenden Validierungen zwischen dem PSP und den Finanztransaktionen gibt, ist es wichtig, dass Sie sich an das Standard-Datenmodell halten, um sicherzustellen, dass alle nachgelagerten Transaktionen wie erwartet ausgeführt werden.
