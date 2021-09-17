---
title: Kopfzeilendetails für Fremdarbeiten
description: In diesem Thema werden die Funktionen erläutert, die in der Kopfzeile für Fremdarbeiten in Project Operations bereitgestellt werden.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323640"
---
# <a name="header-details-for-subcontracts"></a>Kopfzeilendetails für Fremdarbeiten

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

In diesem Thema werden die Funktionen erläutert, die in der Kopfzeile für Fremdarbeiten in Dynamics 365 Project Operations bereitgestellt werden.

Da ein Projektmanager Projekte plant und ausführt, kann er Subunternehmer beschäftigen und Produkte und Dienstleistungen von Lieferanten kaufen. Wenn ein Projektmanager Produkte oder Dienstleistungen kaufen muss, kann er in Project Operations eine Fremdarbeit erstellen.

Gehen Sie wie folgt vor, um eine Fremdarbeit zu erstellen.

1. Wählen Sie im Navigationsbereich **Fremdarbeiten** und auf der Seite **Fremdarbeit** **Neu** aus.
2. Geben Sie die gewünschten Informationen ein und wählen Sie anschließend **Speichern**.

    Die folgende Tabelle enthält Informationen zu den Feldern auf der Kopfzeilenseite des Fremdauftrags.

    | **Feld** | **Beschreibung** |
    | --- | --- | 
    | Name | Der Name der Fremdarbeit. |
    | Beschreibung | Eine kurze Beschreibung der Servicees und Produkte, die in der Fremdarbeit gekauft werden. |
    | Hersteller | Der Name des Unternehmens, von dem die Produkte und Dienstleistungen gekauft werden. Dieser Firmendatensatz hat den Beziehungstyp **Kreditor** oder **Lieferant**. |
    | Datum der Fremdarbeit | Das Datum, an dem die Fremdarbeit erstellt wird. |
    | Statusgrund | Der Status der Fremdarbeit. |
    | Währung | Die Währung, in der Produkte und Dienstleistungen gekauft werden. Der Wert in diesem Feld wird standardmäßig vom Kreditorenkonto verwendet, kann jedoch geändert werden. Projektpreislisten, die für die Preisfindung von Produkten und Dienstleistungen in der Fremdarbeit verwendet werden, sollten in dieser Währung vorliegen. Preislisten in anderen Währungen können der Fremdarbeit nicht zugeordnet werden. Die im Rahmen dieser Fremdarbeit anfallenden Kosten für Produkte und Dienstleistungen werden im Projekt in dieser Währung erfasst. |
    | Vertragseinheit | Die Abteilung des Unternehmens, die mit dem Lieferanten einen Kaufvertrag oder eine Fremdarbeit abschließt. |
    | Zahlungsbedingungen | Die Zahlungsbedingungen auf den Lieferantenrechnungen, die für diese Fremdarbeit ausgestellt werden. Der Wert in diesem Feld wird standardmäßig vom Kreditorfirmendatensatz verwendet. |
    | Zahlungsadresse | Die Adresse, an die die Zahlung auf Kreditorenrechnungen gesendet wird. Der Wert in diesem Feld wird standardmäßig vom Kreditorfirmendatensatz verwendet. |
    | Name für Rechnungsadresse | Der Name der Person oder Abteilung im Unternehmen des Kreditors, die die Rechnung versendet. Der Wert in diesem Feld stammt standardmäßig aus dem Kreditorenfirmendatensatz und wird als Name des Hauptkontakts auf Kreditorenrechnungen verwendet, die für diese Fremdarbeit erstellt wurden. |
    | Rechnungsadresse | Die auf Rechnungen dieses Kreditors verwendete Adresse. Der Wert in diesem Feld wird standardmäßig vom Kreditorfirmendatensatz verwendet. Diese Adresse wird auch als Rechnungsadresse auf Kreditorenrechnungen verwendet, die für diese Fremdarbeit erstellt wurden. |
    | Zwischensumme | Wenn eine Fremdarbeit keine Positionen hat, geben Sie in dieses Feld einen Wert ein, der die Auftragszwischensumme vor Steuern angibt. Wenn die Fremdarbeit Positionen hat, ist dieses Feld schreibgeschützt. Der angezeigte Betrag ist der Zwischensummenbetrag aus allen Zeilen der Fremdarbeit. |
    | Gesamtsteuer | Wenn eine Fremdarbeit keine Positionen hat, geben Sie in dieses Feld einen Wert ein, der die Steuern auf diese Fremdarbeit angibt. Wenn die Fremdarbeit Positionen hat, ist dieses Feld schreibgeschützt. Der angezeigte Betrag ist der Summe der Steuern aus allen Positionen der Fremdarbeit. |
    | Gesamtbetrag |  Dieses berechnete Feld zeigt den Gesamtbetrag der Fremdarbeitsposition nach Einbeziehung der Steuern an.  |
    | Bestätigtes Datum | Das Datum, zu dem die Fremdarbeit bestätigt wurde.  |
    | Angefordert von | Der Wert in diesem Feld ist standardmäßig der Name des Benutzers, der die Fremdarbeit erstellt. Dieser Wert kann vom Ersteller der Fremdarbeit geändert werden, um die Person anzugeben, in deren Namen er die Fremdarbeit erstellt.  |
    | Konto-Manager des Zulieferers | Der Name des primären Kontakts des Kreditorenkontos. Der Wert in diesem Feld wird standardmäßig vom Kreditorfirmendatensatz verwendet. Dieser Feldwert kann vom Benutzer geändert werden, um einen anderen Kontakt als Vendor Account Manager der Fremdarbeit auszuwählen. E-Mail-Benachrichtigungen und Preisverhandlungen können von diesem Kontakt konfiguriert und gesendet werden. |


