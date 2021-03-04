---
title: Einheitengruppen und Einheiten
description: Dieses Thema enthält Informationen zu Einheitengruppen und Einheiten.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145582"
---
# <a name="unit-groups-and-units"></a>Einheitengruppen und Einheiten

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Einheitengruppen und Einheiten sind Basisentitäten in Microsoft Dynamics 365. Eine Einheit ist eine einzelne Maßeinheit, und mehrere Einheiten können zu Einheitengruppen zusammengefasst werden. Eine Einheitengruppe wird in der Dynamics 365-Benutzeroberfläche (UI) manchmal als Einheitszeitplan bezeichnet. 

Hier finden Sie einige Beispiele für Einheiten und Einheitengruppen:
 
- **Einheitengruppe**: Entfernung 
    - **Einheiten**: Meile, Kilometer, usw.
- **Einheitengruppe**: Zeit
    - **Einheiten**: Stunde, Tag, Woche, usw. 

Wenn Sie mehrere Einheiten in einer Einheitengruppe einrichten, müssen Sie auch einen Umrechnungsfaktor zwischen ihnen einrichten, indem Sie die erste Einheit bestimmen, die Sie als Standard- oder primäre Einheit für die Einheitengruppe eingerichtet haben. 

Wenn Sie beispielsweise in einer Einheitengruppe **Zeit** **Stunde** als die erste Einheit einrichten, legt das System **Stunde** als die Standardeinheit fest. Wenn die nächste Einheiten, die Sie einrichten, **Tag** ist, müssen Sie einen Umrechnungsfaktor für **Tag** in **Stunde** einrichten. Wenn Sie dann **Woche** als dritte Einheit hinzufügen, müssen Sie einen Umrechnungsfaktor für **Woche** in **Tag** oder **Stunde** angeben. 

Das folgende Bild zeigt eine Beispielkonfiguration der Einheit **Tag**, bei der das Feld **Menge** die Anzahl Stunden pro Tag und **Woche**, wobei das Feld **Menge** die Anzahl Tage in einer Woche enthält.

> ![Einheitengruppe: Informationsseite](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Verwenden von Einheiten und Einheitengruppen

Dynamics 365 Project Service Automation verwendet Einheiten und Einheitengruppen, um Vorkalkulationen und Einträge für Ausgaben und Zeit zu verarbeiten. 

Bei Ausgaben verfügt jede Ausgabenkategorie über eine Standardeinheitengruppe und eine Standardeinheit. Diese Werte werden bei Preislisteneinträgen als Standardwerte für Ausgabenkategorien eingegeben. 

Sie verfügen beispielsweise über eine Ausgabenkategorie namens **Kilometerstand**. Diese hat eine Einheitengruppe mit dem Namen **Entfernung** und eine Standardeinheit namens **Meile**. Wenn Sie die Einheitengruppe **Entfernung** so einrichten, dass diese zwei Einheiten (etwa **Meile** und **Kilometer**) aufweist, können Sie für die Kategorie **Kilometerstand** bei einer Preisliste zwei Preise festlegen: Preis pro Meile und Preis pro Kilometer.

| Ausgabenkategorie  | Einheitengruppe  | Einheit      | Preisberechnungsmethode  | Einzelpreis  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Kilometerstand           | Entfernung      | Meile      | Einzelpreis    | 10 USD            |
| Kilometerstand           | Entfernung      | Kilometer | Einzelpreis    |  6 USD            |

Wenn Sie bei einem Projekt eine Ausgabe eingeben, ermittelt das System den Preis anhand der Kombination aus Kategorie und Einheit bei der Ausgabe. 

| Ausgabenbeschreibung        | Ausgabenkategorie  | Einheit  | Menge  | Einzelpreis   |
|----------------------------|---------------------|-------|-----------|----------------|
| Fahrt zum Standort des Kunden | Kilometerstand             | Meile  | 10        | 10 USD         |

Für die Zeit enthält jede Kopfzeile der Preisliste ein Feld namens **Standard-Zeiteinheit**. Der Wert wird beim Erstellen der Kopfzeile der Preisliste festgelegt. Diese Einheit wird dann verwendet, um sämtliche rollenbasierten Preise für diese Preisliste festzulegen.

Vorkalkulationspositionen für das Feld **Zeit im Angebot** können in einer beliebigen Zeiteinheit ausgedrückt werden. Allerdings können Vorkalkulationspositionen und Zeiteinträge für Projekte nur die Zeiteinheit **Stunde** verwenden. Wenn die Einheit bei der Zeiteintrags- oder der Vorkalkulationsposition nicht mit der Einheit in der Preislistenzeile für diese Rolle übereinstimmt, konvertiert das System den Preis in die Einheiten, die in der Projektvorkalkulation bzw. der Projekt-Istwerte-Transaktion definiert sind.

Im folgenden Beispiel wird veranschaulicht, wie PSA die Einheitengruppe, die Einheiten und Umrechnungsfaktoren verwendet.
- Einheiten

   - **Einheitengruppe**: Zeit 
   - **Einheiten**: Stunde 
    
    - **Tag** – Umrechnungsfaktor: 8 Stunden       
    - **Woche** – Umrechnungsfaktor: 40 Stunden  
        
- Preislistenkonfiguration bei Projekt A:

    - **Name**: UK Verkaufspreise 2016 
    - **Standardzeiteinheit**: Tag 
    - **Währung**: GBP

| Rolle      | Einheitengruppe | Einheit | Organisationseinheit: | Preis   |
|-----------|------------|------|---------------------|---------|
| Entwickler | Time       | Day  | Koch UK          | 800 GBP |

### <a name="time-entry"></a>Zeiteintrag

Die folgende Tabelle enthält die resultierende verkaufsseitige Transaktion, die von PSA für ein dreistündiges Projekt erstellt wurde.


| Projekt   | Aufgabe    | Rolle      | Menge | Einheit  | Einzelpreis | Nicht fakturierter Umsatzbetrag |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projekt A | Entwurf  | Entwickler | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Zeiteinheit – Häufig gestellte Fragen

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Konvertiert PSA bei Ausgaben in verschiedene Einheiten?
Nr. Einheitenkonvertierung funktioniert nur für die Zeit. Wenn das System für Ausgaben keinen Preis für die Kombination aus Ausgabenkategorie und -Einheit findet, wird der Preis standardmäßig auf 0,00 festgelegt.

### <a name="why-does-psa-convert-time-units"></a>Warum konvertiert PSA Zeiteinheiten?
In einigen Ländern oder Regionen ist es gesetzlich vorgeschrieben, Rechnungssätze in Tagen festzulegen. Preisverhandlungen und die Gewährung von Rabatten finden während des Angebotszyklus statt, indem für jede abrechenbare Rolle Tagessätze verwendet werden. Zeitplanschätzung und Zeiteintrag erfolgen in Stunden. Zur Unterstützung dieses Unterschieds bei den Zeiteinheiten werden diese von PSA konvertiert.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Können Zeiteinheiten bei Projektvorkalkulationen geändert werden?
Nr. Die Zeitplanschätzung ist derzeit auf Stunden begrenzt und kann nicht geändert werden.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Können Einheiten und Einheitengruppen bearbeitet, gelöscht hinzugefügt werden?
Ja. Mit Ausnahme der Einheitengruppe **Zeit** und der Einheit **Stunde** können alle Einheiten gelöscht oder bearbeitet und neue Einheiten hinzugefügt werden. In PSA können die Einheitengruppe **Zeit** und die Einheit **Stunde** nicht gelöscht werden. Sie können jedoch mit einem übersetzten Text für das Feld **Name** aktualisiert werden.
