---
title: Projektbasierte Angebote kopieren
description: Dieses Thema bietet Informationen zum Kopieren von projektbasierten Angeboten in Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1e8611f34a23d6d87317cc785148c1a3f9c26dca
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588045"
---
# <a name="copy-project-based-quotes"></a>Projektbasierte Angebote kopieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Sie können ganz einfach ein neues Projektangebot erstellen, indem Sie ein vorhandenes kopieren. 

- Um ein Projektangebot zu kopieren, klicken Sie auf die **Projektangebote**-Listenseite oder die **Projektangebot**-Detailseite, wählen Sie das Projektangebot aus, das Sie kopieren möchten, und wählen Sie dann aus **Kopieren**.

Dadurch wird eine Dialogseite geöffnet, auf der Sie die Parameter der Kopie eingeben können. In der folgende Tabelle sind die Felder aufgeführt, auf der Dialogseite verfügbar sind. Abhängig von den ausgewählten Werten kann sich der Kopiervorgang ändern.

| **Feld** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- |
| Thema | Geben Sie das relevante Thema oder den Namen des Zielangebots ein. Wenn der Dialog geöffnet wird, legt das System es auf das Thema des Quellangebots fest und hängt **-Kopie** daran. | |
| Potenz. Kunde | Verweis auf die Firma oder den Kontodatensatz des Kunden. Wenn der Dialog geöffnet wird, legt das System es auf das Konto im Quellangebot fest. | Dieses Feld ist der Hauptkunde im Angebot. |
| Vertragseinheit | Die Organisationseinheit, die für die Bereitstellung des/der mit diesem Geschäft verbundenen Projekts/Projekte verantwortlich ist.
Wenn der Dialog geöffnet wird, legt das System es auf die Vertragseinheit des Quellangebots fest. | Vertragseinheit ist die Abteilung des Unternehmens, die die Projekte nach Abschluss des Geschäfts abschließt. Jede Vertragseinheit hat eine Währung. Die Währung wird verwendet, um geschätzte und tatsächliche Kosten zu melden, die während der Ausführung des Projekts anfallen. |
| Währung | Hier die Währung, in der der Deal ausgeführt wird. Wenn der Dialog geöffnet wird, legt das System es auf die Währung des Quellangebots fest. Dies kann geändert werden, und wenn es sich um eine Änderung handelt, wird das **Preise kopieren**-Feld immer auf **Nein** festgelegt. Dies liegt daran, dass die Preislisten im Quellangebot nicht mehr relevant sind. | Die Währung wird verwendet, um eine Preisliste als Standard festzulegen, eine finanzielle Schätzung des Angebots zu erstellen und dem Kunden schließlich eine Rechnung zu stellen, wenn das Geschäft gewonnen wurde. |
| Gewünschtes Lieferdatum | Dies ist der vom Kunden gewünschte Liefertermin. | Dies wird als Enddatum verwendet, wenn Rechnungsdaten entlang einer bestimmten Häufigkeit erstellt werden. |
| Preise kopieren | Ein Ja/Nein-Wert gibt an, ob der Preis für das Angebot aus dem Quellangebot kopiert werden soll. | Wenn **Ja** ausgewählt ist, werden die Referenzen der Projektpreisliste und der Produktpreisliste vom Quellangebot in das Zielangebot kopiert. Wenn **Nein** ausgewählt ist, werden Preislisten basierend auf den neuesten Preislisten, die für die Konto- oder Projektparameter eingerichtet wurden, auf die Standardeinstellungen zurückgesetzt. |

Wenn Sie **OK** auf der Dialogseite auswählen, erstellt das System eine Kopie des Projektangebots basierend auf den im Dialogfeld ausgewählten Parametern. Das neue Projektangebot wird geöffnet. 

> [!NOTE]
> Die folgenden Informationen werden nicht von der Quelle in das Zielangebot kopiert:
>
> - Rechnungszeitpläne
> - Angebots- und Angebotspositionskunden
> - Projektreferenz zu den projektbasierten Angebotspositionen – Informationen zum Kundenbudget
>
>Da diese Informationen für jedes Angebot sehr spezifisch sind, werden diese Felder und Datensätze nicht kopiert. Angebotspositionen für Projekte und Produkte, Schätzungen zu Angebotspositionsdetails und nicht zu überschreitende Werte auf Angebotsebene werden kopiert. Die Standardeinstellungen für Preis und Kostensatz hängen von der **Preise kopieren**-Option ab, die auf der **Parameter kopieren**-Dialogseite ausgewählt sind.


[!INCLUDE[footer-include](../includes/footer-banner.md)]