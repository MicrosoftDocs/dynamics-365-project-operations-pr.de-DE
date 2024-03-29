---
title: Zeiteinträge erstellen
description: In diesem Artikel erfahren Sie, wie Sie Zeiteinträge erstellen.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: 1b707ccb970365ddbac75646da902733e2976d48
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930777"
---
# <a name="create-time-entries"></a>Zeiteinträge erstellen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In früheren Versionen von Dynamics 365 Project Service Automation wurden Zeiteintragungen wöchentlich eingegeben. In Version 3 von Project Service Automation werden Zeiteinträge täglich eingegeben. Nachdem einige Zeiteinträge erstellt wurden, können Sie allerdings Massenerstellungen oder -kopiervorgänge vornehmen.

## <a name="create-a-time-entry"></a>Einen Zeiteintrag erstellen

Führen Sie die folgenden Schritte aus, um einen Zeiteintrag zu erstellen.

1. Wählen Sie auf der Seite **Zeiteinträge** die Option **Neu** aus.
2. Geben Sie im Dialogfeld **Schnellerfassung: Zeiteintrag** die Dauer des Zeiteintrags in Minuten, Stunden oder Tagen ein. Die Dauer muss im folgenden Format eingegeben werden: *x* Minuten, *x* Stunden oder *x* Tage. Stunden und Tagen können auch als Dezimalwerte eingegeben werden, z. B. *x.x* Stunden oder *x.x* Tage.
3. Wählen Sie den Typ des Zeiteintrags und das Projekt aus, für das Sie den Zeiteintrag vornehmen.
4. Suchen Sie im Feld **Projektaufgabe** die Aufgabe für diesen Zeiteintrag.

    > [!NOTE]
    > Wenn Sie einen Zeiteintrag für eine Aufgabe erstellen, die keinem Benutzer zugewiesen ist, wählen Sie im Feld **Projektaufgabe** die Schaltfläche **Suchen** aus, wählen Sie **Ansicht ändern** aus, und wählen Sie dann **Alle aktiven Projektaufgaben** aus, um alle Aufgaben aufzuführen.

5. Geben Sie eine Beschreibung ein, wenn eine Beschreibung erforderlich ist, und wählen Sie dann **Speichern und schließen** aus.

Nachdem der Zeiteintrag erstellt und gespeichert ist, können Sie ihn im Zeiteintragsraster bearbeiten. Das Zeiteintragsraster unterstützt zwei Formate:

- Sie können Zeiteinträge im Format **hh:mm** eingeben. Dieses Format wird dann in Stunden und Bruchteile konvertiert.
- Sie können Stunden und Bruchteile direkt eingeben.

Beachten Sie, dass Bruchteile einer Stunde keine Minuten sind. Daher stellen 1,5 Stunden 1 Stunde und 30 Minuten dar. Dieselbe Regel gilt für Bruchteile eines Tags. Ein Tag besteht aus 24 Stunden, und 0,5 Tage stehen für 12 Stunden.

## <a name="bulk-create-time-entries"></a>Massenerstellung von Zeiteinträgen

Nachdem einige Zeiteinträge erstellt wurden, können Sie diese kopieren, um eine Massenerstellung zusätzlicher Zeiteinträge vorzunehmen.

1. Wählen Sie auf der Seite **Zeiteinträge** die Option **Woche kopieren** aus.
2. In der Feldgruppe **Zeitraum von** in den Feldern **Startdatum** und **Enddatum** definieren Sie den Datumsbereich, von dem Zeiteinträge kopiert werden sollen.
3. In der Feldgruppe **Zeitraum bis** im Feld **Startdatum** geben Sie das Datum ein, für das Zeiteinträge erstellt werden sollen.
4. Wählen Sie **Kopieren** aus, um eine Kopie für die Zeiteinträge zu erstellen, die dem Wochentag entsprechen, der in der Feldgruppe **Zeitraum bis** angegeben ist. Beispielsweise wird der Zeiteintrag für Montag letzter Woche zu Montag dieser Woche kopiert, der in der Feldgruppe **Zeitraum bis** angegeben ist.

## <a name="import-data-for-time-entries"></a>Daten für Zeiteinträge importieren

Sie können Daten aus Projektbuchungen und Arbeitsaufträgen importieren. Wenn Sie Daten importieren, können Sie den Datumsbereich der Buchungen angeben, die importiert werden sollen und dann explizit die Buchungen auswählen, die als **Entwurf**-Zeiteinträge erstellt werden sollen.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Funktionen zum Gruppieren nach, Sortieren, Suchen und Filtern

Sie können Zeiteinträge nach den Dimensionen gruppieren und filtern, die in den Spalten angegeben sind. Wählen Sie im Feld **Gruppieren nach** die Dimension aus, mithilfe der Zeiteinträge gefiltert werden sollen. Sie können auch die Zeiteintragdatensätze in aufsteigender oder absteigender Reihenfolge sortieren, indem Sie den Sortierpfeil in den Spaltenüberschriften verwenden. Zudem können Sie durch Auswahl der Schaltfläche **Filtern** in den Spaltenüberschriften Einträge ein- oder ausblenden. Dann können Sie im Feld **Suchen** den Text eingeben, der für die Suche von Zeiteinträgen anhand von Projektname, Projektaufgabe, Zeiteintrag oder Ressource verwendet werden soll.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
