---
title: Ein Projekt aktualisieren
description: Dieses Thema bietet Informationen zur Aktualisierung von Projekten in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131432"
---
# <a name="update-a-project"></a>Ein Projekt aktualisieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Im Folgenden finden Sie eine Zusammenfassung der Felder, die für ein Projekt aktualisiert werden können, nachdem es erstellt wurde, sowie alle anwendbaren Auswirkungen der Aktualisierungen.

## <a name="project-detail-fields"></a>Projektdetailfelder

- **Name**: Der Titel des Projekts
- **Beschreibung**: Eine Übersicht über das Projekt
- **Kunde**: Das Unternehmen, für das das Projekt bereitgestellt wird
- **Kalendervorlage**: Die Arbeitszeiten des Projekts Wenn das Feld geändert wird, wird der gesamte Zeitplan neu berechnet.
- **Währung**: Die Währung für das Projekt. Dieses Feld basiert standardmäßig auf der in der Vertragseinheit definierten Währung. Wenn die Vertragseinheit aktualisiert wird, wird auch das Feld aktualisiert.
- **Vertragseinheit**: Die Organisationseinheit, die die Unternehmensgruppe oder den Geschäftsbereich darstellt, die bzw. der hauptsächlich für den Verkaufsabschluss und die Verwaltung der Bereitstellung von Arbeit und Services an den Kunden verantwortlich ist. 
- **Projektmanager**: Das Projektteammitglied, das befugt ist, Zeiteinträge und Ausgaben zu überprüfen und zu genehmigen.

## <a name="estimate-fields"></a>Felder schätzen

- **Geschätztes Startdatum** : Das Datum, an dem das Projekt beginnt Wenn dieses Feld aktualisiert wird, werden alle Aufgaben im Projekt proportional zum Startdatum des neuen Startdatums verschoben.
- **Enddatum**: Das Datum, an dem das Projekt enden soll
- **Aufwand**: Der geschätzte Aufwand des Projekts Wenn dem Projekt Aufgaben hinzugefügt werden, kann dieses Feld nicht mehr bearbeitet werden.
- **Geschätzte Arbeitskosten**: Die geschätzten Arbeitskosten des Projekts Wenn dem Projekt Arbeitskosten hinzugefügt werden, kann dieses Feld nicht mehr bearbeitet werden.
- **Geschätzte Kosten**: Die geschätzten Kosten des Projekts Wenn dem Projekt Ausgaben hinzugefügt werden, kann dieses Feld nicht mehr bearbeitet werden.

## <a name="project-actual-fields"></a>Aktuelle Felder des Projekts
- **Tatsächlicher Start**: Das Datum, an dem das Projekt gestartet wurde
- **Tatsächliches Ende**: Wird aktualisiert, wenn ein Projekt abgeschlossen ist

## <a name="project-status-fields"></a>Felder für den Projektstatus

- **Gesamtprojektstatus**: Der vom Projektmanager bereitgestellte Gesamtzustand des Projekts
- **Kommentare**: Eine vom Projektmanager bereitgestellte Darstellung des aktuellen Zustands des Projekts

