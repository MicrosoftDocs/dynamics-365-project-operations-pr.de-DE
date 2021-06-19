---
title: Automatische Rechnungserstellung konfigurieren
description: Dieses Thema enthält Informationen zum Konfigurieren des Systems, damit Rechnungen automatisch generiert werden.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dffa95c163f7f8d5074e02cd56d6f1ed429a7c72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005340"
---
# <a name="configure-automatic-invoice-creation"></a>Automatische Rechnungserstellung konfigurieren

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_


Führen Sie die folgenden Schritte aus, um einen automatisierten Rechnungslauf in Dynamics 365 Project Operations zu konfigurieren.

1. Navigieren Sie zu **Einstellungen** > **Batchaufträge**.
2. Erstellen Sie einen Batchauftrag und nennen Sie ihn **Projektvorgang zum Erstellen von Rechnungen**. Der Name des Batchauftrags muss die Wörter „Rechnungen erstellen“ enthalten.
3. Wählen Sie im Feld **Auftragstyp** **Keiner** aus. Standardmäßig sind die Optionen **Frequenz täglich** und **Ist aktiv** auf **Ja** festgelegt.
4. Wählen Sie **Workflow ausführen** aus. Im Dialogfeld **Datensatz suchen** werden drei Workflows angezeigt:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Wählen Sie **ProcessRunCaller** und dann **Hinzufügen** aus.
6. Wählen Sie im nächsten Dialogfeld die Option **OK** aus. Auf den Workflow **Ruhezustand** folgt der Workflow **Verarbeiten**.

  > [!NOTE]
  > Sie können auch **ProcessRunner** in Schritt 5 auswählen. Wenn Sie dann **OK** auswählen, folgt auf einen **Process**-Workflow ein **Sleep**-Workflow.

Die Workflows **ProcessRunCaller** und **ProcessRunner** erstellen Rechnungen. **ProcessRunCaller** ruft **ProcessRunner** auf. **ProcessRunner** ist der Workflow, der die Rechnungen tatsächlich erstellt. Es durchläuft alle Vertragszeilen, für die Rechnungen erstellt werden sollen, und erstellt Rechnungen für diese Zeilen. Um die Vertragszeilen zu bestimmen, für die Rechnungen erstellt werden müssen, überprüft der Auftrag die Rechnungslaufdaten für die Vertragszeilen. Wenn Vertragszeilen, die zu einem Vertrag gehören, dasselbe Rechnungslaufdatum haben, werden die Transaktionen zu einer Rechnung mit zwei Rechnungszeilen zusammengefasst. Wenn keine Transaktionen zum Erstellen von Rechnungen vorhanden sind, überspringt der Auftrag die Rechnungserstellung.

Nach dem **ProcessRunner** durchgeführt wurde, wird **ProcessRunCaller** aufgerufen, liefert die Endzeit und ist geschlossen. **ProcessRunCaller** startet dann einen Timer, der ab der angegebenen Endzeit 24 Stunden lang läuft. Am Ende des Timers ist **ProcessRunCaller** geschlossen.

Der Batchverarbeitungsauftrag zum Erstellen von Rechnungen ist ein wiederkehrender Auftrag. Wenn dieser Batchauftrag mehrmals ausgeführt wird, werden mehrere Instanzen des Auftrags erstellt und verursachen Fehler. Deshalb sollten Sie die Stapelverarbeitung nur einmal starten und nur dann neu starten, wenn sie nicht mehr ausgeführt wird.

> [!NOTE]
> Die Stapelabrechnung wird nur für Projektvertragszeilen ausgeführt, die durch Rechnungspläne konfiguriert sind. Für eine Vertragszeile mit einer Festpreis-Abrechnungsmethode müssen Meilensteine konfiguriert sein. Für eine Projektvertragsposition mit einer Zeit- und Materialabrechnungsmethode muss ein datumsbasierter Rechnungszeitplan erstellt werden. Gleiches gilt für eine projektbasierte Vertragszeile.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]