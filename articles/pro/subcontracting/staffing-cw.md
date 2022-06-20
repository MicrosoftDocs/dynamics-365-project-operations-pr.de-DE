---
title: Besetzung eines Projekts mit Vertragsmitarbeitern und Fremdarbeitskapazität
description: Dieser Artikel erklärt, wie Sie in Microsoft Dynamics 365 Project Operations Projektanforderungen mit Hilfe von Vertragskräften oder Subunternehmern erfüllen können.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 173e1c20d2d046ee2120ec178e51d4868b70847d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922083"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Besetzung eines Projekts mit Vertragsmitarbeitern und Fremdarbeitskapazität

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Generische Projektteammitglieder können mit Angestellten oder Vertragsmitarbeitern besetzt werden. Wenn Sie ein Projekt mit Vertragsarbeitern besetzen, können Sie Ihre Besetzungsoptionen auf bestimmte Vertragsarbeiter beschränken, die einer Fremdarbeitsposition zugeordnet sind. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Suche nach Personalressourcenbedarf mit Vertragsmitarbeitern, die zu einer bestimmten Fremdarbeitsposition gehören

Gehen Sie wie folgt vor, um nach Personalressourcenbedarf mit Vertragsmitarbeitern zu suchen, die zu einer bestimmten Fremdarbeitsposition gehören:

1. Erstellen Sie ein allgemeines Projektteammitglied, das auf eine Fremdarbeit und eine Fremdarbeitsposition verweist.
2. Generieren Sie einen Ressourcenbedarf für dieses generische Projektteammitglied, indem Sie die Schaltfläche **Anforderung generieren** im Unterraster der Projektteammitglieder verwenden.
3. Wählen Sie die Zeile mit den Teammitgliedern aus und wählen Sie dann die Schaltfläche **Buchen** im Unterraster. 
4. Dadurch wird die Zeitplanübersicht mit dem Anforderungskontext geöffnet. Zusammen mit anderen Attributen wie Datums-, Rollen- und Organisationseinheitsfeldern werden die Zeitplanübersicht-Filter auch automatisch mit den Feldern Kreditor, Fremdarbeit und Fremdarbeitsposition aus dem Ressourcenbedarf gefüllt.
5. Das System sucht nach Ressourcen, die den Filterkriterien entsprechen, und listet sie auf. 
6. Wählen Sie eine der gefilterten Ressourcen aus und buchen Sie die Ressource für die Anforderung. 
7. Ein Projektteammitglied wird erstellt und mit Fremdarbeits‑ und Fremdarbeitspositionsreferenzen aktualisiert. Gehen Sie zu **Projektschätzungen** und wählen Sie **Preise aktualisieren**, um die aktualisierten Kosten der Ressourcenzuweisung anzuzeigen. 

> [!NOTE]
> Das Aktualisieren des Projektteammitglieds mit einem Fremdarbeits‑ und Fremdarbeitspositionsbezug ist während der Buchung möglicherweise nicht immer möglich, wenn die Ressource mehreren Fremdarbeitspositionen zugewiesen ist. Wenn das System das Projektteammitglied nicht mit einer Fremdarbeit und Fremdarbeitsposition aktualisieren kann, öffnen Sie den Projektteammitgliedsdatensatz und aktualisieren Sie diese Felder, damit die Finanzkostenschätzung die Fremdarbeitkosten auf dem Schätzungen-Tab genau widerspiegelt.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Suche nach und Besetzen von Ressourcenanforderungen mit einem beliebigen Vertragsarbeiter

Gehen Sie wie folgt vor, um Ressourcenanforderungen zu suchen und sie mit einem beliebigen Vertragsarbeiter zu besetzen:

1. Erstellen Sie ein generisches Projektteammitglied.
2. Generieren Sie einen Ressourcenbedarf für dieses generische Projektteammitglied, indem Sie die Schaltfläche **Anforderung generieren** im Unterraster der Projektteammitglieder verwenden.
3. Wählen Sie die Zeile mit den Teammitgliedern aus und wählen Sie dann die Schaltfläche **Buchen** im Unterraster. 
4. Dadurch wird die Zeitplanübersicht mit dem Anforderungskontext geöffnet. Zusammen mit anderen Attributen wie Datums-, Rollen- und Organisationseinheitsfeldern werden die Zeitplanübersicht-Filter auch automatisch mit den Feldern Kreditor, Fremdarbeit und Fremdarbeitsposition aus dem Ressourcenbedarf gefüllt. Da für die Anforderung keine Fremdarbeits‑ oder Fremdarbeitspositionswerte ausgefüllt wurden, sind diese Attribute im Filterbereich leer.
5. Das System sucht nach Ressourcen, die den Filterkriterien entsprechen, und listet sie auf.
6. Aktualisieren Sie das Feld **Arbeitertyp** im Filterbereich zu **Vertragsarbeiter**, um die Suche auf Vertragsarbeiter zu beschränken. Aktualisieren Sie **Hersteller** im Filterbereich, um die Suche so einzuschränken, dass nur Vertragsarbeiter angezeigt werden, die zu einem bestimmten Herstellerunternehmen gehören.
7. Wählen Sie einen Vertragsarbeiter aus der Liste aus und buchen Sie die Ressource für den Bedarf.
8. Ein Projektteammitglied wird erstellt. Das Projektteammitglied wird jedoch nicht mit einer Fremdarbeit oder einer Fremdarbeitsposition aktualisiert, und daher wird die Ressourcenzuordnung nicht mit der Fremdarbeitspreiskalkulation kalkuliert. Aktualisieren Sie das Projektteammitglied manuell mit einer Fremdarbeitsposition und gehen Sie zu **Projektschätzungen** und wählen Sie **Preise aktualisieren**, um die aktualisierten Kosten der Ressourcenzuweisung anzuzeigen.

> [!NOTE]
> Projektteammitglieder, bei denen bei **Arbeitertyp** die Option **Vertragsarbeiter**, aber keine Fremdarbeitsreferenz ausgewählt ist, sind als **Ungültig** auf dem **Projektteammitglieder**-Raster gekennzeichnet. Wenn Projektteammitglieder mit diesem Status vorhanden sind, öffnen Sie den Projektteammitgliedsdatensatz und aktualisieren Sie die Felder für die Fremdarbeit und Fremdarbeitspositionen manuell, damit die Finanzkostenschätzung die Fremdarbeitkosten auf dem **Schätzungen**-Tab genau widerspiegelt. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
