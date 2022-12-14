---
title: Eine Projektangebotsposition kalkulieren
description: Dieser Artikel beschreibt, wie Sie einen Kostenvoranschlag in einer Zeile erstellen können.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: bac3a3fa2d14c857edfb469a005406c346c8dbf6
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825986"
---
# <a name="estimate-a-project-quote-line"></a>Eine Projektangebotsposition kalkulieren

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung Project Operations für Ressourcen/nicht vorrätige Szenarien_

Eine projektbasierte Angebotsposition enthält Details, die bei der Schätzung der Kosten und potenziellen Einnahmen der mit der Lieferung der Angebotsposition verbundenen Arbeiten hilfreich sind.

Um eine projektbasierte Angebotsposition zu schätzen, wählen Sie in der projektbasierten Angebotsposition die Option **Angebotspositionsdetail**-Registerkarte. Es gibt zwei Möglichkeiten, eine Schätzung für eine projektbasierte Angebotsposition zu erstellen:

- Erstellen Sie die Schätzung manuell direkt in der Angebotsposition mithilfe von Angebotspositionsdetails. 
- Erstellen Sie ein Projekt und einen Projektplan und ordnen Sie das Projekt und die Aufgaben im Projekt der Angebotsposition zu. Der Prozess zum Importieren der Schätzungen im Projektplan in die Angebotsposition basierend auf den von Ihnen angegebenen Informationen wird aktiviert.

## <a name="create-estimates-directly-on-a-project-quote-line"></a>Schätzungen direkt aus einer Projektangebotsposition erstellen

Um eine Schätzung für eine projektbasierte Angebotsposition zu erstellen, wählen Sie die Option **Angebotspositionsdetail**-Registerkarte. Die Position, die Sie auf dieser Registerkarte erstellen, fasst den angegebenen Wert für diese Angebotsposition zusammen. 

Wählen Sie zum Erstellen von Angebotszeilendetails **Neues Angebotszeilendetail** im **Detailinformationen zur Angebotsposition**-Unterraster aus. Ein Schieberegler zum schnellen Erstellen wird geöffnet. Die folgende Tabelle enthält Details zu den Feldern auf der **Detailinformationen zur Angebotsposition**-Seite und wie sich die Werte auf die Funktionalität auswirken.

| **Feld** | **Speicherort** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- | --- |
| Beschreibung | Schnellerfassung | Eine Beschreibung der bestimmten Schätzung. | Dieser Wert ist standardmäßig das zugehörige Angebotszeilendetail für Kosten, die automatisch erstellt werden. |
| Transaktionsklasse | Schnellerfassung | Diese Dropdownliste enthält die Transaktionsklassen, die auf der **Allgemein**-Registerkarte der projektbasierten Angebotszeile enthalten sind.  | Dieser Wert ist standardmäßig das zugehörige Angebotszeilendetail für Kosten, die automatisch erstellt werden. |
| Produkt auswählen | Schnellerfassung | Gilt, wenn die Transaktionsklasse **Material** ist. Sie können auswählen, dass diese Schätzposition für ein bestimmtes **Vorhandenes** (Katalog-)Produkt oder ein **Manueller Eintrag**-Produkt ist. | Dieser Wert ist standardmäßig das zugehörige Angebotszeilendetail für Kosten, die automatisch erstellt werden. |
| Produkt | Schnellerfassung | Die ID des Produkts aus dem Produktkatalog. Dieses Feld ist nur aktiviert, wenn Sie **Vorhanden** im Feld **Produkt auswählen** gewählt haben. Die ID wird verwendet, um den Verkaufspreis aus der Projektpreisliste im Angebot abzurufen. | Dieser Wert ist standardmäßig das zugehörige Angebotszeilendetail für Kosten, die automatisch erstellt werden. |
| Manuell einzutragendes Produkt | Schnellerfassung | Ein Textfeld zum Schreiben im Namen des Produkts. Dieses Feld ist nur aktiviert, wenn Sie **Manueller Eintrag** im Feld **Produkt auswählen** gewählt haben.| Dieser Wert ist standardmäßig das zugehörige Angebotszeilendetail für Kosten, die automatisch erstellt werden. |
| Rolle | Schnellerfassung | Die Rolle der Person, die diese Arbeit ausführt oder diese Kosten verursacht. | Dieser Wert ist standardmäßig das zugehörige Angebotszeilendetail für Kosten, die automatisch erstellt werden. |
| Kateg. | Schnellerfassung | Die Kategorie der Arbeit oder Ausgabe. | Dieser Wert ist standardmäßig das zugehörige Angebotszeilendetail für Kosten, die automatisch erstellt werden. |
| Startdatum | Schnellerfassung | Das Startdatum der Arbeit. | Dieses Feld ist standardmäßig das Angebotszeilendetail für Kosten, die automatisch erstellt werden. |
| Enddatum | Schnellerfassung | Das Enddatum der Arbeit. | Dieses Feld ist standardmäßig das Angebotszeilendetail für Kosten, die automatisch erstellt werden. |
| Ressourcenzuordnungseinheit | Schnellerfassung | Die Ressourceneinheit, die diese Kosten verursacht und die Ressource bereitstellt, um daran zu arbeiten. | Dieser Wert ist standardmäßig das zugehörige Angebotszeilendetail für Kosten, die automatisch erstellt und beim Abrufen des Einstandspreises verwendet werden. |
| Einheitenzeitplan | Schnellerfassung | Die Einheitsgruppe der Arbeit, des Produkts oder der Kosten. Einheiten gehören zu einem Einheitenplan oder einer Gruppe von Einheiten. Beispielsweise sind Meilen und Kilometer Einheiten, die zu einer Gruppe von Einheiten gehören, die die Entfernung beschreibt. | Dieser Wert ist standardmäßig das zugehörige Angebotszeilendetail für Kosten, die automatisch erstellt werden. |
| Einheit | Schnellerfassung | Die Einheiten der Arbeit, des Produkts oder der Kosten. | Dieser Wert ist standardmäßig das zugehörige Angebotszeilendetail für Kosten, die automatisch erstellt werden. |
| Menge | Schnellerfassung | Die Menge der Arbeit, des Produkts oder der Kosten. | Dieser Wert ist standardmäßig das zugehörige Angebotszeilendetail für Kosten, die automatisch erstellt werden. |
| Einzelpreis | Schnellerstellung |Der Rechnungssatz der Rolle, die die Arbeit ausführt, der Stückpreis des Produkts oder der Verkaufspreis des Produkts oder der Ausgabenkategorie. Der Standardwert für dieses Feld ist **Zeit** basierend auf der Kombination der Preisdimensionswerte in der Rollenpreislinie der Projektpreisliste, die für das Startdatum gültig ist. Für **Kosten** stammt die Standardeinstellung aus der Preiseinstellung für die Transaktionskategorie in der Projektpreisliste, die für das Startdatum gültig ist. Wenn die Preismethode für die Transaktionskategorie nicht Preis pro Einheit ist, gibt es keine Standardeinstellung, und dieses Feld bleibt leer. Für Produkte basiert die Standardeinstellung auf der **Preislisteneintrag**-Position in der Projektpreisliste, die für das Startdatum gültig ist.| Der Kostensatz der Rolle, die die Arbeit ausführt, die Kosten pro Einheit der Ausgabenkategorie oder der Einheitenpreis des Produkts. Der Standardwert für dieses Feld ist **Zeit** basierend auf der Kombination der Preisdimensionswerte in der Rollenpreislinie der Projektpreisliste, die für das Startdatum gültig ist. Für **Kosten** stammt die Standardeinstellung aus der Preiseinstellung für die Transaktionskategorie in der Projektpreisliste, die für das Startdatum gültig ist. Wenn die Preismethode für die Transaktionskategorie nicht Preis pro Einheit ist, gibt es keine Standardeinstellung, und dieses Feld bleibt leer. Für Produkte basiert die Standardeinstellung auf der **Preislisteneintrag**-Position in der Projektpreisliste, die für das Startdatum gültig ist.|
| Geschätzte Steuer | Schnellerfassung | Sie können die geschätzte Steuer für diese Arbeit oder Ausgabe manuell eingeben. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Betrag | Schnellerfassung | Sie können Informationen manuell in dieses Feld eingeben, wenn die **Menge**- und **Preis**-Felder leer bleiben. Wenn diese Felder nicht leer sind, ist dieses Feld schreibgeschützt und wird berechnet als (Menge\* Einheitenpreis) + Steuern. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |


## <a name="update-prices-on-quote-line-details"></a>Aktualisieren der Preise für die Angebotspositionsdetails

Wenn Sie die Preise in der Projektpreisliste, die dem Angebot beigefügt ist, oder in der Kostenpreisliste der Vertragseinheit geändert haben, können Sie **Neu berechnen** auf der **Angebot**-Seite auswählen, um die Preise in den einzelnen Details der Angebotszeile zu aktualisieren, um diese Änderung widerzuspiegeln. Wenn Sie **Neu berechnen** auswählen, wird eine Warnung angezeigt, die Sie darüber informiert, dass die Preise für Angebotszeilendetails für alle Angebotszeilen in diesem Angebot zurückgesetzt werden. Wählen Sie **Ja**, um die Preise sowohl für Verkaufs- als auch für KostenAngebotspositionn zu aktualisieren.

## <a name="access-quote-line-details-for-cost"></a>Zugriff auf Angebotspositionsdetails für Kosten

Auf der **Detailinformationen zur Angebotsposition**-Registerkarte wählen Sie eine Zeile im Raster aus, um Aktionen in der Symbolleiste des Unterrasters zu aktivieren. Die erste Aktion auf der Unterraster-Symbolleiste, wenn ein Zitatzeilendetail ausgewählt wird, ist **Kostendetails öffnen**. Wählen Sie **Kostendetail öffnen**, um den entsprechenden Kostensatz und Betrag für diese Angebotsposition anzuzeigen.

> [!NOTE]
> Durch Ändern der Werte für Ressourceneinheit, Menge, Datum, Rolle oder Kategorie in den Angebotspositionsdetails für Kosten werden die entsprechenden Werte in den Angebotspositionsdetails für Verkäufe geändert.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Währung bei Angebotspositionsdetails für Kosten und Verkäufe

Für die Währung bei Angebotspositionsdetails für Verkauf wird standardmäßig die Projektpreisliste verwendet, die für das Startdatum der Angebotspositionsdetails gültig ist.

Für die Währung bei Angebotspositionsdetails für Kosten wird standardmäßig die Preisliste der Vertragseinheit des Angebots verwendet, die für das Startdatum der Angebotspositionsdetails für Kosten gültig ist.

Bei Rentabilitätsberechnungen wird der Betrag in den Angebotspositionsdetails für Kosten und Verkauf in die Basiswährung der Umgebung umgerechnet, um die geschätzte Gesamtspanne im Angebot anzugeben.

> [!Hinweis Währungsrundungsfehler und geänderte Margen können aufgrund fehlender datumswirksamer Wechselkurse auftreten. Verwenden Sie diese Berechnungen nur für Projektverträge, da es sich um Näherungswerte handelt und nicht für tatsächliche gesetzliche oder andere Berichte, die eine höhere Rundungsgenauigkeit und Kenntnis der Datumseffektivität für Wechselkurse erfordern.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
