---
title: Konfigurieren Sie die Standardkosten für Arbeit und Ausgaben
description: Dieser Artikel erklärt, wie Sie Standardkosten für Arbeit und Spesen für ein Projekt festlegen können.
author: Yowelle
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a51eee8d2eb960b6f24b6511dab7b7a27303dddb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919508"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Konfigurieren Sie die Standardkosten für Arbeit und Ausgaben

[!include [banner](../../includes/banner.md)]

Dieser Artikel erklärt, wie Sie Standardkosten für Arbeit und Spesen für ein Projekt festlegen können. Diese Aufgabe verwendet die USSI Dataset.

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]