---
title: Automatische Rechnungserstellung konfigurieren
description: Dieses Thema enthält Informationen zum Konfigurieren des Systems, damit Rechnungen automatisch generiert werden.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4e7572f2bc6201960ac01ce521adf39ac2577dbe
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076417"
---
# <a name="configure-automatic-invoice-creation"></a>Automatische Rechnungserstellung konfigurieren

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_


Führen Sie die folgenden Schritte aus, um einen automatisierten Rechnungslauf in Dynamics 365 Project Operations zu konfigurieren.

1. Navigieren Sie zu **Einstellungen** > **Batchaufträge**.
2. Erstellen Sie einen Batchauftrag und nennen Sie ihn **Projektvorgang zum Erstellen von Rechnungen**. Der Name des Batchauftrags muss die Wörter „Rechnungen erstellen“ enthalten.
3. Wählen Sie im Feld **Auftragstyp** **Keiner** aus. Standardmäßig sind die Optionen **Frequenz täglich** und **Ist aktiv** auf **Ja** festgelegt.
4. Wählen Sie **Workflow ausführen** aus. Im Dialogfeld **Datensatz nachschlagen** finden Sie drei Workflows:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Wählen Sie **ProcessRunCaller** und dann **Hinzufügen** aus.
6. Wählen Sie im nächsten Dialogfeld **OK** aus. Einem **Sleep** -Workflow folgt ein **Process** -Workflow.

  > [!NOTE]
  > In Schritt 5 können Sie auch **ProcessRunner** auswählen. Wenn Sie dann **OK** auswählen, folgt auf einen **Process** -Workflow ein **Sleep** -Workflow.

Die Workflows **ProcessRunCaller** und **ProcessRunner** erstellen Rechnungen. **ProcessRunCaller** ruft **ProcessRunner** auf. **ProcessRunner** ist der Workflow, der die Rechnungen tatsächlich erstellt. Es durchläuft alle Vertragszeilen, für die Rechnungen erstellt werden sollen, und erstellt Rechnungen für diese Zeilen. Zur Bestimmung der Vertragszeilen, für die Rechnungen erstellt werden sollen, überprüft der Job die Rechnungsdurchlaufdaten für die Vertragszeilen. Wenn Vertragszeilen, die zu einem Vertrag gehören, dasselbe Rechnungsdurchlaufdatum aufweisen, werden die Transaktionen zu einer Rechnung mit zwei Rechnungszeilen zusammengefasst. Wenn keine Transaktionen zum Erstellen von Rechnungen vorhanden sind, überspringt der Job die Rechnungserstellung.

Nachdem **ProcessRunner** ausgeführt wurde, ruft es **ProcessRunCaller** auf, gibt die Endzeit an und wird geschlossen. **ProcessRunCaller** startet dann einen Zeitgeber, der ab der angegebenen Endzeit 24 Stunden lang ausgeführt wird. Am Ende des Zeitgebers wird **ProcessRunCaller** geschlossen.

Beim Stapelverarbeitungsjob zum Erstellen von Rechnungen handelt es sich um einen wiederkehrenden Job. Wenn diese Stapelverarbeitung mehrmals ausgeführt wird, werden mehrere Instanzen des Jobs erstellt und verursachen Fehler. Deshalb sollten Sie die Stapelverarbeitung nur einmal starten und nur dann neu starten, wenn sie nicht mehr ausgeführt wird.

> [!NOTE]
> Die Stapelabrechnung wird nur für Projektvertragszeilen ausgeführt, die durch Rechnungspläne konfiguriert sind. Für eine Vertragsposition mit einer Festpreis-Abrechnungsmethode müssen Meilensteine konfiguriert sein. Für eine Projektvertragsposition mit einer Zeit- und Materialabrechnungsmethode muss ein datumsbasierter Rechnungszeitplan erstellt werden. Gleiches gilt für eine projektbasierte Vertragslinie.     
