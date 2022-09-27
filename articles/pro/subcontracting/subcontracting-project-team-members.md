---
title: Fremdarbeitsprojektteammitglieder
description: Dieser Artikel erklärt, wie Sie in Microsoft Dynamics 365 Project Operations Unteraufträge and Projektteammitglieder vergeben können.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522794"
---
# <a name="subcontracting-project-team-members"></a>Fremdarbeitsprojektteammitglieder

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Bei Microsoft Dynamics 365 Project Operations können Sie unbesetzte oder besetzte Projektteammitglieder mit Fremdarbeit besetzen.

- Nicht besetzten Projektteammitgliedern ist eine generische Ressource zugewiesen.
- Besetzten Teammitgliedern ist eine benannte Ressource zugewiesen.

Wenn Sie ein Projektteammitglied mit einer Fremdarbeitsposition verknüpfen, werden alle Zuweisungen zu Aufgaben, die das Teammitglied hat, basierend auf der Preisliste „Kauf“, die der Fremdarbeit beigefügt ist, neu berechnet.  Wählen Sie auf der Registerkarte **Schätzungen** auf der Seite **Projektdetails** die Schaltfläche **Preise aktualisieren**, um aktualisierte Preise und/oder Kosten anzuzeigen, die sich aus der Entscheidung zur Fremdarbeit ergeben. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Fremdarbeit für ein nicht besetztes Projektteammitglied
Die Seite **Teammitglieddetails** enthält Felder für Fremdarbeit und Fremdarbeitspositionen, die es einem Projektmanager ermöglichen, anzugeben, wie er die erforderliche Kapazität von einer Fremdarbeit beziehen möchte. Gehen Sie folgendermaßen vor, um ein Projektteammitglied als allgemeine Ressource an eine Fremdarbeit zu vergeben:

1.  Wählen Sie einen Unterauftrag auf der Seite **Teammitglieddetails**.

2.  Sie können nur Fremdarbeiten mit dem Status **Entwurf** oder **Bestätigt** auswählen. Fremdarbeiten mit dem Status **Geschlossen** oder **Storniert** können nicht ausgewählt werden. 

3.  Das Feld **Fremdarbeitsposition** wird sichtbar, nachdem Sie eine Fremdarbeit ausgewählt haben.

4.  Im Feld **Fremdarbeitsposition** können Sie nur Fremdarbeitspositionen auswählen, die für Zeit bestimmt sind. Sie können keine Fremdarbeitspositionen für Aufwand oder Material auswählen.

5.  Die Rolle für den Projektteammitgliedsdatensatz muss mit der Rolle in der Fremdarbeitsposition übereinstimmen. Dadurch wird sichergestellt, dass die Zeit für die Rolle, die für das Projekt veranschlagt wird, dieselbe Rolle ist, die in der Fremdarbeitsposition gekauft wird. 

Wenn ein allgemeines Teammitglied einer Fremdarbeit und einer Fremdarbeitsposition zugeordnet ist, wird das Feld **Arbeitertyp** in der generischen Teammitgliedszeile auf **Vertragsarbeiter** aktualisiert und **Gültigkeit der Fremdarbeit** wird auf **Gültig** gesetzt.

## <a name="subcontracting-a-staffed-project-team-member"></a>Fremdarbeit für ein besetztes Projektteammitglied
Wie allgemeine oder unbesetzte Teammitglieder kann auch die für ein Projekt erforderliche personelle Kapazität der Teammitglieder mit einer Fremdarbeit verknüpft werden. Gehen Sie folgendermaßen vor, um ein benanntes Projektteammitglied an eine Fremdarbeit zu vergeben:

1.  Stellen Sie sicher, dass die benannte Ressource als buchbare Ressource vom Typ Vertragsarbeiter eingerichtet ist. Stellen Sie außerdem sicher, dass das Feld **Zulieferer** auf der buchbaren Ressource mit dem Zulieferer auf der von Ihnen ausgewählten Fremdarbeit übereinstimmt. 

2.  Sie können nur Fremdarbeiten mit dem Status **Entwurf** oder **Bestätigt** auswählen. Fremdarbeiten mit dem Status **Geschlossen** oder **Storniert** können nicht ausgewählt werden. 

3.  Das Feld **Fremdarbeitsposition** wird sichtbar, nachdem Sie eine Fremdarbeit ausgewählt haben.

4.  Im Feld **Fremdarbeitsposition** können Sie nur Fremdarbeitspositionen auswählen, die für Zeit bestimmt sind. Sie können keine Fremdarbeitspositionen für Aufwand oder Material auswählen.

5.  Die Rolle für den Projektteammitgliedsdatensatz muss mit der Rolle in der Fremdarbeitsposition übereinstimmen. Dadurch wird sichergestellt, dass die Zeit für die Rolle, die für das Projekt veranschlagt wird, dieselbe Rolle ist, die in der Fremdarbeitsposition gekauft wird. 

Benannte Projektteammitglieder, die als Vertragsarbeiter vom Typ **Buchbare Ressource** eingerichtet sind, werden mit einem Fremdarbeitsgültigkeitsstatus von **Ungültig** angezeigt, wenn sie nicht mit einer Fremdarbeit verbunden sind. Wenn ein benanntes Projektteammitglied einer Fremdarbeit und einer Fremdarbeitsposition zugeordnet ist, wird das Feld **Arbeitertyp** in der Teammitgliedszeile auf **Vertragsarbeiter** aktualisiert und **Gültigkeit der Fremdarbeit** wird auf **Gültig** gesetzt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
