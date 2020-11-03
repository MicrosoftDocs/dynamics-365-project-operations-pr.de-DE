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
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="d260e-103">Implementieren Sie benutzerdefinierte Felder für die mobile Microsoft Dynamics 365 Project Timesheet-App auf iOS und Android</span><span class="sxs-lookup"><span data-stu-id="d260e-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d260e-104">Dieses Thema bietet allgemeine Muster für die Verwendung von Erweiterungen zum Implementieren benutzerdefinierter Felder.</span><span class="sxs-lookup"><span data-stu-id="d260e-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="d260e-105">Folgende Themen werden behandelt:</span><span class="sxs-lookup"><span data-stu-id="d260e-105">The following topics are covered:</span></span>

- <span data-ttu-id="d260e-106">Die verschiedenen Datentypen, die das benutzerdefinierte Feldframework unterstützt</span><span class="sxs-lookup"><span data-stu-id="d260e-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="d260e-107">So zeigen Sie schreibgeschützte oder bearbeitbare Felder in Arbeitszeittabelleneinträgen an und speichern vom Benutzer bereitgestellte Werte wieder in der Datenbank</span><span class="sxs-lookup"><span data-stu-id="d260e-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="d260e-108">Anzeigen schreibgeschützter Felder im Arbeitszeittabellenkopf</span><span class="sxs-lookup"><span data-stu-id="d260e-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="d260e-109">So integrieren Sie andere benutzerdefinierte Geschäftslogik, um Standardwerte in Felder einzugeben und zusätzliche Überprüfungen durchzuführen</span><span class="sxs-lookup"><span data-stu-id="d260e-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="d260e-110">Publikum</span><span class="sxs-lookup"><span data-stu-id="d260e-110">Audience</span></span>

<span data-ttu-id="d260e-111">Dieses Thema ist für Entwickler gedacht, die ihre benutzerdefinierten Felder in die mobile Microsoft Dynamics 365 Project Timesheet-Anwendung integrieren, die für Apple iOS und Google Android verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d260e-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="d260e-112">Es wird davon ausgegangen, dass die Leser mit der X++-Entwicklung und den Funktionen der Projektzeittabelle vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="d260e-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="d260e-113">Datenvertrag – TSTimesheetCustomField X++-Klasse</span><span class="sxs-lookup"><span data-stu-id="d260e-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="d260e-114">Die **TSTimesheetCustomField** -Klasse ist die X++-Datenvertragsklasse, die Informationen zu einem benutzerdefinierten Feld für die Arbeitszeittabellenfunktionalität darstellt.</span><span class="sxs-lookup"><span data-stu-id="d260e-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="d260e-115">Listen der benutzerdefinierten Feldobjekte werden sowohl im TSTimesheetDetails-Datenvertrag als auch im TSTimesheetEntry-Datenvertrag übergeben, um benutzerdefinierte Felder in der mobilen App anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d260e-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="d260e-116">**TSTimesheetDetails** – Der Arbeitszeittabellen-Kopfzeilen-Vertrag.</span><span class="sxs-lookup"><span data-stu-id="d260e-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="d260e-117">**TSTimesheetEntry** – Der Arbeitszeittabellen-Transaktionsvertrag.</span><span class="sxs-lookup"><span data-stu-id="d260e-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="d260e-118">Gruppen dieser Objekte mit identischen Projektinformationen und **timesheetLineRecId** -Werten bilden eine Position.</span><span class="sxs-lookup"><span data-stu-id="d260e-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="d260e-119">fieldBaseType (Typen)</span><span class="sxs-lookup"><span data-stu-id="d260e-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="d260e-120">Die **FieldBaseType** -Eigenschaft im **TsTimesheetCustom** -Objekt bestimmt den Feldtyp, der in der App angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d260e-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="d260e-121">Folgende **Typen** -Werte werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d260e-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="d260e-122">Typen-Wert</span><span class="sxs-lookup"><span data-stu-id="d260e-122">Types value</span></span> | <span data-ttu-id="d260e-123">Typ</span><span class="sxs-lookup"><span data-stu-id="d260e-123">Type</span></span>              | <span data-ttu-id="d260e-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d260e-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="d260e-125">0</span><span class="sxs-lookup"><span data-stu-id="d260e-125">0</span></span>           | <span data-ttu-id="d260e-126">Zeichenfolge (und Enum)</span><span class="sxs-lookup"><span data-stu-id="d260e-126">String (and Enum)</span></span> | <span data-ttu-id="d260e-127">Das Feld wird als Textfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d260e-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="d260e-128">1</span><span class="sxs-lookup"><span data-stu-id="d260e-128">1</span></span>           | <span data-ttu-id="d260e-129">Integer</span><span class="sxs-lookup"><span data-stu-id="d260e-129">Integer</span></span>           | <span data-ttu-id="d260e-130">Der Wert wird als Zahl ohne Dezimalstellen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d260e-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="d260e-131">2</span><span class="sxs-lookup"><span data-stu-id="d260e-131">2</span></span>           | <span data-ttu-id="d260e-132">Real</span><span class="sxs-lookup"><span data-stu-id="d260e-132">Real</span></span>              | <span data-ttu-id="d260e-133">Der Wert wird als Zahl mit Dezimalstellen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d260e-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="d260e-134">Um den tatsächlichen Wert als Währung in der App anzuzeigen, verwenden Sie die **fieldExtenededType** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d260e-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="d260e-135">Sie können die **numberOfDecimals** -Eigenschaft zum Festlegen der Anzahl der angezeigten Dezimalstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d260e-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="d260e-136">3</span><span class="sxs-lookup"><span data-stu-id="d260e-136">3</span></span>           | <span data-ttu-id="d260e-137">Date</span><span class="sxs-lookup"><span data-stu-id="d260e-137">Date</span></span>              | <span data-ttu-id="d260e-138">Datumsformate werden über die **Datum, Uhrzeit und Zahlenformat** -Einstellung vom Benutzer festgelegt, die unter **Sprach- und Länder-/Regionsvoreinstellungen** in den **Benutzeroptionen** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d260e-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="d260e-139">4</span><span class="sxs-lookup"><span data-stu-id="d260e-139">4</span></span>           | <span data-ttu-id="d260e-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="d260e-140">Boolean</span></span>           | |
| <span data-ttu-id="d260e-141">15</span><span class="sxs-lookup"><span data-stu-id="d260e-141">15</span></span>          | <span data-ttu-id="d260e-142">GUID</span><span class="sxs-lookup"><span data-stu-id="d260e-142">GUID</span></span>              | |
| <span data-ttu-id="d260e-143">16</span><span class="sxs-lookup"><span data-stu-id="d260e-143">16</span></span>          | <span data-ttu-id="d260e-144">Int64</span><span class="sxs-lookup"><span data-stu-id="d260e-144">Int64</span></span>             | |

- <span data-ttu-id="d260e-145">Wenn die **stringOptions** -Eigenschaft nicht im **TSTimesheetCustomField** -Objekt zur Verfügung gestellt wird, wird dem Benutzer ein Freitextfeld zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="d260e-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="d260e-146">Mit der **stringLength** -Eigenschaft kann die maximale Zeichenfolgenlänge festgelegt werden, die Benutzer eingeben können.</span><span class="sxs-lookup"><span data-stu-id="d260e-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="d260e-147">Wenn die **stringOptions** -Eigenschaft im **TSTimesheetCustomField** -Objekt zur Verfügung gestellt wird, sind diese Listenelemente die einzigen Werte, die Benutzer mithilfe von Optionsfeldern auswählen können.</span><span class="sxs-lookup"><span data-stu-id="d260e-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="d260e-148">In diesem Fall kann das Zeichenfolgenfeld als Aufzählungswert für die Benutzereingabe dienen.</span><span class="sxs-lookup"><span data-stu-id="d260e-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="d260e-149">Um den Wert als Aufzählung in der Datenbank zu speichern, ordnen Sie den Zeichenfolgenwert manuell dem Aufzählungswert zu, bevor Sie ihn mithilfe der Befehlskette in der Datenbank speichern (siehe Beispiel im Abschnitt „Befehlskette in der TSTimesheetEntryService-Klasse verwenden, um einen Arbeitszeittabelleneintrag aus der App in der Datenbank zu speichern“ weiter unten in diesem Thema).</span><span class="sxs-lookup"><span data-stu-id="d260e-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="d260e-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="d260e-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="d260e-151">Mit dieser Eigenschaft können Sie reale Werte als Währung formatieren.</span><span class="sxs-lookup"><span data-stu-id="d260e-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="d260e-152">Dieser Ansatz ist nur anwendbar, wenn der **fieldBaseType** -Wert **Real** ist.</span><span class="sxs-lookup"><span data-stu-id="d260e-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="d260e-153">**TSCustomFieldExtendedType:None** – Es wird keine Formatierung angewendet.</span><span class="sxs-lookup"><span data-stu-id="d260e-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="d260e-154">**TSCustomFieldExtendedType::Currency** – Wert wird als Währung formatiert.</span><span class="sxs-lookup"><span data-stu-id="d260e-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="d260e-155">Wenn die Währungsformatierung aktiv ist, kann das **stringValue** -Feld verwendet werden, um den Währungscode zu übergeben, der in der App angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d260e-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="d260e-156">Der Wert ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d260e-156">The value is a read-only value.</span></span>

    <span data-ttu-id="d260e-157">Das **realValue** -Feld enthält den Geldbetrag, der in der Datenbank gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d260e-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="d260e-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="d260e-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="d260e-159">Mit dieser Eigenschaft können Sie angeben, wo das benutzerdefinierte Feld in der App angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d260e-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="d260e-160">**TSCustomFieldSection::Header** – Das Feld wird im **Weitere Details anzeigen** -Abschnitt in der App angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d260e-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="d260e-161">Diese Felder sind immer schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d260e-161">These fields are always read-only.</span></span>
- <span data-ttu-id="d260e-162">**TSCustomFieldSection::Line** – Das Feld wird nach allen Standardfeldern in Arbeitszeittabelleneinträgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d260e-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="d260e-163">Diese Felder können entweder bearbeitet oder schreibgeschützt sein.</span><span class="sxs-lookup"><span data-stu-id="d260e-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="d260e-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="d260e-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="d260e-165">Diese Eigenschaft gibt das Feld an, in dem die von der App bereitgestellten Werte in der Datenbank gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d260e-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="d260e-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="d260e-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="d260e-167">Diese Eigenschaft gibt das Feld an, in dem die von der App bereitgestellten Werte in der Datenbank gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d260e-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="d260e-168">isEditable (NeinJa)</span><span class="sxs-lookup"><span data-stu-id="d260e-168">isEditable (NoYes)</span></span>

<span data-ttu-id="d260e-169">Setzen Sie diese Eigenschaft auf **Ja** fest, um festzulegen, dass das Feld im Arbeitszeittabelleneintragsabschnitt von Benutzern bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d260e-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="d260e-170">Setzen Sie die Eigenschaft auf **Nein** , um das Feld schreibgeschützt zu machen.</span><span class="sxs-lookup"><span data-stu-id="d260e-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="d260e-171">isMandatory (NeinJa)</span><span class="sxs-lookup"><span data-stu-id="d260e-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="d260e-172">Setzen Sie diese Eigenschaft auf **Ja** fest, um festzulegen, dass das Feld im Arbeitszeittabelleneintragsabschnitt ein Pflichtfeld ist.</span><span class="sxs-lookup"><span data-stu-id="d260e-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="d260e-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="d260e-173">label (str)</span></span>

<span data-ttu-id="d260e-174">Diese Eigenschaft gibt die Bezeichnung an, die neben dem Feld in der App angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d260e-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="d260e-175">stringOptions (Liste der Zeichenfolgen)</span><span class="sxs-lookup"><span data-stu-id="d260e-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="d260e-176">Diese Eigenschaft gilt nur, wenn der **fieldBaseType** auf **String** eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="d260e-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="d260e-177">Wenn **stringOptions** festgelgt ist, werden die Zeichenfolgenwerte, die über Optionsfelder zur Auswahl stehen, durch die Zeichenfolgen in der Liste angegeben.</span><span class="sxs-lookup"><span data-stu-id="d260e-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="d260e-178">Wenn keine Zeichenfolgen angegeben sind, ist die Freitexteingabe im Zeichenfolgenfeld zulässig (ein Beispiel finden Sie im Abschnitt „Befehlskette in der TSTimesheetEntryService-Klasse verwenden, um einen Arbeitszeittabelleneintrag aus der App in der Datenbank zu speichern“ weiter unten in diesem Thema).</span><span class="sxs-lookup"><span data-stu-id="d260e-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="d260e-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="d260e-179">stringLength (int)</span></span>

<span data-ttu-id="d260e-180">Diese Eigenschaft gibt die maximale Länge für ein Zeichenfolgenfeld an.</span><span class="sxs-lookup"><span data-stu-id="d260e-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="d260e-181">Sie gilt nur, wenn der **fieldBaseType** auf **String** eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="d260e-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="d260e-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="d260e-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="d260e-183">Diese Eigenschaft gibt die Anzahl der Dezimalstellen an, die für ein reales Feld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d260e-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="d260e-184">Sie gilt nur, wenn der **fieldBaseType** auf **Real** eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="d260e-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="d260e-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="d260e-185">orderSequence (int)</span></span>

<span data-ttu-id="d260e-186">Diese Eigenschaft steuert die Reihenfolge, in der die benutzerdefinierten Felder in der App angezeigt werden, wenn mehr als ein benutzerdefiniertes Feld angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d260e-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="d260e-187">Felder mit niedrigeren Zahlen werden zuerst angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d260e-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="d260e-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="d260e-188">booleanValue (boolean)</span></span>

<span data-ttu-id="d260e-189">Für Felder des Typs **Boolean** übergibt diese Eigenschaft den Booleschen Wert des Felds zwischen dem Server und der App.</span><span class="sxs-lookup"><span data-stu-id="d260e-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="d260e-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="d260e-190">guidValue (guid)</span></span>

<span data-ttu-id="d260e-191">Für Felder des Typs **GUID** übergibt diese Eigenschaft den GUID (Globally Unique Identifier)-Wert des Felds zwischen dem Server und der App.</span><span class="sxs-lookup"><span data-stu-id="d260e-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="d260e-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="d260e-192">int64Value (int64)</span></span>

<span data-ttu-id="d260e-193">Für Felder des Typs **Int64** übergibt diese Eigenschaft den Int64-Wert des Felds zwischen dem Server und der App.</span><span class="sxs-lookup"><span data-stu-id="d260e-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="d260e-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="d260e-194">intValue (int)</span></span>

<span data-ttu-id="d260e-195">Für Felder des Typs **Int** übergibt diese Eigenschaft den Int-Wert des Felds zwischen dem Server und der App.</span><span class="sxs-lookup"><span data-stu-id="d260e-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="d260e-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="d260e-196">realValue (real)</span></span>

<span data-ttu-id="d260e-197">Für Felder des Typs **Real** übergibt diese Eigenschaft den Real-Wert des Felds zwischen dem Server und der App.</span><span class="sxs-lookup"><span data-stu-id="d260e-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="d260e-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="d260e-198">stringValue (str)</span></span>

<span data-ttu-id="d260e-199">Für Felder des Typs **String** übergibt diese Eigenschaft den Zeichenfolgen-Wert des Felds zwischen dem Server und der App.</span><span class="sxs-lookup"><span data-stu-id="d260e-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="d260e-200">Es wird auch für Felder des **Real** -Typs verwendet, die als Währung formatiert sind.</span><span class="sxs-lookup"><span data-stu-id="d260e-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="d260e-201">Für diese Felder wird die Eigenschaft verwendet, um den Währungscode an die App zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="d260e-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="d260e-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="d260e-202">dateValue (date)</span></span>

<span data-ttu-id="d260e-203">Für Felder des Typs **Date** übergibt diese Eigenschaft den Datumswert des Felds zwischen dem Server und der App.</span><span class="sxs-lookup"><span data-stu-id="d260e-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="d260e-204">Zeigen Sie ein benutzerdefiniertes Feld im Abschnitt zur Eingabe der Arbeitszeittabelle an, und speichern Sie es</span><span class="sxs-lookup"><span data-stu-id="d260e-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="d260e-205">Unten sehen Sie einen Screenshot der mobilen App bei der Erstellung eines Arbeitszeittabelleneintrags.</span><span class="sxs-lookup"><span data-stu-id="d260e-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="d260e-206">Es werden die Out-of-Box-Felder und ein benutzerdefiniertes Feld im Abschnitt „Zeiteintrag“ mit dem Namen „Testzeichenfolge“ mit dem bereits festgelegten Aufzählungswert „Zweite Option“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d260e-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Benutzerdefiniertes Feld für Testzeichenfolgen in der App](media/timesheet-entry.jpg)



<span data-ttu-id="d260e-208">Unten sehen Sie einen Screenshot der mobilen App des Benutzers, der eine der für das benutzerdefinierte Feld „Testzeichenfolge“ verfügbaren Aufzählungsoptionen auswählt.</span><span class="sxs-lookup"><span data-stu-id="d260e-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="d260e-209">Die beiden Optionen sind „Erste Option“ und „Zweite Option“, die als Optionsfelder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d260e-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="d260e-210">Die zweite Option ist derzeit ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d260e-210">The second option is currently selected.</span></span>

![Optionsfelder für das benutzerdefinierte Testzeichenfolgenfeld](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="d260e-212">Erweitern Sie die TSTimesheetLine-Tabelle so, dass sie ein benutzerdefiniertes Feld enthält</span><span class="sxs-lookup"><span data-stu-id="d260e-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="d260e-213">In typischen Szenarien werden die Daten für ein benutzerdefiniertes Feld im Abschnitt „Arbeitszeittabelleneintrag“ wahrscheinlich in der Tabelle „TSTimesheetLine“ gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d260e-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="d260e-214">Andere Tabellen können jedoch verwendet werden, wenn die Daten basierend auf einem bereitgestellten TSTimesheetTrans-Datensatz abgerufen werden können oder wenn sie keinen bestimmten Datensatzkontext haben (z. B. wenn das Feld in den Projektparametern als schreibgeschützt festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="d260e-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="d260e-215">Beachten Sie, dass benutzerdefinierte Felder keine Sicherungsdatenbankdatensätze enthalten müssen.</span><span class="sxs-lookup"><span data-stu-id="d260e-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="d260e-216">Sie können basierend auf der X++-Logik dynamisch generiert werden.</span><span class="sxs-lookup"><span data-stu-id="d260e-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="d260e-217">Dieser Ansatz kann in schreibgeschützten Szenarien hilfreich sein (ein Beispiel für dynamisch generierte benutzerdefinierte Feldwerte finden Sie im Abschnitt „Befehlskette in der TSTimesheetDetails-Klasse verwenden, buildCustomFieldListForHeader-Methode zum Ausfüllen von Arbeitszeittabellendetails“).</span><span class="sxs-lookup"><span data-stu-id="d260e-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="d260e-218">Unten ist ein Screenshot des Anwendungsobjektbaums von Visual Studio zu sehen.</span><span class="sxs-lookup"><span data-stu-id="d260e-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="d260e-219">Er zeigt eine Erweiterung der TSTimesheetLine-Tabelle, wobei das TestLineString-Feld als benutzerdefiniertes Feld hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d260e-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Positionszeichenfolge](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="d260e-221">Verwenden Sie die Befehlskette für die buildCustomFieldList-Methode der TSTimesheetSettings-Klasse, um ein Feld im Abschnitt zur Eingabe der Arbeitszeittabelle anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="d260e-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="d260e-222">Dieser Code steuert die Anzeigeeinstellungen für das Feld in der App.</span><span class="sxs-lookup"><span data-stu-id="d260e-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="d260e-223">Beispielsweise steuert es den Feldtyp, die Bezeichnung, ob das Feld obligatorisch ist und in welchem Abschnitt das Feld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d260e-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="d260e-224">Das folgende Beispiel zeigt ein Zeichenfolgenfeld für Zeiteinträge.</span><span class="sxs-lookup"><span data-stu-id="d260e-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="d260e-225">Dieses Feld hat zwei Optionen: **Erste Option** und **Zweite Option** , die über Optionsfelder verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d260e-225">This field has two options, **First option** and **Second option** , that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="d260e-226">Das Feld in der App ist dem **TestLineString** -Feld zugeordnet, das der TSTimesheetLine-Tabelle hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d260e-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="d260e-227">Nutzen Sie die **TSTimesheetCustomField::newFromMetatdata()** -Methode zur Vereinfachung der Initialisierung der benutzerdefinierten Feldeigenschaften: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** und **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="d260e-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType** , **tableName** , **fieldname** , **label** , **isEditable** , **isMandatory** , **stringLength** , and **numberOfDecimals**.</span></span> <span data-ttu-id="d260e-228">Sie können diese Parameter auch manuell einstellen, wie Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="d260e-228">You can also set these parameters manually, as you prefer.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="d260e-229">Verwenden Sie die Befehlskette für die buildCustomFieldListForEntry-Methode der TSTimesheetEntry-Klasse, um ein Werte in eine Arbeitszeittabelle einzugeben</span><span class="sxs-lookup"><span data-stu-id="d260e-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="d260e-230">Die **buildCustomFieldListForEntry** -Methode wird verwendet, um Werte in die gespeicherten Arbeitszeittabellenzeilen in der mobilen App einzugeben.</span><span class="sxs-lookup"><span data-stu-id="d260e-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="d260e-231">Es wird ein TSTimesheetTrans-Datensatz als Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="d260e-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="d260e-232">Felder aus diesem Datensatz können verwendet werden, um den benutzerdefinierten Feldwert in der App einzugeben.</span><span class="sxs-lookup"><span data-stu-id="d260e-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="d260e-233">Verwenden Sie die Befehlskette für die TSTimesheetEntryService-Klasse, um einen Arbeitszeittabelleneintrag aus der App zurück in der Datenbank zu speichern</span><span class="sxs-lookup"><span data-stu-id="d260e-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="d260e-234">Um ein benutzerdefiniertes Feld in der typischen Verwendung wieder in der Datenbank zu speichern, müssen Sie mehrere Methoden erweitern:</span><span class="sxs-lookup"><span data-stu-id="d260e-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="d260e-235">Mit der **timesheetLineNeedsUpdating** -Methode wird ermittelt, ob der Zeilendatensatz vom Benutzer in der App geändert wurde und in der Datenbank gespeichert werden muss.</span><span class="sxs-lookup"><span data-stu-id="d260e-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="d260e-236">Wenn die Leistung keine Rolle spielt, kann diese Methode vereinfacht werden, sodass sie immer **wahr** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d260e-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="d260e-237">Die **populateTimesheetLineFromEntryDuringCreate** - und **populateTimesheetLineFromEntryDuringUpdate** -Methoden können erweitert werden, sodass sie Werte in den TSTimesheetLine-Datenbankdatensatz aus dem bereitgestellten TSTimesheetEntry-Datenvertragsdatensatz eingeben.</span><span class="sxs-lookup"><span data-stu-id="d260e-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="d260e-238">Beachten Sie im folgenden Beispiel, wie die Zuordnung zwischen dem Datenbankfeld und dem Eingabefeld manuell über X++-Code erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d260e-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="d260e-239">Die **populateTimesheetWeekFromEntry** -Methode kann auch erweitert werden, wenn das benutzerdefinierte Feld dem **TSTimesheetEntry** -Objekt zugeordnet und in die TSTimesheetLineweek-Datenbanktabelle zurückgeschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="d260e-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="d260e-240">Das folgende Beispiel speichert den Wert von **Erste Option** oder **Zweite Option** , den der Benutzer als Rohzeichenfolgenwert für die Datenbank auswählt.</span><span class="sxs-lookup"><span data-stu-id="d260e-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="d260e-241">Wenn das Datenbankfeld ein Feld des **Enum** -Typs ist, können diese Werte manuell einem Aufzählungswert zugeordnet und dann in einem Aufzählungsfeld in der Datenbanktabelle gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d260e-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="d260e-242">Zeigen Sie ein benutzerdefiniertes Feld im Kopfzeilen-Abschnitt der Arbeitszeittabelle an</span><span class="sxs-lookup"><span data-stu-id="d260e-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="d260e-243">Unten sehen Sie einen Screenshot der mobilen App bei der Benutzeranzeige einer Zeittabelle.</span><span class="sxs-lookup"><span data-stu-id="d260e-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="d260e-244">Die Schaltfläche „Weitere Informationen“ wurde in der oberen rechten Ecke ausgewählt, um die Option „Weitere Details anzeigen“ anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d260e-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Befehl „Weitere Details“ anzeigen](media/show-more.png)

<span data-ttu-id="d260e-246">Unten sehen Sie einen Screenshot der mobilen App mit der Anzeige „Mehr“ der Zeittabelle.</span><span class="sxs-lookup"><span data-stu-id="d260e-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="d260e-247">Ein benutzerdefiniertes Feld mit dem Namen „Auslastungsrate dieser Arbeitszeittabelle (berechnetes benutzerdefiniertes Feld)“ wurde dem Arbeitszeittabellenkopf-Abschnitt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d260e-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="d260e-248">Im benutzerdefinierten Feld wird ein schreibgeschützter Wert von „0,667“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d260e-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Abschnitt „Mehr“](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="d260e-250">Erweitern Sie die TSTimesheetTable-Tabelle so, dass sie ein benutzerdefiniertes Feld enthält</span><span class="sxs-lookup"><span data-stu-id="d260e-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="d260e-251">In typischen Szenarien werden die Daten für ein benutzerdefiniertes Feld im Kopfzeilenabschnitt wahrscheinlich aus der Tabelle „TSTimesheetHeader“ entnommen.</span><span class="sxs-lookup"><span data-stu-id="d260e-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="d260e-252">Andere Tabellen können jedoch verwendet werden, wenn die Daten basierend auf einem bereitgestellten TSTimesheetTable-Datensatz abgerufen werden können oder wenn sie keinen bestimmten Datensatzkontext haben (z. B. wenn das Feld in den Projektparametern als schreibgeschützt festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="d260e-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="d260e-253">Beachten Sie, dass benutzerdefinierte Felder keine Sicherungsdatenbankdatensätze enthalten müssen.</span><span class="sxs-lookup"><span data-stu-id="d260e-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="d260e-254">Sie können basierend auf der X++-Logik dynamisch generiert werden.</span><span class="sxs-lookup"><span data-stu-id="d260e-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="d260e-255">Das folgende Beispiel zeigt diesen Ansatz.</span><span class="sxs-lookup"><span data-stu-id="d260e-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="d260e-256">Felder im Header-Bereich sind in der App immer schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d260e-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="d260e-257">Verwenden Sie die Befehlskette für die buildCustomFieldList-Methode der TSTimesheetSettings-Klasse, um ein Feld im Kopfzeilen-Abschnitt anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="d260e-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="d260e-258">Dieser Code steuert die Anzeigeeinstellungen für das Feld in der App.</span><span class="sxs-lookup"><span data-stu-id="d260e-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="d260e-259">Beispielsweise steuert es den Feldtyp, die Bezeichnung, ob das Feld obligatorisch ist und in welchem Abschnitt das Feld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d260e-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="d260e-260">Das folgende Beispiel zeigt einen berechneten Wert im Header-Bereich der App.</span><span class="sxs-lookup"><span data-stu-id="d260e-260">The following example shows a computed value in the header section in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="d260e-261">Verwenden Sie die Befehlskette für die buildCustomFieldListForHeader-Methode der TSTimesheetDetails-Klasse, um Arbeitszeittabellendetails einzugeben</span><span class="sxs-lookup"><span data-stu-id="d260e-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="d260e-262">Die **buildCustomFieldListForHeader** -Methode wird verwendet, um Arbeitszeittabellen-Kopfzeilendetails in der mobilen App einzugeben.</span><span class="sxs-lookup"><span data-stu-id="d260e-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="d260e-263">Es wird ein TSTimesheetTable-Datensatz als Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="d260e-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="d260e-264">Felder aus diesem Datensatz können verwendet werden, um den benutzerdefinierten Feldwert in der App einzugeben.</span><span class="sxs-lookup"><span data-stu-id="d260e-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="d260e-265">Im folgenden Beispiel werden keine Werte aus der Datenbank gelesen.</span><span class="sxs-lookup"><span data-stu-id="d260e-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="d260e-266">Stattdessen wird X++-Logik verwendet, um einen berechneten Wert zu generieren, der dann in der App angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d260e-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


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

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="d260e-267">Andere Konfigurierbarkeits-/Erweiterungsmöglichkeiten</span><span class="sxs-lookup"><span data-stu-id="d260e-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="d260e-268">Hinzufügen einer zusätzlichen Validierung für die App</span><span class="sxs-lookup"><span data-stu-id="d260e-268">Adding additional validation for the app</span></span>

<span data-ttu-id="d260e-269">Die vorhandene Logik für die Arbeitszeittabellenfunktionalität auf Datenbankebene funktioniert weiterhin wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="d260e-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="d260e-270">Sie können **throw error("message to user")** zum Code über eine Kette von Befehlserweiterungen hinzufügen, um den Abschluss von Speicher- oder Übermittlungsvorgängen zu unterbrechen und eine bestimmte Fehlermeldung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d260e-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="d260e-271">Hier sind drei Beispiele für nützliche erweiterbare Methoden:</span><span class="sxs-lookup"><span data-stu-id="d260e-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="d260e-272">Wenn **validateWrite** in der TSTimesheetLine-Tabelle während eines Speichervorgangs **falsch** für eine Arbeitszeittabellenzeile zurückgibt, wird in der mobilen App eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d260e-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="d260e-273">Wenn **validateSubmit** in der TSTimesheetTable-Tabelle während der Zeittabellenübertragung **falsch** für eine Arbeitszeittabellenzeile zurückgibt, wird dem Benutzer eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d260e-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="d260e-274">Logik, die Felder (z. B. **Positions-Eigenschaft** ) während der **insert** -Methode in der TSTimesheetLine-Tabelle ausfüllt, wird weiterhin ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d260e-274">Logic that fills in fields (for example, **Line Property** ) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="d260e-275">Ausblenden und Markieren von Standardfeldern als schreibgeschützt über die Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d260e-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="d260e-276">Über die Projektparameter können Sie sofort einsatzbereite Felder schreibgeschützt oder in der mobilen App ausgeblendet machen.</span><span class="sxs-lookup"><span data-stu-id="d260e-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="d260e-277">Legen Sie die Optionen im **Mobile Arbeitszeittabellen** -Abschnitt auf der **Arbeitszeittabelle** -Registerkarte der **Projektmanagement- und Buchhaltungsparameter** -Seite fest.</span><span class="sxs-lookup"><span data-stu-id="d260e-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projektparameter](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="d260e-279">Ändern der Aktivitäten, die über Erweiterungen zur Auswahl stehen</span><span class="sxs-lookup"><span data-stu-id="d260e-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="d260e-280">Die Aktivitäten, die für ein Projekt zur Auswahl stehen, werden über die **getActivitiesForProject()** - und **getActivityQuery()** -Methoden in der **TsTimesheetProjectService** -Klasse ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="d260e-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="d260e-281">Mithilfe der Befehlskette können Sie dieses Verhalten so ändern, dass es Ihrem Geschäftsszenario für die Aktivitäten entspricht, die für ein bestimmtes Projekt zur Auswahl stehen.</span><span class="sxs-lookup"><span data-stu-id="d260e-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="d260e-282">Eingabe einer Standardprojektkategorie in Arbeitszeittabelleneinträgen</span><span class="sxs-lookup"><span data-stu-id="d260e-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="d260e-283">Die Eingabe einer Standardprojektkategorie in Arbeitszeittabelleneinträge erfolgt auf drei Ebenen.</span><span class="sxs-lookup"><span data-stu-id="d260e-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="d260e-284">Sie können die Befehlskette verwenden, um das Verhalten auf einer oder allen dieser Ebenen zu erweitern und das gewünschte Verhalten zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="d260e-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="d260e-285">Dabei kommt folgende Hierarchie zum Einsatz:</span><span class="sxs-lookup"><span data-stu-id="d260e-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="d260e-286">Die App versucht, die Standardkategorie aus der Projektressource zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="d260e-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="d260e-287">Diese Standardkategorie wird in den **getCurrentUserResource** - und **getDelegatedResourcesForCurrentUser** -Methoden in der **TSTimesheetSettingsService** -Klasse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d260e-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="d260e-288">Wenn die Standardkategorie auf Projektressourcenebene nicht bereitgestellt wird, versucht die App, sie aus der Projektaktivität abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d260e-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="d260e-289">Diese Standardkategorie wird in der **getActivitiesForProject** -Methode in der **TSTimesheetProjectService** -Klasse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d260e-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="d260e-290">Wenn die Standardkategorie auf Projektaktivitätsebene nicht bereitgestellt wird, wird die Standardkategorie aus den Projektparametern abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d260e-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="d260e-291">Diese Standardkategorie wird in der **getProjectDetailsbyRule** -Methode in der **TSTimesheetProjectService** -Klasse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d260e-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
