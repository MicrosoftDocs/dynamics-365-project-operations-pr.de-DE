---
title: Kostenschätzung von Fremdarbeitsressourcenzuweisungen
description: In diesem Thema wird erklärt, wie Microsoft Dynamics 365 Project Operations die Kostenschätzung von Fremdarbeitsressourcenzuweisungen berechnet.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f276e12713261538d1e7520dac17243e578db433
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596693"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Kostenschätzung von Fremdarbeitsressourcenzuweisungen

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Aufgabenzuweisungen von Fremdarbeit-Projektteammitgliedern werden anhand der Preisliste **Kauf** kalkuliert, die der Fremdarbeit im entsprechenden Teammitgliedsdatensatz beigefügt ist. Dies unterscheidet sich von der Kalkulation von Mitarbeiterressourcenzuweisungen, bei denen Aufgabenzuweisungen von Mitarbeiterressourcen mithilfe der Preisliste **Kosten** kalkuliert werden, die der Vertragseinheit des Projekts beigefügt ist. 

Für generische Fremdarbeit-Projektteammitgliedern werden die Zuweisungen anhand der rollenbasierten Preisgestaltung in der Preisliste „Kauf“ kalkuliert, die der Fremdarbeit beigefügt ist. Auch Einkaufspreise können für jede Ressource spezifisch eingerichtet werden. Diese ressourcenspezifischen Preise werden bei der Kalkulation von Aufgabenzuweisungen von benannten Projektteammitgliedern als Vertragsarbeiter bevorzugt. 

Die Priorität der Verwendung des rollenspezifischen Einkaufspreises gegenüber dem ressourcenspezifischen wird durch die Einrichtung der Preisdimensionspriorität in **Parameter > Betragsbasierte Preisdimension** bestimmt.

Diese Funktionalität des dynamischen Ableitens von Preisen basierend auf der Dimensionseinstellung für Einkaufspreise von Subunternehmern ähnelt der Ableitung von Kosten- und Rechnungssätzen für Vollzeitmitarbeiter. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Erstellen von Aufgabenzuweisungen zum Abrufen von Kostenschätzungen von Subunternehmerressourcen

Aufgabenzuordnungen für Subunternehmer können auf zwei Arten erstellt werden: 
- Verwendung des **Aufgaben**-Tab.
- Verwendung des **Team**-Tab.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Erstellen von Ressourcenzuweisungen über die Registerkarte „Aufgaben“
Mit der **Ressourcen**-Liste in der **Aufgaben**-Registerkarte für eine bestimmte Aufgabe können Sie eine Aufgabenzuweisung für eine benannte Ressource oder eine generische Ressource erstellen. Wenn Sie eine benannte Ressource aus dem **Zugewiesene Ressourcen**-Drop-down-Menü für die Aufgabe auswählen und diese Ressource ist ein Vertragsarbeiter, wird die benannte Ressource der Aufgabe zugewiesen und ein entsprechender Datensatz für Projektteammitglieder wird erstellt, wobei der Arbeitertyp auf **Vertragsarbeiter** und **Gültigkeit** auf **Ungültig** eingestellt ist. Als nächsten Schritt müssen Sie den Datensatz des Projektteammitglieds öffnen und eine Fremdarbeit und eine Fremdarbeitsposition auswählen. Dadurch wird die Aufgabenzuordnung aktualisiert, sodass sie einen Verweis auf die Fremdarbeit und die Fremdarbeitsposition hat, und auch der Status des Teammitglieds wird auf **Gültig** aktualisiert.

Wenn Sie sich dafür entscheiden, ein allgemeines Teammitglied aus dem **Zugewiesene Ressourcen**-Dropdown der Aufgabe zu erstellen, können Sie im **Generische Teammitgliedererstellung**-Dialog eine Fremdarbeit und eine Fremdarbeitsposition auswählen. Wenn die generische Ressource der Aufgabe zugewiesen und der entsprechende Projektteammitgliedsdatensatz erstellt wird, werden Sie feststellen, dass der Projektteammitgliederdatensatz mit dem Arbeitskrafttyp auf **Vertragsarbeiter** und **Gültigkeit** auf **Gültig** erstellt wird.

### <a name="creating-project-team-members-using-the-team-tab"></a>Erstellen von Projektteammitgliedern über die Registerkarte „Team“
Über die Registerkarte „Team“ im Projekt können Sie ein allgemeines oder ein benanntes Teammitglied erstellen. Beim Anlegen des Teammitglieds können Sie die Fremdarbeit und die Fremdarbeitsposition auswählen. Nachdem das Teammitglied erstellt wurde, müssen Sie das Teammitglied mithilfe des **Zugewiesene Ressourcen**-Dropdown der Aufgabe einer Aufgabe zuweisen. 

## <a name="updating-estimates"></a>Schätzungen aktualisieren
Nachdem Sie Projektteammitgliedern Aufgaben zugewiesen haben, müssen Sie zum Tab **Schätzungen** des Projekts navigieren und **Preise aktualisieren** wählen, um sicherzustellen, dass die Kostensätze der Fremdarbeitsressourcenzuweisungen basierend auf der Preisliste „Kauf“ aktualisiert werden, die der Fremdarbeit beigefügt ist. Schätzungen werden nicht für nicht zugewiesene Aufgaben in Microsoft Dynamics 365 Project Operations generiert. Daher müssen Sie Aufgabenzuordnungen erstellen, um verschiedene Aufgaben in Ihrem Projekt zu bepreisen und zu kalkulieren. 

> [HINWEIS!] Projektteammitglieder, bei denen bei **Arbeitertyp** die Option **Vertragsarbeiter**, aber keine Fremdarbeitsreferenz ausgewählt ist, sind als **Ungültig** auf dem **Projektteammitglieder**-Raster gekennzeichnet. Wenn Projektteammitglieder mit diesem Status vorhanden sind, öffnen Sie den Projektteammitgliedsdatensatz und aktualisieren Sie die Felder für die Fremdarbeit und Fremdarbeitspositionen manuell, damit die Finanzkostenschätzung die Fremdarbeitkosten auf dem **Schätzungen**-Tab genau widerspiegelt. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
