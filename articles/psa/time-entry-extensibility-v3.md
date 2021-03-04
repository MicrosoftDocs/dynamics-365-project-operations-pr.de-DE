---
title: Wöchentlichen Zeiteintrag anpassen
description: Dieses Thema enthält Informationen darüber, wie Sie benutzerdefinierte Geschäftsregeln implementieren, die die Verfahrensweise einer Organisation unterstützen.
author: stsporen
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
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
ms.openlocfilehash: a34244884bc81da74ae3bf550bde6f982d04abd3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149632"
---
# <a name="customize-weekly-time-entry"></a>Wöchentlichen Zeiteintrag anpassen 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In Microsoft Dynamics 365 Project Service Automation Version 3.3 hat Microsoft ein modernes Raster eingeführt, mit dem Projektressourcen schnell mit einem Mal die Zeit für bis zu eine Woche eingeben können. Im neuen Raster für den wöchentlichen Zeiteintrag können Summen für Einträge nach Datum, Zeile oder Woche angezeigt werden. Ressourcen können Kopien von Zeiteinträgen innerhalb der Woche und auch Massenkopien von vorherigen Wochen erstellen. Systemanpasser können die Ansicht anpassen, indem sie Felder und Suchen für die anderen Entitäten hinzufügen und benutzerdefinierte Geschäftsregeln implementieren, um die Verfahrensweise ihrer Organisation zu unterstützen.

Der Zeiteintrag und das neue wöchentliche Zeitraster können über die Siteübersicht aufgerufen werden. Der nicht erweiterbare benutzerdefinierte Zeiteintrag, der in früheren PSA-Versionen vorhanden war, wurde durch das erweiterbare Raster für den wöchentlichen Zeiteintrag ersetzt. Außerdem wurde er durch eine alternative Funktion im schreibgeschützten Raster und im Kalender ersetzt. Aufgrund dieser Änderung können Benutzer die Zeit in wöchentlichen Beträgen eingeben.

## <a name="page-layout"></a>Seitenlayout
Das neue Raster für den wöchentlichen Zeiteintrag ist ein benutzerdefiniertes Steuerelement mit einer Symbolleiste und zwei Hauptbereichen, **Dimensionen** und **Dauer**. Die Symbolleiste enthält eine Schaltfläche, die nur für dieses benutzerdefinierte Steuerelement für das Zeiteintragsraster gilt. Im Gegensatz dazu gelten die Schaltflächen im Aktionsbereich oben auf der Seite auf die drei Arten von Steuerelementen, die für den Zeiteintrag unterstützt werden: das Steuerelement für den wöchentlichen Zeiteintrag, das schreibgeschützte Steuerelement und das Steuerelement für den Kalender.

### <a name="dimensions"></a>Dimensionen
Der Abschnitt **Dimensionen** zeigt, wie Spaltenüberschriften, alle Dimensionen, für die eine Zeit eingegeben werden kann. Die folgenden Dimensionen werden standardmäßig unterstützt:

- Projekt
- Projektaufgabe
- Rolle
- Typ
- Eintragsstatus

Im Abschnitt **Dimensionen** ist keine Inlinebearbeitung zulässig. Dieser Abschnitt wird durch eine Ansicht unterstützt, in der benutzerdefinierte Felder dem Raster für den wöchentlichen Zeiteintrag hinzugefügt werden können. Informationen dazu, wie benutzerdefinierte Felder hinzugefügt werden können, finden Sie im Abschnitt "Erweiterbarkeit" weiter unten in diesem Thema.

### <a name="duration"></a>Dauer
Im Abschnitt „Dauer” werden die Wochentage als Spaltenüberschriften angezeigt. In diesem Abschnitt ist die Inlinebearbeitung zulässig. Nachdem eine Zeiteintragungszeile erstellt wurde, die über entsprechende Dimensionen verfügt, können Benutzer schnell inline die Zeit eingeben, die sie für die jeweiligen Dimensionen gebraucht haben.

## <a name="create-a-new-time-entry"></a>Erstellen eines neuen Zeiteintrags
Um einen neuen Zeiteintrag im Raster für den Zeiteintrag zu erstellen, wählen Sie **Neu** aus. Das Dialogfeld **Schnellerfassung für Zeiteintrag** wird angezeigt. In diesem Dialogfeld können Benutzer das Zeiteintragungsdatum auswählen und dann Daten für die Dimensionen **Projekt**, **Projektaufgabe**, **Rolle** und **Dauer** in Minuten, Stunden oder Tagen angeben, indem sie **h**, **m** oder **d** zusammen mit der Zahl eingeben. Benutzer können auch eine Beschreibung und Kommentare eingeben, die extern für den Zeiteintrag freigegeben werden können. Wenn Benutzer ihre Änderungen speichern, erscheinen die Werte, die sie für die Dimensionen eingegeben haben, im Abschnitt **Dimensionen**. Informationen zur Dauer, die sie im Feld **Dauer** eingegeben haben, werden im Datum angezeigt, für das der Zeiteintrag erstellt wurde.

Suchfelder werden von Systemansichten unterstützt. Wenn ein Benutzer beispielsweise ein Projekt eingibt, wird das Feld **Projektaufgabe** standardmäßig auf die Ansicht **Kopieren** eingestellt. Wenn Sie Zeiteinträge für Aufgaben erstellen möchten, die keinem Benutzer zugewiesen sind, wählen Sie im Dialogfeld für die Suche die Option **Ansicht ändern** und dann die Ansicht **Alle aktiven Projektaufgaben** aus.

## <a name="edit-a-time-entry"></a>Bearbeiten eines Zeiteintrags
Informationen aus einigen Feldern auf der Seite für den Zeiteintrag, wie **Beschreibung** und **Externe Kommentare**, werden nicht im Raster für den wöchentlichen Zeiteintrag angezeigt. Stattdessen erscheint eine kleine dreieckige Anzeige in den Zellen für die Dauer, die über zusätzliche Details verfügen. Wählen Sie die Zelle und dann **Details bearbeiten** aus, um die Daten im Bereich **Schnellbearbeitung** anzuzeigen. Wenn Sie die Details für einen bestimmten Zeiteintrag bearbeiten oder aktualisieren möchten, der nicht zum Raster für den wöchentlichen Zeiteintrag gehört, müssen Benutzer den Bereich **Schnellbearbeitung** öffnen.

## <a name="copy-a-time-entry-row"></a>Kopieren einer Zeiteintragszeile
Nachdem die erste Zeiteintragszeile erstellt wurde, können Benutzer **Zeile kopieren** auswählen, um die gesamte Zeile in eine neue Zeile zu kopieren. Wenn eine Zeile auf diese Weise kopiert wird, werden Dimensionen und Dauern ebenfalls kopiert. Benutzer können auch **Zeile bearbeiten** auswählen, um Dimensionswerte und Dauern inline im Abschnitt **Dauer** zu aktualisieren.

## <a name="open-a-time-entry"></a>Öffnen eines Zeiteintrags
Um eine optimale und schnelle Eintragung in den auffälligsten Feldern zu unterstützen, zeigt das Raster für den wöchentlichen Zeiteintrag eine Teilmenge der ausgewählten Dimensionen und Dauern an. Um sich alle Details eines einzelnen Zeiteintrags anzusehen, wählen Sie unter **Eintrag bearbeiten** die Option **Öffnen** aus.

## <a name="submit-a-time-entry"></a>Übermitteln eines Zeiteintrags
Benutzer können einen einzelnen Zeiteintrag oder eine Gruppe von Zeiteinträgen übermitteln, indem sie einen Zellenblock oder eine gesamte Zeiteintragszeile auswählen, und anschließend **Übermitteln** auswählen. Übermittelte Zeiteinträge werden auf der Seite **Genehmigung** als Einträge angezeigt, für die eine Genehmigung durch die genehmigende Person aussteht. Nachdem Zeiteinträge übermittelt wurden, können sie nicht mehr bearbeitet werden.

## <a name="recall-a-time-entry"></a>Zurückrufen eines Zeiteintrags
Sie können eingereichte Zeiteinträge zurückrufen. Sie können einen einzelnen Zeiteintrag, einen Block von Zeiteinträgen oder eine gesamte Zeile von Zeiteinträgen zurückrufen. Zurückgerufene Zeiteinträge können von Ressourcen bearbeitet werden.

## <a name="time-entry-status"></a>Zeiteintragsstatus
Neuen Zeiteinträgen wird automatisch der Status **Entwurf** zugewiesen. Wenn ein Zeiteintrag übermittelt wurde, wird der Status auf **Übermittelt** aktualisiert. Wenn ein übermittelter Zeiteintrag genehmigt wurde, wird der Status auf **Genehmigt** aktualisiert. Wenn ein Zeiteintrag abgelehnt wurde, wird der Status auf **Zurückgegeben** aktualisiert, und der Eintrag kann korrigiert und erneut übermittelt werden. Nur Zeiteinträge mit dem Status **Entwurf** können gelöscht werden.

## <a name="view-rejection-comments"></a>Anzeigen von Kommentaren zur Ablehnung
Wenn ein Zeiteintrag von einer genehmigenden Person abgelehnt wurde, kann diese Person Kommentare zur Ablehnung angeben, um der Ressource den Grund für die Ablehnung zu erklären. Um sich die Kommentare für die Ablehnung zu einem Zeiteintrag anzusehen, wählen Sie **Eintrag öffnen** aus. Die Kommentare zur Ablehnung werden in einer Zeitskala angezeigt. In der Zeitskala kann die Ressource auf die Kommentare zur Ablehnung antworten, bevor sie den Eintrag erneut übermittelt.

## <a name="copy-week"></a>Kopieren einer Woche
Nachdem einige Zeiteinträge erstellt wurden, können Benutzer **Woche kopieren** auswählen, um eine Massenerstellung zusätzlicher Zeiteinträge vorzunehmen. Das Dialogfeld **Kopieren** wird angezeigt. Verwenden Sie im Abschnitt **Zeitraum von** die Felder **Startdatum** und **Enddatum**, um den Datumsbereich festzulegen, von dem Zeiteinträge kopiert werden sollen. Geben Sie im Abschnitt **Zeitraum bis** im Feld **Startdatum** das Datum ein, für das Zeiteinträge erstellt werden sollen. Wählen Sie dann **Kopieren** aus. Für das festgelegte Datum im Zeitraum „bis” wird eine Kopie der Zeiteinträge für den entsprechenden Wochentag im Zeitraum „von” erstellt. Beispielsweise wird der Zeiteintrag für Montag von letzter Woche in Montag dieser Woche kopiert, der als Zeitraum „bis” angegeben ist.

## <a name="import"></a>Importieren
Derselbe grundlegende Vorgang wird verwendet, um Elemente aus Buchungen, Arbeitsaufträgen und Austausch zu importieren. Benutzer können den Datumsbereich angeben, aus dem Buchungen importiert werden. Sie müssen Buchungen dann explizit auswählen, die in Entwurf-Zeiteintragungen kopiert werden sollen. In der vorherigen Version erschienen vorgeschlagene Zeiteinträge im Raster und im Kalender und gingen verloren, wenn die Sitzung aktualisiert wurde.

## <a name="extensibility"></a>-Erweiterbarkeit
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Hinzufügen benutzerdefinierter Felder, die Suchen für andere Entitäten aufweisen
Es gibt drei Hauptschritte zum Hinzufügen eines benutzerdefinierten Felds zum Raster für den wöchentlichen Zeiteintrag.

1.  Fügen Sie das benutzerdefinierte Feld dem Schnellerfassungs-Dialogfeld hinzu.
2.  Konfigurieren Sie das Raster, um das benutzerdefinierte Feld anzuzeigen.
3.  Fügen Sie das benutzerdefinierte Feld entweder dem Aufgabenfluss „Zeile bearbeiten” oder dem Aufgabenfluss „Zelle bearbeiten” hinzu.

Sie müssen auch sicherstellen, dass das neue Feld über die erforderlichen Prüfungen im Aufgabenfluss „Zeile bearbeiten” oder „Zelle bearbeiten” verfügt. Im Rahmen dieses Schritts müssen Sie das Feld basierend auf dem Status des Zeiteintrags sperren.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Hinzufügen des benutzerdefinierten Felds zum Schnellerfassungs-Dialogfeld
Sie müssen das benutzerdefinierte Feld dem Dialogfeld „Schnellerfassung für Zeiteintrag” hinzufügen. damit Benutzer einen Wert für ihn eingeben können, wenn sie Zeiteinträge über die Schaltfläche **Neu** hinzufügen.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurieren des Rasters, um das benutzerdefinierte Feld anzuzeigen
Es gibt zwei Möglichkeiten zum Hinzufügen eines benutzerdefinierten Felds zum Raster für den wöchentlichen Zeiteintrag. Die ersten Option besteht darin, die Ansicht **Meine wöchentlichen Zeiteinträge** anzupassen und ihr das benutzerdefinierte Feld hinzuzufügen. Sie können die Position und Größe des benutzerdefinierten Felds im Raster auswählen, indem Sie diese Eigenschaften in der Ansicht bearbeiten.

Die zweite Option besteht darin, eine neue benutzerdefinierte Zeiteintragsansicht zu erstellen und diese als Standardansicht festzulegen. Diese Ansicht sollte die Felder **Beschreibung** und **Externe Kommentare** enthalten, zusätzlich zu den Spalten, die Sie im Raster haben möchten. Sie können die Position, Größe und standardmäßige Sortierreihenfolge des Rasters auswählen, indem Sie diese Eigenschaften in der Ansicht bearbeiten. Anschließend konfigurieren Sie das benutzerdefinierte Steuerelement für diese Ansicht, damit es zu einem Steuerelement **Zeiteintragsraster** wird. Fügen Sie dieses Steuerelement der Ansicht hinzu, und wählen Sie es für Internet, Smartphone und Tablet aus. Konfigurieren Sie dann die Parameter für das Raster für den wöchentlichen Zeiteintrag. Legen Sie das Feld **Startdatum** auf **msdyn_date**, das Feld **Dauer** auf **msdyn_duration** und das Feld **Status** auf **msdyn_entrystatus** fest. Für die standardmäßige Ansicht wird das Feld **Schreibgeschützte Statusliste** auf **192350002,192350003,192350004**, das Feld **Aufgabenflow zur Zeilenbearbeitung** auf **msdyn_timeentryrowedit** und das Feld **Aufgabenflow zur Zellenbearbeitung** auf **msdyn_timeentryedit** festgelegt. Sie können diese Felder anpassen, um den schreibgeschützten Status hinzuzufügen oder zu entfernen, oder eine andere aufgabenbasierte Umgebung (task-based experience, TBX) für die Zeilen- oder Zellenbearbeitung zu verwenden. Diese Felder sollten an einen statischen Wert gebunden werden.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Hinzufügen des benutzerdefinierten Felds zum entsprechenden Bearbeitungs-Aufgabenfluss
Die TBX-Seiten, die zum Bearbeiten verwendet werden, sind unter **Prozesse** zu finden. Die Standardseiten sind **Project Service – Bearbeiten der Zeile mit Zeiteintrag** und **Project Service – Bearbeiten von Zeiteinträgen**. Sie können entweder diese Standardseiten bearbeiten oder neue benutzerdefinierte TBX-Seiten erstellen.

> [!NOTE] 
> Durch beide Optionen werden einige der standardmäßigen Filterungen bei den Entitäten **Projekt** und **Projektaufgabe** entfernt, sodass alle Suchansichten für die Entitäten sichtbar werden. Standardmäßig sind nur die relevanten Suchansichten sichtbar.

Sie müssen den entsprechenden Aufgabenfluss für das benutzerdefinierte Feld festlegen. Wenn Sie das Feld dem Raster hinzugefügt haben, sollte es höchstwahrscheinlich in den Aufgabenfluss „Zeile bearbeiten” verschoben werden, der für Felder verwendet wird, die auf die gesamte Zeile mit Zeiteinträgen angewendet werden. Wenn das benutzerdefinierte Feld jeden Tag einen eindeutigen Wert hat, wie ein benutzerdefiniertes Feld für **Endzeit**, sollte es in den Aufgabenfluss „Zelle bearbeiten” verschoben werden.

Um einem Aufgabenfluss ein benutzerdefiniertes Feld hinzuzufügen, ziehen Sie ein Element **Feld** an die geeignete Position auf der Seite, und legen Sie dann die Eigenschaften fest. Legen Sie die Eigenschaft **Quelle** auf **Zeiteintrag** und dann die Eigenschaft **Datenfeld** für das benutzerdefinierte Feld fest. Die Eigenschaft **Feld** gibt den Anzeigenamen auf der TBX-Seite an. Wählen Sie **Anwenden** aus, um die Änderungen an dem Feld zu speichern. Wählen Sie dann **Aktualisieren** aus, um die Änderungen an der Seite zu speichern.

Um stattdessen eine neue benutzerdefinierte TBX-Seite zu verwenden, erstellen Sie einen neuen Prozess. Legen Sie die Kategorie auf **Geschäftsprozessflow**, die Entität auf **Zeiteintrag** und den Geschäftsprozesstyp auf **Prozess als Aufgabenflow ausführen** fest. Unter **Eigenschaften** sollte die Eigenschaft **Seitenname** auf den Anzeigenamen für die Seite festgelegt werden. Fügen Sie der TBX-Seite alle relevanten Felder hinzu. Speichern und aktivieren Sie den Prozess, und aktualisieren Sie dann die Eigenschaft für das benutzerdefinierte Steuerelement für den relevanten Aufgabenfluss auf den Wert **Name** im Prozess.

### <a name="add-new-option-set-values"></a>Hinzufügen neuer Optionssatzwerte
Um Optionssatzwerte einem standardmäßigen Feld hinzuzufügen, öffnen Sie die Bearbeitungsseite des Felds und wählen Sie dann unter **Typ** die Option **Bearbeiten** neben dem Optionssatz aus. Fügen Sie dann eine neue Option hinzu, die eine benutzerdefinierte Beschriftung und Farbe hat. Wenn Sie einen neuen Zeiteintragsstatus hinzufügen möchten, wird das standardmäßige Feld **Eintragsstatus** und nicht **Status** genannt.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Festlegen eines neuen Zeiteintragsstatus als „schreibgeschützt”
Wenn Sie einen neuen Zeiteintragsstatus als „schreibgeschützt” festlegen möchten, fügen Sie den neuen Zeiteintragswert (die Zahl, nicht die Beschriftung) der Eigenschaft **Schreibgeschützte Statusliste** hinzu. Der bearbeitbare Teil des Zeiteintragsrasters wird für Zeilen mit dem Status „Neu” gesperrt.
Fügen Sie dann Geschäftsregeln hinzu, um alle Felder auf den TBX-Seiten **Bearbeiten der Zeile mit Zeiteintrag** und **Bearbeiten von Zeiteinträgen** zu sperren. Sie können auf die Geschäftsregeln für diese Seiten zugreifen, indem Sie den Editor für den Geschäftsprozessfluss für die Seite öffnen und dann **Geschäftsregeln** auswählen. Sie können den neuen Status der Bedingung in vorhandenen Geschäftsregeln hinzufügen, oder Sie können eine neue Geschäftsregel für den neuen Status hinzufügen.

### <a name="add-custom-validation-rules"></a>Hinzufügen benutzerdefinierter Prüfungsregeln
Es gibt zwei Arten von Prüfungsregeln, die Sie für das Raster für den wöchentlichen Zeiteintrag hinzufügen können: •   Clientseitige Geschäftsregeln, die in Schnellerfassungs-Dialogfeldern und auf TBX-Seiten verwendet werden können •   Serverseitige Plug-In-Prüfungen, die auf alle Zeiteintragsaktualisierungen angewendet werden können

#### <a name="business-rules"></a>Geschäftsregeln
Mithilfe von Geschäftsregeln können Sie Felder sperren und entsperren, Standardwerte in Felder eingeben und Prüfungen festlegen, die Informationen nur aus dem aktuellen Zeiteintrags-Datensatz erfordern. Sie können auf die Geschäftsregeln für eine TBX-Seite zugreifen, indem Sie den Editor für den Geschäftsprozessfluss für die Seite öffnen und dann **Geschäftsregeln** auswählen. Sie können dann die vorhandenen Geschäftsregeln bearbeiten oder eine neue Geschäftsregel hinzufügen. Wenn Sie die Prüfungen noch weiter anpassen möchten, können Sie JavaScript mithilfe einer Geschäftsregel ausführen.

#### <a name="plug-in-validations"></a>Plug-In-Prüfungen
Sie sollten Plug-In-Prüfungen für alle Prüfungen, bei denen mehr Kontext erforderlich ist, als in einem einzelnen Zeiteintrags-Datensatz vorhanden ist, oder für alle Prüfungen verwenden, die Sie für Inline-Aktualisierungen im Raster ausführen möchten. Um die Prüfung abzuschließen, erstellen Sie ein benutzerdefiniertes Plug-In in der Entität **Zeiteintrag**.

> [!IMPORTANT] 
> Derzeit verhindert ein bekannter Issue auf den TBX-Seiten, dass Benutzer Informationen korrigieren und „Fertig” auswählen können, wenn eine Aktualisierung eine Plug-In-Prüfung nicht besteht. Als Problemumgehung können Sie Geschäftsregelprüfungen einrichten, um diese Situation so gut wie möglich zu verhindern.
