---
title: Schätzen Sie den Umsatz und die Kosten eines Projekts, wenn eine buchbare Ressource mehrere Rollen in einem Projekt ausfüllt
description: In diesem Thema wird erläutert, wie Preisdimensionen verwendet werden, um Preis- und Kostenschätzungen für eine Ressource zu unterstützen, die mehrere Rollen in einem Projekt ausfüllt.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2cc632d43bfcbdd23c1d06ff5203385bccf9926d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589149"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Schätzen Sie den Umsatz und die Kosten eines Projekts, wenn eine buchbare Ressource mehrere Rollen in einem Projekt ausfüllt 

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung, Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigung_ 

Projektbasierte Unternehmen benötigen häufig eine Ressource, um mehrere Rollen in einem Projekt zu besetzen. Jede Rolle kann unterschiedlich bewertet und kostenpflichtig sein. Dies bedeutet, dass die Zeit derselben Ressource für ein Projekt abhängig von der Rechnung und den Kostensätzen für jede Rolle eine andere finanzielle Schätzung erhalten kann. Sie können die Werte im Teammitgliedsdatensatz für die benannte Ressource mit unterschiedlichen Überschreibungen für jede der Aufgaben einrichten, denen das Teammitglied zugewiesen ist.

Das folgende Beispiel führt Sie durch die einfache Überschreibung eines Werts, die es einer Ressource ermöglicht, mehrere Rollen in einem Projekt mit unterschiedlichen Kosten und Abrechnungssätzen zu haben.

## <a name="create-tasks"></a>Aufgaben erstellen
Um Aufgaben zu erstellen, müssen Sie Aufgaben sowie zusammenfassende Aufgaben hinzufügen. Anschließend müssen Sie die Aufgabe zuweisen, bevor Sie die Aufgabendauer hinzufügen. 

### <a name="add-tasks-and-summary-tasks"></a>Fügen Sie Aufgaben und Zusammenfassungsaufgaben hinzu
Führen Sie zum Hinzufügen einer Aufgabe folgende Schritte aus.

1. Gehen Sie zu **Projekte** und öffnen Sie das Projekt, zu dem Sie Aufgaben hinzufügen möchten.
2. Wählen Sie **Neue Aufgabe hinzufügen** aus. Benennen Sie die Aufgabe und drücken Sie die **EINGABETASTE**.
3. Geben Sie einen anderen Namen für die Aufgabe ein und drücken Sie die **EINGABETASTE**. Wiederholen Sie diesen Vorgang, bis Sie eine vollständige Liste der Aufgaben haben.
3. Um Aufgaben unter **Zusammenfassungsaufgaben** einzurücken, wählen Sie die drei vertikalen Punkte neben dem Aufgabennamen aus und dann **Unteraufgabe**. 

  > [!TIP]
  > Um mehr als eine Aufgabe auszuwählen, wählen Sie eine Aufgabe aus, halten **STRG** gedrückt und wählen dann eine andere Aufgabe aus.
  >
  > Sie können auch **Unteraufgabe höherstufen** wählen, um Aufgaben von **Zusammenfassungsaufgaben** zu verschieben.

### <a name="assign-tasks"></a>Aufgaben zuweisen

Führen Sie zum Zuweisen von Aufgaben folgende Schritte aus.

1. Wählen Sie in der Spalte **Zugewiesen an** für eine Aufgabe das Personensymbol aus.
2. Wählen Sie ein Teammitglied aus der Liste aus oder geben Sie Text ein, um nach einem Namen zu suchen.

### <a name="add-task-duration-and-columns"></a>Aufgabendauer und Spalten hinzufügen

Es ist oftmals am einfachsten, bei der Erstellung des Projekts mit der Dauer zu beginnen. Führen Sie zum Hinzufügen einer Aufgabendauer folgende Schritte aus.

1. Geben Sie in der Spalte **Dauer** für eine Aufgabe die Anzahl der Tage ein, die Ihrer Meinung nach zur Ausführung der Aufgabe benötigt werden. Wenn Sie eine andere Zeiteinheit verwenden möchten, geben Sie eine Zahl zuzüglich der Begriffe **Stunden**, **Wochen** oder **Monate** ein.
2. Wenn Sie möchten, dass Ihre Aufgabe als rautenförmiger Meilenstein in der **Zeitleiste**-Ansicht angezeigt wird, geben Sie in der **Dauer**-Spalte **0 Tage** ein.
3. Drücken Sie die **EINGABETASTE**, um zum **Dauer**-Feld der nächsten Aufgabe zu gehen, und fahren Sie mit der Eingabe der Dauer fort.

  > [!NOTE]
  > Sie können keine Dauer für Zusammenfassungsaufgaben eingeben.

Sie können Ihrem Projekt Spalten hinzufügen, um weitere Details bereitzustellen. Wählen Sie dazu **Spalte hinzufügen** aus. 

Weitere Informationen finden Sie unter [Erstellen eines Projekts](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Richten Sie die Rollen- und Organisationseinheit für ein generisches Projektteammitglied ein
Führen Sie die folgenden Schritte aus, um eine Rolle und eine Organisationseinheit für ein generisches Teammitglied einzurichten.

1. Auf der **Aufgaben**-Seite wählen Sie die **Aufgabe**-Zeile für **Aufgabe A** aus. 
2. Wählen Sie unter **Zugewiesen zu** **Generische Ressource hinzufügen** aus. Dies öffnet die Seite **Teammitglied Schnell erstellen**.
3. Geben Sie auf der Seite **Schnellerfassung: Teammitglied** die Attribute des generischen Teammitglieds an, das diese Aufgabe ausführen kann.
4. Wählen Sie die entsprechende Rolle und Organisationseinheit aus, und wählen Sie dann **Speichern und schließen**. Ein generisches Teammitglied wird erstellt und dieser Aufgabe zugewiesen. 
5. Wiederholen Sie die Schritte 1 bis 4 für **Aufgabe B**. **Aufgabe B** muss jedoch für das generische Teammitglied eine andere Rolle und Organisationseinheit zugewiesen sein als **Aufgabe A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Richten Sie die Rollen- und Organisationseinheit für eine Projektaufgabe ein
Führen Sie die folgenden Schritte aus, um eine Rolle und eine Organisationseinheit für eine Aufgabe einzurichten.

1. Nachdem Sie **Aufgabe A** erstellt haben, wählen Sie die Aufgabe und dann das **i**-Symbol zum Öffnen des **Aufgabendetails**-Felds aus. 
2. Im **Aufgabendetails**-Bereich scrollen Sie nach unten und wählen Sie **Details anzeigen** aus, um die **Aufgabendetails**-Seite zu öffnen.
3. Fügen Sie auf der **Aufgabendetails**-Seite in **Rolle** und **Organisationseinheit** die Werte hinzu, die zum Ausführen dieser Aufgabe für die Ressource erforderlich sind. 

  > [!NOTE]
  > Wenn Sie dieses Szenario mit den Demo-Daten von Project Operations abschließen, wählen Sie **Beratungsleiter** für die Rolle und **Fabrikam US** als Organisationseinheit.

4. Wählen Sie **Aufgaben B** und dann die Aufgabe aus.
5. Wählen Sie das **i**-Symbol zum Öffnen des **Aufgabendetails**-Felds aus. 
6. Im **Aufgabendetails**-Bereich scrollen Sie nach unten und wählen Sie **Details anzeigen** aus, um die **Aufgabendetails**-Seite zu öffnen.
7. Fügen Sie auf der **Aufgabendetails**-Seite in **Rolle** und **Organisationseinheit** die Werte hinzu, die zum Ausführen dieser Aufgabe für die Ressource erforderlich sind. Die Werte in **Rolle** und **Organisationseinheit** für **Aufgabe B** müssen anders sein als die für **Aufgabe A**. 

  > [!NOTE]
  > Wenn Sie dieses Szenario mit den Demo-Daten von Project Operations abschließen, wählen Sie **Netzwerktechniker** für die Rolle und **Fabrikam US** als Organisationseinheit.

8. Wählen Sie auf der Seite **Aufgabendetails** „Speichern und schließen“ aus. 

## <a name="team-member-and-estimates-behavior"></a>Teammitglied und Verhaltensschätzungen 
Um das Verhalten auf dem Raster **Teammitglied** zu verstehen, führen Sie die folgenden Schritte aus.

1. Im Raster **Teammitglied** wählen Sie die beiden allgemeinen Teammitglieder aus und dann **Anforderungen generieren**. Dadurch werden Ressourcenanforderungen erstellt. 
2. Wählen Sie die Teammitgliedszeile für **Beratungs-Lead** und dann **Buchen** aus. Die Zeitplanübersicht wird mit einer Liste von Ressourcen geöffnet. Wählen Sie eine Ressource aus und dann **Buchen**, um die Ressource für diese Anforderung zu buchen.
3. Wählen Sie die Teammitgliedszeile für **Netzwerktechniker** und dann **Buchen** aus. Die Zeitplanübersicht wird mit einer Liste von Ressourcen geöffnet. Wählen Sie dieselbe Ressource wie oben aus und dann **Buchen**, um die Ressource für diese Anforderung zu buchen.

### <a name="team-member-grid"></a>Teammitgliedsraster 

Im Raster **Teammitglied** werden die beiden generischen Teammitgliedsdatensätze gelöscht und durch nur eine Ressource ersetzt. Es gibt einen Satz von Werten für diese Ressource, für die es sich um einen Standardwert für **Rolle** und **Organisationseinheit** handelt.

Wenn Sie die Zeile für diesen Teammitgliedsdatensatz erweitern, werden im Teammitgliedsdatensatz für beide Aufgaben unterschiedliche Zuordnungen angezeigt. Jede Zuweisungszeile hat aufgabenspezifische Werte für **Rolle** und **Organisationseinheit**. 

### <a name="estimates-grid"></a>Vorkalkulationsraster 

Im Raster **Schätzungen** werden beide Zuordnungen für dieselbe Ressource unterschiedlich bewertet. Die Zuordnung für die Ressource zu **Aufgabe A** erfolgt über den **Rolle**-Attributwert von **Beratungs-Lead**. Die Zuordnung für die gleiche Ressource zu **Aufgabe B** erfolgt über den **Rolle**-Attributwert von **Netzwerktechniker**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]