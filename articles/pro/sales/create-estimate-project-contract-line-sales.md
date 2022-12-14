---
title: Eine Projektvertragszeile schätzen
description: Dieser Artikel enthält Informationen zur Schätzung einer projektbezogenen Vertragszeile.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 86872aa58067f55243fa19dc865971f76660f594
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824766"
---
# <a name="estimate-a-project-contract-line"></a>Eine Projektvertragszeile schätzen

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

In Dynamics 365 Project Operations enthält eine Projektvertragszeile Details, mit deren Hilfe die Kosten und potenziellen Einnahmen der für die Lieferung der Vertragszeile erforderlichen Arbeiten geschätzt werden können.

Um eine Projektvertragszeile zu schätzen, gehen Sie zur **Vertragszeilendetail**-Registerkarte auf der projektbasierten **Vertragszeile**.  Es gibt zwei Möglichkeiten, eine Schätzung für eine projektbasierte Vertragszeile zu erstellen:

   - Erstellen Sie einen Kostenvoranschlag direkt in der Vertragszeile, indem Sie die Vertragszeilendetails manuell hinzufügen.
   - Erstellen Sie ein Projekt und einen Projektplan und ordnen Sie das Projekt und die Aufgaben der Vertragszeile des Projekts zu. Dies ermöglicht den Prozess, mit dem Sie die Projektplanvorkalkulation basierend auf den in der Vertragszeile enthaltenen Komponenten in die Vertragszeile importieren können.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Eine Schätzung direkt für eine projektbasierte Vertragszeile erstellen

Um eine Schätzung direkt aus einer Projektvertragsposition zu erstellen, gehen Sie folgendermaßen vor:

1. Gehen Sie zur Vertragszeile und wählen Sie die **Vertragszeilendetail**-Registerkarte aus. Die Zeilen, die Sie auf dieser Registerkarte erstellen, werden zusammengefasst und als **Vertragswert** für die **Vertragszeile** angezeigt. 
2. Im **Vertragszeilendetails**-Unterraster wählen Sie **Neues Vertragszeilendetail**. Ein Schnellschieberegler wird geöffnet. Die folgenden Felder sind auf der Seite **Vertragszeilendetails** verfügbar:

| Feld | Speicherort | Beschreibung | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| **Beschreibung** | **Schnellerstellung** | Eine Beschreibung der bestimmten Schätzung. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Transaktionsklasse** | **Schnellerstellung** | Diese Liste der Transaktionsklassen ist auf der **Allgemein**-Registerkarte der projektbasierten Vertragszeile enthalten. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Produkt auswählen** | **Schnellerfassung** | Gilt, wenn die Transaktionsklasse **Material** ist. Sie können festlegen, dass diese Schätzposition für ein bestimmtes **Vorhandenes** (Katalog-)Produkt oder ein **Manueller Eintrag**-Produkt ist. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Produkt** | **Schnellerfassung** | Die ID des Produkts aus dem Produktkatalog. Dieses Feld ist nur aktiviert, wenn Sie **Vorhandenes Produkt** im Feld **Produkt auswählen** gewählt haben. Die ID wird verwendet, um den Verkaufspreis aus der Projektpreisliste im Vertrag abzurufen. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Manuell einzutragendes Produkt** | **Schnellerfassung** | Ein Textfeld zum Eingeben des Namens des Produkts. Dieses Feld ist nur aktiviert, wenn Sie **Manueller Eintrag** im Feld **Produkt auswählen** gewählt haben.| Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Rolle** | **Schnellerstellung** | Die Rolle der Person, die diese Arbeit ausführt oder diese Kosten verursacht. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden.|
| **Kateg.** | **Schnellerstellung** | Die Kategorie der Arbeit oder Ausgabe. |Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden.|
| **Startdatum** | **Schnellerstellung** | Das Startdatum der Arbeit. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Enddatum** | **Schnellerstellung** | Das Enddatum der Arbeit. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Ressourcenzuordnungseinheit** | **Schnellerstellung** | Die Ressourceneinheit, die diese Kosten verursacht und die Ressource bereitstellt, um daran zu arbeiten. |Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt und beim Abrufen des Einstandspreises verwendet werden. |
| **Einheitenzeitplan** | **Schnellerfassung** | Die Einheitsgruppe der Arbeit, des Produkts oder der Kosten. Einheiten gehören zu einem Einheitenplan oder einer Gruppe von Einheiten. Zum Beispiel *Meilen* und *Kilometer (km)* sind Einheiten, die zu einer Gruppe von Einheiten gehören, die die Entfernung beschreiben. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Einheit** | **Schnellerstellung** | Die Einheit der Arbeit, des Produkts oder der Kosten. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Menge** | **Schnellerstellung** | Die Menge der Arbeit, des Produkts oder der Kosten. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **VK-Preis** | **Schnellerstellung** | Der Rechnungssatz der Rolle, die die Arbeit ausführt, der Stückpreis des Produkts oder der Verkaufspreis des Produkts oder der Ausgabenkategorie. Der Standardwert für dieses Feld ist **Zeit** basierend auf der Kombination der Preisdimensionswerte in der Rollenpreislinie der Projektpreisliste, die für das Startdatum gültig ist. Für **Ausgaben** stammt die Standardeinstellung dieses Felds aus der Preiseinstellung für die Transaktionskategorie in der Projektpreisliste, die für das Startdatum gültig ist. Wenn die Preisberechnungsmethode für die Transaktionskategorie nicht **Preis pro Einheit** ist, gibt es keine Standardeinstellung, und dieses Feld bleibt leer. Für Produkte basiert die Standardeinstellung des Felds auf der **Preislisteneintrag**-Position in der Projektpreisliste, die für das Startdatum gültig ist.| Der Kostensatz der Rolle, die die Arbeit ausführt, die Kosten pro Einheit der Ausgabenkategorie oder der Einheitenpreis des Produkts. Der Standardwert für dieses Feld **Zeit** basiert auf der Kombination der Preisdimensionswerte in der Rollenpreislinie der Projektpreisliste, die der Vertragseinheit angefügt und für das Startdatum gültig ist. Für Ausgaben basiert die Standardeinstellung dieses Felds auf der Kategoriepreiszeile der Einstandspreisliste, die der Vertragseinheit zugeordnet und für das Startdatum gültig ist. Wenn die Preisberechnungsmethode für die Transaktionskategorie nicht Preis pro Einheit ist, gibt es keine Standardeinstellung, und dieses Feld bleibt leer. Für Produkte basiert die Standardeinstellung des Felds auf der **Preislistenelement**-Zeile der Einstandspreisliste, die der Vertragseinheit angefügt und für das Startdatum gültig ist.|
| **Geschätzte Steuer** | **Schnellerstellung** | Die geschätzte Steuer für diese Arbeit oder Ausgabe. | Die geschätzte Steuer für diese Arbeit oder Ausgabe. |
| **Betrag** | **Schnellerstellung** | Sie können den Wert in diesem Feld hinzufügen, wenn die **Menge** und **Preis**-Felder leer bleiben. Wenn **Menge** und **Preis** gefüllt sind, ist das **Menge**-Feld schreibgeschützt und wird als **(Menge \* Stückpreis) + Steuern** berechnet. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Aktualisieren Sie die Preise für Vertragsdetails

Wenn Sie die Preise in der Projektpreisliste ändern, die dem Vertrag beigefügt ist, oder in der Kostenpreisliste der Vertragseinheit, können Sie die Preise in den einzelnen Vertragszeilendetails aktualisieren, um die Änderung widerzuspiegeln. Wählen Sie auf der **Vertrag**-Seite **Neu berechnen** aus. Eine Warnung informiert Sie darüber, dass die Preise für alle Vertragslinien in diesem Vertrag zurückgesetzt werden. Wählen Sie **Ja**, um die Preise sowohl für Verkaufs- als auch für Kostenvertragsdetails zu aktualisieren.

## <a name="access-contract-line-details-for-cost"></a>Greifen Sie auf die Kosten der Vertragszeile zu

Auf der **Vertragszeilendetails**-Registerkarte wählen Sie eine Zeile im Raster aus, um Aktionen in der Symbolleiste des Unterrasters anzuzeigen. Die erste Aktion in der Symbolleiste des Unterrasters ist **Kostendetail öffnen**. Wählen Sie **Kostendetail öffnen** aus, um den entsprechenden Kostensatz und den entsprechenden Betrag für diese Vertragszeilendetails anzuzeigen. 

> [!NOTE]
> Durch das Ändern des Ressourcenzuordnungsunternehmen, der Ressourceneinheit, der Menge, der Daten, der Rolle oder der Kategoriewerte in den Vertragszeilendetails für **Kosten** werden auch die entsprechenden Werte im Vertragszeilendetail für **Vertrieb** geändert.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Angaben zur Währung in der Vertragszeile für Kosten und Umsatz

Das Vertragszeilendetail für **Vertrieb** legt die Standardwährung aus der Projektpreisliste fest, die für das Startdatum des Vertragszeilendetails gültig ist.

Das Vertragszeilendetail für **Kosten** legt die Standardwährung aus der Preisliste der Vertragseinheit des Vertrags fest, die für das Startdatum des Vertragszeilendetails für **Kosten** gültig ist.

Rentabilitätsberechnungen konvertieren die Beträge für die Vertragszeilendetails für **Kosten** und **Vertrieb** in die Basiswährung der Umgebung, um die tatsächlichen und geschätzten Gesamtmargen des Vertrags zu melden.

> [!NOTE]
> Währungsrundungsfehler und geänderte Margen können aufgrund fehlender datumswirksamer Wechselkurse auftreten. Verwenden Sie diese Berechnungen nur für Projektverträge, da es sich um Näherungswerte handelt und nicht für tatsächliche gesetzliche oder andere Berichte, die eine höhere Rundungsgenauigkeit und Kenntnis der Datumseffektivität für Wechselkurse erfordern.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
