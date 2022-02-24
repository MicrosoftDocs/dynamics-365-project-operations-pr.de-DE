---
title: Automatische Rechnungserstellung konfigurieren – Lite
description: Diese Thema enthält Informationen zum Konfigurieren der automatischen Erstellung von Proforma-Rechnungen.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ce9cb9090c44762f370bf8d574d179077b6a821
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176565"
---
# <a name="configure-automatic-invoice-creation---lite"></a>Automatische Rechnungserstellung konfigurieren – Lite
 
_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Sie können die automatische Rechnungserstellung in Dynamics 365 Project Operations konfigurieren. Das System erstellt einen Entwurf einer Proforma-Rechnung basierend auf dem Rechnungszeitplan für jeden Projektvertrag und jede Vertragszeile. Rechnungszeitpläne werden auf Vertragszeilenebene konfiguriert. Jede Zeile in einem Vertrag kann einen eigenen Rechnungszeitplan haben, oder in jeder Zeile des Vertrags kann derselbe Rechnungszeitplan enthalten sein.

Wenn Sie eine Rechnung erstellen, erstellt das System immer mindestens eine Rechnung pro Projektvertrag. In einigen Fällen werden möglicherweise mehrere Rechnungen erstellt.

Wenn der Vertrag beispielsweise mehrere Kunden hat, wird dieselbe Anzahl von Rechnungen erstellt wie die Anzahl der Kunden, die fakturierbare Transaktionen für diesen Projektvertrag in Rechnung stellen müssen.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Informationen dazu, wie Transaktionen in einer Rechnung eingeschlossen sind 

Manchmal gibt jede projektbasierte Vertragszeile einen separaten Rechnungszeitplan an. Implementierungsservices für den Adatum-Vertrag haben beispielsweise die folgenden Vertragszeilen:

- Prototyparbeit zum Festpreis mit zwei manuell erstellten Meilensteinen
- Implementierungsarbeiten, die Zeit beinhalten und montags vierzehntägig in Rechnung gestellt werden
- Anfallende Kosten, die monatlich am ersten Montag eines jeden Monats in Rechnung gestellt werden müssen

Die für jede dieser beiden Positionen definierten Rechnungszeitpläne sehen wie folgt aus:

| Vertragszeile | Rechnungsdurchlaufdatum | Transaktionsabschnittsdatum | Meilensteindatum | Meilenstein-Betrag |
| --- | --- | --- | --- | --- |
| Prototyparbeit | Montag, 5. Oktober | - | Montag, 5. Oktober | 5.000 USD |
| - | Dienstag, 3. November | - | Dienstag, 3. November | 12.000 USD |
| Implementierungsarbeit | Montag, 5. Oktober | Sonntag, 4. Oktober | - | - |
| - | Montag, 19. Oktober | Sonntag, 18. Oktober | - | - |
| - | Montag, 2. November | Sonntag, 1. November | - | - |
| - | Montag, 16. November | Sonntag, 15. November | - | - |
| Angefallene Kosten | Montag, 5. Oktober | Sonntag, 4. Oktober | - | - |
| - | Montag, 2. November | Sonntag, 1. November | - | - |

Bei Ausführung der automatischen Rechnungsstellung in diesem Beispiel am folgenden Datum:

- **4. Oktober oder ein Datum davor**: Für diesen Vertrag wird keine Rechnung erstellt, da die Tabelle **Rechnungszeitplan** für jede dieser Vertragszeilen Sonntag, den 4. Oktober nicht als Datum des Rechnungslaufs angibt.
- **Montag, 5. Oktober**: Eine Rechnung wird erstellt für:

    - Prototyparbeit, die den Meilenstein enthält, wenn er als **Bereit für die Rechnungsstellung** markiert ist
    - Implementierungsarbeiten, die alle Zeittransaktionen umfassen, die vor dem Transaktionsstichtag Sonntag, 4. Oktober erstellt und als **Bereit für die Rechnungsstellung** markiert wurden.
    - Angefallene Kosten, die alle Ausgabentransaktionen umfassen, die vor dem Transaktionsstichtag Sonntag, 4. Oktober erstellt und als **Bereit für die Rechnungsstellung** markiert wurden.
  
- **Am 6. Oktober oder an einem Datum vor dem 19. Oktober**: Für diesen Vertrag wird keine Rechnung erstellt, da die Tabelle **Rechnungszeitplan** für jede dieser Vertragszeilen den 06. Oktober oder ein Datum vor dem 19. Oktober nicht als Datum des Rechnungslaufs angibt.
- **Montag, 19. Oktober**: Eine Rechnung wird für Implementierungsarbeiten generiert, die alle Zeittransaktionen enthält, die vor dem Transaktionsstichtag Sonntag, 18. Oktober erstellt und als **Bereit für die Rechnungsstellung** markiert wurden.
- **Montag, 2. November**: Eine Rechnung wird erstellt für:

    - Implementierungsarbeiten, die alle Zeittransaktionen umfassen, die vor dem Transaktionsstichtag Sonntag, 1. November erstellt und als **Bereit für die Rechnungsstellung** markiert wurden.
    - Angefallene Kosten, die alle Ausgabentransaktionen umfassen, die vor dem Transaktionsstichtag Sonntag, 1. November erstellt und als **Bereit für die Rechnungsstellung** markiert wurden.

- **Dienstag, 3. November**: Eine Rechnung wird für Prototyparbeit erstellt, die den Meilenstein für 12.000 USD enthält, sofern dieser als **Bereit für die Rechnungsstellung** markiert ist.

## <a name="configure-automatic-invoicing"></a>Automatische Rechnungsstellung konfigurieren

Führen Sie die folgenden Schritte aus, um einen automatisierten Rechnungslauf zu konfigurieren.

1. Navigieren Sie in **Project Operations** zu **Einstellungen** > **Setup für wiederkehrende Rechnungen**.
2. Erstellen Sie einen Batchauftrag und nennen Sie ihn **Vorgang zum Erstellen von Rechnungen**. Der Name des Batchauftrags muss die Wörter „Rechnungen erstellen“ enthalten.
3. Wählen Sie im Feld **Auftragstyp** **Keiner** aus. Standardmäßig sind die Felder **Frequenz täglich** und **Ist aktiv** auf **Ja** festgelegt.
4. Wählen Sie **Workflow ausführen** aus. Im Dialogfeld **Datensatz nachschlagen** finden Sie drei Workflows:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Wählen Sie **ProcessRunCaller** und dann **Hinzufügen** aus.
6. Wählen Sie im nächsten Dialogfeld **OK** aus. Einem **Sleep**-Workflow folgt ein **Process** -Workflow. 

> [!NOTE]
> In Schritt 5 können Sie auch **ProcessRunner** auswählen. Wenn Sie dann **OK** auswählen, folgt auf einen **Process**-Workflow ein **Sleep**-Workflow.

Die Workflows **ProcessRunCaller** und **ProcessRunner** erstellen Rechnungen. **ProcessRunCaller** ruft **ProcessRunner** auf. **ProcessRunner** ist der Workflow, der die Rechnungen tatsächlich erstellt. Der Workflow durchläuft alle Vertragszeilen, für die Rechnungen erstellt werden sollen, und erstellt Rechnungen für diese Zeilen. Zur Bestimmung der Vertragszeilen, für die Rechnungen erstellt werden sollen, überprüft der Job die Rechnungsdurchlaufdaten für die Vertragszeilen. Wenn Vertragszeilen, die zu einem Vertrag gehören, dasselbe Rechnungsdurchlaufdatum aufweisen, werden die Transaktionen zu einer Rechnung mit zwei Rechnungszeilen zusammengefasst. Wenn keine Transaktionen zum Erstellen von Rechnungen vorhanden sind, überspringt der Auftrag das Erstellen einer Rechnung.

Nachdem **ProcessRunner** ausgeführt wurde, ruft es **ProcessRunCaller** auf, gibt die Endzeit an und wird geschlossen. **ProcessRunCaller** startet dann einen Zeitgeber, der ab der angegebenen Endzeit 24 Stunden lang ausgeführt wird. Am Ende des Zeitgebers wird **ProcessRunCaller** geschlossen.

Beim Stapelverarbeitungsjob zum Erstellen von Rechnungen handelt es sich um einen wiederkehrenden Job. Wenn diese Batchverarbeitung mehrmals ausgeführt wird, werden mehrere Instanzen des Auftrags erstellt, und es werden Fehler verursacht. Deshalb sollten Sie die Batchverarbeitung nur einmal starten und nur dann neu starten, wenn sie nicht mehr ausgeführt wird.

> [!NOTE]
> Die Batchabrechnung wird nur für Projektvertragszeilen in Project Operations ausgeführt, die durch Rechnungszeitpläne konfiguriert sind. Für eine Vertragszeile mit einer Festpreis-Abrechnungsmethode müssen Meilensteine konfiguriert sein. Für eine Projektvertragsposition mit einer Zeit- und Materialabrechnungsmethode muss ein datumsbasierter Rechnungszeitplan erstellt werden.
