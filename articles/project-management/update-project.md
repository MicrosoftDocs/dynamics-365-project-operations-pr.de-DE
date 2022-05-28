---
title: Ein Projekt erstellen und aktualisieren
description: Dieses Thema bietet Informationen zur Aktualisierung von Projekten in Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 07f96973a1341e65e648f126a931d72454334e9c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592507"
---
# <a name="create-and-update-a-project"></a>Ein Projekt erstellen und aktualisieren

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Im Folgenden finden Sie eine Zusammenfassung der Felder, die in einem Projekt aktualisiert werden können, nachdem es erstellt wurde. Dies schließt auch alle anwendbaren Auswirkungen ein, die auf diesen Updates basieren.

## <a name="project-detail-fields"></a>Projektdetailfelder

- **Name**: Der Titel des Projekts
- **Beschreibung**: Eine Übersicht über das Projekt
- **Kunde**: Das Unternehmen, für das das Projekt bereitgestellt wird
- **Kalendervorlage**: Die Arbeitszeiten des Projekts Der gesamte Zeitplan wird neu berechnet, wenn das Feld geändert wird.
- **Währung**: Die Währung für das Projekt. Der Standardwert für dieses Feld basiert auf der in der Vertragseinheit definierten Währung. Bei Aktualisierung der Vertragseinheit wird auch das Feld aktualisiert.
- **Vertragseinheit**: Die Organisationseinheit, die die Unternehmensgruppe oder den Geschäftsbereich darstellt, die bzw. der hauptsächlich für den Verkaufsabschluss und die Verwaltung der Bereitstellung von Arbeit und Services an den Kunden verantwortlich ist.  Wenn die Organisationseinheit des Projektmanagers nicht definiert ist, wird in diesem Feld standardmäßig der in den Projektparametern definierte Wert verwendet.
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
