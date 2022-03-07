---
title: Methoden für die Kosten zur Fertigstellung
description: Dieses Thema enthält Informationen zu den Methoden zur Berechnung der Kosten für die Fertigstellung eines Projekts.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fe42ea0e1a5c562ec648fbf2a2924648af80381b9db8ffe0c209cb5247bb2ba2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997965"
---
# <a name="cost-to-complete-methods"></a>Methoden für die Kosten zur Fertigstellung

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieses Thema enthält Informationen zu den Methoden zur Berechnung der Kosten für die Fertigstellung eines Projekts. Es gibt mehrere Methoden, mit denen Sie die Kosten für die Fertigstellung eines Projekts berechnen können. 

Wenn Sie einen Kostenvoranschlag für ein Projekt erstellen, können Sie auf der **Schätzung erstellen**-Seite im Feld **Kosten für die Fertigstellung der Methode** eine der folgenden Kosten auswählen, um die Methoden abzuschließen.

| Methode für die Kosten zur Fertigstellung    | Beschreibung des Dataflows                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gesamtkosten – Istwert            | Geben Sie die geschätzten Kosten manuell in das Feld **Gesamtkosten** oder die Felder **Gesamtstückzahl** mit der **Geschätzte Kosten**-Schaltfläche auf der **Seite schätzen** ein. Das System subtrahiert die tatsächlichen Kosten von den eingegebenen Summen. Die Summe sind die Kosten für die Fertigstellung des Projekts. Diese Methode verwendet nicht die Kostenschätzungen und Ressourcenzuweisungen, die in Project Operations in Microsoft Dataverse eingegeben wurden. Die Gesamtkosten oder die Gesamtmenge können bei Bedarf manuell aktualisiert werden.  |
| Gesamtprognoseistkosten        | Ressourcenzuweisungen und Kostenschätzungen werden verwendet, um den Gesamtbetrag der Projektprognose zu bestimmen. Die tatsächlichen Kosten werden mit dieser Prognose verglichen, um die auszuführenden Kosten zu berechnen.                                                                                                                                                                                                                                                                          |
| Als vorherige Schätzung         | Hier werden die gleichen Schätzmethoden verwendet, die in der Vorperiode verwendet wurden. Diese Methode erfordert ein Prognosemodell, wenn für die vorherige Periode ein Prognosemodell erforderlich war.                                                                                                                                                                                                                                                                                                                           |
| Setzen Sie die Kosten auf Null | Diese Methode wird normalerweise verwendet, bevor das Schätzprojekt eliminiert wird. Sie vergleicht die Gesamtschätzungen mit den gebuchten tatsächlichen Transaktionen und löscht die **Kosten für die Fertigstellung**-Spalte. Nach Abschluss ist das Ergebnis immer 100 Prozent. Für jede von Ihnen erstellte Kostenzeile wird das **Prognose**-Kontrollkästchen deaktiviert und die Gesamtschätzung wird aus der vorherigen Kostenschätzung kopiert. Der tatsächliche Verbrauch für den geschätzten Zeitraum wird von den Kosten für die Fertigstellung des Projekts abgezogen.              |
| Aus der Kostenvorlage           | Die Methode zum Abschließen der Kosten, die in der Kostenvorlage festgelegt ist, die dem ausgewählten Schätzprojekt zugeordnet ist.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]