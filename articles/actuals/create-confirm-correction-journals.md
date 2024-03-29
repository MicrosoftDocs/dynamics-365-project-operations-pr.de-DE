---
title: Korrekturerfassungen erstellen und bestätigen
description: Dieser Artikel informiert Sie darüber, wie Sie ein Korrekturjournal erstellen und bestätigen.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928063"
---
# <a name="create-and-confirm-correction-journals"></a>Korrekturerfassungen erstellen und bestätigen

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Gelegentlich kann es vorkommen, dass ein Zeit- oder Kosteneintrag falsch eingegeben wird. Beispielsweise kann ein Berater das falsche Datum auswählen, wenn er einen Zeiteintrag erstellt, oder er kann das falsche Projekt auswählen, wenn er eine Ausgabe eingibt. Wenn ein Berater die eingereichten Einträge nicht aktualisieren kann, kann ein Back-End-Administrator die Ist-Werte für ein Projekt direkt korrigieren.

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

7. Nachdem Sie das Korrekturjournal bestätigt haben, kehren Sie zu dem Projekt oder den Projekten zurück, die Sie aktualisiert haben, um Ihre Änderungen anzuzeigen.

8. Auf der Projektseite überprüfen Sie auf der **Ist-Werte**-Registerkarte die Liste **Zugeordnete Ansicht: Tatsächliche Transaktionen**. Die ursprünglichen Einträge und die korrigierten Einträge werden aufgelistet.


## <a name="correct-approved-material-usage-logs"></a>Korrigieren genehmigter Materialverwendungsprotokolle

Führen Sie die folgenden Schritte aus, um einen oder mehrere Materialverbrauchsprotokolleinträge zu korrigieren.

1. Wählen Sie im **Umsätze**-Bereich im linken Navigationsbereich unter **Transaktionen** **Ist-Werte** aus.

2. Verwenden Sie in der Liste **Ist-Werte** Spaltenfilter, um die **Material**-Transaktionsklasse auszuwählen, sodass nur die Ist-Werte für Materialien angezeigt werden. Verwenden Sie andere Spaltenfilter, um die angezeigten Ist-Werte weiter einzuschränken. Nachdem Sie den gewünschten Satz von Ist-Werten gefunden haben, wählen Sie die Ist-Werte aus, und wählen dann **Richtige Einträge** aus. Es wird automatisch eine neue Korrekturerfassung erstellt und der **Materialkorrektur**-Typ wird zugeordnet.

3. Geben Sie auf der **Neue Erfassung**-Seite im Feld **Beschreibung** eine Beschreibung für die Korrektur ein. Wähalen Sie dann auf der **Materialkorrektur**-Registerkarte im Abschnitt **Neue Werte für Materialien** die Datenfelder aus, die für die ausgewählten Materialpositionen korrigiert werden sollen. Beispielsweise können Sie das Material einem anderen Projekt zuordnen oder das Produkt, den Materialtermin oder die Lohnbearbeitung korrigieren.

4. Wählen Sie das Feld **Vorschau** aus. Wählen Sie dann im Dialogfeld die Option **OK** aus.

5. Überprüfen Sie auf der **Erfassungsposition**-Registerkarte die Korrekturen. Sie können eine Liste der ursprünglichen Ist-Werte anzeigen, die sich auf die ausgewählten Materialposten beziehen, die storniert wurden, und die entsprechenden korrigierten Zeilen, die erstellt wurden.

6. Wenn die Korrekturen wie erwartet angezeigt werden, wählen Sie **Bestätigen** aus. Wählen Sie dann im Dialogfeld die Option **OK** aus. Wenn die Werte nicht wie erwartet sind, wählen Sie **Stornieren**, um zur Liste **Ist-Werte** zurückzukehren. Wiederholen Sie dann die Schritte 2 bis 5.

7. Nachdem Sie das Korrekturjournal bestätigt haben, kehren Sie zu dem Projekt oder den Projekten zurück, die Sie aktualisiert haben, um Ihre Änderungen anzuzeigen.

8. Auf der Projektseite überprüfen Sie auf der **Ist-Werte**-Registerkarte die Liste **Zugeordnete Ansicht: Tatsächliche Transaktionen**. Die ursprünglichen Einträge und die korrigierten Einträge werden aufgelistet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
