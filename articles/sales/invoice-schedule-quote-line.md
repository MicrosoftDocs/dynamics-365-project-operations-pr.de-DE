---
title: Rechnungszeitpläne für projektbasierte Angebotspositionen
description: Dieser Artikel enthält Informationen über das Erstellen von Rechnungszeitplänen und Meilensteinen für Angebotszeilen.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b1e431bc3586f9fef7a01348555e4ee4e06cc66c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918311"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Rechnungszeitpläne für projektbasierte Angebotspositionen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Eine projektbasierte Angebotsposition bietet die Möglichkeit, einen Rechnungszeitplan auszudrücken. Dies ist während der Angebotsphase optional, da die Anwendung die Rechnungsstellung eines Projekts nicht unterstützt, wenn es an eine Angebotsposition gebunden ist. Die Rechnungsstellung ist erst zulässig, nachdem das Angebot gewonnen wurde. Die einzige nachgelagerte Auswirkung der Erstellung eines Rechnungszeitplans während der Angebotsphase besteht darin, dass dieser Rechnungszeitplan an die projektbasierte Vertragszeile kopiert wird. Wenn Sie während der Angebotsphase keinen Rechnungszeitplan erstellen, können Sie dies in der projektbasierten Vertragszeile tun.

Insgesamt besteht der Zweck von Rechnungszeitplänen darin, die automatische Erstellung von Rechnungsentwürfen für eine projektbasierte Vertragszeile zu ermöglichen. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Erstellen eines Zeitplans für Zeit- und Materialrechnungen für eine projektbasierte Angebotsposition

Wenn die Abrechnungsmethode für eine projektbasierte Angebotsposition Zeit und Material ist, generiert das System einen datumsbasierten Rechnungszeitplan. Führen Sie die folgenden Schritte aus, um automatisch einen datumsbasierten Rechnungszeitplan zu erstellen.

1. Wechseln Sie zu **Einstellungen** > **Rechnungsintervalle** und richten Sie einen Rechnungsintervall ein.
2. Auf der **Angebote**-Seite öffnen Sie das Projektangebot und auf der **Zusammenfassung**-Registerkarte legen Sie einen gewünschten Liefertermin fest.
3. Öffnen Sie die Angebotsposition für Zeit und Material, für die Sie einen datumsbasierten Rechnungszeitplan erstellen möchten. 
4. Auf der **Rechnungszeitplan**-Registerkarte wählen Sie Werte in der **Abrechnungsstart** und **Rechnungsintervall**-Felder. 
5. Wählen Sie im Unterraster **Rechnungszeitplan erstellen** aus.
6. Die Anwendung generiert den Rechnungszeitplan, bei dem die Felder **Rechnungsdurchlaufdatum**, **Transaktionsabschnittsdatum** und **Ausführungsstatus** wie folgt eingestellt sind:

    - **Rechnungsdurchlaufdatum** wird auf das Datum eingestellt, das basierend auf dem Rechnungsintervall diktiert wird.
    - **Transaktionsabschnittsdatum** wird auf den Tag vor dem **Rechnungsdurchlaufdatum** eingestellt.
    - **Ausführungsstatus** wird automatisch auf **Nichtausführen** festgelegt. Wenn der automatische Rechnungserstellungsauftrag für ein bestimmtes Rechnungsdurchlaufdatum ausgeführt wird, wird dieses Feld entweder auf **Ausführen erfolgreich** oder **Ausführen fehlgeschlagen** aktualisiert.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Erstellen eines Zeitplans für Festpreisrechnungen für eine projektbasierte Angebotsposition

Wenn die projektbasierte Angebotsposition eine **Feste** Abrechnungsmethode hat, erstellt das System einen auf Meilensteinen basierenden Rechnungszeitplan. Führen Sie die folgenden Schritte aus, um diesen Zeitplan automatisch für einen festen Satz von Meilensteinen zu generieren, die für den Kalenderzeitraum gleichmäßig verteilt sind.

1. Wechseln Sie zu **Einstellungen** > **Rechnungsintervalle** und richten Sie einen Rechnungsintervall ein.
2. Auf der **Angebote**-Seite öffnen Sie das Projektangebot und auf der **Zusammenfassung**-Registerkarte legen Sie einen gewünschten Liefertermin fest.
3. Öffnen Sie die Angebotsposition zum Festpreis, für die Sie einen Meilensteinplan erstellen müssen. 
4. Auf der **Rechnungszeitplan**-Registerkarte wählen Sie Werte in der **Abrechnungsstart** und **Rechnungsintervall**-Felder. 
5. Wählen Sie im Unterraster **Periodische Meilensteine generieren** aus.
6. Die Anwendung generiert den Rechnungszeitplan mit einem Meilensteinnamen, einem Datum und einem Betrag.

    - Der Meilensteinname wird auf das Datum eingestellt, das basierend auf dem Rechnungsintervall diktiert wird.
    - Das Meilensteindatum wird auf das Datum eingestellt, das basierend auf dem Rechnungsintervall diktiert wird.
    - Der Meilensteinbetrag wird berechnet, indem der Angebotsbetrag in der projektbasierten Angebotsposition durch die Anzahl der Meilensteine dividiert wird, die durch den Intervall und den Abrechnungsbeginn sowie die angeforderten Liefertermine vorgegeben sind.
    - Wenn die Angebotsposition auch einen geschätzten Steuerbetrag aufweist, wird dieser Wert bei der Erstellung periodischer Meilensteine gleichmäßig auf die einzelnen Meilensteine aufgeteilt.

### <a name="manually-create-milestones"></a>Meilensteine manuell erstellen

Festpreismeilensteine können auch manuell generiert werden, wenn sie nicht regelmäßig aufgeteilt werden. So erstellen Sie Meilensteine manuell:

Öffnen Sie die Festpreisangebotsposition, für die Sie einen Meilenstein erstellen müssen. Wählen Sie auf der **Rechnungszeitplan**-Registerkarte im Unterraster **+ Neuen Meilenstein für die Angebotszeile erstellen** und geben Sie die erforderlichen Informationen anhand der folgenden Tabelle ein.

| **Feld** | **Ort** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- | --- |
| Meilensteinname | Schnellerfassung | Der Namen des Meilensteins. | Dies wird auf den Meilenstein der Projektvertragszeile und auf die Rechnung übertragen |
| Projektaufgabe | Schnellerfassung | Wenn der Meilenstein an die Projektaufgabe gebunden ist, können Sie diese Referenz verwenden, um eine benutzerdefinierte Logik hinzuzufügen, die den Meilensteinstatus basierend auf dem Aufgabenstatus festlegt. | Die Anwendung hat keine nachgelagerten Auswirkungen dieser Referenz auf eine Aufgabe. |
| Meilensteindatum | Schnellerfassung | Legen Sie das Datum fest, an dem der automatische Rechnungserstellungsprozess nach dem Status dieses Meilensteins suchen soll, um ihn für die Rechnungsstellung zu berücksichtigen. | Dies wird auf den Meilenstein der Projektvertragszeile und auf die Rechnung übertragen. |
| Rechnungsstatus | Schnellerfassung | Wenn ein Meilenstein erstellt wird, wird dieser Status immer auf **Nicht bereit für die Rechnungsstellung** festgelegt. | Dies wird auf den Meilenstein der Projektvertragszeile und auf die Rechnung übertragen. |
| Zeilenbetrag | Schnellerfassung | Betrag oder Wert des Meilensteins, der dem Kunden in Rechnung gestellt wird. | Dies wird auf den Meilenstein der Projektvertragszeile und auf die Rechnung übertragen. |
| Steuer | Schnellerfassung | Steuerbetrag, der auf den Meilenstein angewendet wird. | Dies wird auf den Meilenstein der Projektvertragszeile und auf die Rechnung übertragen. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]