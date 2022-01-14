---
title: Fremdarbeitsoptionen für Projektteammitglieder
description: Dieses Thema erklärt die Fremdarbeitoptionen für Projektteammitglieder in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903423"
---
# <a name="subcontracting-options-for-project-team-members"></a>Fremdarbeitsoptionen für Projektteammitglieder

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Bei Microsoft Dynamics 365 Project Operations können Sie die verfügbaren Fremdarbeitsoptionen für ein oder mehrere Projektteammitglieder bewerten. Die verfügbaren Fremdarbeitsoptionen bieten die folgenden Möglichkeiten:

- Erstellen Sie für die ausgewählten Projektteammitglieder eine neue Fremdarbeit und/oder neue Positionen für eine vorhandene Fremdarbeit. 
- Wählen Sie eine Fremdarbeit und Fremdarbeitsposition für die Reservierung aus. 

Sie können aus den verfügbaren Fremdarbeitsoptionen für allgemeine Projektteammitglieder oder aus Projektteammitgliedern auswählen, die mit einer benannten Ressource besetzt wurden, bei der es sich um einen Vertragsarbeiter handelt. 

Es sind keine Fremdarbeitsoptionen für die folgenden Möglichkeiten verfügbar:

- Projektteammitglieder, die mit einem Mitarbeiter besetzt wurden. 
- Projektteammitglieder, die bereits einer Fremdarbeit oder einer Fremdarbeitsposition zugeordnet wurden. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Fremdarbeit für ein nicht besetztes Projektteammitglied

Führen Sie die folgenden Schritte aus, um die verfügbaren Fremdarbeitsoptionen für ein allgemeines oder unbesetztes Projektteammitglied zu überprüfen und auszuwählen:

1. Wählen Sie einen oder mehrere Projektteammitgliederdatensätze aus, bei denen es sich bei der Ressource um eine generische Ressource handelt.
2. Stellen Sie sicher, dass keiner der ausgewählten Projektteammitgliederdatensätze bereits an Fremdarbeit vergeben wurde. 
3. Wählen Sie **Fremdarbeitsoptionen** im Unterraster der Projektteammitglieder. Das Dialogfeld **Fremdarbeitsoptionen** wird geöffnet. 
4. Wenn Sie in Schritt 1 nur einen Projektteammitgliedsdatensatz ausgewählt haben, stehen die folgenden Optionen zur Verfügung:
    - Erstellen von neuen Fremdarbeitspositionen. 
    - Reservieren für eine bestehende Fremdarbeit. Wenn Sie in Schritt 1 mehrere Datensätze für Projektteammitglieder ausgewählt haben, besteht die einzige verfügbare Option darin, neue Fremdarbeitspositionen zu erstellen.
5. Mit der Option zum Reservieren für eine vorhandene Fremdarbeitsposition können Sie eine Fremdarbeit und eine Fremdarbeitsposition auswählen, für die Sie reservieren möchten. Wenn Sie eine Fremdarbeitsposition zur Kapazitätsreservierung auswählen, sollten Sie sicherstellen, dass die ausgewählte Fremdarbeitsposition für Zeit bestimmt ist und dass die erforderliche Rolle für das Projektteammitglied der Rolle entspricht, die für die Fremdarbeitsposition gekauft wurde.
6. Wenn Sie neue Fremdarbeitszeilen für die Projektteammitglieder erstellen möchten, ermöglicht Ihnen das System die Auswahl der Fremdarbeit, für die Sie diese Zeilen erstellen möchten. Die Fremdarbeit, die Sie zum Erstellen neuer Zeilen auswählen, sollte im Status **Entwurf** sein. Mit dieser Option zum Erstellen neuer Fremdarbeitspositionen für die ausgewählten Projektteammitglieder erstellt das System für jedes Projektteammitglied eine Fremdarbeitsposition für Zeit. Die Rolle, die Stunden und das Datum werden vom Projektteammitglied in jede erstellte Fremdarbeitsposition kopiert. 
7. Wenn ein allgemeines Teammitglied einer Fremdarbeit und einer Fremdarbeitsposition zugeordnet ist, wird das Feld **Arbeitertyp** in der generischen Teammitgliedszeile auf **Vertragsarbeiter** aktualisiert und der Wert **Gültigkeit der Fremdarbeit** wird auf **Gültig** gesetzt.

## <a name="subcontracting-a-staffed-project-team-member"></a>Fremdarbeit für ein besetztes Projektteammitglied

Wie bei generischen oder unbesetzten Teammitgliedern können Sie auch die Fremdarbeitsoptionen für ein besetztes Projektteammitglied anzeigen, solange es sich bei dem besetzten Teammitglied um einen Vertragsarbeiter handelt. Führen Sie die folgenden Schritte aus, um die verfügbaren Fremdarbeitsoptionen für ein besetztes oder benanntes Projektteammitglied zu überprüfen und auszuwählen:

1. Wählen Sie einen oder mehrere Projektteammitgliederdatensätze aus, bei denen es sich bei der Ressource um einen benannten Vertragsarbeiter handelt.
2. Stellen Sie sicher, dass keiner der ausgewählten Projektteammitgliederdatensätze bereits an Fremdarbeit vergeben wurde. 
3. Wählen Sie **Fremdarbeitsoptionen** im Unterraster der Projektteammitglieder. Das Dialogfeld **Fremdarbeitsoptionen** wird geöffnet. 
4. Wenn Sie in Schritt 1 nur einen Projektteammitgliedsdatensatz ausgewählt haben, stehen die folgenden Optionen zur Verfügung:
      - Erstellen von neuen Fremdarbeitspositionen.
      - Für eine vorhandene Fremdarbeit reservieren.
  Wenn Sie in Schritt 1 mehrere Datensätze für Projektteammitglieder ausgewählt haben, besteht die einzige verfügbare Option darin, neue Fremdarbeitspositionen zu erstellen.
5. Mit der Option zum Reservieren für eine vorhandene Fremdarbeitsposition können Sie eine Fremdarbeit und eine Fremdarbeitsposition auswählen, für die Sie reservieren möchten. Bei der Auswahl einer Fremdarbeitsposition zur Kapazitätsreservierung sollten Sie Folgendes beachten:
      - Die ausgewählte Fremdarbeitsposition ist für Zeit. 
      - Die für das Projektteammitglied erforderliche Rolle stimmt mit der Rolle überein, die in der Fremdarbeitsposition gekauft wurde. 
      - Der Kreditor, dem der Vertragsarbeiter zugeordnet ist, ist mit dem Kreditor der Fremdarbeit identisch.
6. Wenn Sie neue Fremdarbeitszeilen für die Projektteammitglieder erstellen möchten, ermöglicht Ihnen das System die Auswahl der Fremdarbeit, für die Sie diese Zeilen erstellen möchten. Mit dieser Option sollten Sie sicherstellen, dass der Kreditor, zu dem der Vertragsarbeiter gehört, mit dem Kreditor der Fremdarbeit identisch ist. 
7. Die Fremdarbeit, die Sie zum Erstellen neuer Zeilen auswählen, sollte im Status **Entwurf** sein. Mit dieser Option zum Erstellen neuer Fremdarbeitspositionen für die ausgewählten Projektteammitglieder erstellt das System für jedes Projektteammitglied eine Fremdarbeitsposition für Zeit. Die Rolle, die Stunden und das Datum werden vom Projektteammitglied in jede erstellte Fremdarbeitsposition kopiert.  
8. Wenn ein benanntes Teammitglied einer Fremdarbeit und einer Fremdarbeitsposition zugeordnet ist, wird das Feld **Arbeitertyp** in der benannten Teammitgliedszeile auf **Vertragsarbeiter** aktualisiert und der Wert **Gültigkeit der Fremdarbeit** wird auf **Gültig** gesetzt.

## <a name="re-costing-subcontractor-assignments"></a>Nachkalkulation von Fremdarbeitszuweisungen

Wenn ein Projektteammitglied (generisch oder benannt) durch Verwendung des Dialogs **Fremdarbeitsoptionen** mit Fremdarbeitspositionen verknüpft ist, werden alle Zuweisungen zu Aufgaben, die das Teammitglied hat, basierend auf der Preisliste „Kauf“, die der Fremdarbeit beigefügt ist, neu berechnet. Wählen Sie auf der Registerkarte **Schätzungen** auf der Seite **Projektdetails** die Schaltfläche **Preise aktualisieren**, um aktualisierte Preise und/oder Kosten anzuzeigen, die sich aus der Entscheidung zur Fremdarbeit ergeben.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
