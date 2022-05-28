---
title: Erstellen von Rechnungszeitplänen für eine projektbasierte Vertragszeile – Lite
description: Dieses Thema enthält Informationen zum Erstellen von Rechnungsplänen und Meilensteinen.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: edacae144f5c4879d3cfdf9585281858d7312589
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581973"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Erstellen von Rechnungszeitplänen für eine projektbasierte Vertragszeile – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Sie können Rechnungszeitplan für eine projektbasierte Vertragszeile anhängen: Die Rechnungsstellung ist erst nach Abschluss des Vertrags zur Erstellung eines Projektvertrags zulässig. Mit Rechnungsplänen können Rechnungsentwürfe für eine projektbasierte Vertragszeile automatisch erstellt werden. Wenn Sie vorhaben, Rechnungen immer manuell zu erstellen, können Sie das Erstellen von Rechnungsplänen in einer projektbasierten Vertragszeile oder einer Vertragszeile überspringen.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Einen Zeit- und Materialrechnungszeitplan für eine projektbasierte Vertragszeile erstellen

Wenn eine projektbasierte Vertragszeile eine Fakturierungsmethode für Zeit und Material enthält, können Sie einen datumsbasierten Rechnungszeitplan erstellen. Führen Sie die folgenden Schritte aus, um automatisch einen datumsbasierten Rechnungszeitplan zu erstellen.

1. Gehen Sie zu **Einstellungen** > **Rechnungshäufigkeiten**, um eine Rechnungsfrequenz einzurichten.
2. Öffnen Sie den Projektvertrag und auf der **Zusammenfassung**-Registerkarte legen Sie den gewünschten Liefertermin fest.
3. Öffnen Sie die Zeit- und Materialvertragszeile, für die Sie einen datumsbasierten Rechnungsplan erstellen möchten. 
4. Auf der **Rechnungsplan**-Registerkarte wählen Sie Rechnungsstartdatum und Rechnungshäufigkeit aus. 
5. Wählen Sie im Unterraster **Rechnungszeitplan erstellen** aus.

    Das System generiert den Rechnungsplan mit folgenden Feldinformationen:

    - **Rechnungslaufdatum** wird basierend auf der Rechnungshäufigkeit auf das Datum eingestellt.
    - **Transaktionsabschnittsdatum** wird auf den Tag vor dem **Rechnungsdurchlaufdatum** eingestellt.
    - **Ausführungsstatus** wird automatisch auf **Nichtausführen** festgelegt. Wenn der automatische Rechnungserstellungsauftrag für ein bestimmtes **Rechnungsdurchlaufdatum** ausgeführt wird, wird dieses Feld entweder auf **Ausführen erfolgreich** oder **Ausführen fehlgeschlagen** aktualisiert.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Einen Festpreis-Rechnungszeitplan für eine projektbasierte Vertragszeile erstellen

Wenn eine projektbasierte Vertragszeile über eine Festpreisabrechnungsmethode verfügt, können Sie einen auf Meilensteinen basierenden Rechnungsplan erstellen. Führen Sie die folgenden Schritte aus, um automatisch einen auf Meilensteinen basierenden Rechnungsplan für einen festen Satz von Meilensteinen zu erstellen, die für den Kalenderzeitraum gleichmäßig verteilt sind.

1. Gehen Sie zu **Einstellungen** > **Rechnungshäufigkeiten**, um eine Rechnungsfrequenz einzurichten.
2. Öffnen Sie den Projektvertrag und auf der **Zusammenfassung**-Registerkarte legen Sie den gewünschten Liefertermin fest.
3. Öffnen Sie die Festpreisvertragszeile, in der Sie einen Meilensteinplan erstellen müssen. 
4. Auf der **Rechnungsplan (Fakturierungsmeilensteine)**-Registerkarte wählen Sie Rechnungsstartdatum und Rechnungshäufigkeit aus. 
5. Wählen Sie im Unterraster **Periodische Meilensteine generieren** aus.

    Das System generiert den Rechnungsplan mit folgenden Meileinsteininformationen.

    - **Meilensteinname** wird auf das Datum eingestellt, das basierend auf der Rechnungshäufigkeit diktiert wird.
    - **Meilensteindatum** wird auf das Datum eingestellt, das basierend auf der Rechnungshäufigkeit diktiert wird.
    - **Meilensteinbetrag** wird berechnet, indem der Vertragsbetrag in der projektbasierten Vertragszeile durch die Anzahl der Meilensteine dividiert wird, die durch die Häufigkeit, den Abrechnungsbeginn und die angeforderten Liefertermine vorgegeben sind.
    - Wenn die Vertragszeile einen Wert im **Geschätzter Steuerbetrag**-Feld hat, wird dieses Feld auch bei der Generierung periodischer Meilensteine gleichmäßig auf jeden Meilenstein verteilt.

Abrechnungsmeilensteine sollten dem vertraglich vereinbarten Wert der projektbasierten Vertragszeile entsprechen. Wenn sie nicht gleich sind, tritt ein Fehler auf. Sie können diesen Fehler beheben, indem Sie überprüfen, ob die Abrechnungsmeilensteine den vertraglich vereinbarten Wert der Zeile summieren, indem Sie Meilensteine erstellen, bearbeiten oder löschen. Aktualisieren Sie die Seite, nachdem die Änderungen vorgenommen wurden.

### <a name="manually-create-milestones"></a>Meilensteine manuell erstellen

Festpreismeilensteine können manuell generiert werden, wenn sie nicht regelmäßig aufgeteilt werden. Führen Sie die folgenden Schritte aus, um einen Meilenstein manuell zu erstellen.

1. Öffnen Sie die Festpreisvertragszeile, in der Sie einen Meilenstein erstellen möchten. 
2. Auf der **Rechnungsplan**-Registerkarte wählen Sie im Unterraster **+ Einen neuen Meilenstein für die Vertragszeile erstellen** aus.
3. Geben Sie im Formular **Meilensteinerstellung** die erforderlichen Informationen anhand der folgenden Tabelle ein. 

| Feld | Position | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| Meilensteinname | Schnellertellung | Textfeld für den Namen des Meilensteins | Dieses Feld ist im Meilenstein der Projektvertragszeile und in der Rechnung enthalten. |
| Projektaufgabe | Schnellertellung | Wenn der Meilenstein an eine Projektaufgabe gebunden ist, verwenden Sie diese Referenz, um benutzerdefinierte Logik hinzuzufügen und den Meilensteinstatus basierend auf dem Aufgabenstatus festzulegen. | Dieser Verweis auf eine Aufgabe hat keine nachgelagerten Auswirkungen. |
| Meilensteindatum | Schnellertellung | Das Datum, an dem der automatische Rechnungserstellungsprozess nach dem Status dieses Meilensteins suchen sollte, um ihn für die Rechnungsstellung zu berücksichtigen. | Dies ist im Meilenstein der Projektvertragszeile und in der Rechnung enthalten. |
| Rechnungsstatus | Schnellertellung | Wenn der Meilenstein erstellt wird, wird dieser Status immer auf **Nicht bereit für die Rechnungsstellung** oder **Nicht gestartet** gesetzt. | Dies ist im Meilenstein der Projektvertragszeile und in der Rechnung enthalten. |
| Zeilenbetrag | Schnellertellung | Der Betrag oder Wert des Meilensteins, der dem Kunden in Rechnung gestellt wird. | Dieses Feld ist im Meilenstein der Projektvertragszeile und in der Rechnung enthalten. |
| Steuer | Schnellertellung | Der auf den Meilenstein angewendete Steuerbetrag. | Dies ist im Meilenstein der Projektvertragszeile und in der Rechnung enthalten. |

4. Klicken Sie auf **Speichern und schließen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]