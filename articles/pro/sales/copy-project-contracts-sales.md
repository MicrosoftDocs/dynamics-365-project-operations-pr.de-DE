---
title: Projektverträge kopieren – Lite
description: Dieses Thema enthält Informationen zum Kopieren von Projektverträgen in Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 082cd6597a066f6dac8a7583a377d8e34bc74e2e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594071"
---
# <a name="copy-project-contracts---lite"></a>Projektverträge kopieren – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Sie können ganz einfach neue Projektverträge erstellen, indem Sie Kopien bestehender Verträge auf zwei Arten erstellen: 

  - Wählen Sie auf der Listenseite **Projektverträge** einen Projektvertrag und dann **Kopieren** aus.
  - Wählen Sie auf der Detailseite **Projektvertrag** die Option **Kopieren** aus.

Eine Dialogseite wird geöffnet, auf der Sie die Parameter des kopierten Vertrags auswählen können. Die folgenden Felder sind im Dialog enthalten. Abhängig von den ausgewählten Werten in diesem Dialog kann sich der Kopiervorgang ändern.

| **Feld** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- |
| Thema | Geben Sie das Thema des Zielvertrags ein. Wenn die Dialogseite geöffnet wird, legt das System dieses Feld auf den Namen des Quellvertrags fest und hängt **copy** an. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Kunde | Verweis auf die Firma oder den Kontodatensatz des Kunden. Wenn der Dialog geöffnet wird, legt das System dieses Feld auf das Konto im Quellvertrag fest. | Dieses Feld ist der Hauptkunde im Vertrag. |
| Vertragseinheit | Die Organisationseinheit, die für die Bereitstellung des/der mit diesem Geschäft verbundenen Projekts/Projekte verantwortlich ist. Wenn die Dialogseite geöffnet wird, legt das System es auf die Vertragseinheit des Quellvertrags fest. | Die Vertragseinheit ist die Abteilung des Unternehmens, die die Projekte nach Abschluss des Geschäfts abschließt. Jede Vertragseinheit hat eine Währung. Diese Währung wird verwendet, um geschätzte und tatsächliche Kosten zu melden, die während der Ausführung des Projekts anfallen. |
| Währung | Die Währung, in der das Geschäft ausgeführt wird Wenn die Dialogseite geöffnet wird, legt das System das Feld auf die Währung des Quellvertrags fest. Die Währung kann geändert werden. Wenn dies der Fall ist, ist das Feld **Preisberechnung kopieren** immer auf **Nein** festgelegt, da die Preislisten im Quellvertrag nicht länger relevant sind. | Die Währung wird für Standardpreislisten, zum Erstellen von finanziellen Schätzungen zum Vertrag und zum Erstellen einer Rechnung an den Kunden verwendet, wenn das Geschäft gewonnen wurde. |
| Gewünschtes Lieferdatum | Das vom Kunden angeforderte Bereitstellungsdatum | Dieses Datum wird als Enddatum verwendet, wenn Sie Rechnungsdaten mit einer bestimmten Häufigkeit erstellen. |
| Preise kopieren | Gibt an, ob die Preise im Vertrag aus dem Quellvertrag kopiert werden sollen | Wenn das Feld auf **Ja** festgelegt ist, werden die Referenzen der Projekt- und Produktpreislisten aus dem Quell- in den Zielvertrag kopiert. Wenn **Nein** ausgewählt ist, werden Preislisten basierend auf den neuesten Preislisten in den Konto- oder Projektparametern auf die Standardeinstellungen gesetzt. |

Wenn Sie **OK** auf der Dialogseite auswählen, erstellt das System eine Kopie des Vertrags basierend auf den ausgewählten Parametern. Der neue Vertrag wird eröffnet.

Die folgenden Informationen werden nicht vom **Quell-** in den **Zielvertrag** kopiert:

  - Rechnungszeitpläne
  - Vertrags- und Vertragszeilen-Kunden
  - Projektreferenz in den projektbasierten Vertragszeilen
  - Kundenbudgetinformationen

Da diese Informationen für jeden Vertrag spezifisch sind, werden diese Felder und Datensätze nicht kopiert. Vertragszeilen für Projekte und Produkte, Schätzungen zu Vertragszeilendetails und nicht zu überschreitende Werte auf Vertragsebene werden kopiert. Die Standardeinstellungen für Preis und Kostensatz hängen von der Auswahl im Feld **Preisberechnung kopieren** auf der Dialogseite **Parameter kopieren** ab.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]