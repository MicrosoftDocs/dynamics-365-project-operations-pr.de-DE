---
title: Eine Projektvertragszeile schätzen
description: Dieses Thema enthält Informationen zu Schätzungen in einer Projektvertragszeile.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 53e3c291043ab102eb2f59221ae879acf766bb98
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589061"
---
# <a name="estimate-a-project-contract-line"></a>Eine Projektvertragszeile schätzen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_ 

In Dynamics 365 Project Operations enthält eine projektbasierte Vertragszeile Details, mit deren Hilfe die Kosten und potenziellen Einnahmen der für die Lieferung der Vertragszeile erforderlichen Arbeiten geschätzt werden können.

Um eine projektbasierte Vertragszeile zu schätzen, gehen Sie zur **Vertragszeilendetail**-Registerkarte auf der projektbasierten **Vertragszeile**.  Es gibt zwei Möglichkeiten, eine Schätzung für eine projektbasierte Vertragszeile zu erstellen:

   - Erstellen Sie einen Kostenvoranschlag direkt in der Vertragszeile, indem Sie die Vertragszeilendetails manuell hinzufügen.
   - Erstellen Sie ein Projekt und einen Projektplan und ordnen Sie das Projekt und die Aufgaben der Vertragszeile des Projekts zu. Dies ermöglicht den Prozess, mit dem Sie die Projektplanvorkalkulation basierend auf den in der Vertragszeile enthaltenen Komponenten in die Vertragszeile importieren können.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Erstellen Sie eine Schätzung direkt aus einer Projektvertragsposition

Um eine Schätzung direkt aus einer Projektvertragsposition zu erstellen, gehen Sie folgendermaßen vor:

1. Gehen Sie zur Vertragszeile und wählen Sie die **Vertragszeilendetail**-Registerkarte aus. Die Zeilen, die Sie auf dieser Registerkarte erstellen, werden zusammengefasst und als **Vertragswert** für die **Vertragszeile** angezeigt. 
2. Im **Vertragszeilendetails**-Unterraster wählen Sie **Neues Vertragszeilendetail**. Ein Schnellschieberegler wird geöffnet. Die folgenden Felder sind auf der Seite **Vertragszeilendetails** verfügbar:

| Feld | Speicherort | Beschreibung | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| **Beschreibung** | **Schnellerstellung** | Eine Beschreibung der bestimmten Schätzung. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Transaktionsklasse** | **Schnellerstellung** | Diese Liste der Transaktionsklassen ist auf der **Allgemein**-Registerkarte der projektbasierten Vertragszeile enthalten. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Produkt auswählen** | **Schnellerfassung** | Gilt, wenn die Transaktionsklasse **Material** ist. Sie können auswählen, dass diese Schätzposition für ein bestimmtes **Vorhandenes** (Katalog-)Produkt oder ein **Manueller Eintrag**-Produkt ist. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Produkt** | **Schnellerfassung** | Die ID des Produkts aus dem Produktkatalog. Dieses Feld ist nur aktiviert, wenn Sie **Vorhandenes Produkt** im Feld **Produkt auswählen** gewählt haben. Die ID wird verwendet, um den Verkaufspreis aus der Projektpreisliste im Vertrag abzurufen. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Manuell einzutragendes Produkt** | **Schnellerfassung** | Ein Textfeld zum Eingeben des Namens des Produkts. Dieses Feld ist nur aktiviert, wenn Sie **Manueller Eintrag** im Feld **Produkt auswählen** gewählt haben.| Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Rolle** | **Schnellerstellung** | Die Rolle der Person, die diese Arbeit ausführt oder diese Kosten verursacht. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden.|
| **Kateg.** | **Schnellerstellung** | Die Kategorie der Arbeit oder Ausgabe. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden.|
| **Startdatum** | **Schnellerstellung** | Das Startdatum der Arbeit. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Enddatum** | **Schnellerstellung** | Das Enddatum der Arbeit. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Ressourcenzuordnungsunternehmen** | **Schnellerstellung** | Das Ressourcenunternehmen oder die juristische Person, die diese Kosten verursachen und die Ressource bereitstellen, um daran zu arbeiten. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt und beim Abrufen des Einstandspreises verwendet werden. |
| **Ressourcenzuordnungseinheit** | **Schnellerstellung** | Die Ressourceneinheit, die diese Kosten verursacht und die Ressource bereitstellt, um daran zu arbeiten. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt und beim Abrufen des Einstandspreises verwendet werden. |
| **Einheitenzeitplan** | **Schnellerfassung** | Die Einheitsgruppe der Arbeit, des Produkts oder der Kosten. Einheiten gehören zu einem Einheitenplan oder einer Gruppe von Einheiten. Zum Beispiel *Meilen* und *Kilometer (km)* sind Einheiten, die zu einer Gruppe von Einheiten gehören, die die Entfernung beschreiben. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Einheit** | **Schnellerstellung** | Die Einheit der Arbeit, des Produkts oder der Kosten. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **Menge** | **Schnellerstellung** | Die Menge der Arbeit, des Produkts oder der Kosten. | Dieser Wert ist standardmäßig das zugehörige Vertragszeilendetail für Kosten, die automatisch erstellt werden. |
| **VK-Preis** | **Schnellerstellung** | Der Rechnungssatz der Rolle, die die Arbeit ausführt, der Stückpreis des Produkts oder der Verkaufspreis des Produkts oder der Ausgabenkategorie. Der Standardwert für dieses Feld ist **Zeit** basierend auf der Kombination der Preisdimensionswerte in der Rollenpreislinie der Projektpreisliste, die für das Startdatum gültig ist. Für **Kosten** stammt die Standardeinstellung des Felds aus der Preiseinstellung für die Transaktionskategorie in der Projektpreisliste, die für das Startdatum gültig ist. Wenn die Preisberechnungsmethode für die Transaktionskategorie nicht **Preis pro Einheit** ist, gibt es keine Standardeinstellung, und dieses Feld bleibt leer. Für Produkte basiert die Standardeinstellung des Felds auf der **Preislisteneintrag**-Position in der Projektpreisliste, die für das Startdatum gültig ist.| Der Kostensatz der Rolle, die die Arbeit ausführt, die Kosten pro Einheit der Ausgabenkategorie oder der Einheitenpreis des Produkts. Der Standardwert für **Zeit** basiert auf der Kombination der Preisdimensionswerte in der Rollenpreislinie der Projektpreisliste, die der Vertragseinheit angefügt und für das Startdatum gültig ist. Für **Kosten** basiert die Standardeinstellung des Felds aus der Kategoriepreiszeile der Einstandspreisliste, die der Vertragseinheit angefügt und für das Startdatum gültig ist. Wenn die Preisberechnungsmethode für die Transaktionskategorie nicht Preis pro Einheit ist, gibt es keine Standardeinstellung, und dieses Feld bleibt leer. Für Produkte basiert die Standardeinstellung des Felds auf der **Preislistenelement**-Zeile der Einstandspreisliste, die der Vertragseinheit angefügt und für das Startdatum gültig ist.|
| **Geschätzte Steuer** | **Schnellerstellung** | Die geschätzte Steuer für diese Arbeit oder Ausgabe, wie vom Benutzer eingegeben. | &nbsp; |
| **Betrag** | **Schnellerstellung** | Der Wert in diesem Feld kann hinzugefügt werden, wenn die **Menge** und **Preis**-Felder leer bleiben. Wenn die **Menge** und **Preis**-Felder gefüllt sind, ist das Feld **Menge** schreibgeschützt und wird als **(Menge \* Stückpreis) + Steuern** berechnet. | &nbsp; |

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
