---
title: Eine projektbasierte Angebotsposition kalkulieren
description: Dieses Thema enthält Informationen zum Erstellen einer projektbasierten Schätzung in einer Angebotsposition.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dbd3876e555ee6bc70308ef11a3528a5dd8b6a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273512"
---
# <a name="estimating-a-project-based-quote-line"></a>Eine projektbasierte Angebotsposition kalkulieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Eine projektbasierte Angebotsposition enthält Details, die bei der Schätzung der Kosten und potenziellen Einnahmen der mit der Lieferung der Angebotsposition verbundenen Arbeiten hilfreich sind.

Um eine projektbasierte Angebotsposition zu schätzen, wählen Sie in der projektbasierten Angebotsposition die Option **Angebotspositionsdetail**-Registerkarte. Es gibt zwei Möglichkeiten, eine Schätzung für eine projektbasierte Angebotsposition zu erstellen:

- Erstellen Sie die Schätzung manuell direkt in der Angebotsposition mithilfe von Angebotspositionsdetails 
- Erstellen Sie ein Projekt und einen Projektplan und ordnen Sie das Projekt und die Aufgaben im Projekt der Angebotsposition zu. Der Prozess zum Importieren der Schätzungen im Projektplan in die Angebotsposition basierend auf den von Ihnen angegebenen Informationen wird aktiviert.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Schätzungen direkt aus einer projektbasierten Angebotsposition erstellen

Um eine Schätzung für eine projektbasierte Angebotsposition zu erstellen, wählen Sie die Option **Angebotspositionsdetail**-Registerkarte. Die Position, die Sie auf dieser Registerkarte erstellen, fasst den angegebenen Wert für diese Angebotsposition zusammen. 

Wählen Sie zum Erstellen von Angebotszeilendetails **+ Neues Angebotszeilendetail** im **Detailinformationen zur Angebotsposition**-Unterraster aus. Ein Schieberegler zum schnellen Erstellen wird geöffnet. Die folgenden Felder im Formular **Angebotsposition**:

| **Feld** | **Ort** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- | --- |
| Beschreibung des Dataflows | Schnellerfassung | Eine Beschreibung der bestimmten Schätzung. | In diesem Feld werden standardmäßig die zugehörigen Angebotspositionsdetails für Kosten verwendet, die automatisch erstellt werden. |
| Transaktionsklasse | Schnellerfassung | Diese Dropdown-Liste enthält die Transaktionsklassen, die in der **Allgemeines**-Registerkarte der projektbasierten Angebotsposition enthalten sind.  | In diesem Feld werden standardmäßig die zugehörigen Angebotspositionsdetails für Kosten verwendet, die automatisch erstellt werden. |
| Rolle | Schnellerfassung | Die Person, die diese Arbeit ausführt oder diese Kosten verursacht. | In diesem Feld werden standardmäßig die zugehörigen Angebotspositionsdetails für Kosten verwendet, die automatisch erstellt werden. |
| Kateg. | Schnellerfassung | Kategorie der Arbeit oder Ausgabe. | In diesem Feld werden standardmäßig die zugehörigen Angebotspositionsdetails für Kosten verwendet, die automatisch erstellt werden. |
| Startdatum | Schnellerfassung | Startdatum der Arbeit. | In diesem Feld werden standardmäßig die zugehörigen Angebotspositionsdetails für Kosten verwendet, die automatisch erstellt werden. |
| Enddatum | Schnellerfassung | Enddatum der Arbeit. | In diesem Feld werden standardmäßig die zugehörigen Angebotspositionsdetails für Kosten verwendet, die automatisch erstellt werden. |
| Ressourcenzuordnungseinheit | Schnellerfassung | Ressourcenzuordnungseinheit, die diese Kosten verursacht und die Ressource bereitstellt, um daran zu arbeiten. | In diesem Feld werden standardmäßig die zugehörigen Angebotspositionsdetails für Kosten verwendet, die automatisch erstellt werden. Dieses Feld wird auch zum Abrufen von Einstandspreisen verwendet. |
| Einheitenzeitplan | Schnellerfassung | Einheitsgruppe der Arbeit oder Ausgabe. Einheiten gehören zu einem Einheitenplan oder einer Gruppe von Einheiten. Beispielsweise sind Meilen und km Einheiten, die zu einer Gruppe von Einheiten gehören, die die Entfernung beschreiben. | In diesem Feld werden standardmäßig die zugehörigen Angebotspositionsdetails für Kosten verwendet, die automatisch erstellt werden. |
| Einheit | Schnellerfassung | Einheit der Arbeit oder Ausgabe. | In diesem Feld werden standardmäßig die zugehörigen Angebotspositionsdetails für Kosten verwendet, die automatisch erstellt werden. |
| Menge | Schnellerfassung | Menge der Arbeit oder Ausgabe | In diesem Feld werden standardmäßig die zugehörigen Angebotspositionsdetails für Kosten verwendet, die automatisch erstellt werden. |
| Einheitenpreis | Schnellerfassung | Fakturierungsrate der Rolle, die die Arbeit ausführt, oder der Verkaufspreis der Ausgabenkategorie. Dieses Feld wird standardmäßig für die Zeit basierend auf der Kombination aus Rolle und Ressourceneinheit in der Projektpreisliste verwendet, die für das Startdatum gültig ist. Für Ausgaben wird in diesem Feld standardmäßig die Preiseinstellung für die Transaktionskategorie in der Projektpreisliste verwendet, die für das Startdatum gültig ist. Wenn die Preisberechnungsmethode für die Transaktionskategorie nicht Preis pro Einheit ist, gibt es keine Standardeinstellung, und dieses Feld bleibt leer. | Kostenrate der Rolle, die die Arbeit ausführt, oder die Kosten pro Einheit der Ausgabenkategorie. Dieses Feld wird standardmäßig für die Zeit basierend auf der Kombination aus Rolle und Ressourceneinheit im Preis der Vertragseinheit der Angebotspreisliste verwendet, die für das Startdatum gültig ist. Für Ausgaben wird in diesem Feld standardmäßig die Preiseinstellung für die Transaktionskategorie in der Einstandspreisliste der Vertragseinheit verwendet, die für das Startdatum gültig ist. Wenn die Preisberechnungsmethode für die Transaktionskategorie nicht Preis pro Einheit ist, gibt es keine Standardeinstellung, und dieses Feld bleibt leer. |
| Geschätzte Steuer | Schnellerfassung | Sie können die geschätzte Steuer für diese Arbeit oder Ausgabe manuell eingeben. | Es gibt keine nachgelagerten Auswirkungen von diesem Feld. |
| Betrag | Schnellerfassung | Sie können Informationen manuell in dieses Feld eingeben, wenn die **Menge**- und **Preis**-Felder leer bleiben. Wenn diese Felder nicht leer sind, ist dieses Feld schreibgeschützt und wird berechnet als (Menge\* Einheitenpreis) + Steuern. | Es gibt keine nachgelagerten Auswirkungen von diesem Feld. |

## <a name="update-prices-on-quote-line-details"></a>Aktualisieren der Preise für die Angebotspositionsdetails

Wenn Sie die Preise in der dem Angebot beigefügten Projektpreisliste oder in der Selbstkostenpreisliste der Vertragseinheit geändert haben, können Sie **Neu berechnen** auf der **Angebot**-Seite auswählen, um die Preise in den einzelnen Angebotspositionsdetails zu aktualisieren, um diese Änderung widerzuspiegeln. Wenn Sie **Neu berechnen** auswählen wird eine Warnung angezeigt, die Sie darüber informiert, dass die Preise für Angebotspositionsdetails für alle Angebotspositionen in diesem Angebot zurückgesetzt werden. Wählen **Ja**, um die Preise sowohl für Verkaufs- als auch für KostenAngebotspositionn zu aktualisieren.

## <a name="access-quote-line-details-for-cost"></a>Zugriff auf Angebotspositionsdetails für Kosten

Auf der **Detailinformationen zur Angebotsposition**-Registerkarte wählen Sie eine Zeile im Raster aus, um Aktionen in der Symbolleiste des Unterrasters zu aktivieren. Die erste Aktion auf der Unterraster-Symbolleiste, wenn ein Zitatzeilendetail ausgewählt wird, ist **Kostendetails öffnen**. Wählen Sie **Kostendetail öffnen**, um den entsprechenden Kostensatz und Betrag für diese Angebotsposition anzuzeigen.

> [!NOTE]
> Durch Ändern der Werte für Ressourceneinheit, Menge, Datum, Rolle oder Kategorie in den Angebotspositionsdetails für Kosten werden die entsprechenden Werte in den Angebotspositionsdetails für Verkäufe geändert.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Währung bei Angebotspositionsdetails für Kosten und Verkäufe

Für die Währung bei Angebotspositionsdetails für Verkauf wird standardmäßig die Projektpreisliste verwendet, die für das Startdatum der Angebotspositionsdetails gültig ist.

Für die Währung bei Angebotspositionsdetails für Kosten wird standardmäßig die Preisliste der Vertragseinheit des Angebots verwendet, die für das Startdatum der Angebotspositionsdetails für Kosten gültig ist.

Bei Rentabilitätsberechnungen wird der Betrag in den Angebotspositionsdetails für Kosten und Verkauf in die Basiswährung der Umgebung umgerechnet, um die geschätzte Gesamtspanne im Angebot anzugeben.

Dies könnte zu Währungsrundungsfehlern und sich ändernden Spannen führen, da keine datumswirksamen Wechselkurse vorhanden sind. Verwenden Sie diese Berechnungen für Projektangebote nur als Näherungswerte und nicht als tatsächliche gesetzliche oder sonstige Berichterstattung, die eine höhere Rundungsgenauigkeit und Kenntnis der Datumseffektivität für Wechselkurse erfordert.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]