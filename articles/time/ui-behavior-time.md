---
title: Verhalten der Zeiteintrags-Benutzeroberfläche
description: Dieses Thema bietet Informationen über das Verhalten der Benutzeroberfläche bei Zeiteinträgen.
author: stsporen
ms.date: 03/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: fd62fb1d8e0b2d859cb7da8b99cb725af587ff2f
ms.sourcegitcommit: 639ec8a41fda15dedfd6918702d33ea406999ba6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304300"
---
# <a name="time-entry-ui-behavior"></a>Verhalten der Zeiteintrags-Benutzeroberfläche

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


Das Raster **Wöchentlicher Zeiteintrag** ist ein benutzerdefiniertes Steuerelement mit den zwei Hauptbereichen **Dimensionen** und **Dauer**.

## <a name="keyboard-shortcuts"></a>Tastenkombinationen
| Aktion        | Verknüpfung                  |
|------------   |------------------------   |
| Neu           | ALT + UMSCHALT + N           |
| Zeile kopieren      | ALT + UMSCHALT + C           |
| Eintrag bearbeiten    | ALT + UMSCHALT + E           |
| Zeile bearbeiten      | ALT + UMSCHALT + STRG + E    |
| Eintrag öffnen    | ALT + UMSCHALT + O           |
| Senden        | ALT + UMSCHALT + S           |
| Rückruf        | ALT + UMSCHALT + R           |
| Entf        | ALT + UMSCHALT + D           |
| Woche kopieren     | ALT + UMSCHALT + W           |

## <a name="dimensions"></a>Dimensionen
Der Abschnitt **Dimensionen** zeigt die Dimensionen an, für die eine Zeit eingegeben werden kann. Die folgenden Dimensionen werden standardmäßig unterstützt:

  - Project
  - Projektaufgabe
  - Rolle
  - Art
  - Eintragsstatus

Im Abschnitt **Dimensionen** ist keine Inlinebearbeitung zulässig. Dieser Abschnitt wird durch eine Ansicht unterstützt, in der benutzerdefinierte Felder dem Raster für den wöchentlichen Zeiteintrag hinzugefügt werden können.

## <a name="duration"></a>Dauer
Im Abschnitt „Dauer” werden die Wochentage als Spaltenüberschriften angezeigt. In diesem Abschnitt ist die Inlinebearbeitung zulässig. Nachdem eine Zeiteintragungszeile mit den entsprechenden Dimensionen erstellt wurde, können Benutzer schnell inline die Zeit eingeben, die sie für die jeweiligen Dimensionen gebraucht haben.

## <a name="create-a-new-time-entry"></a>Erstellen eines neuen Zeiteintrags

1. Wählen Sie im Zeiteintragsraster die Option **Neu** aus. 
2. Wählen Sie im Dialogfeld **Schnellerfassung für Zeiteintrag** das Datum der Zeiteingabe aus.
3. Geben Sie Daten für die Dimensionen **Projekt**, **Projektaufgabe**, **Rolle** und **Dauer** ein. Geben Sie diese Informationen in Minuten, Stunden oder Tagen an, indem Sie **h**, **m** oder **t** zusammen mit der Zahl eingeben. 
4. Geben Sie eine Beschreibung für den Eintrag und Kommentare ein, die extern für den Zeiteintrag freigegeben werden können. 

Wenn Sie den Eintrag speichern, erscheinen die eingegebenen Werte im Abschnitt **Dimensionen**. Die Informationen, die im Feld **Dauer** eingegeben wurden, erscheinen an dem Datum, für das der Zeiteintrag erstellt wurde.

Suchfelder werden von Systemansichten unterstützt. Nachdem ein Benutzer beispielsweise ein Projekt eingegeben hat, wird das Feld **Projektaufgabe** standardmäßig auf die Ansicht **Kopieren** gesetzt. Wenn Sie Zeiteinträge für Aufgaben erstellen möchten, die keinem Benutzer zugewiesen sind, wählen Sie im Dialogfeld für die Suche die Option **Ansicht ändern** und dann die Ansicht **Alle aktiven Projektaufgaben** aus.

## <a name="edit-a-time-entry"></a>Bearbeiten eines Zeiteintrags 
Informationen aus einigen Feldern auf der Seite für den Zeiteintrag, wie **Beschreibung** und **Externe Kommentare**, werden nicht im Raster für den wöchentlichen Zeiteintrag angezeigt. Stattdessen erscheint eine kleine dreieckige Anzeige in den Zellen für die **Dauer**, die über zusätzliche Details verfügen. 

1. Um einen Zeiteintrag zu bearbeiten, wählen Sie die Zelle aus, die Sie im Zeiteintrag aktualisieren möchten.
2. Wählen Sie **Details bearbeiten** aus, um die Daten im Bereich **Zeiterfassungs-Hauptformular** zu aktualisieren. 

## <a name="copy-a-time-entry-row"></a>Kopieren einer Zeiteintragszeile
Nachdem die Zeile erstellt wurde, können Sie **Zeile kopieren** auswählen, um die gesamte Zeile in eine neue Zeile zu kopieren. Wenn eine Zeile auf diese Weise kopiert wird, werden Dimensionen und Dauern ebenfalls kopiert. Sie können auch **Zeile bearbeiten** auswählen, um Dimensionswerte und Dauern im Abschnitt **Dauer** zu aktualisieren.

## <a name="open-a-time-entry-behavior"></a>Zeiteintragsverhalten öffnen
Um eine optimale und schnelle Eingabe in den auffälligsten Feldern zu unterstützen, zeigt das Raster für den wöchentlichen Zeiteintrag eine Teilmenge der ausgewählten Dimensionen und Dauern an. Um sich alle Details eines einzelnen Zeiteintrags anzusehen, wählen Sie unter **Eintrag bearbeiten** die Option **Öffnen** aus.

## <a name="submit-a-time-entry"></a>Übermitteln eines Zeiteintrags
Sie können einen einzelnen Zeiteintrag oder eine Gruppe von Zeiteinträgen übermitteln, indem sie einen Zellenblock oder eine gesamte Zeiteintragszeile auswählen, und anschließend **Übermitteln** auswählen. Übermittelte Zeiteinträge werden auf der Seite **Genehmigung** als Einträge angezeigt, für die eine Genehmigung durch die genehmigende Person aussteht. Nachdem Zeiteinträge übermittelt wurden, können sie nicht mehr bearbeitet werden.

## <a name="recall-a-time-entry"></a>Zurückrufen eines Zeiteintrags
Sie können eingereichte Zeiteinträge zurückrufen. Sie können einen einzelnen Zeiteintrag, einen Block von Zeiteinträgen oder eine gesamte Zeile von Zeiteinträgen zurückrufen. Abgerufene Zeiteinträge können bearbeitet werden.

## <a name="time-entry-status"></a>Zeiteintragsstatus

- **Entwurf**: Neuen Zeiteinträgen wird automatisch der Status **Entwurf** zugewiesen. Nur Zeiteinträge mit dem Status **Entwurf** können gelöscht werden.
- **Übermittelt**: Wenn ein Zeiteintrag übermittelt wurde, wird der Status in **Übermittelt** aktualisiert. 
- **Genehmigt**: Wenn ein übermittelter Zeiteintrag genehmigt wurde, wird der Status auf **Genehmigt** aktualisiert. 
- **Zurückgegeben**: Wenn ein Zeiteintrag abgelehnt wurde, wird der Status in **Zurückgegeben** aktualisiert, und der Eintrag kann korrigiert und erneut übermittelt werden. 

## <a name="view-rejection-comments"></a>Anzeigen von Kommentaren zur Ablehnung
Wenn ein Zeiteintrag von einer genehmigenden Person abgelehnt wird, kann diese Person Kommentare zur Ablehnung angeben, um der Ressource den Grund für die Ablehnung zu erklären. Um sich die Kommentare für die Ablehnung zu einem Zeiteintrag anzusehen, wählen Sie **Eintrag öffnen** aus. Die Kommentare zur Ablehnung werden in einer Zeitskala angezeigt. Der Benutzer kann auf die Ablehnungskommentare antworten, bevor er den Eintrag erneut einreicht.

## <a name="copy-week"></a>Woche kopieren
Nachdem einige Zeiteinträge erstellt wurden, können Benutzer mehrere Zeiteinträge gleichzeitig erstellen.

1. Wählen Sie im Formular **Zeiteinträge** die Option **Woche kopieren** aus, um zusätzliche Zeiteinträge in großen Mengen zu erstellen. 
2. Verwenden Sie im Dialogfeld **Kopieren** im Abschnitt **Zeitraum von** die Felder **Startdatum** und **Enddatum**, um den Datumsbereich festzulegen, von dem Zeiteinträge kopiert werden sollen. 
3. Geben Sie im Abschnitt **Zeitraum bis** im Feld **Startdatum** das Datum ein, für das Zeiteinträge erstellt werden sollen. 
4. Klicken Sie auf **Kopieren**. Für das festgelegte Datum im **Zeitraum bis** wird eine Kopie der Zeiteinträge für den entsprechenden Wochentag im **Zeitraum von** erstellt. Beispielsweise wird der Zeiteintrag für Montag von letzter Woche in Montag dieser Woche kopiert, der als **Zeitraum bis** angegeben ist.

## <a name="import"></a>Import
Derselbe grundlegende Vorgang wird verwendet, um Elemente aus Buchungen, Arbeitsaufträgen und Austausch zu importieren. Sie können den Datumsbereich angeben, aus dem Buchungen import werden werden sollen und dann explizit die Buchungen auswählen, die als Entwurf-Zeiteinträge kopiert werden sollen. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
