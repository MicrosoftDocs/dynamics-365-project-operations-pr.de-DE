---
title: Methoden für die Kosten zur Fertigstellung
description: Dieser Artikel informiert Sie über die Methoden zur Berechnung der Kosten für den Abschluss eines Projekts.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 39c10673afd04ad7d4a94a01211c2f9d335a02c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920289"
---
# <a name="cost-to-complete-methods"></a>Methoden für die Kosten zur Fertigstellung

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel informiert Sie über die Methoden zur Berechnung der Kosten für den Abschluss eines Projekts. Es gibt mehrere Methoden, mit denen Sie die Kosten für die Fertigstellung eines Projekts berechnen können. 

Wenn Sie einen Kostenvoranschlag für ein Projekt erstellen, können Sie auf der **Schätzung erstellen**-Seite im Feld **Kosten für die Fertigstellung der Methode** eine der folgenden Kosten auswählen, um die Methoden abzuschließen.

| Methode für die Kosten zur Fertigstellung    | Beschreibung des Dataflows                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gesamtkosten – Istwert            | Geben Sie die geschätzten Kosten manuell in das Feld **Gesamtkosten** oder die Felder **Gesamtstückzahl** mit der **Geschätzte Kosten**-Schaltfläche auf der **Seite schätzen** ein. Das System subtrahiert die tatsächlichen Kosten von den eingegebenen Summen. Die Summe sind die Kosten für die Fertigstellung des Projekts. Diese Methode verwendet nicht die Kostenschätzungen und Ressourcenzuweisungen, die in Project Operations in Microsoft Dataverse eingegeben wurden. Die Gesamtkosten oder die Gesamtmenge können bei Bedarf manuell aktualisiert werden.  |
| Gesamtprognoseistkosten        | Ressourcenzuweisungen und Kostenschätzungen werden verwendet, um den Gesamtbetrag der Projektprognose zu bestimmen. Die tatsächlichen Kosten werden mit dieser Prognose verglichen, um die auszuführenden Kosten zu berechnen.                                                                                                                                                                                                                                                                          |
| Als vorherige Schätzung         | Hier werden die gleichen Schätzmethoden verwendet, die in der Vorperiode verwendet wurden. Diese Methode erfordert ein Prognosemodell, wenn für die vorherige Periode ein Prognosemodell erforderlich war.                                                                                                                                                                                                                                                                                                                           |
| Setzen Sie die Kosten auf Null | Diese Methode wird normalerweise verwendet, bevor das Schätzprojekt eliminiert wird. Sie vergleicht die Gesamtschätzungen mit den gebuchten tatsächlichen Transaktionen und löscht die **Kosten für die Fertigstellung**-Spalte. Nach Abschluss ist das Ergebnis immer 100 Prozent. Für jede von Ihnen erstellte Kostenzeile wird das **Prognose**-Kontrollkästchen deaktiviert und die Gesamtschätzung wird aus der vorherigen Kostenschätzung kopiert. Der tatsächliche Verbrauch für den geschätzten Zeitraum wird von den Kosten für die Fertigstellung des Projekts abgezogen.              |
| Aus der Kostenvorlage           | Die Methode zum Abschließen der Kosten, die in der Kostenvorlage festgelegt ist, die dem ausgewählten Schätzprojekt zugeordnet ist.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]