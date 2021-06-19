---
title: Eine projektbasierte Proforma-Rechnung verwalten
description: Dieses Thema enthält Informationen zur Verwaltung und Arbeit mit projektbasierten Proforma-Rechnungen.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b1b0f70f25d157e1d7e2d14dc011a048d698d299
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012540"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Eine projektbasierte Proforma-Rechnung verwalten

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

In Dynamics 365 Project Operations werden Proforma-Rechnungen als Erweiterung der Rechnungen in Dynamics 365 Sales erstellt. Es gibt jedoch viele Unterschiede im Rechnungsstellungsprozess zwischen Sales und Project Operations, wenn es um die Rechnungsstellung geht. Beispielsweise ist es nicht möglich, eine neue Rechnung über die Seite **Rechnungsliste** in Project Operations zu erstellen. Dies ist jedoch in Sales möglich. Diese Unterschiede und Erweiterungen unterstützen Rechnungsstellungsprozesse für Projekte, die sich von einer typischen Rechnung für einen Kundenauftrag unterscheiden.

> [!IMPORTANT]
> Rechnungen sind in Sales und Project Operations aufgrund der Unterschiede nicht austauschbar.

## <a name="invoice-header"></a>Rechnungskopf

Die folgenden Informationen sind in einem Proforma-Rechnungskopf in Project Operations verfügbar.

| Feld | Speicherort | Beschreibung |
| --- | --- | --- | 
| **Rechnungs-ID** | Registerkarte **Zusammenfassung** | Die ID wird bei Erstellung der Proforma-Rechnung automatisch generiert. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. Dieses Feld wird als Referenz für jede Proforma-Rechnung verwendet. |
| **Name** | Registerkarte **Zusammenfassung** | Standardmäßig auf den Namen des Projektvertrags festgelegt. Dieses Feld kann bearbeitet werden. | 
| **Währung** | Registerkarte **Zusammenfassung** | Standardmäßig auf die Währung des Projektvertrags festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Preisliste** | Registerkarte **Zusammenfassung** | Standardmäßig auf die Preisliste des Projektvertrags festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Verkaufschance** | Registerkarte **Zusammenfassung** | Der Verweis auf die verknüpfte Opportunity. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Vertrag** | Registerkarte **Zusammenfassung** | Verweis auf den verknüpften Projektvertrag. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Kunde** | Registerkarte **Zusammenfassung** | Verweis auf den verknüpften Projektvertrag. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Beschreibung** | Registerkarte **Zusammenfassung** | Das Textfeld, das die Rechnung beschreibt. Dieses Feld kann bearbeitet werden. | 
| **Rechnungsadresse** und verwandte Felder | Registerkarte **Zusammenfassung** | Die Standardeinstellungen werden vom Projektvertragskunden festgelegt. Dieses Feld kann bearbeitet werden.  | 
| **Status** | Registerkarte **Zusammenfassung** | Legt die folgenden Optionen fest: **Aktiv**, **Geschlossen**, **Bezahlt** und **Storniert** und kann bearbeitet werden. Nicht unterstützte Status für Project Operations umfassen **Geschlossen** und **Abgebrochen**. </br> Der Status ist auf **Aktiv** festgelegt, wenn die Rechnung erstellt wird. </br>Der Status sollte auf **Bezahlt** gesetzt sein, nachdem die Rechnung bestätigt wurde.  | 
| **Projektrechnungsstatus** | Registerkarte **Zusammenfassung** | Legt die folgenden Optionen fest: **Entwurf**, **In Überprüfung** und **Bestätigt** und kann bearbeitet werden. In den Status **Entwurf** und **In Überprüfung** kann die Rechnung bearbeitet werden. Die Rechnung kann nach Bestätigung nicht mehr bearbeitet werden. | 
| **Angebotsbetrag** | Registerkarte **Zusammenfassung** | Die Summe der Beträge auf allen Rechnungspositionen nach Vorschüssen und Abzügen. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist.  In diesem Feld wird der Endbetrag berechnet. | 
| **Rabatt (%)** | Registerkarte **Zusammenfassung** | Dieses Feld kann bearbeitet werden, um einen Rabattprozentsatz einzugeben. Dieses Feld wird von der Project Operations-Funktionalität nicht unterstützt. Dieses Feld wird nicht unterstützt.|  
| **Rabattbetrag** | Registerkarte **Zusammenfassung** | Dieses Feld kann bearbeitet werden, um den Rabattbetrag einzugeben. Dieses Feld wird von der Project Operations-Funktionalität nicht unterstützt. Dieses Feld wird nicht unterstützt. |  
| **Rabattierter Betrag** | Registerkarte **Zusammenfassung** | Der Gesamtrechnungsbetrag nach Anwendung der Rabatte. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. In diesem Feld wird der Endbetrag berechnet.  | 
| **Frachtgebühr** | Registerkarte **Zusammenfassung** | Dieses Feld kann bearbeitet werden, um die Frachtgebühr einzugeben. Dieses Feld wird von der Project Operations-Funktionalität nicht unterstützt. Dieses Feld wird nicht unterstützt. |
| **Steuern gesamt** | Registerkarte **Zusammenfassung** | Die Gesamtsteuer aus allen Rechnungspositionen auf der Rechnung. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Gesamtbetrag** | Registerkarte **Zusammenfassung** | Die Summe des Betrags nach Rabatten und Steuern. Die Summe ist der Betrag, den der Kunde bezahlen muss. | 

## <a name="project-based-invoice-lines"></a>Projektbasierte Rechnungszeilen

Im Project Operations gibt es für jede Projektvertragsposition immer eine Rechnungsposition. Die Rechnungsposition wird auch dann erstellt, wenn keine Istdaten vorhanden sind. Die folgenden Informationen sind in einer Proforma-Rechnungszeile verfügbar.

| Feld | Speicherort | Beschreibung | 
| --- | --- | --- |
| **Rechnungs-ID** | Registerkarte **Allgemein** | Der Verweis auf die Rechnungs-ID. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. Über den Link „Rechnungs-ID“ können Sie zurück zum Rechnungskopf navigieren. | 
| **Name** | Registerkarte **Allgemein** | Der Name der Rechnungsposition, der standardmäßig aus dem Namen der Vertragszeile festgelegt wird. Dieses Feld kann bearbeitet werden. |
| **Project** | Registerkarte **Allgemein** | Das Projekt der verwandten Projektvertragszeile. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. Über den Projektlink können Sie zum Projekt navigieren. | 
| **Fakturierungsmethode** | Registerkarte **Allgemein** | Die Abrechnungsmethode der verwandten Projektvertragszeile. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Vertragszeilenbetrag** | Registerkarte **Allgemein** | Der Vertragsbetrag der verwandten Projektvertragszeile. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Fakturiert bis Datum** | Registerkarte **Allgemein** | Die Summe der Beträge in allen Rechnungszeilendetails dieser Rechnung. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Betrag** | Registerkarte **Allgemein** | Die Summe der Beträge in allen fakturierbaren Rechnungszeilendetails dieser Rechnung. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. In diesem Feld wird der Endbetrag auf dem Rechnungskopf berechnet. | 
| **Steuer** | Registerkarte **Allgemein** | Die Summe der Steuerbeträge in allen Rechnungszeilendetails dieser Rechnungszeile. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. In diesem Feld wird der Endsteuerbetrag auf dem Rechnungskopf berechnet. | 
| **Erweiterter Betrag** | Registerkarte **Allgemein** | Die Summe der Gesamtbeträge (**Steuer + Beträge**) in allen fakturierbaren Rechnungszeilendetails dieser Rechnungszeile. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. In diesem Feld wird der Endbetrag auf dem Rechnungskopf berechnet. |

## <a name="invoice-line-details"></a>Rechnungspositionsdetails

Jede Rechnungsposition in einer Projektrechnung enthält Details zur Rechnungsposition. Diese Zeilendetails beziehen sich auf die nicht in Rechnung gestellten Verkaufszahlen und Meilensteine, die sich auf die Vertragszeile beziehen, auf die in der Rechnungszeile verwiesen wird. All diese Transaktionen sind als **Bereit für die Rechnungsstellung** markiert.

Für eine **Zeit- und Materialrechnung**-Zeile werden Rechnungszeilendetails in **Fakturierbar**, **Nicht fakturierbar** und **Kostenlos** auf der Seite **Rechnungszeile** gruppiert. **Fakturierbare Rechnungszeile**-Details addieren sich zur Rechnungszeilensumme. **Kostenlos** und **Nicht fakturierbare Istwerte** addieren Sie nicht zur Rechnungszeilensumme.

Für eine **Festpreisrechnung**-Zeile werden Rechnungszeilendetails aus Meilensteinen erstellt, die als **Bereit für die Rechnungsstellung** auf der zugehörigen Vertragszeile gekennzeichnet sind. Nachdem die Rechnungszeilendetails aus einem Meilenstein erstellt wurde, wird der Abrechnungsstatus des Meilensteins auf **Erstellte Kundenrechnung** aktualisiert.

### <a name="edit-invoice-line-details"></a>Rechnungspositionsdetails bearbeiten

Die folgenden Felder sind in den Rechnungszeilendetails verfügbar, die durch einen nicht in Rechnung gestellten tatsächlichen Umsatz abgesichert sind.

| Feld | Beschreibung |
| --- | --- | 
| **Rechnungsposition** | Ein Verweis auf die **Rechnungsposition-ID**. Dieses Feld ist schreibgeschützt und für die Bearbeitung gesperrt. Über diesen Link können Sie zurück zum Rechnungskopf navigieren. | 
| **Beschreibung** | Eine Beschreibung der Rechnungsposition. Standardmäßig über das Feld **Interne Kommentare** unter **Zeiteintrag** und über das Feld **Beschreibung** im **Ausgabeneintrag** festgelegt. Das Feld kann bearbeitet werden.| 
| **Externe Beschreibung** | Eine Beschreibung der Rechnungsposition. Standardmäßig über das Feld **Externe Kommentare** unter **Zeiteintrag** und über das Feld **Beschreibung** im **Ausgabeneintrag** festgelegt. Das Feld kann bearbeitet werden. Diese Beschreibung kann verwendet werden, um zu bestimmen, was auf der gedruckten Rechnung stehen soll, die an den Kunden gesendet wird. In Project Operations verfügt eine Proforma-Rechnung nicht über alle erforderlichen Funktionen zum Konfigurieren der Druckeinstellungen für eine Rechnung. | 
| **Startdatum** | Dies ist ein schreibgeschütztes Feld, das standardmäßig aus der tatsächlichen Quelle festgelegt wird. |
| **Project** | Dies ist ein schreibgeschütztes Feld, das standardmäßig von der tatsächlichen Quelle zum Projekt in der zugehörigen Vertragszeile festgelegt wird. |  
| **Aufgabe** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Transaktionskategorie** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Rolle** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |  
| **Buchbare Ressource** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Ressourcenzuordnungsunternehmen** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Ressourcenzuordnungseinheit** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Menge** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |  
| **Einheitenzeitplan** | Für Zeit-Rechnungszeilendetails ist dies immer auf Zeit eingestellt und kann nicht bearbeitet werden. Für Ausgaben wird dies standardmäßig aus den tatsächlichen Quellkosten festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Einheit** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |  
| **Preis** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Währung** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Betrag** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Steuer** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Das Feld kann bearbeitet werden.| 
| **Erweiterter Betrag** | Ein berechnetes Feld, berechnet als **Betrag + Steuer**. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Fakturierungstyp** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Das Feld kann bearbeitet werden. Durch Auswählen von **Fakturierbar** wird die Zeile zur Rechnungszeilensumme hinzugefügt. **Kostenlos** und **Nicht fakturierbar** schließt es von der Rechnungszeilensumme aus.| 
| **Produkt auswählen** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Produkt** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Produktname** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |  
| **Beschreibung des manuell einzutragenden Produkts** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Transaktionstyp** | Dies ist ein schreibgeschütztes Feld, das standardmäßig aus der tatsächlichen Quelle auf **Fakturierte Umsätze** festgelegt wird. |  
| **Transaktionsklasse** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 

Die folgenden Felder sind in den Rechnungszeilendetails verfügbar, die durch einen Meilenstein abgesichert sind.

| Feld | Beschreibung |
| --- | --- | 
| **Rechnungsposition** | Verweis auf die **Rechnungsposition-ID**. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. Über den Link können Sie zurück zum Rechnungskopf navigieren.  | 
| **Beschreibung** | Beschreibung der Rechnungsposition. Standardmäßig aus der Beschreibung des Quellmeilensteins festgelegt. | 
|**Externe Beschreibung** | Beschreibung des Rechnungszeilendetails, das standardmäßig aus der Beschreibung des Quellmeilensteins festgelegt wird. Dieses Feld kann verwendet werden, um zu bestimmen, was auf der gedruckten Rechnung stehen soll, die an den Kunden gesendet wird. In Project Operations verfügt eine Proforma-Rechnung nicht über alle erforderlichen Funktionen zum Konfigurieren der Druckeinstellungen für eine Rechnung. | 
| **Startdatum** | Standardmäßig über das **Meilenstein**-Datum auf dem Quellmeilenstein festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Project** | Standardmäßig aus dem Quellmeileinstein festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Aufgabe** | Standardmäßig aus dem Quellmeileinstein festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Transaktionskategorie** | Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Rolle** | Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Buchbare Ressource** | Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Ressourcenzuordnungseinheit** | Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Einheitenzeitplan** | Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Einheit** | Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Preis** | Standardmäßig aus der Menge des Quellmeilensteins festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Währung** | Standardmäßig aus dem Quellmeileinstein festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Betrag** | Standardmäßig aus der Menge des Quellmeilensteins festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Steuer** | Standardmäßig aus dem Steuerbetrag des Quellmeilensteins festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Erweiterter Betrag** | Standardmäßig aus dem erweiterten Betrag des Quellmeilensteins festgelegt. Das Feld kann bearbeitet werden. | 
| **Fakturierungstyp** | Immer standardmäßig auf **Fakturierbar** gesetzt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Transaktionstyp** | Standardmäßig aus dem Quellmeileinstein festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 
| **Transaktionsklasse** | Standardmäßig aus dem Quellmeileinstein festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | 

## <a name="refresh-invoice-transactions"></a>Transaktionen für Rechnung aktualisieren

Wenn Sie Istdaten haben, die nach dem Erstellen der Rechnung eingegangen sind, können Sie diese Istdaten in die Rechnung aufnehmen.

1. In der **Projektabrechnungsansicht** markieren Sie die Daten als **Bereit für die Rechnungsstellung**.   
2. Öffnen Sie den Entwurf der Proforma-Rechnung und wählen Sie im **Aktionen**-Menüband **Transaktionen für Rechnungszeile aktualisieren** aus.

  Rechnungszeilendetails werden für alle tatsächlichen Daten erstellt, die über das Datum hinausgehen und als **Bereit für die Rechnungsstellung** gekennzeichnet, jedoch nicht auf der Rechnung enthalten sind.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
