---
title: Einbehaltene Kreditorenbeträge einrichten
description: In diesem Thema wird erläutert, wie einbehaltene Kreditorenbeträge eingerichtet werden.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e0cd7669c7d6b916261e2c85cce0f24ff241a075
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583703"
---
# <a name="set-up-vendor-retention"></a>Einbehaltene Kreditorenbeträge einrichten

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel bietet Informationen dazu, wie Sie einbehaltene Kreditorenbeträge einrichten.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Richten Sie ein Kreditoreneinbehaltungskonto im Hauptbuch ein

1. Gehen Sie in Dynamics 365 Finance zu **Hauptbuch** > **Buchungseinrichtung** > **Konten für automatische Transaktionen**.
2. Eine neue Position hinzufügen.
3. Wählen Sie im Feld **Buchungsart** die Option **Einbehaltene Kreditorenbeträge** aus.
4. Wählen Sie das Hauptkonto für die Kreditoreneinbehaltsbuchung aus.

## <a name="create-vendor-retention-terms"></a>Bedingungen für einbehaltene Kreditorenbeträge erstellen

Verwenden Sie die Seite **Lieferantenbindungsbedingungen** zum Einrichten und Verwalten von Aufbewahrungsfristen für Kreditorenzahlungen. Geben Sie den einzubehaltenden Prozentsatz einer Kreditorenzahlung ein wie auch den freizugebenden Prozentsatz der zuvor einbehaltenen Beträge. Beträge werden automatisch auf Kreditorenrechnungen einbehalten, bis der Vertrag den angegebenen Fertigstellungsstatus erreicht. Nachdem Aufbewahrungsbedingungen für einen Kreditor eingerichtet wurden, können Sie sie auf jedes Projekt anwenden, an dem der Kreditor arbeitet.

1. Gehen Sie in Finance zu **Projektmanagement und Buchhaltung** > **Einstellungen** > **Aufbewahrung** > **Aufbewahrungsbedingungen für Lieferantenzahlungen**.
2. Wählen Sie **Neu** aus, um eine neue Bedingung für die Einbehaltung von Kreditorenzahlungen hinzuzufügen. Der Wert im Feld **Regelkennung** für die neue Bedingung wird automatisch eingegeben. 
3. Geben Sie im Feld **Beschreibung** einen beschreibenden Namen für den neuen Term ein.
4. Auf der Registerkarte **Bedingungen** wählen Sie **Position hinzufügen**, um eine Lieferantenbindungsfrist einzugeben.
5. Geben Sie im Feld **Prozentsatz gelieferter Einheiten** einen Vollendungsgrad für die Regel ein. Beträge werden bei Kreditorenrechnungen automatisch einbehalten, bis die Projektvollendungsstufe gleich dem Prozentsatz ist, den Sie eingeben. Wenn Sie beispielsweise 50,00 eingeben, werden die Beträge einbehalten, bis das Projekt zu 50 Prozent abgeschlossen ist.
6. Geben Sie im Feld **Einzubehaltender Prozentsatz** den einzubehaltenden Prozentsatz eines Kreditorenrechnungsbetrags ein. Wenn Sie beispielsweise 10,00 in dieses Feld eingeben, werden 10 Prozent des Betrags für Kreditorenrechnungen einbehalten, bis das Projekt den Vollendungsgrad erreicht, den Sie im Feld **Prozentsatz der gelieferten Einheiten** ausgewählt haben.
7. Geben Sie im Feld **Feizugebender Prozentsatz** den Prozentsatz zuvor einbehaltener Kreditorenrechnungsbeträge ein, die beim ausgewählten Vollendungsgrad des Projekts freizugeben sind.

> [!NOTE]
> Wenn Sie mehrere Meilensteine für verschiedene Vollendungsgrade des Projekts bestimmt haben, geben Sie für jede Einbehaltungsregel eine separate Position für Bedingungen für die einbehaltenen Kreditorenbeträge ein. Jede Position kann jeweils unterschiedliche Prozentsätze zur Einbehaltung oder zur Prozentsätze für die Freigabe für jeden Vollendungsgrad des Projekts bestimmen.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Kreditorenvereibarung für das Projekt einrichten

Richten Sie die Lieferantenaufbewahrungsbedingungen ein, die für das Projekt gelten. Die Bedingungen für die Einbehaltung von Kreditorenzahlungen werden auch in Bestellungen angezeigt, die Sie für den Kreditor erstellen.

1. Wechseln Sie in Finance zu **Projektmanagement und ‑buchhaltung** > **Projekte** > **Alle Projekte**. 
2. Wählen Sie ein Projekt aus, und wählen Sie im Aktivitätsbereich **Projektgruppe** > **Lieferantenvereinbarungen**.
3. Fügen Sie auf der Seite **Lieferantenvereinbarungen** eine neue Position hinzu.
4. Wählen Sie im Feld **Kontocode** eine der folgenden Optionen aus:
   - **Tabelle**: Die Bedingungen für die Einbehaltung von Kreditorenzahlungen gelten für einen einzelnen Kreditor.
   - **Gruppe** : Die Bedingungen für die Einbehaltung von Kreditorenzahlungen gelten für alle Kreditoren in einer Kreditorengruppe.
   - **Alle**: Die Bedingungen für die Einbehaltung von Kreditorenzahlungen gelten für alle Kreditoren.
5. Wählen Sie im Feld **Kreditor/Kreditorengruppe** den Kreditor oder die Kreditorengruppe aus, für die die Bedingungen für die Einbehaltung von Kreditorenzahlungen gelten soll. Wenn Sie im vorherigen Schritt **Alle** ausgewählt haben, ist dieses Feld nicht verfügbar.
6. Wählen Sie im Feld **Lieferantenbindungsbedingungen** die Regel-ID für die Aufbewahrungsbedingungen aus, die für diesen Kreditor gelten sollen.

