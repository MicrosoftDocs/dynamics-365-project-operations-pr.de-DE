---
title: Eine Proforma-Rechnung verwalten
description: Dieses Thema enthält Informationen zum Verwalten und zum Arbeiten mit Proforma-Rechnungen.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f3aab57f159dbb522ebe5d24dc3693034f6f81f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181451"
---
# <a name="manage-a-proforma-invoice"></a>Eine Proforma-Rechnung verwalten

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

In Dynamics 365 Project Operations werden Proforma-Rechnungen als Erweiterung der Rechnungen in Dynamics 365 Sales erstellt. Es gibt jedoch viele Unterschiede im Rechnungsstellungsprozess zwischen Sales und Project Operations, wenn es um die Fakturierung geht. Beispielsweise ist es nicht möglich, eine neue Rechnung aus der Seite **Rechnungsliste** in Project Operations zu erstellen, dies ist jedoch in Sales möglich. Diese Unterschiede und Erweiterungen unterstützen Rechnungsstellungsprozesse für Projekte, die sich von einer typischen Rechnung für einen Kundenauftrag unterscheiden.

> [!IMPORTANT]
> Rechnungen sind in Sales und Project Operations aufgrund der Unterschiede nicht austauschbar.

## <a name="invoice-header"></a>Rechnungskopf

Die folgenden Informationen sind in einem Proforma-Rechnungskopf in Project Operations verfügbar.

| Feld | Position | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| **Rechnungs-ID** | Registerkarte **Zusammenfassung** | Die ID wird bei Erstellung der Proforma-Rechnung automatisch generiert. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Dieses Feld wird als Referenz für jede Proforma-Rechnung verwendet. |
| **Name** | Registerkarte **Zusammenfassung** | Standardmäßig auf den Namen des Projektvertrags festgelegt. Dieses Feld kann vom Benutzer bearbeitet werden. | &nbsp;  |
| **Währung** | Registerkarte **Zusammenfassung** | Standardmäßig auf die Währung des Projektvertrags festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |&nbsp; |
| **Preisliste** | Registerkarte **Zusammenfassung** | Standardmäßig auf die Preisliste des Projektvertrags festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Verkaufschance** | Registerkarte **Zusammenfassung** | Der Verweis auf die verknüpfte Opportunity. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp;  |
| **Vertrag** | Registerkarte **Zusammenfassung** | Verweis auf den verknüpften Projektvertrag. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Kunde** | Registerkarte **Zusammenfassung** | Verweis auf den verknüpften Projektvertrag. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |&nbsp;  |
| **Beschreibung** | Registerkarte **Zusammenfassung** | Das Textfeld, das die Rechnung beschreibt. Dieses Feld kann vom Benutzer bearbeitet werden. | &nbsp; |
| **Rechnungsadresse** und verwandte Felder | Registerkarte **Zusammenfassung** | Die Standardeinstellungen werden vom Projektvertragskunden festgelegt. Dieses Feld kann vom Benutzer bearbeitet werden.  | &nbsp; |
| **Status** | Registerkarte **Zusammenfassung** | Legt die folgenden Optionen fest: **Aktiv**, **Geschlossen**, **Bezahlt** und **Abgebrochen** und kann vom Benutzer bearbeitet werden. | Nicht unterstützte Status für Projektvorgänge umfassen **Geschlossen** und **Abgebrochen**. </br> Der Status ist auf **Aktiv** festgelegt, wenn die Rechnung erstellt wird. </br>Der Status sollte auf **Bezahlt** gesetzt sein, nachdem die Rechnung bestätigt wurde. |
| **Projektrechnungsstatus** | Registerkarte **Zusammenfassung** | Legt die folgenden Optionen fest: **Entwurf**, **In Überprüfung** und **Bestätigt** und kann vom Benutzer bearbeitet werden. | In den Status **Entwurf** und **In Überprüfung** kann die Rechnung bearbeitet werden. Die Rechnung kann nach Bestätigung nicht mehr bearbeitet werden. |
| **Angebotsbetrag** | Registerkarte **Zusammenfassung** | Die Summe der Beträge auf allen Rechnungspositionen nach Vorschüssen und Abzügen. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | In diesem Feld wird der Endbetrag berechnet. |
| **Rabatt (%)** | Registerkarte **Zusammenfassung** | Dieses Feld kann bearbeitet werden, um einen Rabattprozentsatz einzugeben. Dieses Feld wird von der Project Operations-Funktionalität nicht unterstützt. | Dieses Feld wird nicht unterstützt. |
| **Rabattbetrag** | Registerkarte **Zusammenfassung** | Dieses Feld kann bearbeitet werden, um den Rabattbetrag einzugeben. Dieses Feld wird von der Project Operations-Funktionalität nicht unterstützt. | Dieses Feld wird nicht unterstützt. |
| **Rabattierter Betrag** | Registerkarte **Zusammenfassung** | Der Gesamtrechnungsbetrag nach Anwendung der Rabatte. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | In diesem Feld wird der Endbetrag berechnet. |
| **Frachtgebühr** | Registerkarte **Zusammenfassung** | Dieses Feld kann bearbeitet werden, um die Frachtgebühr einzugeben. Dieses Feld wird von der Project Operations-Funktionalität nicht unterstützt. | Dieses Feld wird nicht unterstützt. |
| **Steuern gesamt** | Registerkarte **Zusammenfassung** | Die Gesamtsteuer aus allen Rechnungspositionen auf der Rechnung. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Keine |
| **Gesamtbetrag** | Registerkarte **Zusammenfassung** | Die Summe des Betrags nach Rabatten und Steuern. | Die Summe ist der Betrag, den der Kunde bezahlen muss. |

## <a name="project-based-invoice-lines"></a>Projektbasierte Rechnungszeilen

Im Project Operations gibt es für jede Projektvertragsposition immer eine Rechnungsposition. Die Rechnungsposition wird auch dann erstellt, wenn keine Istdaten vorhanden sind. Die folgenden Informationen sind in einer Proforma-Rechnungszeile verfügbar.

| Feld | Position | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| **Rechnungs-ID** | Registerkarte **Allgemein** | Der Verweis auf die Rechnungs-ID. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Über den Link „Rechnungs-ID“ können Sie zurück zum Rechnungskopf navigieren. |
| **Name** | Registerkarte **Allgemein** | Der Name der Rechnungsposition, der standardmäßig aus dem Namen der Vertragszeile festgelegt wird. Dieses Feld kann vom Benutzer bearbeitet werden. | &nbsp; |
| **Project** | Registerkarte **Allgemein** | Das Projekt der verwandten Projektvertragszeile. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Über den Projektlink können Sie zum Projekt navigieren. |
| **Fakturierungsmethode** | Registerkarte **Allgemein** | Die Abrechnungsmethode der verwandten Projektvertragszeile. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Vertragszeilenbetrag** | Registerkarte **Allgemein** | Der Vertragsbetrag der verwandten Projektvertragszeile. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Fakturiert bis Datum** | Registerkarte **Allgemein** | Die Summe der Beträge in allen Rechnungszeilendetails dieser Rechnung. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Betrag** | Registerkarte **Allgemein** | Die Summe der Beträge in allen fakturierbaren Rechnungszeilendetails dieser Rechnung. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | In diesem Feld wird der Endbetrag auf dem Rechnungskopf berechnet. |
| **Steuer** | Registerkarte **Allgemein** | Die Summe der Steuerbeträge in allen Rechnungszeilendetails dieser Rechnungszeile. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | In diesem Feld wird der Endsteuerbetrag auf dem Rechnungskopf berechnet. |
| **Erweiterter Betrag** | Registerkarte **Allgemein** | Die Summe der Gesamtbeträge (**Steuer + Beträge**) in allen fakturierbaren Rechnungszeilendetails dieser Rechnungszeile. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | In diesem Feld wird der Endbetrag auf dem Rechnungskopf berechnet. |

## <a name="invoice-line-details"></a>Rechnungspositionsdetails

Jede Rechnungsposition in einer Projektrechnung enthält Details zur Rechnungsposition. Diese Zeilendetails beziehen sich auf die nicht in Rechnung gestellten Verkaufszahlen und Meilensteine, die sich auf die Vertragszeile beziehen, auf die in der Rechnungszeile verwiesen wird. All diese Transaktionen sind als **Bereit für die Rechnungsstellung** markiert.

Für die **Zeit- und Materialrechnung**-Zeile werden Rechnungszeilendetails in **Fakturierbar**, **Nicht fakturierbar** und **Kostenlos** auf der Seite **Rechnungszeile** gruppiert. **Fakturierbare Rechnungszeile**-Details addieren sich zur Rechnungszeilensumme. **Kostenlos** und **Nicht fakturierbare Istwerte** addieren Sie nicht zur Rechnungszeilensumme.

Für die **Festpreisrechnung**-Zeile werden Rechnungszeilendetails aus Meilensteinen erstellt, die als **Bereit für die Rechnungsstellung** auf der zugehörigen Vertragszeile gekennzeichnet sind. Nachdem die Rechnungszeilendetails aus einem Meilenstein erstellt wurde, wird der Abrechnungsstatus des Meilensteins auf **Erstellte Kundenrechnung** aktualisiert.

### <a name="edit-invoice-line-details"></a>Rechnungspositionsdetails bearbeiten

Die folgenden Felder sind in den Rechnungszeilendetails verfügbar, die durch einen nicht in Rechnung gestellten tatsächlichen Umsatz abgesichert sind.

| Feld | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- |
| **Rechnungsposition** | Ein Verweis auf die **Rechnungsposition-ID**. Schreibgeschütztes Feld, Bearbeitung gesperrt. | Über diesen Link können Sie zurück zum Rechnungskopf navigieren. |
| **Beschreibung** | Eine Beschreibung der Rechnungsposition. Standardmäßig über das Feld **Interne Kommentare** unter **Zeiteintrag** und über das Feld **Beschreibung** im **Ausgabeneintrag** festgelegt. Dieses Feld kann vom Benutzer bearbeitet werden.| &nbsp; |
| **Externe Beschreibung** | Eine Beschreibung der Rechnungsposition. Standardmäßig über das Feld **Externe Kommentare** unter **Zeiteintrag** und über das Feld **Beschreibung** im **Ausgabeneintrag** festgelegt. Dieses Feld kann vom Benutzer bearbeitet werden. | Diese Beschreibung kann verwendet werden, um zu bestimmen, was auf der gedruckten Rechnung stehen soll, die an den Kunden gesendet wird. In Project Operations verfügt eine Proforma-Rechnung nicht über alle erforderlichen Funktionen zum Konfigurieren der Druckeinstellungen für eine Rechnung. |
| **Startdatum** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Dieses Feld kann für ein neues Rechnungszeilendetail bearbeitet werden, das nicht von einer tatsächlichen Quelle unterstützt wird. |
| **Project** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Standardmäßig auf das Projekt der verwandten Projektzeile festgelegt. |
| **Aufgabe** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Das Feld kann für ein neues Rechnungszeilendetail bearbeitet werden, das nicht von einer tatsächlichen Quelle unterstützt wird. Eine Dropdown-Liste zeigt alle Aufgaben an, die der zugehörigen Projektvertragszeile zugeordnet sind.  |
| **Transaktionskategorie** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Dieses Feld kann für ein neues Rechnungszeilendetail bearbeitet werden, das nicht von einer tatsächlichen Quelle unterstützt wird. |
| **Rolle** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Dieses Feld kann für ein neues Rechnungszeilendetail bearbeitet werden, das nicht von einer tatsächlichen Quelle unterstützt wird. |
| **Buchbare Ressource** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Dieses Feld kann für ein neues Rechnungszeilendetail bearbeitet werden, das nicht von einer tatsächlichen Quelle unterstützt wird. |
| **Ressourcenzuordnungsunternehmen** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Dieses Feld kann für ein neues Rechnungszeilendetail bearbeitet werden, das nicht von einer tatsächlichen Quelle unterstützt wird. |
| **Ressourcenzuordnungseinheit** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Dieses Feld kann für ein neues Rechnungszeilendetail bearbeitet werden, das nicht von einer tatsächlichen Quelle unterstützt wird. |
| **Menge** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Dieses Feld kann für ein neues Rechnungszeilendetail bearbeitet werden, das nicht von einer tatsächlichen Quelle unterstützt wird. |
| **Einheitenzeitplan** | Für Zeit-Rechnungszeilendetails ist dies immer auf Zeit eingestellt und kann nicht bearbeitet werden. Für Ausgaben wird dies standardmäßig aus den tatsächlichen Quellkosten festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Standardmäßig auf **Zeit** auf einem neuen Rechnungszeilendetail eingestellt, das nicht durch ein tatsächliches gesichert ist. |
| **Einheit** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Dieses Feld kann für ein neues Rechnungszeilendetail bearbeitet werden, das nicht von einer tatsächlichen Quelle unterstützt wird |
| **Preis** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Dieses Feld kann für ein neues Rechnungszeilendetail bearbeitet werden, das nicht von einer tatsächlichen Quelle unterstützt wird. Wenn kein Wert eingegeben wird, wird dieser standardmäßig auf **Speichern** eingestellt. |
| **Währung** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Wird standardmäßig über den Rechnungskopf festgelegt, wenn ein neues Rechnungsdetail ohne tatsächliche Sicherung erstellt wird.  Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Betrag** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Berechnet als **Menge\*Preis** beim Erstellen eines neuen Rechnungsdetails ohne tatsächlichen Hintergrund. Es wird nach **Speichern** berechnet. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |
| **Steuer** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Dieses Feld kann vom Benutzer bearbeitet werden | Das Feld kann vom Benutzer bearbeitet werden, wenn ein neues Rechnungszeilendetail ohne Hintergrund erstellt wird. |
| **Erweiterter Betrag** | Ein berechnetes Feld, berechnet als **Betrag + Steuer**. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Fakturierungstyp** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Dieses Feld kann vom Benutzer bearbeitet werden. | Durch Auswählen von **Fakturierbar** wird die Zeile zur Rechnungszeilensumme hinzugefügt. **Kostenlos** und **Nicht fakturierbar** schließt es von der Rechnungszeilensumme aus. |
| **Transaktionstyp** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Standardmäßig auf **Fakturierte Umsätze** eingestellt und beim Erstellen eines neuen **Rechnungszeilendetail** ohne eine tatsächliche Unterstützung gesperrt.  |
| **Transaktionsklasse** | Standardmäßig aus der tatsächlichen Quelle festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Standardmäßig basierend darauf, ob der Benutzer ein **Zeit**-, **Kosten**- oder **Gebühren**-Rechnungszeilendetail beim Erstellen eines neuen **Rechnungszeilendetails** ohne tatsächliche Unterstützung erstellen möchte. Für Bearbeitung gesperrt. |

Die folgenden Felder sind in den Rechnungszeilendetails verfügbar, die durch einen Meilenstein abgesichert sind:

| Feld | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- |
| **Rechnungsposition** | Verweis auf die **Rechnungsposition-ID**. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | Über den Link können Sie zurück zum Rechnungskopf navigieren. |
| **Beschreibung** | Beschreibung der Rechnungsposition. Standardmäßig aus der Beschreibung des Quellmeilensteins festgelegt. | &nbsp; |
|**Externe Beschreibung** | Beschreibung des Rechnungszeilendetails, das standardmäßig aus der Beschreibung des Quellmeilensteins festgelegt wird. | Dieses Feld kann verwendet werden, um zu bestimmen, was auf der gedruckten Rechnung stehen soll, die an den Kunden gesendet wird. In Project Operations verfügt eine Proforma-Rechnung nicht über alle erforderlichen Funktionen zum Konfigurieren der Druckeinstellungen für eine Rechnung. |
| **Startdatum** | Standardmäßig über das **Meilenstein**-Datum auf dem Quellmeilenstein festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Project** | Standardmäßig aus dem Quellmeileinstein festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Aufgabe** | Standardmäßig aus dem Quellmeileinstein festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Transaktionskategorie** | Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Rolle** | Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Buchbare Ressource** | Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Ressourcenzuordnungseinheit** | Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Einheitenzeitplan** | Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Einheit** | Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Preis** | Standardmäßig aus der Menge des Quellmeilensteins festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Währung** | Standardmäßig aus dem Quellmeileinstein festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. |&nbsp; |
| **Betrag** | Standardmäßig aus der Menge des Quellmeilensteins festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Steuer** | Standardmäßig aus dem Steuerbetrag des Quellmeilensteins festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Erweiterter Betrag** | Standardmäßig aus dem erweiterten Betrag des Quellmeilensteins festgelegt. Dieses Feld kann vom Benutzer bearbeitet werden | &nbsp; |
| **Fakturierungstyp** | Immer standardmäßig auf **Fakturierbar** gesetzt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Transaktionstyp** | Standardmäßig aus dem Quellmeileinstein festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |
| **Transaktionsklasse** | Standardmäßig aus dem Quellmeileinstein festgelegt. Ein schreibgeschütztes Feld, das für die Bearbeitung gesperrt ist. | &nbsp; |

## <a name="refresh-invoice-transactions"></a>Transaktionen für Rechnung aktualisieren

Wenn Sie Istdaten haben, die nach dem Erstellen der Rechnung eingegangen sind, können Sie diese Istdaten in die Rechnung aufnehmen.

1. In der **Projektabrechnungsansicht** markieren Sie die Daten als **Bereit für die Rechnungsstellung**.   
2. Öffnen Sie den Entwurf der Proforma-Rechnung und auf dem Menüband **Aktionen** klicken Sie auf **Transaktionen für Rechnungszeile aktualisieren**.

  Dadurch werden Rechnungszeilendetails für alle tatsächlichen Daten erstellt, deren Datum überschritten und als **Bereit für die Rechnungsstellung** markiert, aber nicht in der Rechnung enthalten ist.


[!INCLUDE[footer-include](../includes/footer-banner.md)]