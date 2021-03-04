---
title: Zeiteinträge verlängern
description: Dieses Thema enthält Informationen darüber, wie Entwickler die Zeiteintragssteuerung erweitern können.
author: stsporen
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d9c14f0550d4429ac794607a3fb61717566207e4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124637"
---
# <a name="extending-time-entries"></a>Zeiteinträge verlängern

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations enthält ein erweiterbares benutzerdefiniertes Steuerelement für den Zeiteintrag. Dieses Steuerelement bietet die folgenden neuen Funktionen:

- Die Zeit horizontal über eine Woche eingeben
- Summen nach Tag, Zeile oder Woche
- Zeilen oder Wochen kopieren
- Zeiteintrag über HH:mm oder HH.hh (wird automatisch in HH.hh konvertiert)
- Import aus Arbeitsaufträgen, Buchungen oder Terminen

Das Verlängern von Zeiteinträgen ist in zwei Bereichen möglich:
- [Hinzufügen benutzerdefinierter Zeiteinträgen für Ihren eigenen Gebrauch](#add)
- [Wöchentliches Zeiteintragssteuerelement anpassen](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Benutzerdefinierte Zeiteinträge für Ihren eigenen Gebrauch hinzufügen

Zeiteinträge sind eine Kernentität, die in mehreren Szenarien verwendet wird. In der April-Welle 1 2020 wurde die TESA-Kernlösung eingeführt. TESA stellt die Entität **Einstellungen** und eine neue Sicherheitsrolle **Zeiteintragsbenutzer** bereit. Die neuen Felder **msdyn_start** und **msdyn_end**, die eine direkte Beziehung zu **msdyn_duration** haben, wurden ebenfalls eingeführt. Die neue Entität, Sicherheitsrolle und die Felder ermöglichen einen einheitlicheren Zeitansatz für mehrere Produkte.


### <a name="time-source-entity"></a>Zeitquellentität
| Feld | Beschreibung des Dataflows | 
|-------|------------|
| Name des Dataflows  | Der Name der Zeitquelleneingabe, der bei der Erstellung von Zeiteinträgen als Auswahlwert verwendet wird. |
| Standardzeitquelle [Zeitquelle: isdefault] | Standardmäßig darf nur eine Zeitquelle als Standard markiert sein. Hiermit können Eingaben standardmäßig auf eine Zeitquelle zurückgesetzt werden, wenn keine angegeben ist. |
|Zeitquellentyp [Zeitquelle: sourcetype] | Der Quelltyp ist eine Option (Zeiteintragsquellentyp), mit der die Zeitquelle einer App zugeordnet werden kann. Microsoft reserviert Werte, die größer als 190.000.000 sind.|


### <a name="time-entries-and-the-time-source-entity"></a>Zeiteinträge und die Zeitquellenentität
Jeder Zeiteintrag ist einem Zeitquellendatensatz zugeordnet. Dieser Datensatz legt fest, wie und welche Anwendungen der Zeiteintrag verarbeiten sollen.

Zeiteinträge sind immer ein zusammenhängender Zeitblock, mit dem Start, Ende und Dauer verknüpft sind.

Die Logik aktualisiert den Zeiteintragsdatensatz in den folgenden Situationen automatisch:

- Wenn zwei der drei folgenden Felder angegeben sind, wird das dritte automatisch berechnet: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Die Felder **msdyn_start** und **msdyn_end** sind zeitzonenbewusst.
- Zeiteinträge, die nur die Angabe **msdyn_date** und **msdyn_duration** erstellt wurden, beginnen um Mitternacht. Die Felder **msdyn_start** und **msdyn_end** werden entsprechend aktualisiert.

#### <a name="time-entry-types"></a>Zeiteintragstyp

Zeiteintragsdatensätze haben einen zugeordneten Typ, der das Verhalten im Übermittlungsfluss für die zugeordnete Anwendung definiert.

|Etikett | Wert|
|-----|-----|
|In Pause   |192,355,000|
|Reisen | 192,355,001|
|Überstunden   | 192,354,320|
|Arbeiten   | 192,350,000|
|Abwesenheit    | 192,350,001|
|Urlaub   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Wöchentliches Zeiteintragssteuerelement anpassen
Entwickler können anderen Entitäten zusätzliche Felder und Suchvorgänge hinzufügen und benutzerdefinierte Geschäftsregeln implementieren, um ihre Geschäftsszenarien zu unterstützen.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Hinzufügen benutzerdefinierter Felder mit Suchen für andere Entitäten
Es gibt drei Hauptschritte zum Hinzufügen eines benutzerdefinierten Felds zum Raster für den wöchentlichen Zeiteintrag.

1. Fügen Sie das benutzerdefinierte Feld dem Schnellerfassungs-Dialogfeld hinzu.
2. Konfigurieren Sie das Raster, um das benutzerdefinierte Feld anzuzeigen.
3. Fügen Sie das benutzerdefinierte Feld dem Aufgabenfluss „Zeile bearbeiten“ oder dem Aufgabenfluss „Zelle bearbeiten“ hinzu.

Stellen Sie sicher, dass das neue Feld über die erforderlichen Prüfungen im Aufgabenfluss „Zeile bearbeiten“ oder „Zelle bearbeiten“ verfügt. Sperren Sie im Rahmen dieses Schritts das Feld basierend auf dem Status des Zeiteintrags.

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Hinzufügen des benutzerdefinierten Felds zum Schnellerfassungs-Dialogfeld
Fügen Sie das benutzerdefinierte Feld dem Dialogfeld **Schnellerfassung für Zeiteintrag** hinzu. Wenn Zeiteinträge anschließend hinzugefügt werden, kann ein Wert durch Auswahl von **Neu** eingegeben werden.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurieren des Rasters, um das benutzerdefinierte Feld anzuzeigen
Es gibt zwei Möglichkeiten zum Hinzufügen eines benutzerdefinierten Felds zum Raster für den wöchentlichen Zeiteintrag:

  - Anpassen einer Ansicht und Hinzufügen eines benutzerdefinierten Felds
  - Erstellen eines standardmäßigen benutzerdefinierten Zeiteintrags 


#### <a name="customize-a-view-and-add-a-custom-field"></a>Anpassen einer Ansicht und Hinzufügen eines benutzerdefinierten Felds

Passen Sie die Ansicht **Meine wöchentlichen Zeiteinträge** an, und fügen Sie ihr das benutzerdefinierte Feld hinzu. Sie können die Position und Größe des benutzerdefinierten Felds im Raster auswählen, indem Sie die Eigenschaften in der Ansicht bearbeiten.

#### <a name="create-a-new-default-custom-time-entry"></a>Erstellen eines standardmäßigen benutzerdefinierten Zeiteintrags

Diese Ansicht sollte die Felder **Beschreibung** und **Externe Kommentare** enthalten, zusätzlich zu den Spalten, die Sie im Raster haben möchten. 

1. Wählen Sie die Position, Größe und standardmäßige Sortierreihenfolge des Rasters aus, indem Sie diese Eigenschaften in der Ansicht bearbeiten. 
2. Konfigurieren Sie das benutzerdefinierte Steuerelement für diese Ansicht, damit es zu einem Steuerelement **Zeiteintragsraster** wird. 
3. Fügen Sie dieses Steuerelement der Ansicht hinzu, und wählen Sie es für Internet, Smartphone und Tablet aus. 
4. Konfigurieren Sie die Parameter für das Raster für den wöchentlichen Zeiteintrag. 
5. Legen Sie das Feld **Startdatum** auf **msdyn_date**, das Feld **Dauer** auf **msdyn_duration** und das Feld **Status** auf **msdyn_entrystatus** fest. 
6. Für die Standardansicht wird das Feld **Schreibgeschützte Statusliste** auf **192350002,192350003,192350004** festgelegt. Das Feld **Aufgabenflow zur Zeilenbearbeitung** ist auf **msdyn_timeentryrowedit** festgelegt. Das Feld **Aufgabenflow zur Zellenbearbeitung** ist auf **msdyn_timeentryedit** festgelegt. 
7. Sie können diese Felder anpassen, um den schreibgeschützten Status hinzuzufügen oder zu entfernen, oder eine andere aufgabenbasierte Umgebung (task-based experience, TBX) für die Zeilen- oder Zellenbearbeitung zu verwenden. Diese Felder werden nun an einen statischen Wert gebunden.


> [!NOTE] 
> Durch beide Optionen werden einige der standardmäßigen Filterungen bei den Entitäten **Projekt** und **Projektaufgabe** entfernt, sodass alle Suchansichten für die Entitäten sichtbar werden. Standardmäßig sind nur die relevanten Suchansichten sichtbar.

Legen Sie den entsprechenden Aufgabenfluss für das benutzerdefinierte Feld fest. Wenn Sie das Feld dem Raster hinzugefügt haben, sollte es höchstwahrscheinlich in den Aufgabenflow „Zeile bearbeiten“ verschoben werden, der für Felder verwendet wird, die auf die gesamte Zeile mit Zeiteinträgen angewendet werden. Wenn das benutzerdefinierte Feld jeden Tag einen eindeutigen Wert hat, wie ein benutzerdefiniertes Feld für **Endzeit**, sollte es in den Aufgabenfluss „Zelle bearbeiten” verschoben werden.

Um einem Aufgabenfluss ein benutzerdefiniertes Feld hinzuzufügen, ziehen Sie ein Element **Feld** an die geeignete Position auf der Seite, und legen Sie dann die Feldeigenschaften fest. Legen Sie die Eigenschaft **Quelle** auf **Zeiteintrag** und dann die Eigenschaft **Datenfeld** für das benutzerdefinierte Feld fest. Die Eigenschaft **Feld** gibt den Anzeigenamen auf der TBX-Seite an. Wählen Sie **Anwenden**, um Ihre Änderungen im Feld zu speichern, und wählen Sie dann **Aktualisieren**, um Ihre Änderungen an der Seite zu speichern.

Um stattdessen eine neue benutzerdefinierte TBX-Seite zu verwenden, erstellen Sie einen neuen Prozess. Legen Sie die Kategorie auf **Geschäftsprozessflow**, die Entität auf **Zeiteintrag** und den Geschäftsprozesstyp auf **Prozess als Aufgabenflow ausführen** fest. Unter **Eigenschaften** sollte die Eigenschaft **Seitenname** auf den Anzeigenamen für die Seite festgelegt werden. Fügen Sie der TBX-Seite alle relevanten Felder hinzu. Speichern und aktivieren Sie den Prozess. Aktualisieren Sie dann die Eigenschaft für das benutzerdefinierte Steuerelement für den relevanten Aufgabenflow auf den Wert **Name** im Prozess.

### <a name="add-new-option-set-values"></a>Hinzufügen neuer Optionssatzwerte
Um Optionssatzwerte einem standardmäßigen Feld hinzuzufügen, öffnen Sie die Bearbeitungsseite des Felds und wählen Sie unter **Typ** die Option **Bearbeiten** neben dem Optionssatz aus. Fügen Sie eine neue Option hinzu, die eine benutzerdefinierte Beschriftung und Farbe hat. Wenn Sie einen neuen Zeiteintragsstatus hinzufügen möchten, wird das standardmäßige Feld **Eintragsstatus** und nicht **Status** genannt.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Festlegen eines neuen Zeiteintragsstatus als „schreibgeschützt”
Wenn Sie einen neuen Zeiteintragsstatus als „schreibgeschützt“ festlegen möchten, fügen Sie den neuen Zeiteintragswert der Eigenschaft **Schreibgeschützte Statusliste** hinzu. Der bearbeitbare Teil des Zeiteintragsrasters wird für Zeilen mit dem Status „Neu” gesperrt.
Fügen Sie dann Geschäftsregeln hinzu, um alle Felder auf den TBX-Seiten **Bearbeiten der Zeile mit Zeiteintrag** und **Bearbeiten von Zeiteinträgen** zu sperren. Sie können auf die Geschäftsregeln für diese Seiten zugreifen, indem Sie den Editor für den Geschäftsprozessfluss für die Seite öffnen und dann **Geschäftsregeln** auswählen. Sie können den neuen Status der Bedingung in vorhandenen Geschäftsregeln hinzufügen, oder Sie können eine neue Geschäftsregel für den neuen Status hinzufügen.

### <a name="add-custom-validation-rules"></a>Hinzufügen benutzerdefinierter Prüfungsregeln
Es gibt zwei Arten von Validierungsregeln, die Sie für das wöchentliche Zeiteintragsraster hinzufügen können:

- Clientseitige Geschäftsregeln, die in Dialogfeldern zum schnellen Erstellen und auf TBX-Seiten funktionieren.
- Serverseitige Plug-In-Überprüfungen, die für alle Aktualisierungen von Zeiteinträgen gelten.

#### <a name="business-rules"></a>Geschäftsregeln
Mithilfe von Geschäftsregeln können Sie Felder sperren und entsperren, Standardwerte in Felder eingeben und Prüfungen festlegen, die Informationen nur aus dem aktuellen Zeiteintrags-Datensatz erfordern. Sie können auf die Geschäftsregeln für eine TBX-Seite zugreifen, indem Sie den Editor für den Geschäftsprozessfluss für die Seite öffnen und dann **Geschäftsregeln** auswählen. Sie können dann die vorhandenen Geschäftsregeln bearbeiten oder eine neue Geschäftsregel hinzufügen. Wenn Sie die Prüfungen noch weiter anpassen möchten, können Sie JavaScript mithilfe einer Geschäftsregel ausführen.

#### <a name="plug-in-validations"></a>Plug-In-Prüfungen
Verwenden Sie Plug-In-Prüfungen für alle Prüfungen, bei denen mehr Kontext erforderlich ist, als in einem einzelnen Zeiteintrags-Datensatz vorhanden ist, oder für alle Prüfungen, die Sie für Inline-Aktualisierungen im Raster ausführen möchten. Um die Prüfung abzuschließen, erstellen Sie ein benutzerdefiniertes Plug-In in der Entität **Zeiteintrag**.

### <a name="copying-time-entries"></a>Kopieren von Zeiteinträgen
Verwenden Sie die Ansicht **Zeiteintragsspalten kopieren**, um die Liste der Felder zu definieren, die während der Zeiteingabe kopiert werden sollen. **Datum** und **Dauer** sind Pflichtfelder und sollten nicht aus der Ansicht entfernt werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]