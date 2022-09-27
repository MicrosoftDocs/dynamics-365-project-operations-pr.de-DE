---
title: Fremdarbeitspositionsmeilensteine
description: Dieser Artikel erklärt, wie Sie einen auf Meilensteinen basierenden Rechnungszeitplan für einen Untervertrag mit einem Lieferanten erstellen und pflegen können.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 431a57adf82c79f72d44886636183d48e0931f53
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522463"
---
# <a name="subcontract-line-milestones"></a>Fremdarbeitspositionsmeilensteine

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

In Dynamics 365 Project Operations kann eine Fremdarbeitsposition mit Festpreisabrechnungsmethode einen meilensteinbasierten Rechnungsplan mit dem Kreditor festlegen.

Meilensteine für die Kreditorenrechnung können automatisch mit einer festgelegten Häufigkeit generiert werden, oder Sie können sie manuell erstellen.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Erstellen Sie automatisch einen meilensteinbasierten Rechnungsplan für eine Fremdarbeitsposition

Führen Sie die folgenden Schritte aus, um automatisch einen meilensteinbasierten Rechnungsplan für einen festen Satz gleichmäßig verteilter Meilensteine zu generieren.

1. Wechseln Sie zu **Einstellungen** > **Rechnungsintervalle**, und richten Sie die Rechnungsintervalle für Fremdarbeitspositionen ein.
2. Öffnen Sie die **Fremdarbeiten**-Seite, öffnen Sie die Fremdarbeit, mit der Sie arbeiten möchten, und öffnen Sie dann die Festpreis-Fremdarbeitsposition, für die Sie einen Meilensteinplan erstellen möchten.
3. Auf der **Meilensteine der Fremdarbeitsposition**-Registerkarte wählen Sie **Periodische Meilensteine generieren** aus.
4. Geben Sie im Dialogfenster einen Datumsbereich, die Anzahl der Meilensteine und die Rechnungshäufigkeit ein oder wählen Sie sie aus. Sie können ein Startdatum oder die Anzahl der Meilensteine und die Rechnungshäufigkeit oder das Startdatum oder das Enddatum und die Rechnungshäufigkeit auswählen. Sie können das Enddatum und die Anzahl der Meilensteine nicht auswählen.
Anhand dieser Informationen generiert das System Meilensteine und Datensätze, die im **Meilensteine**-Raster angezeigt werden.

   - **Meilensteinname** – Der Name des Meilensteins wird basierend auf der Rechnungshäufigkeit auf das Datum des Meilensteins gesetzt.
   - **Meilensteindatum** – Das Datum basierend auf der Rechnungshäufigkeit.
   - **Meilensteinbetrag** – Wird berechnet, indem der Zwischensummenbetrag in der Fremdarbeitsposition durch die Anzahl der Meilensteine dividiert wird.

Wenn die Fremdarbeitsposition einen Wert im Feld **Geschätzter Steuerbetrag** aufweist, wird dieser Wert jedem Meilenstein gleichmäßig hinzugefügt, wenn periodische Meilensteine generiert werden.

Die Summe des Fremdarbeitspositions-Meilensteinbetrags sollte gleich dem Wert der Fremdarbeitsposition sein. Wenn sie nicht gleich sind, tritt ein Fehler auf. Sie können den Fehler beheben und überprüfen, ob die Meilensteinsumme dem Fremdarbeitspositionswert entspricht, indem Sie Meilenstein- und Steuerbeträge erstellen, bearbeiten oder löschen. Nachdem die Änderungen vorgenommen wurden, speichern und aktualisieren Sie die Seite, um sicherzustellen, dass keine Fehler mehr auftreten.

## <a name="manually-create-subcontract-line-milestones"></a>Fremdarbeitspositions-Meilensteine manuell erstellen

Festpreismeilensteine in einer Fremdarbeitsposition können manuell generiert werden, wenn sie nicht regelmäßig aufgeteilt werden. Führen Sie die folgenden Schritte aus, um manuell einen Meilenstein für eine Fremdarbeitsposition zu erstellen.

1. Wählen Sie im Navigationsbereich **Fremdarbeiten** aus, und öffnen Sie die Fremdarbeit, mit der Sie arbeiten möchten.
2. Öffnen Sie die Festpreis-Fremdarbeitsposition, für die Sie einen Meilenstein erstellen möchten.
3. Auf der **Meilensteine für die Fremdarbeitspositions**-Registerkarte wählen Sie im Unterraster **+ Neuer Meilenstein für die Fremdarbeitsposition**.
4. Auf der **Neuer Meilenstein für die Fremdarbeitsposition**-Seite geben Sie die erforderlichen Informationen basierend auf der folgenden Tabelle ein.

    | Feld | Beschreibung |Funktionsauswirkung|
    | --- | --- |----------------------|
    | Meilensteinname | Der Namen des Meilensteins. |Dies wird als erste Spalte in allen Nachschlagevorgängen basierend auf Fremdauftragspositionsmeilensteinen angezeigt. Der auf Grundlage dieses Meilensteins erstellte Kreditorenrechnungsposten verwendet auch den Namen des Unterauftragsposten-Meilensteins als Standardnamen des Kreditorenrechnungspostens.|
    | Beschreibung | Eine Beschreibung des Meilensteins. |Der auf Grundlage dieses Meilensteins erstellte Kreditorenrechnungsposten verwendet auch die Beschreibung des Unterauftragsposten-Meilensteins als Standardbeschreibung des Kreditorenrechnungspostens.|
    | Meilensteindatum | Das Datum, an dem der automatische Rechnungserstellungsprozess nach dem Status dieses Meilensteins suchen soll, um ihn für die Rechnungsstellung zu berücksichtigen.| Dieser Wert wird als Standarddatum der Kreditorenrechnungsposition bei der Rechnungsstellung für diese Unterauftragsposition verwendet. |
    | Höhe | Der Betrag oder Wert des Meilensteins, der dem Kunden in Rechnung gestellt wird. |Dieser Wert wird als Standardbetrag der Kreditorenrechnungsposition bei der Rechnungsstellung für diese Unterauftragsposition verwendet. |
    | Steuer | Der auf den Meilenstein angewendete Steuerbetrag.| Dieser Wert wird als Standardsteuerbetrag der Kreditorenrechnungsposition bei der Rechnungsstellung für diese Unterauftragsposition verwendet. |
    | Betrag nach Steuer | Dieses Feld ist schreibgeschützt und wird berechnet als Vertraglicher Betrag + Steuern.|Dieser Wert wird als Standardwert der Kreditorenrechnungsposition bei der Rechnungsstellung für diese Unterauftragsposition verwendet. |
    | Rechnungsstatus | Beim Anlegen des Meilensteins wird dieser Status immer auf **Nicht bereit für die Rechnungsstellung** festgelegt.|  Wenn der Status **Bereit für Rechnung** ist, enthält die Kreditorenrechnungserstellung diesen Meilenstein in der Kreditorenrechnung. |

5. Klicken Sie auf **Speichern und schließen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
