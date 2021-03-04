---
title: Projektprognosen und Budgets
description: Microsoft Dynamics 365 Finance stellt Projektprognosen und Projektbudgets bereit, um Ihre Projekte zu verwalten und zu steuern.
author: Yowelle
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f99c00effbb0678f1f55e5068a7128cbfb86f5ce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076637"
---
# <a name="project-forecasts-and-budgets"></a>Projektprognosen und Budgets

[!include [banner](../includes/banner.md)]

Es gibt zwei Möglichkeiten, Ihre Projekte zu verwalten und zu steuern: Projektprognosen und Projektbudgets. 

Sie können Projektprognosen verwenden, wenn Ihre Organisation eine betriebliche Perspektive hat und sich auf die Einnahmen und Kosten konzentriert, die aus bestimmten Transaktionen abgeleitet werden. Verwenden Sie Projektprognosen, wenn sich Ihre Organisation mehr auf finanzielle Beträge konzentriert, 

Sowohl Projektprognosen als auch Projektbudgets verwenden Prognosemodelle, um die projizierten Transaktionsbeträge zu speichern. 

Jede Methode hat ihre Vorteile. Sie sollten die folgenden Punkte berücksichtigen, bevor Sie eine Methode für Ihre Organisation auswählen.

|   Zuordnungsmethode       |           Projektprognose            |        Projektbudgetierung                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Periodenzuteilung**     | Sie können Transaktionen nicht explizit über ein Buchhaltungsperiode zuordnen. Stattdessen basieren die Prognose und die Steuerung der Prognose auf der Laufzeit des Projekts. Da Prognosen auf einem bestimmten Datum basieren, müssen Sie den Zeitraum aus dem Datum ableiten. | Sie können Transaktionen nicht explizit über eine Buchhaltungsperiode oder das gesamte Projekt zuordnen. Wenn Sie über einen Zeitraum hinweg zuweisen, können Sie nicht verwendete Beträge auf die nächste Buchhaltungsperiode übertragen. |
| **Transaktionen anzeigen**  | Sie können Transaktionen in den Prognoseformularen anzeigen, in denen Sie die Prognosen für das gesamte Unternehmen und für alle Projekte unabhängig von der Hierarchie anzeigen. Um sich auf ein bestimmtes Projekt zu konzentrieren, müssen Sie die Daten filtern.                                       | Sie können budgetierte Transaktionen für eine einzelne Projekthierarchie anzeigen. Daher können Sie Transaktionsdetails für ein übergeordnetes Projekt oder seine Unterprojekte anzeigen.                 |
| **Transaktionsvariablen** | Wenn Sie Prognosetransaktionen eingeben, können Sie jedes Attribut verwenden, das für eine tatsächliche Transaktion vorhanden ist. Dies ermöglicht detailliertere Angaben in der Prognose. Sie können beispielsweise Details für Mengen, Arbeiter, Artikel oder Zeileneigenschaften eingeben.         | Wenn Sie Budgetdetails eingeben, können Sie nur Beträge, Kategorien und Aktivitäten verwenden.                    |
| **Sicherheit**              | Die Prognose basiert auf Transaktionen, die Sie in die Prognoseformulare eingeben, und beinhaltet keinen Prozesssteuerungsmechanismus. Jeder Mitarbeiter, der über Berechtigungen für ein Prognoseformular verfügt, kann Informationen ohne Genehmigung überarbeiten.                                        | Bei der Budgetierung wird das Workflow-System verwendet, das das Änderungsmanagement ermöglicht und es Ihnen ermöglicht, einen Verlauf der Revisionen zu führen.         |
| **Eingabetypen**           | Prognosetransaktionseinträge basieren auf der Anzahl der Einheiten sowie auf Kosten und Verkaufspreis.  | Budgetdetails basieren auf Beträgen, die zwischen Kosten und Einnahmen aufgeteilt werden.                                          |
| **Prognosemodelle**       | Da jede Prognose einem Modell zugeordnet sein muss, können Sie mehrere Prognosemodelle erstellen und auch Untermodelle einrichten.           | Die Projektbudgetierung begrenzt die Prognosemodelle, die für die Budgetierung verwendet werden. Weniger Prognosemodelle können dazu beitragen, die Konsistenz der Projektionen zu erhöhen.                           |
| **Kostenüberschreitungen**         | Sie können nur die Eingabe von Transaktionen zulassen oder untersagen, die zu einer Kostenüberschreitung führen.   | Die Projektbudgetierung bietet zusätzliche Steuerungsoptionen für Benutzer. Sie können Warnungen und Überschreitungen zulassen.                    |
| **Steuerelement**               | Die Prognosesteuerung erfolgt mithilfe der Prognosereduzierung. Die tatsächlichen Beträge werden von den prognostizierten Transaktionssalden ohne Audit-Trail abgezogen. Dies kann es schwieriger machen zu verfolgen, wo die tatsächlichen Transaktionen stattgefunden haben.                   | Bei der Projektbudgetkontrolle werden die tatsächlichen Beträge von den Beträgen im verbleibenden Budget abgezogen. Dies ermöglicht einen klareren Audit-Trail.                                   |

## <a name="project-forecasts"></a>Projektprognosen
Wenn Sie die Projektprognose verwenden, können Sie für jeden Transaktionstyp Prognosetransaktionen eingeben. Jedes Attribut, das für eine tatsächliche Transaktion verfügbar ist, kann für eine Prognosetransaktion verwendet werden, z. B. Zeilenrentabilität, Zeilenattribute, Mitarbeiter oder Beschreibungen. Sie können auch projizieren, wie lange Sie nach dem Entstehen von Kosten einem Kunden eine Rechnung stellen. 

Projektprognosetransaktionen basieren auf Einheiten und Beträgen. 

Sie müssen jede Projektprognose einem Prognosemodell zuordnen. Wenn Sie eine Prognosetransaktion eingeben, wird automatisch ein Prognosemodell vorgeschlagen. Das Prognosemodell fungiert als Behältnis für die Prognosetransaktionen. 

Sie können Prognosemodelle als Untermodelle für ein Modell festlegen. Auf diese Weise können Sie Prognosen nach Region, Zeitraum oder Abteilung erstellen. Sie können die Prognosetransaktionen in ein Modell kopieren, um ein neues Modell zu erstellen, und Sie können die Transaktionen auch in das Hauptbuch übertragen. Da zwischen einer Prognose und einem Modell eine Eins-zu-Eins-Beziehung besteht, bildet jedes Prognosemodell ein separates Budget für ein Projekt. 

Prognosemodelle können die Prognosereduzierung als Kontrollmechanismus für Projekte verwenden. Bei der Prognosereduzierung reduzieren tatsächliche Transaktionen die prognostizierten Transaktionssalden. Da die Prognosereduzierung jedoch auf das höchste Projekt in der Hierarchie angewendet wird, bietet sie eine eingeschränkte Ansicht der Änderungen in der Prognose. Wenn beispielsweise ein Worker einem Teilprojekt zugeordnet ist, werden die tatsächlichen Transaktionen für den Worker in das übergeordnete Projekt gebucht. Dies kann es schwierig machen, Änderungen zu verfolgen, da Sie nicht leicht feststellen können, welche Transaktion in welchem Teilprojekt zu einer Reduzierung des prognostizierten Betrags geführt hat. Daher ist es eine gute Idee, eine Kopie eines Prognosemodells zu erstellen, damit die Prognosereduzierung verwendet werden kann. Sie können dann Berichte verwenden, um anzuzeigen, was ursprünglich prognostiziert wurde. 

Sie können Projektprognosen überarbeiten, kopieren, löschen oder in ein Hauptbuchbudget übertragen. Es gibt jedoch keine Prozesssteuerung. Jeder Mitarbeiter, der über Berechtigung für ein Prognoseformular verfügt, kann Überarbeitungen ohne Bewertung machen.

-   **Überarbeitungen** – Sie können eine Prognosetransaktion in denselben Formen überarbeiten, in denen die ursprünglichen Einträge vorgenommen wurden.
-   **Kopieren oder löschen** – Wenn Sie Prognosetransaktionen kopieren, kopieren Sie die Transaktionszeilen eines Prognosemodells in ein anderes Prognosemodell. Wenn Sie eine Prognose löschen, löschen Sie die Prognosetransaktionen aus einem Prognosemodell. Wählen Sie bestimmte Transaktionstypen und -daten aus, um die prognostizierten Transaktionen zu begrenzen, die kopiert oder gelöscht werden. Auf diese Weise können Sie nur bestimmte Teile einer Prognose kopieren oder löschen.
-   **Übertragung** – Wenn Sie eine Projektprognose in ein Hauptbuchbudget übertragen, übertragen Sie die Prognosetransaktionen eines Prognosemodells in ein Hauptbuchbudget. Sie können alle zuvor übertragenen Transaktionen im Hauptbuchbudget überschreiben, in das Sie Ihre Projektprognose übertragen.

## <a name="project-budgets"></a>Projektbudgets
Die Projektbudgetierung ist eine einfachere Methode als die Prognose, obwohl sie in Prognosemodelle integriert ist. Es verwendet ein einzelnes Eingabeformular für ursprüngliche Budgetdetails und -Revisionen und ermöglicht Projektionen, die nur auf Betrag, Kategorie oder Aktivität basieren. 

Bei der Projektbudgetierung müssen alle ursprünglichen Budgets und Überarbeitungen zur Genehmigung an einen Projektworkflow gesendet werden. Mit Workflows können Sie den Prozess besser steuern und einen Änderungsverlaufsdatensatz erstellen. 

Die Projektbudgetierung ähnelt der Hauptbuchbudgetierung, ist jedoch schneller und einfacher einzurichten. Viele der Optionen in der Hauptbuchbudgetierung, wie z. B. Zahlenfolgen oder Währung, müssen für Projekte nicht separat eingerichtet werden.

Projektbudgets werden automatisch zwei Prognosemodellen zugeordnet, eines für das ursprüngliche Budget und eines für das verbleibende Budget. Daher können Berichte, die auf Prognosemodellen basieren, Budgetdaten verwenden. Wenn ein Projektbudget festgelegt wird, erstellt das System Prognosetransaktionen basierend auf den zugehörigen Modellen, die für Berichts- und Kontrollzwecke verwendet werden.

## <a name="forecast-models"></a>Prognosemodelle
Prognosemodelle haben eine einschichtige Hierarchie. Dies bedeutet, dass eine Projektprognose einem Prognosemodell zugeordnet werden muss.

Wenn Sie die Projektprognose verwenden, können Sie Modelle als Untermodelle identifizieren. So können Sie Prognosen nach Region, Zeitraum oder Abteilung erstellen. Sie können beispielsweise ein Prognosemodell für ein Jahr erstellen und anschließend Untermodelle für die regionalen Prognosen für Nordosten, Südosten, Nordwesten und Südwesten erstellen, die von regionalen Leitern übermittelt werden. Durch Auswahl verschiedener Optionen in den verfügbaren Berichten können Sie Informationen nach Gesamtprognose oder nach Untermodell anzeigen.





[!INCLUDE[footer-include](../includes/footer-banner.md)]