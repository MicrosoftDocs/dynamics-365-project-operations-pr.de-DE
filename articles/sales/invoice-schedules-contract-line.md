---
title: Rechnungszeitpläne für eine projektbasierte Vertragszeile erstellen
description: Dieser Artikel beschreibt, wie Sie Rechnungszeitpläne und Meilensteine für Vertragszeilen erstellen können.
author: rumant
ms.date: 10/17/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: afc6357b7b221b91674035ae3181ef84eed8d586
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825096"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line"></a>Rechnungszeitpläne für eine projektbasierte Vertragszeile erstellen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Sie können einer projektbasierten Vertragszeile einen Rechnungszeitplan hinzufügen. Die Rechnungsstellung ist erst zulässig, nachdem der Vertrag abgeschlossen wurde und Sie einen Projektvertrag erstellen. Mit einem Rechnungszeitplan können automatisch Rechnungsentwürfe für eine projektbasierte Vertragszeile erstellt werden. Wenn Sie jedoch nur manuell Rechnungen erstellen, können Sie das Erstellen von Rechnungszeitplänen in Vertragszeilen überspringen.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Einen Zeit‑ und Materialrechnungsplan für eine Vertragszeile erstellen

Wenn eine projektbasierte Vertragszeile über eine Zeit‑ und Materialabrechnungsmethode verfügt, können Sie einen datumsbasierten Rechnungsplan erstellen. Führen Sie die folgenden Schritte aus, um automatisch einen datumsbasierten Rechnungszeitplan zu erstellen.

1. Navigieren Sie zu **Einstellungen** > **Rechnungshäufigkeiten**, und richten Sie eine Rechnungshäufigkeit ein.
2. Navigieren Sie zum Projektvertragsdatensatz, und wählen Sie auf der Registerkarte **Zusammenfassung** im Feld **Gewünschtes Lieferdatum** ein Datum aus.
3. Öffnen Sie die Vertragszeile **Zeit und Material**, für die Sie den datumsbasierten Rechnungsplan erstellen. 
4. Wählen Sie auf der Registerkarte **Rechnungszeitplan** das Rechnungsstartdatum und die Rechnungshäufigkeit aus.
5. Wählen Sie im Unterraster die Option **Rechnungszeitplan generieren** aus. Der Rechnungszeitplan wird mit den Feldern **Rechnungsdurchlaufdatum**, **Transaktionsabschnittsdatum** und **Ausführungsstatus** wie folgt eingestellt:

    - **Rechnungsdurchlaufdatum**: Dieses Datum wird von der Rechnungshäufigkeit vorgegeben.
    - **Transaktionsabschnittsdatum**: Der Tag vor dem Rechnungsdurchlaufdatum
    - **Ausführungsstatus**: Ist automatisch auf **Nicht ausführen** festgelegt. Wenn der automatische Rechnungserstellungsauftrag für ein bestimmtes Rechnungsdurchlaufdatum ausgeführt wird, wird dieses Feld entweder auf **Ausführen erfolgreich** oder **Ausführen fehlgeschlagen** aktualisiert.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Einen Zeitplan für eine Festpreisrechnung für eine Vertragszeile erstellen

Wenn die Vertragszeile eine feste Fakturierungsmethode hat, können Sie einen meilensteinbasierten Rechnungszeitplan erstellen. 

> [!NOTE]
> Meilensteine können nicht in einer Vertragszeile erstellt werden, wenn der Vertragszeile kein Projekt zugeordnet ist.

Führen Sie die folgenden Schritte aus, um einen meilensteinbasierten Rechnungszeitplan für einen festen Satz von gleichmäßig verteilten Meilensteinen für den Kalenderzeitraum zu erstellen.

1. Navigieren Sie zu **Einstellungen** > **Rechnungshäufigkeiten**, und richten Sie eine Rechnungshäufigkeit ein.
2. Navigieren Sie zum Projektvertragsdatensatz, und wählen Sie auf der Registerkarte **Zusammenfassung** im Feld **Gewünschtes Lieferdatum** ein Datum aus.
3. Öffnen Sie die Vertragszeile **Festpreis**, für die Sie den Meilensteinzeitplan erstellen. Wählen Sie auf der Registerkarte **Fakturierungsmeilensteine** das Rechnungsstartdatum und die Rechnungshäufigkeit aus. 
4. Wählen Sie im Unterraster die Option **Periodische Meilensteine generieren** aus. Der Rechnungszeitplan wird mit den Feldern **Meilensteinname**, **Meilensteindatum** und **Meilensteinbetrag** wie folgt eingestellt:

    - **Meilensteinname**: Dieser Name wird durch die Rechnungshäufigkeit bestimmt.
    - **Meilensteindatum**: Dieses Datum wird von der Rechnungshäufigkeit vorgegeben.
    - **Meilensteinbetrag**: Dieser Meilensteinbetrag wird berechnet, indem der Vertragsbetrag in der Vertragszeile durch die Anzahl der Meilensteine dividiert wird, die durch die Häufigkeit, den Abrechnungsbeginn sowie die angeforderten Liefertermine vorgegeben sind.

    Wenn die Vertragszeile einen Wert im Feld **Geschätzter Steuerbetrag** hat, dann wird dieses Feld auch bei der Generierung periodischer Meilensteine gleichmäßig auf jeden Meilenstein verteilt.

Abrechnungsmeilensteine sollten dem vertraglich vereinbarten Wert der Vertragszeile entsprechen. Wenn dies nicht der Fall ist, erhalten Sie einen Fehler auf der Seite **Vertragszeile**. Sie können den Fehler beheben, indem Sie überprüfen, ob die Abrechnungsmeilensteine den vertraglich vereinbarten Wert der Zeile summieren, indem Sie Meilensteine erstellen, bearbeiten oder löschen. Aktualisieren Sie nach den Änderungen die Seite, um den Fehler zu beheben.

### <a name="manually-create-milestones"></a>Meilensteine manuell erstellen

Sie können Festpreismeilensteine auch manuell generieren, wenn sie nicht regelmäßig aufgeteilt werden. Führen Sie folgende Schritte aus, um einen Meilenstein manuell zu erstellen.

1. Öffnen Sie die Festpreisvertragszeile, für die Sie einen Meilenstein erstellen, und wählen Sie auf der Registerkarte **Rechnungszeitplan** im Unterregister die Option **+ Neuen Meilenstein für Vertragszeile erstellen** aus. 
2. Geben Sie auf der Seite **Meilensteinerstellung** die erforderlichen Informationen basierend auf der folgenden Tabelle ein.

| Feld | Position | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| Meilensteinname | Schnellertellung | Textfeld für den Namen des Meilensteins | Dies wird auf den Meilenstein der Projektvertragszeile und auf die Rechnung übertragen. |
| Projektaufgabe | Schnellertellung | Wenn der Meilenstein an die Projektaufgabe gebunden ist, verwenden Sie diese Referenz, um eine benutzerdefinierte Logik hinzuzufügen, die den Meilensteinstatus basierend auf dem Aufgabenstatus festlegt. | Die Anwendung hat keine nachgelagerten Auswirkungen dieser Referenz auf eine Aufgabe. |
| Meilensteindatum | Schnellertellung | Legen Sie das Datum fest, an dem der automatische Rechnungserstellungsprozess nach dem Status dieses Meilensteins suchen soll, um ihn für die Rechnungsstellung zu berücksichtigen. | Dies wird auf den Meilenstein der Projektvertragszeile und auf die Rechnung übertragen. |
| Rechnungsstatus | Schnellertellung | Wenn ein Meilenstein erstellt wird, wird dieser Status immer auf **Nicht bereit für die Rechnungsstellung** oder **Nicht gestartet** festgelegt. | Dies wird auf den Meilenstein der Projektvertragszeile und auf die Rechnung übertragen. |
| Zeilenbetrag | Schnellertellung | Betrag oder Wert des Meilensteins, der dem Kunden in Rechnung gestellt wird. | Dies wird auf den Meilenstein der Projektvertragszeile und auf die Rechnung übertragen. |
| Steuer | Schnellertellung | Der auf den Meilenstein angewendete Steuerbetrag. | Dies wird auf den Meilenstein der Projektvertragszeile und auf die Rechnung übertragen. |

3. Klicken Sie auf **Speichern und schließen**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
