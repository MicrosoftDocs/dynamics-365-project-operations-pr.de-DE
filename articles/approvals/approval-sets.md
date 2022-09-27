---
title: Genehmigungssätze
description: Dieser Artikel erklärt, wie Sie mit Genehmigungssätzen, Anträgen und den Untergruppen dieser Vorgänge arbeiten können.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524915"
---
# <a name="approval-sets"></a>Genehmigungssätze

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Genehmigungssätze gruppieren Genehmigungsanforderungen in kleinere Teilmengen von Vorgängen. Diese Gruppierung ermöglicht die Bearbeitung von Genehmigungen nach Projekt in einer bestimmten Reihenfolge und ermöglicht Wiederholungsversuche und Sequenzierung. Das Zusammenfassen der Genehmigungsanfragen verbessert die Zuverlässigkeit und Nachvollziehbarkeit der Genehmigungsverarbeitung bei großen Genehmigungsmengen.

Genehmigungssätze geben den Gesamtverarbeitungsstatus ihrer zugehörigen Datensätze an. Wenn ein Genehmigungsdatensatz mit einem Genehmigungssatz verarbeitet wird, verschiebt sich der Datensatz von **Eingereicht** zu **Zugelassen**, und ist nicht mehr mit dem Genehmigungssatz verknüpft. Wenn ein Datensatz beim Einreichen zur Genehmigung fehlschlägt, bleibt der Datensatz im Status **Eingereicht** und der Genehmigungssatz wird als fehlgeschlagen markiert. Der Genehmigungssatz protokolliert die Fehlermeldung des Fehlers.

## <a name="processing-approvals-and-approval-sets"></a>Genehmigungen und Genehmigungssets bearbeiten
Genehmigungen, die zur Bearbeitung anstehen, sind in der Ansicht **Verarbeitungsgenehmigungen**. Das System verarbeitet alle Eingaben mehrmals asynchron, einschließlich des erneuten Versuchs einer Genehmigung, wenn vorherige Versuche fehlgeschlagen sind.

Das Feld **Gültigkeitsdauer des Genehmigungssatzes** zeichnet die Anzahl der verbleibenden Versuche auf, den Satz zu verarbeiten, bevor er als fehlgeschlagen markiert wird.

Genehmigungssätze werden durch die periodische Aktivierung basierend auf einem **Cloud-Flow** namens **Project Service –  Projektgenehmigungssätze wiederholt planen** verarbeitet. Dies findet sich in der **Lösung** namens **Project Operations**. 

Stellen Sie sicher, dass der Flow aktiviert ist, indem Sie die folgenden Schritte ausführen.

1. Melden Sie sich als Administrator bei [flow.microsoft.com](https://powerautomate.microsoft.com) an.
2. Wechseln Sie in der oberen rechten Ecke zu der Umgebung, die Sie für Dynamics 365 Project Operations verwenden.
3. Wählen Sie **Lösungen** aus, um die Lösungen aufzuführen, die in der Umgebung installiert sind.
4. In der Lösungsliste wählen Sie **Project Operations**.
5. Ändern Sie den Filter von **Alle** in **Cloud-Flows**.
6. Überprüfen Sie, ob der **Project Service – Projektgenehmigungssätze regelmäßig planen**-Flow auf **Ein** eingestellt. Wenn dies nicht der Fall ist, wählen Sie den Flow aus, und wählen Sie dann **Aktivieren** aus.
7. Überprüfen Sie, ob die Verarbeitung alle fünf Minuten erfolgt, indem Sie die **Systemaufträge**-Liste im **Einstellungen**-Bereich innerhalb Ihrer Project Operations Dataverse-Umgebung überprüfen.

## <a name="failed-approvals-and-approval-sets"></a>Fehlgeschlagene Genehmigungen und Genehmigungseinstellungen
Die **Fehlgeschlagene Genehmigungen**-Ansicht listet alle Genehmigungen auf, die ein Eingreifen des Benutzers erfordern. Öffnen Sie die zugehörigen Genehmigungssatzprotokolle, um die Fehlerursache zu ermitteln.
Die Auswahl von **Wiederholen** zählt zur Anzahl des Genehmigungssatzes, verschiebt den Genehmigungssatz zurück in den Status **wird bearbeitet** und versucht, die verbleibenden Datensätze zu verarbeiten.

## <a name="configure-approval-sets"></a>Genehmigungssätze konfigurieren

### <a name="enable-the-approval-sets-feature"></a>Aktivieren Sie die Funktion Genehmigungssätze
Bevor Sie die Funktion Genehmigungssätze aktivieren, vergewissern Sie sich, dass derzeit keine Genehmigungen verarbeitet werden. Nachdem diese Funktion aktiviert wurde, kann sie nicht mehr deaktiviert werden.

- Gehen Sie zur Seite **Projektparameter** und wählen Sie **Funktionssteuerung** > **Moderne Genehmigungen aktivieren**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfigurieren des asynchronen Schwellenwerts 
Wenn Genehmigungssätze erstellt werden, verlagert sich die Verarbeitung in den Hintergrund, wenn die ausgewählte Anzahl von zu genehmigenden Datensätzen den angegebenen Schwellenwert überschreitet. Verwenden Sie das Feld **Asynchroner Schwellenwert**, um zu konfigurieren, wann die Genehmigungsverarbeitung synchron oder asynchron ausgeführt werden soll. Wählen Sie eine der folgenden Werte aus:

  - Null: Alle Anfragen sollten asynchron verarbeitet werden. 
  - Zahlen größer als Null: Genehmigungen werden nur dann asynchron verarbeitet, wenn die übermittelte Anzahl der Genehmigungen diesen Wert überschreitet.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
