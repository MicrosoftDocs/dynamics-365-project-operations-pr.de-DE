---
title: Umsatzschätzungen verwalten
description: Dieses Thema enthält Informationen zum Arbeiten mit Umsatzschätzungen für Projekte.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8d118826f8c63b9540435e320924d4562ab191ba126088560f5def1c1ff0b908
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996525"
---
# <a name="manage-revenue-estimates"></a>Umsatzschätzungen verwalten

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Sie können Umsatzschätzungen erstellen, berechnen, buchen, stornieren oder entfernen. Sie können dies entweder manuell oder in regelmäßigen Abständen tun. Dieses Thema enthält Informationen zum Arbeiten mit Umsatzschätzungen für Projekte.

### <a name="manage-revenue-estimates-manually"></a>Umsatzschätzungen manuell verwalten

Wählen Sie im Festpreis-Umsatzschätzungsprojekt oder auf der Seite **Schätzungsanfrage** (**Projektmanagement und Buchhaltung** > **Berichte und Anfragen** > **Schätzungsanfragen und -berichte**) **Schätzungen** aus.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Verwalten Sie Umsatzschätzungen mithilfe eines regelmäßigen Prozesses

Gehen Sie zu **Projektmanagement und Buchhaltung** > **Periodisch** > **Schätzungen** und wählen Sie den entsprechenden Prozess aus.

## <a name="create-a-revenue-estimate"></a>Erstellen Sie eine Umsatzschätzung

Führen Sie die folgenden Schritte aus, um eine Umsatzschätzung zu erstellen. 

1. Gehen Sie zu **Projektmanagement und Buchhaltung** > **Periodisch** > **Schätzungen**.
2. Wählen Sie **Neu**. Wählen Sie auf der Seite **Schätzungserstellung** die folgenden Parameter aus:

   - **Periodencode**: Dieser Code bestimmt, wie häufig Schätzungen veröffentlicht werden.
   - **Voraussichtliches Datum**: Das Datum, an dem die Schätzung verarbeitet wird.
   - **Kontinuierlich**: Aktivieren Sie dieses Kontrollkästchen, um Schätzungen nur dann zu erstellen, wenn Schätzungen in der vorherigen Periode gebucht wurden oder wenn die Schätzung die erste Schätzung ist, die erstellt wurde. Wenn diese Option nicht ausgewählt ist, werden Schätzungen erstellt, auch wenn in der vorherigen Periode keine Schätzungen gebucht wurden.
   - **Kosten für die Fertigstellung der Methode**: Definieren Sie, wie die verbleibende Projektarbeit geschätzt werden soll. Weitere Informationen finden Sie unter [Methoden für die Kosten zur Fertigstellung](cost-complete-methods.md).
   - **Abschlussmethode**: Wählen Sie eine Abschlussmethode aus den folgenden Optionen:
     - **Automatisch**: Der Fertigstellungsgrad wird automatisch berechnet und basiert auf den in die Berechnung einbezogenen Kostenpositionen. Die Kostenvorlage definiert die Kostenpositionen, die enthalten sind.
     - **Manuell**: Der Abschlussprozentsatz entspricht dem Abschlussprozentsatz der letzten Schätzung. Nachdem die Schätzung erstellt wurde, können Sie die **Manuelle Berechnung** auf der **Schätzungen**-Seite ändern.
     - **Aus der Kostenvorlage**: Eine Kombination der automatischen und manuellen Methoden. Diese Option wird abhängig vom Standardwert in der Kostenvorlage automatisch oder manuell festgelegt.
   - **Prognosemodell**: Wählen Sie ein Prognosemodell für die Schätzung aus.
   - **Schätzungsliste drucken**: Erstellen Sie eine Schätzungsliste und zeigen Sie sie an. Die Liste enthält den Status der aktuellen Funktion. Sie können alle Warnungen bezüglich der Schätzung in den Bericht drucken. Die folgenden Bedingungen führen dazu, dass Warnungen in der Schätzliste angezeigt werden:
     - Ein Fertigstellungsgrad von mehr als 100 Prozent.
     - Ein Fertigstellungsgrad von weniger als null Prozent.
     - Ein negativer Betrag in der **Fertigstellen**-Zeile.
     - Eine Schätzung ohne entsprechenden Vertragsbetrag.
     - Eine Schätzung ohne beigefügte Kostenschätzung.
   - **Infolog anzeigen**: Wählen Sie diese Option aus, um eine Nachricht zu erhalten, die Informationen zu den Schätzprojekten enthält, die bei der Ausführung des Jobs verarbeitet wurden.


## <a name="post-wip-or-accruals"></a>WIP oder Abgrenzungen buchen

Nachdem die Schätzungen ausgewertet wurden, werden sie beibehalten, verringert oder erhöht. Sie können dann den WIP veröffentlichen, wenn Sie mit dem **Vertrag abgeschlossen**-Bewertungsprinzip arbeiten, oder Sie buchen die Abgrenzungen, wenn Sie mit dem **Prozentsatz abgeschlossen**-Bewertungsprinzip arbeiten.
  
Der Status des Schätzzeitraums ändert sich von **Erstellt** in **Gebucht**.

## <a name="reverse-wip-or-accruals"></a>WIP oder Abgrenzungen stornieren

Verwenden Sie die Stornierungsoption, um bereits gebuchte WIP oder Abgrenzungen gutzuschreiben und dann Schätzungen für den Zeitraum zu erstellen.

> [!NOTE]
> Um einen Zeitraum zwischen anderen Zeiträumen umzukehren, kehren Sie die erforderlichen Schätzzeiträume um und veröffentlichen Sie sie erneut. Da alle nachfolgenden Perioden von den Schätzungen der vorherigen Periode abhängen, überspringen Sie keine Perioden.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Löschen Sie das geschätzte Projekt und beenden Sie das Projekt

Der letzte Schritt im Schätzprozess besteht darin, das Schätzprojekt zu eliminieren und das Festpreisprojekt zu beenden, wenn der Fertigstellungsgrad 100 Prozent erreicht.

Folgendes tritt auf, wenn Sie die Eliminierung ausführen:

- Bei einem Festpreisprojekt mit abgeschlossenem Vertrag werden die WIP-Werte von den Saldokonten gelöscht und auf die Gewinn- und Verlustrechnung gebucht.
- Bei einem Festpreisprojekt mit einem abgeschlossenen Prozentsatz werden die Rückstellungen aus der Gewinn- und Verlustrechnung entfernt.

Die Schätzung ändert den Status in **Eliminiert**.

> [!NOTE]
> In besonderen Fällen kann der Prozentsatz über 100 Prozent hinausgehen. Reduzieren Sie in diesem Fall den Fertigstellungsgrad mithilfe von **Kosten für die Fertigstellung auf Null-Methode festlegen** 100 Prozent erreichen.

## <a name="reverse-elimination"></a>Eliminierung stornieren

1. Wechseln Sie zu **Projektmanagement und Buchhaltung** > **Periodisch** > **Schätzungen** > **Eliminierung stornieren**. 
2. Wählen Sie im Aktionsbereich auf der Registerkarte **Prozess** in der Gruppe **Verwalten** die Option **Schätzen** aus. 
3. Wählen Sie **Eliminierung stornieren**.

Auf dieser Seite können Sie alle Eliminierungen mit einem bestimmten Schätzdatum und dem Schätzstatus von **Eliminiert** rückgängig machen. Der Transaktionsstatus ändert sich, nachdem Sie die entsprechenden Felder ausgewählt haben.

Dadurch wird auch der Projektstatus automatisch in **In Bearbeitung** geändert, wenn die Projektphase auf beendet eingestellt ist. Der Schätzstatus des Projektzeitraums ändert sich wieder in **Gebucht**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]