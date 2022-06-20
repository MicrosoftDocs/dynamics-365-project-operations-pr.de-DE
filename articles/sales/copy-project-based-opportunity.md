---
title: Projektbasierte Verkaufschancen kopieren
description: Dieser Artikel enthält Informationen über das Kopieren von projektbasierten Verkaufschancen in Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cc772391de97f4b2de6e9e29f97a6af4d5514319
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926131"
---
# <a name="copy-project-based-opportunities"></a>Projektbasierte Verkaufschancen kopieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


Projektverkaufschancen können ganz einfach kopiert werden, um neue Projektverkaufschancen zu erstellen. 

1. Navigieren Sie zur Listenseite **Projektverkaufschancen**, und wählen Sie eine Verkaufschance aus der Liste aus. Oder öffnen Sie die Detailseite einer bestimmten Verkaufschance. 
2. Wählen Sie über eine der Seiten **Kopieren** aus. Eine Dialogseite mit den folgenden Feldinformationen wird geöffnet. Abhängig von den ausgewählten Werten in diesem Dialog kann sich der Kopiervorgang ändern.

    | **Feld** | **Beschreibung** | **Downstream-Auswirkungen** |
    | --- | --- | --- |
    | Thema | Geben Sie das relevante Thema der Zielverkaufschance ein. Wenn der Dialog geöffnet wird, legt das System es auf das Thema der Quellverkaufschance fest und hängt **copy** an. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
    | Konto | Verweise auf das Unternehmen oder den Firmendatensatz des Kunden Wenn der Dialog geöffnet wird, legt das System es auf das Konto in der Quellverkaufschance fest. | Dieses Feld ist der Hauptkunde in der Verkaufschance. |
    | Vertragseinheit | Die Organisationseinheit, die für die Bereitstellung der mit diesem Geschäft verbundenen Projekte verantwortlich ist. Wenn der Dialog geöffnet wird, legt das System es auf die Vertragseinheit der Quellverkaufschance fest. | Die Vertragseinheit ist die Abteilung des Unternehmens, die die Projekte nach Abschluss des Geschäfts durchführt. Jede Vertragseinheit hat eine Währung, und diese Währung wird verwendet, um geschätzte und tatsächliche Kosten zu melden, die während des Projekts anfallen. |
    | Währung | Die Währung, in der das Geschäft ausgeführt wird Wenn die Dialogseite geöffnet wird, legt das System es auf die Währung der Quellverkaufschance fest. | Die Währung wird verwendet, um eine Preisliste als Standard festzulegen und finanzielle Schätzungen für das Angebot zu erstellen. Schließlich wird die Währung verwendet, um dem Kunden eine Rechnung zu stellen, wenn das Geschäft gewonnen wird. |
    | Preise kopieren | Ein Ja/Nein-Wert, der angibt, ob der Preis für die Verkaufschance von der Quellverkaufschance kopiert werden soll. | Wenn **Ja** ausgewählt ist, werden Preislisten von der Quell- in die Zielverkaufschance kopiert. Wenn **Nein** ausgewählt ist, werden Preislisten basierend auf den neuesten Preislisten, die eingerichtet wurden, auf die Standardeinstellungen zurückgesetzt. |

3. Klicken Sie auf **OK**. Das System erstellt anhand der ausgewählten Parameter eine Kopie der Projektverkaufschance und die neue Projektverkaufschance wird geöffnet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]