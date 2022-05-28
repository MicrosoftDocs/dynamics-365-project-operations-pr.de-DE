---
title: Zeiteinträge verlängern
description: Dieses Thema enthält Informationen darüber, wie Entwickler die Zeiteintragssteuerung erweitern können.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582985"
---
# <a name="extending-time-entries"></a>Zeiteinträge verlängern

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations enthält ein benutzerdefinierbares Steuerelement für die erweiterbare Zeiteingabe. Dieses Steuerelement bietet die folgenden neuen Funktionen:

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
Jeder Zeiteintrag ist einem Zeitquellendatensatz zugeordnet. Dieser Datensatz legt fest, welche Anwendungen den Zeiteintrag wie verarbeiten sollen.

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

1. Fügen Sie benutzerdefinierte Feld dem **Schnellerfassung**-Dialogfeld hinzu.
2. Konfigurieren Sie das Raster, um das benutzerdefinierte Feld anzuzeigen.
3. Fügen Sie das benutzerdefinierte Feld wie erforderlich zu der Seite **Zeile bearbeiten** oder **Zeiteintrag bearbeiten**.

Stellen Sie sicher, dass das neue Feld auf der Seite **Bearbeiten von Zeilen** oder **Bearbeiten von Zeiteinträgen** über die erforderlichen Validierungen verfügt. Im Rahmen dieser Aufgabe müssen Sie das Feld basierend auf dem Status des Zeiteintrags sperren.

Wenn Sie ein benutzerdefiniertes Feld zum **Zeiteintrag**-Raster hinzufügen und dann Zeiteinträge direkt im Raster erstellen, wird das benutzerdefinierte Feld für diese Einträge automatisch so festgelegt, dass es mit der Zeile übereinstimmt. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Das benutzerdefinierte Feld dem Schnellerfassungs-Dialogfeld hinzufügen
Fügen Sie das benutzerdefinierte Feld dem Dialogfeld **Schnellerfassung: Zeiteintrag erstellen** hinzu. Benutzer können dann einen Wert eingeben, wenn sie Zeiteinträgen hinzufügen, indem sie **Neu** auswählen.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurieren des Rasters, um das benutzerdefinierte Feld anzuzeigen
Es gibt zwei Möglichkeiten zum Hinzufügen eines benutzerdefinierten Felds zum Raster **Wöchentlicher Zeiteintrag**.

- Passen Sie die Ansicht **Meine wöchentlichen Zeiteinträge** an, und fügen Sie ihr das benutzerdefinierte Feld hinzu. Sie können die Position und Größe des benutzerdefinierten Felds im Raster angeben, indem Sie die Eigenschaften in der Ansicht bearbeiten.
- Erstellen Sie eine neue benutzerdefinierte Zeiteintragsansicht, und legen Sie diese als Standardansicht fest. Diese Ansicht sollte die Felder **Beschreibung** und **Externe Kommentare** enthalten, zusätzlich zu den Spalten, die im Raster enthalten sein sollen. Sie können die Position, Größe und standardmäßige Sortierreihenfolge des Rasters angeben, indem Sie die Eigenschaften in der Ansicht bearbeiten. Anschließend konfigurieren Sie das benutzerdefinierte Steuerelement für diese Ansicht, damit es zu einem Steuerelement **Zeiteintragsraster** wird. Fügen Sie das Steuerelement der Ansicht hinzu, und wählen Sie es für **Internet**, **Smartphone** und **Tablet** aus. Konfigurieren Sie dann die Parameter für das Raster **Wöchentlicher Zeiteintrag**. Legen Sie das Feld **Startdatum** auf **msdyn\_date**, das Feld **Dauer** auf **msdyn\_duration** und das Feld **Status** auf **msdyn\_entrystatus** fest. Das **Schreibgeschützte Statusliste**-Feld ist auf **192350002 (Genehmigt)**, **192350003 (Eingereicht)** oder **192350004 (Rückruf angefordert)** festgelegt.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Hinzufügen des benutzerdefinierten Felds zur entsprechenden Bearbeitungsseite
Die Seiten, die zum Bearbeiten eines Zeiteintrags oder einer Zeile von Zeiteinträgen verwendet werden, finden Sie unter **Formulare**. Die **Eintrag bearbeiten**-Schaltfläche im Raster öffnet die **Eintrag bearbeiten**-Seite und die **Zeile bearbeiten**-Schaltfläche öffnet die **Zeile bearbeiten**-Seite. Sie können diese Seiten bearbeiten, sodass sie benutzerdefinierte Felder enthalten.

Durch beide Optionen werden einige der standardmäßigen Filterungen bei den Entitäten **Projekt** und **Projektaufgabe** entfernt, sodass alle Suchansichten für die Entitäten sichtbar werden. Standardmäßig sind nur die relevanten Suchansichten sichtbar.

Sie müssen die entsprechende Seite für das benutzerdefinierte Feld festlegen. Wenn Sie das Feld dem Raster hinzugefügt haben, sollte es höchstwahrscheinlich auf der Seite **Zeile bearbeiten** verschoben werden, der für Felder verwendet wird, die auf die gesamte Zeile mit Zeiteinträgen angewendet werden. Wenn das benutzerdefinierte Feld jeden Tag in der Zeile einen eindeutigen Wert hat, (z. B. wenn es ein benutzerdefiniertes Feld für Endzeit ist) , sollte es auf die Seite **Zelle bearbeiten** verschoben werden.

Um einer Seite ein benutzerdefiniertes Feld hinzuzufügen, ziehen Sie ein Element **Feld** an die geeignete Position auf der Seite, und legen Sie dann die Eigenschaften fest.

### <a name="add-new-option-set-values"></a>Hinzufügen neuer Optionssatzwerte
Um die Optionssatzwerte einem Standardfeld hinzufügen, gehen Sie folgendermaßen vor.

1. Öffnen Sie die Bearbeitungsseite des Felds und wählen Sie dann unter **Typ** die Option **Bearbeiten** neben dem Optionssatz aus.
2. Fügen Sie eine neue Option hinzu, die eine benutzerdefinierte Beschriftung und Farbe hat. Wenn Sie einen neuen Zeiteintragsstatus hinzufügen möchten, wird das standardmäßige Feld **Eintragsstatus** genannt.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Festlegen eines neuen Zeiteintragsstatus als „schreibgeschützt“
Wenn Sie einen neuen Zeiteintragsstatus als „schreibgeschützt“ festlegen möchten, fügen Sie den neuen Zeiteintragswert der Eigenschaft **Schreibgeschützte Statusliste** hinzu. Achten Sie darauf, die Nummer hinzuzufügen, nicht die Bezeichnung. Der bearbeitbare Teil des Zeiteintragsrasters wird jetzt für Zeilen mit dem Status „Neu“ gesperrt. Wenn Sie die **Schreibgeschützte Statusliste**-Eigenschaft für verschiedene **Zeiteintrag**-Ansichten unterschiedlich einrichten möchten, fügen Sie das **Zeiteintrag**-Raster im Abschnitt **Benutzerdefinierte Steuerelemente** einer Ansicht hinzu, und konfigurieren Sie die Parameter entsprechend.

Fügen Sie dann Geschäftsregeln hinzu, um alle Felder auf den TBX-Seiten **Bearbeiten der Zeile** und **Bearbeiten von Zeiteinträgen** zu sperren. Um auf die Geschäftsregeln für diese Seiten zugreifen, öffnen Sie den Formulareditor für jede Seite und wählen dann **Geschäftsregeln**. Sie können den neuen Status der Bedingung in vorhandenen Geschäftsregeln hinzufügen, oder Sie können eine neue Geschäftsregel für den neuen Status hinzufügen.

### <a name="add-custom-validation-rules"></a>Hinzufügen benutzerdefinierter Prüfungsregeln
Sie können zwei Arten von Validierungsregeln für die **Wöchentlicher Zeiteintrag**-Rastererfahrung hinzufügen:

- Clientseitige Geschäftsregeln, die auf Seiten funktionieren
- Serverseitige Plug-In-Validierungen, die für alle Aktualisierungen von Zeiteinträgen gelten

#### <a name="client-side-business-rules"></a>Clientseitige Geschäftsregeln
Mithilfe von Geschäftsregeln können Sie Felder sperren und entsperren, Standardwerte in Felder eingeben und Prüfungen festlegen, die Informationen nur aus dem aktuellen Zeiteintrags-Datensatz erfordern. Um auf die Geschäftsregeln für eine Seite zugreifen, öffnen Sie den Formulareditor und wählen dann **Geschäftsregeln**. Sie können dann die vorhandenen Geschäftsregeln bearbeiten oder eine neue Geschäftsregel hinzufügen.

#### <a name="server-side-plug-in-validations"></a>Serverseitige Plug-In-Validierungen
Sie sollten Plug-In-Prüfungen für alle Prüfungen, bei denen mehr Kontext erforderlich ist, als in einem einzelnen Zeiteintrags-Datensatz vorhanden ist. Sie sollten sie auch für alle Validierungen verwenden, die Sie für Inline-Updates im Raster ausführen möchten. Um die Validierungen abzuschließen, erstellen Sie ein benutzerdefiniertes Plug-In in der Entität **Zeiteintrag**.

### <a name="limits"></a>Grenzwerte
Derzeit hat das **Zeiteintrag**-Raster eine Größenbeschränkung von 500 Zeilen. Wenn mehr als 500 Zeilen vorhanden sind, werden die überschüssigen Zeilen nicht angezeigt. Es gibt keine Möglichkeit, diese Größenbeschränkung zu erhöhen.

### <a name="copying-time-entries"></a>Kopieren von Zeiteinträgen
Verwenden Sie die Ansicht **Zeiteintragsspalten kopieren**, um die Liste der Felder zu definieren, die während der Zeiteingabe kopiert werden sollen. **Datum** und **Dauer** sind Pflichtfelder und sollten nicht aus der Ansicht entfernt werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
