---
title: Projektbasierte Verträge kopieren
description: Dieser Artikel enthält Informationen über das Kopieren von Projektverträgen in Microsoft Dynamics 365 Project Operations
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410321"
---
# <a name="copy-project-based-contracts"></a>Projektbasierte Verträge kopieren

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Sie können ganz einfach neue Projektverträge erstellen, indem Sie Kopien bestehender Verträge auf zwei Arten erstellen:

- Wählen Sie auf der Listenseite **Projektverträge** einen Projektvertrag und dann **Kopieren** aus.
- Wählen Sie auf der Detailseite **Projektvertrag** die Option **Kopieren** aus.

In beiden Fällen öffnet sich eine Dialogseite, auf der Sie die Parameter des kopierten Vertrags auswählen können. Die folgenden Felder sind im Dialogfeld enthalten. Abhängig von den ausgewählten Werten kann sich der Kopiervorgang allenfalls ändern.

| Feld | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- |
| Thema | Geben Sie das Thema des Zielvertrags ein. Wenn die Dialogseite offen ist, legt das System dieses Feld auf den Namen des Quellvertrags fest und hängt das Wort Kopie an. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
| Kundin/Kunde | Ein Verweis auf das Unternehmen des Kunden oder den Firmendatensatz Wenn der Dialog offen ist, legt das System dieses Feld auf das Konto im Quellvertrag fest. | Dieses Feld ist der Hauptkunde im Vertrag. |
| Zuständiges Unternehmen | Die Organisation, die für die Bereitstellung des mit diesem Geschäft verbundenen Projekts verantwortlich ist. Wenn der Dialog offen ist, legt das System dieses Feld auf das Konto im Quellvertrag der Organisation fest. | Die Eigentümergesellschaftt ist die Abteilung des Unternehmens, die die Projekte nach Abschluss des Geschäfts abschließt. Die Währung der Eigentümergesellschaft muss die Währung der Vertragseinheit des Projekts abgleichen. |
| Vertragseinheit | Die Organisationseinheit, die für die Bereitstellung des/der mit diesem Geschäft verbundenen Projekts verantwortlich ist. Wenn der Dialog offen ist, legt das System dieses Feld auf das Konto im Quellvertrag der Vertragseinheit fest. | Die Vertragseinheit ist die Abteilung des Unternehmens, die die Projekte nach Abschluss des Geschäfts abschließt. Jede Vertragseinheit hat eine Währung. Diese Währung wird verwendet, um geschätzte und tatsächliche Kosten zu melden, die während der Ausführung des Projekts anfallen. |
| Währungen | Die Währung, in der das Geschäft ausgeführt wird Wenn die Dialogseite geöffnet wird, legt das System das Feld auf die Währung des Quellvertrags fest. Die Währung kann geändert werden. Wenn dies der Fall ist, ist das Feld **Preisberechnung kopieren** immer auf **Nein** festgelegt, da die Preislisten im Quellvertrag nicht länger relevant sind. | Diese Währung wird für Standardpreislisten, zum Erstellen von finanziellen Schätzungen zum Vertrag und zum Erstellen einer Rechnung an den Kunden verwendet, wenn das Geschäft gewonnen wurde. |
| Gewünschtes Lieferdatum | Das vom Kunden angeforderte Bereitstellungsdatum. | Dieses Datum wird als Enddatum verwendet, wenn Sie Rechnungsdaten mit einer bestimmten Häufigkeit erstellen. |
| Preise kopieren | Ein Wert, der angibt, ob die Preise im Vertrag aus dem Quellvertrag kopiert werden sollen | Wenn das Feld auf **Ja** festgelegt ist, werden die Referenzen der Projekt- und Produktpreislisten aus dem Quell- in den Zielvertrag kopiert. Wenn auf **Nein** festgelegt, werden Preislisten basierend auf den neuesten Preislisten in den Konto- oder Projektparametern auf die Standardeinstellungen gesetzt. |

Wenn Sie **OK** auf der Dialogseite auswählen, erstellt das System eine Kopie des Vertrags basierend auf den ausgewählten Parameterwerten. Dann wird der neue Vertrag geöffnet.

Die folgenden Informationen sind **nicht** aus dem Quellvertrag in den Zielvertrag kopiert, da es für jeden Vertrag spezifisch ist:

- Rechnungszeitpläne
- Vertrags- und Vertragszeilen-Kunden
- Projektreferenz in den projektbasierten Vertragszeilen
- Kundenbudgetinformationen

Vertragszeilen für Projekte und Produkte, Schätzungen zu Vertragszeilendetails und nicht zu überschreitende Werte auf Vertragsebene werden kopiert. Die Standardeinstellungen für Preis und Kostensatz hängen von der Auswahl im Feld **Preisberechnung kopieren** auf der Dialogseite **Parameter kopieren** ab.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
