---
title: Konfigurieren Sie die Standardkosten für Arbeit und Ausgaben
description: In diesem Thema wird erläutert, wie Standardkosten für Arbeitskräfte und Kosten für ein Projekt eingerichtet werden.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3716505"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Konfigurieren Sie die Standardkosten für Arbeit und Ausgaben

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Thema wird erläutert, wie Standardkosten für Arbeitskräfte und Kosten für ein Projekt eingerichtet werden. Diese Aufgabe verwendet die USSI Dataset.

1. Gehen Sie im Navigationsbereich zu **Module > Projektmanagement und -buchhaltung > Einrichtung > Preise > Einstandspreis (Stunden)**.
2. Wählen Sie **Neu**.
3. Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.
4. Geben Sie in das Feld **Einstandspreis** eine Zahl ein. Sie können einen Standardeinstandspreis für die Projektkategorie oder einen Einstandspreis nach Arbeiternummer, Projektnummer, Kategorie, Datum oder einer beliebigen Kombination davon festlegen. Der angewandte Einstandspreis ist der Einstandspreis mit dem höchsten Detaillierungsgrad.  
5. Wählen Sie **Speichern** aus.
6. Gehen Sie im Navigationsbereich zu **Module > Projektmanagement und -buchhaltung > Einrichtung > Preise > Verkaufspreis (Stunden)**.
7. Wählen Sie **Neu**.
8. Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.
9. Wählen Sie im Feld **Gültig zum** eine Option aus.
10. Geben Sie im Feld **Preisberechnung** eine Zahl ein. Sie können einen Standardverkaufspreis für Stundentransaktionen oder für eine Projektkategorie festlegen. Sie können Verkaufspreise auch nach Mitarbeiternummer, Projektnummer, Kategorie, Transaktionsdatum oder einer beliebigen Kombination davon einrichten. Der tatsächliche Verkaufspreis, der angewendet wird, wenn ein Mitarbeiter eine Transaktion in das Stundenjournal eingibt, ist der Verkaufspreis mit dem höchsten Detaillierungsgrad. Wenn beispielsweise sowohl ein allgemeiner Verkaufspreis als auch ein arbeiterspezifischer Verkaufspreis festgelegt sind, wird der arbeiterspezifische Verkaufspreis verwendet.  
11. Wählen Sie **Speichern** aus.
12. Schließen Sie die Seite.
13. Gehen Sie im Navigationsbereich zu **Module > Projektmanagement und -buchhaltung > Einrichtung > Preise > Einstandspreis (Ausgaben)**.
14. Wählen Sie **Neu**.
15. Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.
16. Geben Sie in das Feld **Einstandspreis** eine Zahl ein. Es können mehrere Felder ausgefüllt werden, dies ist jedoch das Minimum, das zum Speichern des Datensatzes erforderlich ist.  
17. Wählen Sie **Speichern** aus.
18. Gehen Sie im Navigationsbereich zu **Module > Projektmanagement und -buchhaltung > Einrichtung > Preise > Verkaufspreis (Ausgaben)**.
19. Wählen Sie **Neu**.
20. Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.
21. Wählen Sie im Feld **Gültig zum** eine Option aus.
22. Geben Sie im Feld **Preisberechnung** eine Zahl ein. Der tatsächliche Verkaufspreis, der angewendet wird, wenn ein Mitarbeiter Transaktionen in die Ausgabenerfassung eingibt, ist der Verkaufspreis mit dem höchsten Detaillierungsgrad. Wenn beispielsweise sowohl ein allgemeiner Verkaufspreis als auch ein arbeiterspezifischer Verkaufspreis festgelegt sind, wird der arbeiterspezifische Verkaufspreis verwendet.  
23. Wählen Sie **Speichern** aus.

