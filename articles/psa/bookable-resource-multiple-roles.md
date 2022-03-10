---
title: Schätzen Sie den Umsatz und die Kosten eines Projekts, wenn eine buchbare Ressource mehrere Rollen für ein Projekt ausfüllt
description: In diesem Thema wird erläutert, wie Informationen zu Preisdimensionen verwendet werden können, um Preis- und Kostenschätzungen für eine Ressource zu unterstützen, die mehrere Rollen in einem Projekt ausfüllt.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: be24bb3bdf2f3c8351fc396ae67457b5213e1cd800e9d2ad23d59d0d038f22b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987480"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Schätzen Sie den Umsatz und die Kosten eines Projekts, wenn eine buchbare Ressource mehrere Rollen für ein Projekt ausfüllt 

[!include [banner](../includes/psa-now-project-operations.md)]

Projektbasierte Unternehmen benötigen häufig eine Ressource, um mehrere Rollen in einem Projekt auszuführen. Jede dieser Rollen kann unterschiedlich bewertet und kostenpflichtig sein, was bedeutet, dass die Zeit der gleichen Ressource für das Projekt abhängig von der Rechnung und den Kostensätzen für jede der Rollen eine andere finanzielle Schätzung erhalten kann. Project Service Automation ermöglicht die Einrichtung der Werte im Teammitgliedsdatensatz für die benannte Ressource und unterschiedliche Überschreibungen für jede der Aufgaben, denen das Teammitglied zugewiesen ist.

Im folgenden Beispiel wird erläutert, wie durch die einfache Überschreibung dieses Werts eine Ressource mehrere Rollen in einem Projekt mit unterschiedlichen Kosten und Abrechnungssätzen haben kann.

## <a name="create-tasks"></a>Aufgaben erstellen
Erstellen Sie zwei Projektaufgaben für jeweils 40 Stunden, Aufgabe A und Aufgabe B. Wählen Sie Aufgabe A als Vorgänger von Aufgabe B aus.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Richten Sie die Rollen- und Organisationseinheit für ein generisches Projektteammitglied ein

1. Auf der Seite **Zeitplan** wählen Sie die Zeile **Aufgabe** für Aufgabe A. 
2. Wählen Sie im Feld **Ressourcen** in der Dropdownliste **Erstellen** aus.
3. Geben Sie auf der Seite **Schnellerfassung: Teammitglied** die Attribute des generischen Teammitglieds an, das diese Aufgabe ausführen kann.
4. Wählen Sie die entsprechende Rolle und Organisationseinheit aus, und wählen Sie dann **Speichern und schließen**. Ein generisches Teammitglied wird erstellt und dieser Aufgabe zugewiesen. 

Wiederholen Sie diese Schritte für Aufgabe B und stellen Sie sicher, dass sich die Rolle und Organisationseinheit des für Aufgabe B erstellten generischen Teammitglieds von Aufgabe A unterscheidet. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Richten Sie die Rollen- und Organisationseinheit für eine Projektaufgabe ein

1. Nachdem Sie Aufgabe A erstellt haben, wählen Sie die Aufgabe aus, und wählen Sie dann **Aufgabe bearbeiten**.
2. Suchen Sie auf der Seite **Aufgabendetails** die **Rolle** und **Organisationseinheit**, und fügen Sie in den Feldern die Werte hinzu, die für eine Ressource erforderlich sind, die diese Aufgabe ausführen würde. 

  > [!NOTE]
  > Wenn Sie diese Szenarien mit Project Service Automation-Demodaten abschließen, wählen Sie **Beratungs-Lead** für die Rolle und **Fabrikam USA** als Organisationseinheit.

3. Wählen Sie Aufgabe B aus, und wählen Sie dann **Aufgabe bearbeiten** aus.
4. Suchen Sie auf der Seite **Aufgabendetails** die **Rolle** und **Organisationseinheit**, und fügen Sie in den Feldern die Werte hinzu, die für eine Ressource erforderlich sind, die diese Aufgabe ausführen würde. Stellen Sie sicher, dass die Werte in den Felder **Rolle** und **Organisationseinheit** für Aufgabe B sich von den Werten für Aufgabe A unterscheiden. 

  > [!NOTE]
  > Wenn Sie diese Szenarien mit Project Service Automation-Demodaten abschließen, wählen Sie **Netzwerktechniker** für die Rolle und **Fabrikam USA** als Organisationseinheit.

5. Wählen Sie auf der Seite **Aufgabendetails** „Speichern und schließen“ aus. 

## <a name="team-member-and-estimates-behavior"></a>Teammitglied und Verhaltensschätzungen 

1. Wählen Sie auf der Seite **Aufgabendetails** unter **Teammitglied** die beiden allgemeinen Teammitglieder aus, und wählen Sie dann **Anforderungen generieren** aus. 
2. Wählen Sie die Teammitgliedszeile für **Beratungs-Lead** und dann **Buchen** aus. Die Zeitplanübersicht wird geöffnet und eine Ressource für diese Anforderung wird gebucht.
3. Wählen Sie die Teammitgliedszeile für **Netzwerktechniker** und dann **Buchen** aus. Die Zeitplanübersicht wird geöffnet und die gleiche Ressource für diese Anforderung wird gebucht.

### <a name="team-member-grid"></a>Teammitgliedsraster 
Im Raster **Teammitglied** sehen Sie, dass die beiden generischen Teammitgliedsdatensätze gelöscht wurden und durch eine Ressource ersetzt wurden. Für diese Ressource gibt es einen Wertesatz, für den ein Standardwertsatz für **Rolle** und **Organisationseinheit** angezeigt wird.
Wenn Sie die Zeile dieses Teammitgliedsdatensatzes erweitern, werden im Teammitgliedsdatensatz für beide Aufgaben unterschiedliche Zuordnungen angezeigt. Jede Zuweisungszeile hat aufgabenspezifische Werte für **Rolle** und **Organisationseinheit**. 

### <a name="estimates-grid"></a>Vorkalkulationsraster 
Wenn Sie zum Raster **Schätzungen** navigieren, werden Sie feststellen, dass beide Zuweisungen für dieselbe Ressource unterschiedliche Preise haben.
Die Zuordnung für die Ressource zu Aufgabe A erfolgt über den **Rolle**-Attributwert von **Beratungs-Lead**. Die Zuordnung für die gleiche Ressource zu Aufgabe B erfolgt über den **Rolle**-Attributwert von **Netzwerktechniker**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]