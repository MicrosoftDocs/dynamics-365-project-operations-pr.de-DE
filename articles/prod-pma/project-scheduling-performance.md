---
title: Planungsleistung für Projektressourcen
description: Dieses Thema enthält Informationen zur Verbesserung der Leistung der Ressourcenplanung für eine große Anzahl von Projekten.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076507"
---
# <a name="project-resource-scheduling-performance"></a>Planungsleistung für Projektressourcen

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Leistungsprobleme im Zusammenhang mit der Ressourcenplanung können auftreten, wenn die Anzahl der Projekte in die Tausende geht. Um die Leistung der Ressourcenplanung zu verbessern, steht eine Funktion zur Verfügung, mit der Benutzer die Zeit reduzieren können, die zum Starten des Ressourcenverfügbarkeitsformulars erforderlich ist. Dies entfernt insbesondere den Rollup-Synchronisierungsprozess für die Ressourcenkapazität und verwendet die Tabelle **ResProjectResource** , um die Ressourcensuche zu beschleunigen. Beachten Sie, dass die Tabelle **ResRollup** nicht länger verwendet wird.

> [!IMPORTANT]
> Wenn eine Abhängigkeit entweder vom Rollup-Synchronisierungsprozess der Ressourcenkapazität oder von der Tabelle **ResProjectResource** besteht, verwenden Sie diese Funktion nicht.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Leistungsverbesserung bei der Ressourcenplanung aktivieren
Führen Sie die folgenden Schritte aus, um die Leistungsverbesserung bei der Ressourcenplanung zu aktivieren.

1. Navigieren Sie zu **Funktionsverwaltung** > **Alle** , und suchen Sie in der Funktionsliste **Funktion zur Leistungsverbesserung der Ressourcenplanung aktivieren**.
2. Wählen Sie **Jetzt aktivieren** aus.

> [!NOTE]
> Wenn Sie die Funktion in der Liste nicht finden können, wählen Sie **Auf Updates prüfen** aus, um die Liste zu aktualisieren.

3. Aktualisieren Sie Ihren Browser, und navigieren Sie dann zu **Projektmanagement und -buchhaltung** > **Periodisch** > **Projektressourcen** > **Kapazität der Ressourcenkalender in allen Unternehmen synchronisieren**.
4. Legen Sie **Vorhandene Kapazitätssätze entfernen** auf **Ja** fest, um vorherige Daten zu entfernen. Wenn Sie inkrementelle Daten generieren möchten, legen Sie diese auf **Nein** fest.
5. Wählen Sie im Feld **Periodencode** die Periode aus, in der die Daten generiert werden sollen. Wenn Sie einen Periodencode auswählen, müssen Sie kein Start- und Enddatum definieren.
6. Wenn Sie das Feld **Periodencode** leer lassen, wählen Sie die entsprechenden Start- und Enddaten zum Generieren von Daten aus.
7. Klicken Sie auf **OK**.

 > [!NOTE]
 > Dadurch werden allgemeine Daten an die Tabelle **ResCalendarCapacity** für alle Unternehmen in Ihrer Umgebung verteilt, sodass der Batchauftrag nur in einer juristischen Person ausgeführt werden muss. Die Daten in diesem Batchauftrag werden benötigt, um die Ressourcenkapazität über den zugehörigen Kalender zu berechnen.

8. Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Periodisch** > **Projektressourcen** > **Projektressourcen in allen Unternehmen ausfüllen** , und wählen Sie dann **OK** aus. Dies ist das Datenaktualisierungsskript für allgemeine Daten in den Tabellen **ResProjectResource** , **ResCalendarDateTimeRange** und **ResEffectiveDateTimeRange**. Werte für die Felder **PSAPRojSchedRole.RootActivity** werden ebenfalls aktualisiert. Wenn dies nicht ausgeführt wird, erhalten Sie eine Warnung, wenn Sie versuchen, Ressourcenplanungsvorgänge auszuführen.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Leistungsverbesserung bei der Ressourcenplanung deaktivieren

1. Navigieren Sie zu **Funktionsverwaltung** > **Alle** , und suchen Sie nach **Funktion zur Leistungsverbesserung der Ressourcenplanung aktivieren**.
2. Wählen Sie die Funktion und dann die Schaltfläche **Deaktivieren** aus.
3. Aktualisieren Sie Ihren Browser.
4. Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Periodisch** > **Kapazitätssynchronisierung** > **Synchronisation der Rollup-Kapazität**.
5. Legen Sie auf der Seite **Synchronisation der Rollup-Kapazität** die Option **Vorhandene Kapazitätssätze entfernen** auf **Ja** fest, um die vorherigen Daten zu entfernen. Wenn Sie inkrementelle Daten generieren möchten, legen Sie diese auf **Nein** fest.
6. Wählen Sie im Feld **Periodencode** die Periode aus, in der die Daten generiert werden sollen. Wenn Sie einen Periodencode auswählen, müssen Sie kein Start- und Enddatum definieren.
7. Wenn Sie das Feld **Periodencode** leer lassen, wählen Sie die entsprechenden Start- und Enddaten zum Generieren von Daten aus.
8. Klicken Sie auf **OK**.

> [!NOTE]
> Dadurch werden allgemeine Daten an die Tabelle **ResRollup** für alle Unternehmen in Ihrer Umgebung verteilt, sodass der Batchauftrag nur in einer juristischen Person ausgeführt werden muss. Dieser Batchauftrag ist für alle **Ressourcenverfügbarkeits** -Ansichten erforderlich. Wenn dieser Batchauftrag nicht ausgeführt wird, werden die **ResRollup** -Daten während der Bearbeitung generiert, was einige Zeit dauern kann.


[!INCLUDE[footer-include](../includes/footer-banner.md)]