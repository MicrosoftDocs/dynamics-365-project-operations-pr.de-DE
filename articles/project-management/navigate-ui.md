---
title: Navigieren in der Benutzeroberfläche
description: Dieses Thema enthält Informationen zur Projektverwaltung in Dynamics 365 Project Vorgängen.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: deedfe0c6601fd09e09460034c9a0db936b6566e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127517"
---
# <a name="navigating-the-user-interface"></a>Navigieren in der Benutzeroberfläche

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

## <a name="overview"></a>Überblick

Das Hauptprojektformular ist in mehrere Registerkarten unterteilt. Jede Registerkarte repräsentiert eine andere Detailebene innerhalb des Projekts.

- **Zusammenfassung**: Bietet eine Beschreibung des Projekts und aggregiert sowohl die geplante als auch die tatsächliche Projektleistung.

    ![Registerkarte und Felder der Zusammenfassung](media/navigation7.png)

- **Aufgaben**: Enthält die Details zum Projektstrukturplan, die durch eine Rasteransicht, eine Übersicht und ein Gantt dargestellt werden.

    ![Registerkarte und Felder der Aufgaben](media/navigation8.png)

- **Team**: Enthält Details zu den Projektteilnehmern In dieser Ansicht wird auch der zugewiesene Aufwand jedes Teammitglieds zusammengefasst.

    ![Registerkarte und Felder des Teams](media/navigation9.png)

- **Ressourcenzuweisungen**: Bietet eine zeitgesteuerte Ansicht des Aufwands für jede Ressource in einem Projekt.

    ![Registerkarte und Felder für Ressourcenzuweisungen](media/navigation10.png)

- **Ressourcenabstimmung**: Bietet eine zeitgesteuerte Ansicht der Unterschiede zwischen den Zuweisungen der einzelnen benannten Ressourcen und ihren Buchungen.

    ![Registerkarte und Felder für die Abstimmung](media/navigation11.png)

- **Schätzungen**: Bietet eine zeitgesteuerte Ansicht der Kosten- und Umsatzschätzungen eines Projekts

    ![Registerkarte und Felder der Schätzung](media/navigation12.png)

- **Verfolgung**: Bietet eine Ansicht, die den Fortschritt von Aufgaben in der Projektstrukturplan für Aufwand, Kosten und Umsatz anzeigt

    ![Registerkarte und Felder der Verfolgung](media/navigation13.png)

- **Vertrieb**: Bietet Deep Links zu Angeboten und Verträgen, die mit dem Projekt verbunden sind

- **Ausgabenschätzungen**: Stellt ein Raster bereit, das die Projektkosten basierend auf den Kategorien der Organisationskosten definiert

    ![Registerkarte und Felder der Ausgabenschätzungen](media/navigation14.png)

## <a name="grid-controls"></a>Rastersteuerungen

Im Folgenden finden Sie eine kurze Übersicht über die typischen Steuerelemente auf den verschiedenen Registerkarten für die Projektplanung.

### <a name="refresh"></a>Refresh

**Aktualisierung**: Ruft die neuesten Daten vom Server ab, wenn nach dem Laden des Rasters Änderungen aufgetreten sind

![Schaltfläche „Aktualisieren“](media/navigation7.png)

### <a name="group-by"></a>Gruppieren nach

**Gruppieren nach**: Aktualisiert die Gruppierung der Zeilen im Raster, um entweder Ressourcen, Rollen oder Kategorien entsprechend den Anforderungen des Benutzers wiederzugeben

![Nach Schaltfläche gruppieren](media/navigation6.png)

### <a name="previousnext"></a>Zurück/Weiter

**Zurück**/**Weiter**: Aktualisieren Sie die sichtbaren Zeiträume in den zeitgesteuerten Rastern.

![Schaltflächen „Zurück“ und „Weiter“](media/navigation2.png)

### <a name="timescale"></a>Zeitskala

**Zeitskala**: Ändern Sie die Aggregation der zeitlich gesteuerten Daten zwischen Tagen, Wochen, Monaten und Jahren.

![Schaltfläche „Zeitskala“](media/navigation3.png)

### <a name="expand"></a>Aufklappen

**Erweitern**: Rendern Sie das sichtbare Raster im Vollbildmodus, um zusätzliche Rollen besser erkennen zu können.

![Schaltfläche 'Erweitern'](media/navigation4.png)

### <a name="time-phase-by"></a>Zeitphase bis

**Zeitphase bis**: Aktualisieren Sie die Gruppierung der Zeilen im Raster, um Kostenschätzungen für Umsatzschätzungen widerzuspiegeln. Diese Steuerung gilt auch für das Schätzungsskript und das Verfolgungsraster.

![Zeitphase nach Schaltfläche](media/navigation0.png)

### <a name="add-column"></a>Spalte hinzufügen

**Spalte hinzufügen**: Ermöglicht dem Benutzer, die sichtbaren Spalten im Raster zu definieren Zu den Rastern im Formular **Projektplanung** können nur Standardspalten hinzugefügt werden.

![Schaltfläche „Spalte hinzufügen“](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]