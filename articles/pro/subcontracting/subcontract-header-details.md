---
title: Kopfzeilendetails für Fremdarbeiten
description: Dieser Artikel erläutert die Funktionen, die in Project Operations in der Kopfzeile für Unteraufträge zur Verfügung stehen.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 85649d08228b16178eb8d6be9af5a6731def74bf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914171"
---
# <a name="header-details-for-subcontracts"></a>Kopfzeilendetails für Fremdarbeiten

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieser Artikel erklärt die Funktionen, die in der Kopfzeile des Untervertrags in Dynamics 365 Project Operations zur Verfügung stehen.

Da ein Projektmanager Projekte plant und ausführt, kann er Subunternehmer beschäftigen und Produkte und Dienstleistungen von Lieferanten kaufen. Wenn ein Projektmanager Produkte oder Dienstleistungen kaufen muss, kann er in Project Operations eine Fremdarbeit erstellen.

Gehen Sie wie folgt vor, um eine Fremdarbeit zu erstellen.

1. Wählen Sie im Navigationsbereich **Fremdarbeiten** und auf der Seite **Fremdarbeit** **Neu** aus.
2. Geben Sie die gewünschten Informationen ein und wählen Sie anschließend **Speichern**.

    Die folgende Tabelle enthält Informationen zu den Feldern auf der **Kopfzeilenseite des Fremdauftrags**.

    | Feld | Beschreibung |Funktionsauswirkung |
    |---|------|---| 
    | Name | Der Name der Fremdarbeit. | In allen Dropdown-Listen für Unteraufträge wird der Name des Unterauftrags in der ersten Spalte aufgeführt, um Ihnen die Identifizierung des Unterauftrags zu erleichtern. | 
    | Beschreibung | Eine kurze Beschreibung der Servicees und Produkte, die in der Fremdarbeit gekauft werden. | Kein Wert |
    | Hersteller | Der Name des Unternehmens, von dem die Produkte und Dienstleistungen gekauft werden. Dieser Firmendatensatz hat den Beziehungstyp **Kreditor** oder **Lieferant**. | Basierend auf dem ausgewählten Lieferanten werden automatisch Vorschlagswerte für die folgenden Felder eingegeben:<br/> **• Währung** </br> **• Preislisten** </br> **• Zahlungsbedingungen**</br> **• Zahlungsadresse**</br> **• Rechnungsadresse**</br> **• Name für Rechnungsadresse** </br>**• Konto-Manager des Zulieferers**|
    | Datum der Fremdarbeit | Das Datum, an dem der Untervertrag erstellt wird. | Das Lohnbearbeitungsdatum wird verwendet, um die richtige Einkaufspreisliste entweder aus den Preislisten, die dem zugehörigen Lieferanten beigefügt sind, oder aus den Projektparametern auszuwählen. |
    | Statusgrund | Der Status der Fremdarbeit. | Der Status bestimmt, wo sich der Lohnbearbeiter im Geschäftsprozess befindet und ob er bearbeitet werden kann. <br/>Zu den Werten gehören folgende:<br>• **Entwurf**: Der Untervertrag kann bearbeitet werden. Sie können nur Unteraufträge mit dem Status **Entwurf** bearbeiten.<br/>• **Bestätigt**: Die Verhandlungen mit dem Lieferanten sind abgeschlossen und der Unterauftrag zur Lieferung freigegeben. <br/>• **Abgeschlossen**: Die Lieferung des Unterauftrags ist abgeschlossen.<br/>• **Abgebrochen**: Der Lohnauftrag wurde storniert und es ist keine Lieferung geplant.  | 
    | Währung | Die Währung, in der Produkte und Dienstleistungen gekauft oder verkauft werden. Der Standardwert wird automatisch aus dem Kreditorenkonto eingegeben, kann jedoch geändert werden. | Die Währung des Lohnauftrags wird verwendet, um die richtige Einkaufspreisliste entweder aus den Preislisten, die dem zugehörigen Lieferanten beigefügt sind, oder aus den Projektparametern auszuwählen. Preislisten in einer anderen Währung können dem Unterauftrag nicht zugeordnet werden. Die Kosten für Zeit, Spesen und Materialien, die Lieferantenressourcen aus diesem Untervertrag liefern, werden in dieser Währung im Projekt erfasst. Nach dem Speichern des Unterauftragsdatensatzes kann die Währung des Unterauftrags nicht mehr geändert werden.|
    | Vertragseinheit | Die Abteilung des Unternehmens, die mit dem Lieferanten einen Kaufvertrag oder eine Fremdarbeit abschließt. | Kein Wert |
    | Zahlungsbedingungen | Die Zahlungsbedingungen für Kreditorenrechnungen, die auf diesem Untervertrag ausgestellt werden. Der Standardwert wird automatisch aus dem Kreditorenkonto eingegeben. | Zahlungsbedingungen aus dem Untervertrag werden in alle Kreditorenrechnungen kopiert, die sich auf diesen Untervertrag beziehen. Zahlungsbedingungen können aktualisiert werden, wenn der Unterauftrag den Status **Entwurf** hat. | 
    | Zahlungsadresse | Die Adresse des Verkäufers, an den die Zahlungen gesendet werden müssen. Der Standardwert wird automatisch aus dem Kreditorenkonto eingegeben. | Die Zahlungsadresse aus dem Untervertrag wird als Zahlungsadresse in alle Kreditorenrechnungen übernommen, die für diesen Untervertrag erstellt werden. Die Zahlungsadresse kann aktualisiert werden, wenn der Unterauftrag den Status **Entwurf** hat.|
    | Name für Rechnungsadresse | Der Name der Person oder Abteilung im Unternehmen des Kreditors, die die Rechnung versendet. Der Standardwert wird automatisch aus dem Kreditorenkonto eingegeben. | Der Wert **Name für Rechnungsadresse** aus dem Untervertrag werden in alle Kreditorenrechnungen kopiert, die sich auf diesen Untervertrag beziehen. Dieses Feld kann aktualisiert werden, wenn der Unterauftrag den Status **Entwurf** hat.|
    | Rechnungsadresse | Die Adresse, die auf Rechnungen des Kreditors verwendet wird. Der Standardwert wird automatisch aus dem Kreditorenkonto eingegeben. | Diese Adresse ist die „Rechnung von“-Adresse auf Kreditorenrechnungen, die für diesen Untervertrag erstellt werden. |
    | Zwischensumme | Wenn ein Unterauftrag keine Zeilen hat, geben Sie die Auftragszwischensumme vor Steuern ein. Wenn die Fremdarbeit Positionen hat, ist dieses Feld schreibgeschützt. Der angezeigte Betrag ist der Zwischensummenbetrag aus allen Zeilen des Lohnauftrags. | Kein Wert |
    | Gesamtsteuer | Wenn ein Unterauftrag keine Zeilen hat, geben Sie die gesamten Steuern auf diesem Lohnauftrag an. Wenn die Fremdarbeit Positionen hat, ist dieses Feld schreibgeschützt. Der angezeigte Betrag ist die Gesamtsumme an Steuern aus allen Zeilen des Lohnauftrags. | Kein Wert |
    | Gesamtbetrag | Dieses berechnete Feld zeigt den Gesamtbetrag der Fremdarbeitsposition nach Einbeziehung der Steuern an. | Kein Wert |
    | Bestätigtes Datum | Das Datum, zu dem der Lohnauftrag bestätigt wurde. | Kein Wert |
    | Angefordert von | Standardmäßig ist dieses Feld auf den Namen des Benutzers gesetzt, der den Untervertrag erstellt. Der Ersteller des Untervertrags kann jedoch den Wert ändern, um die Person anzugeben, für die er den Untervertrag erstellt. | Kein Wert |
    | Konto-Manager des Zulieferers | Der Name des primären Kontakts des Kreditorenkontos. Der Standardwert wird automatisch aus dem Kreditorenkonto eingegeben. Sie können einen anderen Kontakt als Vendor Account Manager des Lohnbearbeiters auswählen. | Sie können E-Mail-Benachrichtigungen einrichten, um den Kontakt zu benachrichtigen, wenn aufgrund von Preisverhandlungen Änderungen am Unterauftrag vorgenommen werden. |
