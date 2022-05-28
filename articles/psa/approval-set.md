---
title: Genehmigungssätze in Project Service Automation
description: Dieses Thema enthält Informationen über Genehmigungssätze, Anforderungen und Untergruppen dieser Vorgänge.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0783441d3bf7ed80192a3890a2e297fea05fe425
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583307"
---
# <a name="approval-sets-in-project-service-automation"></a>Genehmigungssätze in Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Genehmigungssätze gruppieren Genehmigungsanforderungen in kleinere Teilmengen von Vorgängen. Diese Gruppierung ermöglicht die Verarbeitung von Genehmigungen nach Projektreihenfolge und ermöglicht Wiederholungsversuche und Sequenzierungen. Die Gruppierung verbessert die Zuverlässigkeit und Nachvollziehbarkeit der Genehmigungsverarbeitung bei großen Genehmigungsmengen.

Genehmigungssätze geben den Gesamtverarbeitungsstatus ihrer zugehörigen Datensätze an. Wenn ein Genehmigungsdatensatz mit einem Genehmigungssatz verarbeitet wird, verschiebt sich der Datensatz von **Eingereicht** zu **Genehmigt**, und ist nicht mit dem Genehmigungssatz verknüpft. Wenn ein Datensatz beim Einreichen zur Genehmigung fehlschlägt, bleibt der Datensatz im Status **Eingereicht** und der Genehmigungssatz wird als fehlgeschlagen markiert. Der Genehmigungssatz protokolliert die Fehlermeldung des Fehlers.

## <a name="processing-approvals-and-approval-sets"></a>Genehmigungen und Genehmigungssets bearbeiten
Genehmigungen, die zur Bearbeitung anstehen, sind in der Ansicht **Verarbeitungsgenehmigungen**. Das System versucht, alle Einträge mehrmals asynchron zu verarbeiten, einschließlich eines erneuten Versuchs einer Genehmigung, wenn vorherige Versuche fehlgeschlagen sind.

Das Feld **Gültigkeitsdauer des Genehmigungssatzes** zeichnet die Anzahl der verbleibenden Versuche auf, den Satz zu verarbeiten, bevor er als fehlgeschlagen markiert wird.

## <a name="failed-approvals-and-approval-sets"></a>Fehlgeschlagene Genehmigungen und Genehmigungseinstellungen
Die Ansicht **Fehlgeschlagene Genehmigungen** führt alle Genehmigungen auf, die ein Eingreifen des Benutzers erfordern. Öffnen Sie die zugehörigen Genehmigungssatzprotokolle, um die Fehlerursache zu ermitteln.
Die Auswahl von **Wiederholen** zählt zur Anzahl des Genehmigungssatzes, verschiebt den Genehmigungssatz zurück in den Status **wird bearbeitet** und versucht, die verbleibenden Datensätze zu verarbeiten.

## <a name="configure-approval-sets"></a>Genehmigungssätze konfigurieren

###  <a name="enable-the-approval-sets-feature"></a>Aktivieren Sie die Funktion Genehmigungssätze
Bevor Sie die Funktion Genehmigungssätze aktivieren, vergewissern Sie sich, dass derzeit keine Genehmigungen verarbeitet werden.

- Gehen Sie zur Seite **Projektparameter** und wählen Sie **Funktionssteuerung** > **Moderne Genehmigungen aktivieren**.

### <a name="turn-off-the-approval-sets-feature"></a>Deaktivieren Sie die Funktion Genehmigungssätze
Bevor Sie die Funktion Genehmigungssätze deaktivieren, vergewissern Sie sich, dass derzeit keine Genehmigungen verarbeitet werden.

- Gehen Sie zur Seite **Parameter** und wählen Sie **Funktionssteuerung** > **Moderne Genehmigungen deaktivieren**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfigurieren des asynchronen Schwellenwerts 
Wenn Genehmigungssätze erstellt werden, verlagert sich die Verarbeitung in den Hintergrund, wenn die ausgewählte Anzahl von zu genehmigenden Datensätzen den angegebenen Schwellenwert überschreitet. Verwenden Sie das Feld **Asynchroner Schwellenwert**, um zu konfigurieren, wann die Genehmigungsverarbeitung synchron oder asynchron ausgeführt werden soll.
Gültige Werte sind:

  - Null: Alle Anfragen sollten asynchron verarbeitet werden. 
  - Zahlen größer als Null: Genehmigungen werden nur dann asynchron verarbeitet, wenn die übermittelte Anzahl der Genehmigungen diesen Wert überschreitet.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
