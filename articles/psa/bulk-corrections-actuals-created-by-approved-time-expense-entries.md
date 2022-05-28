---
title: Massenkorrekturen von Istwerten, die durch genehmigte Zeit- und Kosteneinträge erstellt wurden
description: In diesem Thema wird erläutert, wie ein Administrator Einzel- oder Massenkorrekturen an zuvor genehmigten Zeit- oder Kosteneinträgen vornehmen kann, wenn die Abrechnung nicht abgeschlossen ist.
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 107ba01f2fd5717e1717824631aeee099d8a8205
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683361"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Massenkorrekturen von Istwerten, die durch genehmigte Zeit- und Kosteneinträge erstellt wurden

[!include [banner](../includes/psa-now-project-operations.md)]

Gelegentlich kommt es vor, dass ein Zeit- oder Kosteneintrag falsch eingegeben wird. Beispielsweise kann ein Berater beim Erstellen eines Zeiteintrags das falsche Datum auswählen oder die Zahlen bei der Eingabe einer Ausgabe umsetzen. Wenn ein Berater die übermittelten Einträge nicht aktualisieren kann, kann ein Administrator den Eintrag für ein Projekt direkt korrigieren.

Sie benötigen Administratorberechtigungen, um die Verfahren in diesem Artikel nachvollziehen zu können.

## <a name="correct-approved-time-entries"></a>Genehmigte Zeiteinträge korrigieren     

Führen Sie die folgenden Schritte aus, um einzelne oder mehrere Zeiteinträge für ein Projekt zu korrigieren.

1. In dem Bereich **Vertrieb** wählen Sie **Buchungen** und dann **Genehmigte Zeit** aus. 

2. Suchen Sie in der Liste **Genehmigte Zeit** einen oder mehrere genehmigte Zeiteinträge, um sie zu korrigieren. Mit dem Filter können Sie verwandte Einträge suchen. Sie können beispielsweise nach einer Projekt-ID filtern und alle genehmigten Zeiteinträge mit dieser Projekt-ID auswählen.

3. Wählen Sie **Richtige Einträge** aus. Ein neues Korrekturjournal mit dem zugewiesenen Typ **Zeitkorrektur** wird automatisch erstellt. Die von Ihnen ausgewählten Einträge werden dem Journal hinzugefügt. 

4. Geben Sie auf der Seite **Neues Journal** eine **Beschreibung** für Ihr Korrekturjournal ein, und wählen Sie dann die Registerkarte **Zeiteintragskorrekturen** aus.  
5. Aktualisieren Sie im Abschnitt **Neue Werte für Zeiteinträge** mit den richtigen Informationen nach Bedarf. Sie können beispielsweise das zugewiesene Projekt oder die buchbare Ressource ändern.

6. Wählen Sie **Vorschau** aus. Wählen Sie im Dialogfeld **OK** aus. Auf der Registerkarte **Erfassungspositionen** können Sie eine Liste der ursprünglichen Istwerte anzeigen, die sich auf die ausgewählten Zeiteinträge beziehen, die rückgängig gemacht wurden, und die korrigierten entsprechenden Zeilen, die erstellt wurden. Wenn zusätzliche Korrekturen erforderlich sind, wiederholen Sie die Schritte 5 und 6. 

> [!NOTE]
> Alle korrigierten Istwerte haben dieselben Werte, die Sie im Abschnitt **Neue Werte für Zeiteinträge** ausgewählt haben.

7. Wenn die Korrekturen wie erwartet angezeigt werden, wählen Sie **Bestätigen** aus. Wählen Sie im Dialogfeld **OK** aus.

8. Kehren Sie zurück zum Bereich **Vertrieb**, wählen Sie **Projekte** aus, und öffnen Sie dann das Projekt, für das Sie gerade die Zeiteinträge aktualisiert haben. 

9. Zeigen Sie auf der Seite **Projekte**, auf der Registerkarte **Istwerte** die vorgenommenen Änderungen an. 

> [!NOTE]
> Wenn die Registerkarte **Istwerte** nicht sichtbar ist, wählen Sie **Verknüpft** > **Istwerte** aus.  

10. In der Liste **Zugeordnete Ansicht: Ist-Werte** können Sie sehen, dass die ursprünglichen Zeiteinträge, die rückgängig gemacht wurden, weiterhin aufgelistet sind, ebenso wie die entsprechenden korrigierten Zeiteinträge. 


## <a name="correct-approved-expense-entries"></a>Genehmigte Ausgabeneinträge korrigieren

Führen Sie die folgenden Schritte aus, um einen oder mehrere Ausgabeneinträge zu korrigieren. 

1. Wählen Sie unter **Vertrieb** im linken Navigationsbereich unter **Buchungen** die Option **Genehmigte Ausgaben** aus.

2. Wählen Sie in der Liste **Genehmigte Ausgaben** das Projekt aus, das Sie korrigieren möchten, und klicken Sie dann auf **Richtige Einträge**. Ein neues Korrekturjournal mit dem zugewiesenen Typ **Ausgabenkorrektur** wird automatisch erstellt. 

3. Geben Sie auf der Seite **Neues Journal** eine **Beschreibung** für die Korrektur ein. Wählen Sie dann auf der Registerkarte **Ausgabenkorrektur** im Abschnitt **Neue Werte für Ausgaben** die Datenfelder aus, die Sie für die ausgewählten Ausgabenpositionen korrigieren möchten. Beispielsweise können Sie die Ausgaben einem anderen **Projekt** zuordnen oder die Felder **Ausgabenkategorie**, **Ausgabendatum** oder **Buchbare Ressource** korrigieren.

4. Wählen Sie **Vorschau** aus. Wählen Sie im Dialogfeld **OK** aus. 

5. Überprüfen Sie die Korrekturen uf der Registerkarte **Erfassungspositionen**. Sie können eine Liste der ursprünglichen Istwerte anzeigen, die sich auf die ausgewählten Ausgabeneinträge beziehen, die rückgängig gemacht wurden, und die korrigierten entsprechenden Zeilen, die erstellt wurden.

6. Wenn die Korrekturen wie erwartet angezeigt werden, wählen Sie **Bestätigen** aus. Wählen Sie im Dialogfeld **OK** aus. Wenn die Werte nicht wie erwartet angezeigt werden, wählen Sie **Stornieren** aus, um zur Liste **Genehmigte Ausgaben** zurückzukehren. Wiederholen Sie die Schritte 2 bis 5. 

> [!NOTE]
> Die korrigierten Istwerte haben dieselben Werte, die Sie im Abschnitt **Neue Werte für Ausgaben** ausgewählt haben.

7. Navigieren Sie nach Bestätigung des Korrekturjournals zurück zu dem oder den aktualisierten Projekten, um Ihre Änderungen anzuzeigen.  

8. Auf der Projektseite, auf der Registerkarte **Istwerte** überprüfen Sie die **Zugeordnete Ansicht: Istwerte**. Die ursprünglichen Einträge und die korrigierten Einträge werden aufgelistet. Die folgende Grafik zeigt die ursprünglichen Ausgabeneinträge und die entsprechenden korrigierten Ausgabeneinträge. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
