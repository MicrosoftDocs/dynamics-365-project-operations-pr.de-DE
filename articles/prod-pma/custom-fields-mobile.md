---
title: Implementieren Sie benutzerdefinierte Felder für die mobile Microsoft Dynamics 365 Project Timesheet-App auf iOS und Android
description: Dieses Thema bietet allgemeine Muster für die Verwendung von Erweiterungen zum Implementieren benutzerdefinierter Felder.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076578"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementieren Sie benutzerdefinierte Felder für die mobile Microsoft Dynamics 365 Project Timesheet-App auf iOS und Android

[!include [banner](../includes/banner.md)]

Dieses Thema bietet allgemeine Muster für die Verwendung von Erweiterungen zum Implementieren benutzerdefinierter Felder. Folgende Themen werden behandelt:

- Die verschiedenen Datentypen, die das benutzerdefinierte Feldframework unterstützt
- So zeigen Sie schreibgeschützte oder bearbeitbare Felder in Arbeitszeittabelleneinträgen an und speichern vom Benutzer bereitgestellte Werte wieder in der Datenbank
- Anzeigen schreibgeschützter Felder im Arbeitszeittabellenkopf
- So integrieren Sie andere benutzerdefinierte Geschäftslogik, um Standardwerte in Felder einzugeben und zusätzliche Überprüfungen durchzuführen

## <a name="audience"></a>Publikum

Dieses Thema ist für Entwickler gedacht, die ihre benutzerdefinierten Felder in die mobile Microsoft Dynamics 365 Project Timesheet-Anwendung integrieren, die für Apple iOS und Google Android verfügbar ist. Es wird davon ausgegangen, dass die Leser mit der X++-Entwicklung und den Funktionen der Projektzeittabelle vertraut sind.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Datenvertrag – TSTimesheetCustomField X++-Klasse

Die **TSTimesheetCustomField** -Klasse ist die X++-Datenvertragsklasse, die Informationen zu einem benutzerdefinierten Feld für die Arbeitszeittabellenfunktionalität darstellt. Listen der benutzerdefinierten Feldobjekte werden sowohl im TSTimesheetDetails-Datenvertrag als auch im TSTimesheetEntry-Datenvertrag übergeben, um benutzerdefinierte Felder in der mobilen App anzuzeigen.

- **TSTimesheetDetails** – Der Arbeitszeittabellen-Kopfzeilen-Vertrag.
- **TSTimesheetEntry** – Der Arbeitszeittabellen-Transaktionsvertrag. Gruppen dieser Objekte mit identischen Projektinformationen und **timesheetLineRecId** -Werten bilden eine Position.

### <a name="fieldbasetype-types"></a>fieldBaseType (Typen)

Die **FieldBaseType** -Eigenschaft im **TsTimesheetCustom** -Objekt bestimmt den Feldtyp, der in der App angezeigt wird. Folgende **Typen** -Werte werden unterstützt.

| Typen-Wert | Typ              | Hinweise |
|-------------|-------------------|-------|
| 0           | Zeichenfolge (und Enum) | Das Feld wird als Textfeld angezeigt. |
| 1           | Integer           | Der Wert wird als Zahl ohne Dezimalstellen angezeigt. |
| 2           | Real              | Der Wert wird als Zahl mit Dezimalstellen angezeigt.<p>Um den tatsächlichen Wert als Währung in der App anzuzeigen, verwenden Sie die **fieldExtenededType** -Eigenschaft. Sie können die **numberOfDecimals** -Eigenschaft zum Festlegen der Anzahl der angezeigten Dezimalstellen verwenden.</p> |
| 3           | Date              | Datumsformate werden über die **Datum, Uhrzeit und Zahlenformat** -Einstellung vom Benutzer festgelegt, die unter **Sprach- und Länder-/Regionsvoreinstellungen** in den **Benutzeroptionen** angegeben ist. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Wenn die **stringOptions** -Eigenschaft nicht im **TSTimesheetCustomField** -Objekt zur Verfügung gestellt wird, wird dem Benutzer ein Freitextfeld zur Verfügung gestellt.

    Mit der **stringLength** -Eigenschaft kann die maximale Zeichenfolgenlänge festgelegt werden, die Benutzer eingeben können.

- Wenn die **stringOptions** -Eigenschaft im **TSTimesheetCustomField** -Objekt zur Verfügung gestellt wird, sind diese Listenelemente die einzigen Werte, die Benutzer mithilfe von Optionsfeldern auswählen können.

    In diesem Fall kann das Zeichenfolgenfeld als Aufzählungswert für die Benutzereingabe dienen. Um den Wert als Aufzählung in der Datenbank zu speichern, ordnen Sie den Zeichenfolgenwert manuell dem Aufzählungswert zu, bevor Sie ihn mithilfe der Befehlskette in der Datenbank speichern (siehe Beispiel im Abschnitt „Befehlskette in der TSTimesheetEntryService-Klasse verwenden, um einen Arbeitszeittabelleneintrag aus der App in der Datenbank zu speichern“ weiter unten in diesem Thema).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Mit dieser Eigenschaft können Sie reale Werte als Währung formatieren. Dieser Ansatz ist nur anwendbar, wenn der **fieldBaseType** -Wert **Real** ist.

- **TSCustomFieldExtendedType:None** – Es wird keine Formatierung angewendet.
- **TSCustomFieldExtendedType::Currency** – Wert wird als Währung formatiert.

    Wenn die Währungsformatierung aktiv ist, kann das **stringValue** -Feld verwendet werden, um den Währungscode zu übergeben, der in der App angezeigt werden soll. Der Wert ist schreibgeschützt.

    Das **realValue** -Feld enthält den Geldbetrag, der in der Datenbank gespeichert werden soll.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Mit dieser Eigenschaft können Sie angeben, wo das benutzerdefinierte Feld in der App angezeigt werden soll.

- **TSCustomFieldSection::Header** – Das Feld wird im **Weitere Details anzeigen** -Abschnitt in der App angezeigt. Diese Felder sind immer schreibgeschützt.
- **TSCustomFieldSection::Line** – Das Feld wird nach allen Standardfeldern in Arbeitszeittabelleneinträgen angezeigt. Diese Felder können entweder bearbeitet oder schreibgeschützt sein.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Diese Eigenschaft gibt das Feld an, in dem die von der App bereitgestellten Werte in der Datenbank gespeichert werden.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Diese Eigenschaft gibt das Feld an, in dem die von der App bereitgestellten Werte in der Datenbank gespeichert werden.

### <a name="iseditable-noyes"></a>isEditable (NeinJa)

Setzen Sie diese Eigenschaft auf **Ja** fest, um festzulegen, dass das Feld im Arbeitszeittabelleneintragsabschnitt von Benutzern bearbeitet werden kann. Setzen Sie die Eigenschaft auf **Nein** , um das Feld schreibgeschützt zu machen.

### <a name="ismandatory-noyes"></a>isMandatory (NeinJa)

Setzen Sie diese Eigenschaft auf **Ja** fest, um festzulegen, dass das Feld im Arbeitszeittabelleneintragsabschnitt ein Pflichtfeld ist.

### <a name="label-str"></a>label (str)

Diese Eigenschaft gibt die Bezeichnung an, die neben dem Feld in der App angezeigt wird.

### <a name="stringoptions-list-of-strings"></a>stringOptions (Liste der Zeichenfolgen)

Diese Eigenschaft gilt nur, wenn der **fieldBaseType** auf **String** eingestellt ist. Wenn **stringOptions** festgelgt ist, werden die Zeichenfolgenwerte, die über Optionsfelder zur Auswahl stehen, durch die Zeichenfolgen in der Liste angegeben. Wenn keine Zeichenfolgen angegeben sind, ist die Freitexteingabe im Zeichenfolgenfeld zulässig (ein Beispiel finden Sie im Abschnitt „Befehlskette in der TSTimesheetEntryService-Klasse verwenden, um einen Arbeitszeittabelleneintrag aus der App in der Datenbank zu speichern“ weiter unten in diesem Thema).

### <a name="stringlength-int"></a>stringLength (int)

Diese Eigenschaft gibt die maximale Länge für ein Zeichenfolgenfeld an. Sie gilt nur, wenn der **fieldBaseType** auf **String** eingestellt ist.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Diese Eigenschaft gibt die Anzahl der Dezimalstellen an, die für ein reales Feld angezeigt werden. Sie gilt nur, wenn der **fieldBaseType** auf **Real** eingestellt ist.

### <a name="ordersequence-int"></a>orderSequence (int)

Diese Eigenschaft steuert die Reihenfolge, in der die benutzerdefinierten Felder in der App angezeigt werden, wenn mehr als ein benutzerdefiniertes Feld angegeben ist. Felder mit niedrigeren Zahlen werden zuerst angezeigt.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Für Felder des Typs **Boolean** übergibt diese Eigenschaft den Booleschen Wert des Felds zwischen dem Server und der App.

### <a name="guidvalue-guid"></a>guidValue (guid)

Für Felder des Typs **GUID** übergibt diese Eigenschaft den GUID (Globally Unique Identifier)-Wert des Felds zwischen dem Server und der App.

### <a name="int64value-int64"></a>int64Value (int64)

Für Felder des Typs **Int64** übergibt diese Eigenschaft den Int64-Wert des Felds zwischen dem Server und der App.

### <a name="intvalue-int"></a>intValue (int)

Für Felder des Typs **Int** übergibt diese Eigenschaft den Int-Wert des Felds zwischen dem Server und der App.

### <a name="realvalue-real"></a>realValue (real)

Für Felder des Typs **Real** übergibt diese Eigenschaft den Real-Wert des Felds zwischen dem Server und der App.

### <a name="stringvalue-str"></a>stringValue (str)

Für Felder des Typs **String** übergibt diese Eigenschaft den Zeichenfolgen-Wert des Felds zwischen dem Server und der App. Es wird auch für Felder des **Real** -Typs verwendet, die als Währung formatiert sind. Für diese Felder wird die Eigenschaft verwendet, um den Währungscode an die App zu übergeben.

### <a name="datevalue-date"></a>dateValue (date)

Für Felder des Typs **Date** übergibt diese Eigenschaft den Datumswert des Felds zwischen dem Server und der App.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Zeigen Sie ein benutzerdefiniertes Feld im Abschnitt zur Eingabe der Arbeitszeittabelle an, und speichern Sie es

Unten sehen Sie einen Screenshot der mobilen App bei der Erstellung eines Arbeitszeittabelleneintrags. Es werden die Out-of-Box-Felder und ein benutzerdefiniertes Feld im Abschnitt „Zeiteintrag“ mit dem Namen „Testzeichenfolge“ mit dem bereits festgelegten Aufzählungswert „Zweite Option“ angezeigt.

![Benutzerdefiniertes Feld für Testzeichenfolgen in der App](media/timesheet-entry.jpg)



Unten sehen Sie einen Screenshot der mobilen App des Benutzers, der eine der für das benutzerdefinierte Feld „Testzeichenfolge“ verfügbaren Aufzählungsoptionen auswählt.  Die beiden Optionen sind „Erste Option“ und „Zweite Option“, die als Optionsfelder angezeigt werden. Die zweite Option ist derzeit ausgewählt.

![Optionsfelder für das benutzerdefinierte Testzeichenfolgenfeld](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Erweitern Sie die TSTimesheetLine-Tabelle so, dass sie ein benutzerdefiniertes Feld enthält

In typischen Szenarien werden die Daten für ein benutzerdefiniertes Feld im Abschnitt „Arbeitszeittabelleneintrag“ wahrscheinlich in der Tabelle „TSTimesheetLine“ gespeichert. Andere Tabellen können jedoch verwendet werden, wenn die Daten basierend auf einem bereitgestellten TSTimesheetTrans-Datensatz abgerufen werden können oder wenn sie keinen bestimmten Datensatzkontext haben (z. B. wenn das Feld in den Projektparametern als schreibgeschützt festgelegt ist).

Beachten Sie, dass benutzerdefinierte Felder keine Sicherungsdatenbankdatensätze enthalten müssen. Sie können basierend auf der X++-Logik dynamisch generiert werden. Dieser Ansatz kann in schreibgeschützten Szenarien hilfreich sein (ein Beispiel für dynamisch generierte benutzerdefinierte Feldwerte finden Sie im Abschnitt „Befehlskette in der TSTimesheetDetails-Klasse verwenden, buildCustomFieldListForHeader-Methode zum Ausfüllen von Arbeitszeittabellendetails“).

Unten ist ein Screenshot des Anwendungsobjektbaums von Visual Studio zu sehen. Er zeigt eine Erweiterung der TSTimesheetLine-Tabelle, wobei das TestLineString-Feld als benutzerdefiniertes Feld hinzugefügt wurde.

![Positionszeichenfolge](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Verwenden Sie die Befehlskette für die buildCustomFieldList-Methode der TSTimesheetSettings-Klasse, um ein Feld im Abschnitt zur Eingabe der Arbeitszeittabelle anzuzeigen

Dieser Code steuert die Anzeigeeinstellungen für das Feld in der App. Beispielsweise steuert es den Feldtyp, die Bezeichnung, ob das Feld obligatorisch ist und in welchem Abschnitt das Feld angezeigt wird.

Das folgende Beispiel zeigt ein Zeichenfolgenfeld für Zeiteinträge. Dieses Feld hat zwei Optionen: **Erste Option** und **Zweite Option** , die über Optionsfelder verfügbar sind. Das Feld in der App ist dem **TestLineString** -Feld zugeordnet, das der TSTimesheetLine-Tabelle hinzugefügt wird.

Nutzen Sie die **TSTimesheetCustomField::newFromMetatdata()** -Methode zur Vereinfachung der Initialisierung der benutzerdefinierten Feldeigenschaften: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** und **numberOfDecimals**. Sie können diese Parameter auch manuell einstellen, wie Sie möchten.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Verwenden Sie die Befehlskette für die buildCustomFieldListForEntry-Methode der TSTimesheetEntry-Klasse, um ein Werte in eine Arbeitszeittabelle einzugeben

Die **buildCustomFieldListForEntry** -Methode wird verwendet, um Werte in die gespeicherten Arbeitszeittabellenzeilen in der mobilen App einzugeben. Es wird ein TSTimesheetTrans-Datensatz als Parameter verwendet. Felder aus diesem Datensatz können verwendet werden, um den benutzerdefinierten Feldwert in der App einzugeben.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Verwenden Sie die Befehlskette für die TSTimesheetEntryService-Klasse, um einen Arbeitszeittabelleneintrag aus der App zurück in der Datenbank zu speichern

Um ein benutzerdefiniertes Feld in der typischen Verwendung wieder in der Datenbank zu speichern, müssen Sie mehrere Methoden erweitern:

- Mit der **timesheetLineNeedsUpdating** -Methode wird ermittelt, ob der Zeilendatensatz vom Benutzer in der App geändert wurde und in der Datenbank gespeichert werden muss. Wenn die Leistung keine Rolle spielt, kann diese Methode vereinfacht werden, sodass sie immer **wahr** zurückgibt.
- Die **populateTimesheetLineFromEntryDuringCreate** - und **populateTimesheetLineFromEntryDuringUpdate** -Methoden können erweitert werden, sodass sie Werte in den TSTimesheetLine-Datenbankdatensatz aus dem bereitgestellten TSTimesheetEntry-Datenvertragsdatensatz eingeben. Beachten Sie im folgenden Beispiel, wie die Zuordnung zwischen dem Datenbankfeld und dem Eingabefeld manuell über X++-Code erfolgt.
- Die **populateTimesheetWeekFromEntry** -Methode kann auch erweitert werden, wenn das benutzerdefinierte Feld dem **TSTimesheetEntry** -Objekt zugeordnet und in die TSTimesheetLineweek-Datenbanktabelle zurückgeschrieben werden muss.

> [!NOTE]
> Das folgende Beispiel speichert den Wert von **Erste Option** oder **Zweite Option** , den der Benutzer als Rohzeichenfolgenwert für die Datenbank auswählt. Wenn das Datenbankfeld ein Feld des **Enum** -Typs ist, können diese Werte manuell einem Aufzählungswert zugeordnet und dann in einem Aufzählungsfeld in der Datenbanktabelle gespeichert werden.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Zeigen Sie ein benutzerdefiniertes Feld im Kopfzeilen-Abschnitt der Arbeitszeittabelle an

Unten sehen Sie einen Screenshot der mobilen App bei der Benutzeranzeige einer Zeittabelle. Die Schaltfläche „Weitere Informationen“ wurde in der oberen rechten Ecke ausgewählt, um die Option „Weitere Details anzeigen“ anzuzeigen.  

![Befehl „Weitere Details“ anzeigen](media/show-more.png)

Unten sehen Sie einen Screenshot der mobilen App mit der Anzeige „Mehr“ der Zeittabelle. Ein benutzerdefiniertes Feld mit dem Namen „Auslastungsrate dieser Arbeitszeittabelle (berechnetes benutzerdefiniertes Feld)“ wurde dem Arbeitszeittabellenkopf-Abschnitt hinzugefügt. Im benutzerdefinierten Feld wird ein schreibgeschützter Wert von „0,667“ festgelegt.

![Abschnitt „Mehr“](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Erweitern Sie die TSTimesheetTable-Tabelle so, dass sie ein benutzerdefiniertes Feld enthält

In typischen Szenarien werden die Daten für ein benutzerdefiniertes Feld im Kopfzeilenabschnitt wahrscheinlich aus der Tabelle „TSTimesheetHeader“ entnommen. Andere Tabellen können jedoch verwendet werden, wenn die Daten basierend auf einem bereitgestellten TSTimesheetTable-Datensatz abgerufen werden können oder wenn sie keinen bestimmten Datensatzkontext haben (z. B. wenn das Feld in den Projektparametern als schreibgeschützt festgelegt ist).

Beachten Sie, dass benutzerdefinierte Felder keine Sicherungsdatenbankdatensätze enthalten müssen. Sie können basierend auf der X++-Logik dynamisch generiert werden. Das folgende Beispiel zeigt diesen Ansatz.

Felder im Header-Bereich sind in der App immer schreibgeschützt.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Verwenden Sie die Befehlskette für die buildCustomFieldList-Methode der TSTimesheetSettings-Klasse, um ein Feld im Kopfzeilen-Abschnitt anzuzeigen

Dieser Code steuert die Anzeigeeinstellungen für das Feld in der App. Beispielsweise steuert es den Feldtyp, die Bezeichnung, ob das Feld obligatorisch ist und in welchem Abschnitt das Feld angezeigt wird.

Das folgende Beispiel zeigt einen berechneten Wert im Header-Bereich der App.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Verwenden Sie die Befehlskette für die buildCustomFieldListForHeader-Methode der TSTimesheetDetails-Klasse, um Arbeitszeittabellendetails einzugeben

Die **buildCustomFieldListForHeader** -Methode wird verwendet, um Arbeitszeittabellen-Kopfzeilendetails in der mobilen App einzugeben. Es wird ein TSTimesheetTable-Datensatz als Parameter verwendet. Felder aus diesem Datensatz können verwendet werden, um den benutzerdefinierten Feldwert in der App einzugeben. Im folgenden Beispiel werden keine Werte aus der Datenbank gelesen. Stattdessen wird X++-Logik verwendet, um einen berechneten Wert zu generieren, der dann in der App angezeigt wird.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Andere Konfigurierbarkeits-/Erweiterungsmöglichkeiten

### <a name="adding-additional-validation-for-the-app"></a>Hinzufügen einer zusätzlichen Validierung für die App

Die vorhandene Logik für die Arbeitszeittabellenfunktionalität auf Datenbankebene funktioniert weiterhin wie erwartet. Sie können **throw error("message to user")** zum Code über eine Kette von Befehlserweiterungen hinzufügen, um den Abschluss von Speicher- oder Übermittlungsvorgängen zu unterbrechen und eine bestimmte Fehlermeldung anzuzeigen. Hier sind drei Beispiele für nützliche erweiterbare Methoden:

- Wenn **validateWrite** in der TSTimesheetLine-Tabelle während eines Speichervorgangs **falsch** für eine Arbeitszeittabellenzeile zurückgibt, wird in der mobilen App eine Fehlermeldung angezeigt.
- Wenn **validateSubmit** in der TSTimesheetTable-Tabelle während der Zeittabellenübertragung **falsch** für eine Arbeitszeittabellenzeile zurückgibt, wird dem Benutzer eine Fehlermeldung angezeigt.
- Logik, die Felder (z. B. **Positions-Eigenschaft** ) während der **insert** -Methode in der TSTimesheetLine-Tabelle ausfüllt, wird weiterhin ausgeführt.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Ausblenden und Markieren von Standardfeldern als schreibgeschützt über die Konfiguration

Über die Projektparameter können Sie sofort einsatzbereite Felder schreibgeschützt oder in der mobilen App ausgeblendet machen. Legen Sie die Optionen im **Mobile Arbeitszeittabellen** -Abschnitt auf der **Arbeitszeittabelle** -Registerkarte der **Projektmanagement- und Buchhaltungsparameter** -Seite fest.

![Projektparameter](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Ändern der Aktivitäten, die über Erweiterungen zur Auswahl stehen

Die Aktivitäten, die für ein Projekt zur Auswahl stehen, werden über die **getActivitiesForProject()** - und **getActivityQuery()** -Methoden in der **TsTimesheetProjectService** -Klasse ausgefüllt. Mithilfe der Befehlskette können Sie dieses Verhalten so ändern, dass es Ihrem Geschäftsszenario für die Aktivitäten entspricht, die für ein bestimmtes Projekt zur Auswahl stehen.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Eingabe einer Standardprojektkategorie in Arbeitszeittabelleneinträgen

Die Eingabe einer Standardprojektkategorie in Arbeitszeittabelleneinträge erfolgt auf drei Ebenen. Sie können die Befehlskette verwenden, um das Verhalten auf einer oder allen dieser Ebenen zu erweitern und das gewünschte Verhalten zu erzielen. Dabei kommt folgende Hierarchie zum Einsatz:

1. Die App versucht, die Standardkategorie aus der Projektressource zu übernehmen. Diese Standardkategorie wird in den **getCurrentUserResource** - und **getDelegatedResourcesForCurrentUser** -Methoden in der **TSTimesheetSettingsService** -Klasse festgelegt.
2. Wenn die Standardkategorie auf Projektressourcenebene nicht bereitgestellt wird, versucht die App, sie aus der Projektaktivität abzurufen. Diese Standardkategorie wird in der **getActivitiesForProject** -Methode in der **TSTimesheetProjectService** -Klasse festgelegt.
3. Wenn die Standardkategorie auf Projektaktivitätsebene nicht bereitgestellt wird, wird die Standardkategorie aus den Projektparametern abgerufen. Diese Standardkategorie wird in der **getProjectDetailsbyRule** -Methode in der **TSTimesheetProjectService** -Klasse festgelegt.
