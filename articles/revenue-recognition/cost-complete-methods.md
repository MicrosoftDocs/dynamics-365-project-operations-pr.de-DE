---
title: Methoden für die Kosten zur Fertigstellung
description: Dieses Thema enthält Informationen zu den Methoden zur Berechnung der Kosten für die Fertigstellung eines Projekts.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 790b5c98182acdc0a37e3741a40baf7152f0bf66
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531430"
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
