---
title: Eine projektbasierte Vertragszeile kalkulieren – Lite
description: Dieses Thema enthält Informationen zur Schätzung von projektbasierten Vertragszeilen.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2d0d8309fcb4300e33ed2f5933259f99ad7e0d6a
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180416"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Eine projektbasierte Vertragszeile kalkulieren – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

In Dynamics 365 Project Operations enthält eine projektbasierte Vertragszeile Details, mit deren Hilfe die Kosten und potenziellen Einnahmen der für die Lieferung der Vertragszeile erforderlichen Arbeiten geschätzt werden können.

Um eine projektbasierte Vertragszeile zu schätzen, gehen Sie zur **Vertragszeilendetail**-Registerkarte auf der projektbasierten **Vertragszeile**.  Es gibt zwei Möglichkeiten, eine Schätzung für eine projektbasierte Vertragszeile zu erstellen:

   - Erstellen Sie einen Kostenvoranschlag direkt in der Vertragszeile, indem Sie die Vertragszeilendetails manuell hinzufügen.
   - Erstellen Sie ein Projekt und einen Projektplan und ordnen Sie das Projekt und die Aufgaben der Vertragszeile des Projekts zu. Dies ermöglicht den Prozess, mit dem Sie die Projektplanschätzung basierend auf den in der Vertragszeile enthaltenen Komponenten in die Vertragszeile importieren können.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Eine Schätzung direkt für eine projektbasierte Vertragszeile erstellen

1. Gehen Sie zur Vertragszeile und wählen Sie die **Vertragszeilendetail**-Registerkarte aus. Die Zeilen, die Sie auf dieser Registerkarte erstellen, werden zusammengefasst und als **Vertragswert** für die **Vertragszeile** angezeigt. 
2. Im **Vertragszeilendetails**-Unterraster wählen Sie **+ Neues Vertragszeilendetail**. Ein Schnellschieberegler wird geöffnet. Die folgenden Felder sind im **Vertragszeilendetails**-Formular verfügbar:

| Feld | Position | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| **Beschreibung** | **Schnellertellung** | Eine Beschreibung der bestimmten Schätzung. | In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden. |
| **Transaktionsklasse** | **Schnellertellung** | Diese Dropdown-Liste enthält eine Liste der Transaktionsklassen, die auf der **Allgemein**-Registerkarte der projektbasierten Vertragszeile enthalten sind. | In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden. |
| **Rolle** | **Schnellertellung** | Die Rolle der Person, die diese Arbeit ausführt oder diese Kosten verursacht. | In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden. |
| **Kategorie** | **Schnellertellung** | Die Kategorie der Arbeit oder Ausgabe. | In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden. |
| **Startdatum** | **Schnellertellung** | Das Startdatum der Arbeit. | In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden. |
| **Enddatum** | **Schnellertellung** | Das Enddatum der Arbeit. | In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden. |
| **Ressourcenzuordnungseinheit** | **Schnellertellung** | Die Ressourceneinheit , die diese Kosten verursacht und die Ressource bereitstellt, um daran zu arbeiten. | In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden. Dieses Feld wird auch zum Abrufen von Einstandspreisen verwendet. |
| **Einheitenzeitplan** | **Schnellerfassung** | Die Einheitsgruppe der Arbeit oder des Aufwands. Einheiten gehören zu einem Einheitenplan oder einer Gruppe von Einheiten. Zum Beispiel *Meilen* und *Kilometer (km)* sind Einheiten, die zu einer Gruppe von Einheiten gehören, die die Entfernung beschreiben. | In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden. |
| **Einheit** | **Schnellertellung** | Die Einheit der Arbeit oder des Aufwands. | In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden. |
| **Menge** | **Schnellertellung** | Die Menge der Arbeit oder des Aufwands. | In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden. |
| **Einheitenpreis** | **Schnellertellung** | Der Rechnungssatz der Rolle, die die Arbeit ausführt, oder der Verkaufspreis der Ausgabenkategorie. Dieses Feld wird standardmäßig für die **Zeit** basierend auf der Kombination aus Rolle und Ressourceneinheit in der Projektpreisliste verwendet, die für das Startdatum gültig ist. Für Ausgaben stammt die Standardeinstellung dieses Felds aus der Preiseinstellung für die Transaktionskategorie in der Projektpreisliste, die für das Startdatum gültig ist. Wenn die Preisberechnungsmethode für die Transaktionskategorie nicht **Preis pro Einheit** ist, gibt es keine Standardeinstellung, und dieses Feld bleibt leer. | Der Kostensatz der Rolle, die die Arbeit ausführt, oder die Kosten pro Einheit der Ausgabenkategorie. Dieses Feld ist standardmäßig auf **Zeit basierend auf der Rolle** und die Kombination der Ressourceneinheiten in der Rollenpreislinie der Kostenpreisliste, die der Vertragseinheit zum Stichtag beigefügt ist, eingestellt. Für Ausgaben basiert die Standardeinstellung dieses Felds auf der Kategoriepreiszeile der Einstandspreisliste, die der Vertragseinheit zugeordnet und für das Startdatum gültig ist. Wenn die Preisberechnungsmethode für die Transaktionskategorie nicht Preis pro Einheit ist, gibt es keine Standardeinstellung, und dieses Feld bleibt leer. |
| **Geschätzte Steuer** | **Schnellertellung** | Die geschätzte Steuer für diese Arbeit oder Ausgabe, wie vom Benutzer eingegeben. | Die geschätzte Steuer für diese Arbeit oder Ausgabe, wie vom Benutzer eingegeben. |
| **Betrag** | **Schnellertellung** | Dieser Wert in diesem Feld kann vom Benutzer hinzugefügt werden, wenn die Felder **Menge** und **Preis** leer bleiben. Wenn **Menge** und **Preis** gefüllt sind, ist das **Menge**-Feld schreibgeschützt und wird als **(Menge \* Stückpreis) + Steuern** berechnet. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Aktualisieren Sie die Preise für Vertragsdetails

Wenn Sie die Preise in der Projektpreisliste ändern, die dem Vertrag beigefügt ist, oder in der Kostenpreisliste der Vertragseinheit, können Sie die Preise in den einzelnen Vertragszeilendetails aktualisieren, um die Änderung widerzuspiegeln. Wählen Sie auf der **Vertrag**-Seite **Neu berechnen** aus. Eine Warnung informiert Sie darüber, dass die Preise für alle Vertragszeilen in diesem Vertrag zurückgesetzt werden. Wählen Sie **Ja**, um die Preise sowohl für Verkaufs- als auch für Kostenvertragsdetails zu aktualisieren.

## <a name="access-contract-line-details-for-cost"></a>Greifen Sie auf die Kosten der Vertragszeile zu

Auf der **Vertragszeilendetails**-Registerkarte wählen Sie eine Zeile im Raster aus, um Aktionen in der Symbolleiste des Unterrasters anzuzeigen. Die erste Aktion in der Symbolleiste des Unterrasters ist **Kostendetail öffnen**. Wählen Sie **Kostendetail öffnen** aus, um den entsprechenden Kostensatz und den entsprechenden Betrag für diese Vertragszeilendetails anzuzeigen. 

> [!NOTE]
> Durch das Ändern des Ressourcenzuordnungsunternehmen, der Ressourceneinheit, der Menge, der Daten, der Rolle oder der Kategoriewerte in den Vertragszeilendetails für **Kosten** werden auch die entsprechenden Werte im Vertragszeilendetail für **Vertrieb** geändert.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Angaben zur Währung in der Vertragszeile für Kosten und Umsatz

Das Vertragszeilendetail für **Vertrieb** legt die Standardwährung aus der Projektpreisliste fest, die für das Startdatum des Vertragszeilendetails gültig ist.

Das Vertragszeilendetail für **Kosten** legt die Standardwährung aus der Preisliste der Vertragseinheit des Vertrags fest, die für das Startdatum des Vertragszeilendetails für **Kosten** gültig ist.

Rentabilitätsberechnungen konvertieren die Beträge für die Vertragszeilendetails für **Kosten** und **Vertrieb** in die Basiswährung der Umgebung, um die tatsächlichen und geschätzten Gesamtmargen des Vertrags zu melden.

> [!NOTE]
> Währungsrundungsfehler und geänderte Margen können aufgrund fehlender datumswirksamer Wechselkurse auftreten. Verwenden Sie diese Berechnungen für Projektverträge nur als Näherungswerte und nicht für tatsächliche gesetzliche oder andere Berichte, die eine höhere Rundungsgenauigkeit und Kenntnis der Datumseffektivität für Wechselkurse erfordern.
