---
title: Teammitglieder verwalten
description: Diese Thema enthält Informationen zum Buchen benannter Ressourcen für Projektteams und zum Zuweisen dieser Ressourcen zu Aufgaben.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961865"
---
# <a name="maintain-team-members"></a>Teammitglieder verwalten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Sie können Ihrem Projektteam eine benannte Ressource hinzufügen, indem Sie diese direkt für das Team buchen.

1. Wechseln Sie in Dynamics 365 Project Operations zu **Projekte**, wählen Sie das Projekt aus, für das Sie buchen möchten und öffnen Sie es.
2. Wählen Sie auf der Seite **Projekt** auf der Registerkarte **Team** **Neu** aus. 
3. Wählen Sie im Dialogfeld **Schnellerfassung: Projektteammitglied** die buchbare Ressource aus. Das Feld **Rolle** wird mit der Standardrolle der Ressource vorausgefüllt, sofern eine zugewiesen wurde. Sie können die Rolle ändern. 
4. Wählen Sie das Start- und Enddatum aus, an denen die Ressource benötigt wird, und wählen Sie die Zuweisungsmethode für die Ressourcenkapazität aus. 
5. Wählen Sie im Feld **Projektgenehmiger** **Ja** aus, wenn das Teammitglied ein Projektgenehmiger sein soll. Das Teammitglied kann übermittelte Zeit- und Ausgabeneinträge für dieses Projekt genehmigen. 
6. Wählen Sie **Speichern** aus.

Sie können die gebuchte Ressource nun Aufgaben im Projekt zuweisen. Weisen Sie auf der Seite **Projekt** auf die Registerkarte **Zeitplan** der neuen Ressource Aufgaben zu. Die Ressourcenauswahl, die über das Feld **Ressourcen** im Aufgabenraster gestartet wird, zeigt die Teammitglieder an, die Sie auswählen können.


Im Project Operations sind Ressourcenbuchungen und Aufgabenzuweisungen nicht eng miteinander verbunden. Wenn Sie also die Ressourcenauswahl im Zeitplan verwenden, können Sie Teammitgliedern Aufgaben für mehr Stunden zuweisen, als ihre Buchungen für das Projekt umfassen.

Die Unterschiede zwischen Buchungen und Zuweisungen von Teammitgliedern werden auf den Registerkarten **Team** und **Ressourcenabstimmung** gezeigt. Sie können die Unterschiede zwischen Buchungen und Zuweisungen für Ressourcen auch detaillierter abgleichen.

Verwenden Sie die Ressourcenauswahl auf der Registerkarte **Zeitplan**, um nach buchbaren Ressourcen zu suchen und sie auszuwählen, die nicht bereits Teil des Projektteams sind. Diese Ressourcen werden in der Ressourcenauswahl als **Weitere Ressourcen** angezeigt.

Wenn Sie eine Auswahl treffen, wird die Ressource dem Projektteam hinzugefügt und der Aufgabe zugewiesen, es werden jedoch keine Buchungen generiert.

Mithilfe der Funktion „Buchung erweitern” auf der Registerkarte **Abstimmung** oder der **Zeitplanübersicht** können Sie die Kapazität der Ressource für das Projekt buchen.

Nachdem ein Teammitglied für Ihr Projekt gebucht wurde, können Sie **Buchungen verwalten** oder die **Zeitplanübersicht** zum direkten Verwalten der Buchungen verwenden.
