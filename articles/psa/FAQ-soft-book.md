---
title: Eine Ressource unverbindlich buchen
description: In diesem Thema finden Sie Informationen zum unverbindlichen Planen bzw. Buchen von Projektteammitgliedern.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: cb506a519dbc490ecdd579edf1e3fa5dd0153bdb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076649"
---
# <a name="soft-book-a-resource"></a>Eine Ressource unverbindlich buchen

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Sie können eine Ressource für ein Projektteam unverbindlich planen oder buchen, um zu zeigen, dass Sie dem Projekt eine Ressource zuweisen möchten. Unverbindliche Buchungen nutzen die verfügbare Kapazität einer Ressource nicht, und Sie können unverbindlich-gebuchte Teammitglieder Projektaufgaben zuweisen. Da die unverbindliche Buchung jedoch nicht die Kapazität einer Ressource beansprucht, können Sie die Ressource im selben Zeitraum für andere Aufgaben verbindlich buchen. Generische Ressourcen können nicht unverbindlich gebucht werden, und unverbindliche Buchungen könne keine Anforderung für eine allgemeine Ressource erfüllen.

Unverbindlich gebuchte Projektteammitglieder werden auf der Registerkarte **Team** auf der Seite **Projekt** aufgelistet, wenn die unverbindlich gebuchten Stunden in der Spalte **Unverbindlich gebuchte Stunden** in der Ansicht **Benannte Teammitglieder** angezeigt werden. Unverbindlich gebuchte Teammitglieder werden auch in der Zeitplanübersicht aufgelistet. Da sie unverbindlich gebucht sind, wird in der Zeitplanübersicht kein Kapazitätsverbrauch für diese Ressourcen angezeigt. Unverbindlich gebuchte Zeit wird nicht auf der Registerkarte **Abstimmung** und auch nicht im Feld **Buchungen erweitern** auf der Registerkarte **Abstimmung** der Zeitplanübersicht angezeigt. 

Es gibt zwei Möglichkeiten, um ein Teammitglied unverbindlich für ein Projekt zu buchen: direkt über die Zeitplanübersicht oder durch Hinzufügen des Teammitglieds auf der Registerkarte **Team**. 

## <a name="soft-book-from-the-schedule-board"></a>Unverbindliches Buchen über die Zeitplanübersicht
Führen Sie die folgenden Schritte aus, um eine Ressource über die Zeitplanübersicht unverbindlich zu buchen. 

1. Öffnen Sie die Zeitplanübersicht und wählen Sie dann im Bereich **Buchungsanforderungen** die Registerkarte **Projekt** aus.
2. Suchen Sie das Projekt, für das eine Ressource unverbindlich gebucht werden soll. Wenn die Liste eine große Anzahl von Projekten enthält, wählen Sie die Spaltenüberschrift **Projekt** aus und verwenden Sie den Filter, um nach einem oder mehreren Projekten zu suchen.
3. Wählen Sie das Projekt aus und ziehen Sie es auf das Zeitraster der Ressource.
5. Passen Sie im Bereich **Ressourcenbuchung erstellen** das Start- und Enddatum an, setzen Sie den **Buchungsstatus** auf **Unverbindlich** und legen Sie anschließend die Stunden fest. 
6. Klicken Sie auf **Buchen**. Die Ressource wird auf der Registerkarte **Team** nun als Ressource für das Projekt angezeigt. In der Ansicht **Benannte Teammitglieder** sehen Sie die unverbindlich gebuchten Stunden in der Spalte **Unverbindlich gebuchte Stunden**.

> [!NOTE]
> Jetzt können Sie die unverbindlich gebuchten Aufgaben auf der Registerkarte **Zeitplan** zuweisen. Auf der Registerkarte **Abstimmung** zeigt die Ressource ein Buchungsdefizit in Bezug auf die Aufgabenzuweisung an, da auf der Registerkarte **Abstimmung** nur verbindliche Buchungen berücksichtigt werden. Sie können nun die Funktion **Buchungen erweitern** nutzen, um die Ressource verbindlich zu buchen, um Defizite von verbindlichen Buchungen mit Ressourcenzuweisungen zu vermeiden. Sie müssen die unverbindliche Buchung für die Ressource mithilfe von **Buchungen verwalten** manuell stornieren.

## <a name="soft-book-on-the-team-tab"></a>Auf der Teamregisterkarte vorsorglich buchen

Sie können Teammitgliedern direkt auf der Registerkarte **Team** hinzufügen und den Buchungsstatus anschließend mithilfe von **Buchungen verwalten** von **Verbindlich** in **Unverbindlich** ändern. Wenn Sie ein Teammitglied auf diese Art hinzufügen, wird es immer eine verbindliche Buchung sein, es sei denn, Sie wählen als Zuordnungsmethode **Keine** aus.

Führen Sie die folgenden Schritte aus, um diese Methode zu verwenden.

1. Klicken Sie auf der Seite **Projekt** auf der Registerkarte **Team** auf **Neu**.
2. Wählen Sie die buchbare Ressource, die Rolle sowie das Anfangs- und Enddatum aus.
3. Wählen Sie eine andere Zuordnungsmethode als **Keine** aus.
4. Wählen Sie **Speichern** aus. Die Ressource wird im Raster und ihre Stunden werden in der Spalte **Verbindlich gebuchte Stunden** angezeigt.
5. Sie können die Buchungen der Ressource verwalten, indem Sie **Buchungen verwalten** auswählen.
6. Erweitern Sie beim Öffnen der Zeitübersicht die Ressource, um ihre Buchungen anzuzeigen. Die Buchung wird als **Verbindlich** angezeigt.
7. Klicken Sie mit der rechten Maustaste auf die Buchung und wählen SIe unter **Status ändern** die Option **Unverbindlich buchen** \> **Unverbindlich** aus. Der Buchungsstatus lautet nun **Unverbindlich**.
8. Nachdem Sie die Zeitplanübersicht geschlossen haben, werden Sie feststellen, dass die Stunden für die Ressource von der Spalte **Verbindlich gebuchte Stunden** in die Spalte **Unverbindlich gebuchte Stunden** auf das Raster der Registerkarte **Team** verschoben wurden, wenn Sie die Ansicht **Benannte Teammitglieder** betrachten.

> [!NOTE]
> Wenn Sie **Buchungen verwalten** verwenden, um den Status von **Verbindlich** in **Unverbindlich** zu ändern, bleiben beim verbindlichen Buchen einer Ressource für ein Team und beim Zuweisen von Aufgaben zur Ressource die Aufgabenzuweisungen zur Ressource erhalten. Auf der Registerkarte **Abstimmung** weist die Ressource ein Buchungsdefizit auf, da bei der Abstimmung von Buchungen mit den Zuweisungen nur verbindliche Buchungen berücksichtigt werden. Sie können nun die Funktion **Buchungen erweitern** auf der Registerkarte **Abstimmung** verwenden, um die Ressource verbindlich zu buchen, um das Defizit an verbindlichen Buchungen für die Ressourcenzuweisungen zu beseitigen. Sie müssen die unverbindliche Buchung für die Ressource mithilfe von **Buchungen verwalten** manuell stornieren.

Wenn Sie bereit sind, eine unverbindlich gebuchte Teammitgliedsressource in ein verbindlich gebuchtes Teammitglied zu ändern, gehen Sie folgendermaßen vor:

1. Erweitern Sie auf der Zeitplanübersicht die Ressource, um ihre Buchungen anzuzeigen. Die Buchung wird als **Unverbindlich** angezeigt.
2. Klicken Sie mit der rechten Maustaste auf die Buchung und wählen Sie unter **Status ändern** **Verbindlich buchen** \> **Verbindlich** aus. Der Buchungsstatus lautet nun **Verbindlich**.
3. Nachdem Sie die Zeitplanübersicht geschlossen haben, kehren Sie zum Projekt zurück und öffnen Sie die Registerkarte **Team**. Es wird angezeigt, dass in der Ansicht **Benannte Teammitglieder** die Stunden für die Ressource auf der Registerkarte **Team** von der Spalte **Unverbindlich gebuchte Stunden** in die Spalte **Verbindlich gebuchte Stunden** verschoben wurden. Wenn die Ressource Aufgaben zugewiesen wurde, weisen diese auf der Registerkarte **Abstimmung** kein Buchungsdefizit mehr auf, da ihre Buchungen nun verbindlich sind.

