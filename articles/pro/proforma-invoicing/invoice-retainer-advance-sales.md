---
title: Eine Vorauszahlung oder einen Vorschuss abrechnen
description: Dieses Thema enthält Informationen zum Fakturieren einer Vorauszahlung oder eines Vorschusses in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ed3b71d5f0ac035403de9fa213f3f45d14038e0
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087919"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Eine Vorauszahlung oder einen Vorschuss abrechnen

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dynamics 365 Project Operations unterstützt auf Vorauszahlungen basierende Verträge und einmalige Vorschüsse. In einem Projektvertrag können Sie einen Zeitplan für Vorauszahlungen oder einen einmaligen Vorschuss aufzeichnen. Durch die Aufzeichnung auf Projektvertragsebene wird jedoch nicht sofort eine Vorauszahlung oder Vorschuss zur Verwendung verfügbar. Um eine Vorauszahlung oder einen Vorschuss auf einer Rechnung zu verwenden, der den Kunden tatsächlich belastet, muss die Vorauszahlung oder der Vorschuss zuerst in Rechnung gestellt werden.

Führen Sie die folgenden Schritte aus, um eine Vorauszahlung oder einen Vorschuss zu fakturieren.

1. Wählen Sie **Vertrieb** > **Abrechnung** > **Vorauszahlungen und Vorschüsse** aus. 
2. Verwenden Sie auf der Registerkarte **Vorauszahlungen und Vorschüsse** den Filter, um die bestimmte Vorauszahlung oder den Vorschuss auszuwählen, der fakturiert werden soll, und markieren Sie in als **Bereit für die Rechnungsstellung**.
3. Erstellen Sie eine Rechnung manuell entweder über die Liste **Projektvertrag** oder über die Detailseite. Die Vorauszahlung oder der Vorschuss wird auf dem Rechnungsentwurf im Abschnitt **Vorschüsse und Vorauszahlungen** auf der Seite **Rechnung** angezeigt.
4. Bestätigen Sie die Rechnung. Dadurch wird die Vorauszahlung oder der Vorschuss zur Verwendung verfügbar. Sie können die Rechnung auf der Listenseite **Vorauszahlungen und Vorschüsse** überprüfen. Für einen in Rechnung gestellten Vorschuss oder eine Vorauszahlung wird der verfügbare Betrag im Raster angezeigt.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Eine Vorauszahlung oder einen Vorschuss über das Rechnungsraster erstellen

Sie können eine Vorauszahlung oder einen Vorschuss direkt auf einer Rechnung erstellen.

1. Wählen Sie auf einem Rechnungsentwurf im Unterraster **Vorauszahlungen und Vorschüsse** die Option **Neu** aus, um eine neue Vorauszahlung oder einen Vorschuss zu erstellen. 
2. Fügen Sie auf der Seite **Schnellerfassung** die erforderlichen Informationen hinzu, und wählen Sie dann **Speichern** aus. Die Vorauszahlung oder der Vorschuss wird in dem mit der Rechnung verbundenen Projektvertrag erstellt. Die Vorauszahlung oder der Vorschuss wird automatisch als **Bereit für die Rechnungsstellung** markiert und dann dem Unterraster **Vorauszahlungen und Vorschüsse** auf der Seite **Rechnung** hinzugefügt.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Eine Vorauszahlung oder einen Vorschuss abgleichen

Nachdem eine Vorauszahlung oder ein Vorschuss in Rechnung gestellt wurde, können diese auf einer Rechnung mit Zeit, Kosten, Meilensteinen oder anderen projektbezogenen Kosten verwendet oder abgeglichen werden. Dem Kunden wird der Rechnungsbetrag um den auf dieser Rechnung verwendeten Vorauszahlungs- oder Vorschussbetrag reduziert.

Auf jeder Rechnung, die für einen Projektvertrag generiert wurde, und die Vorauszahlungen oder Vorschüsse enthält, wendet Project Operations automatisch die Vorauszahlung oder den Vorschuss auf die Rechnung an.

Dies ist im Raster **Angewendete Vorauszahlungen und Vorschüsse** auf der Seite **Rechnung**. Die folgende Tabelle enthält Informationen zu den Feldern im Raster **Angewendete Vorauszahlungen und Vorschüsse** der Seite **Projektrechnung**.

| Feld | Position | Relevanz, Zweck und Anleitung | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| Beschreibung des Dataflows | Das Raster **Angewendete Vorauszahlungen und Vorschüsse** auf der Seite **Projektrechnung** |Dieses schreibgeschützte Feld enthält eine Beschreibung der auf dieser Rechnung verwendeten Vorauszahlung oder des Vorschusses. Dieser Wert kann auf der Rechnung nicht geändert werden. Dieser Wert kann im Unterraster auf der Seite **Projektvertrag** aktualisiert werden. | Dieses Feld kann dem Kunden auf der gedruckten Rechnung angezeigt werden, um anzugeben, welche Vorauszahlung bzw. welcher Vorschuss auf der Rechnung angewendet wird. |
| Geliefert am | Das Raster **Angewendete Vorauszahlungen und Vorschüsse** auf der Seite **Projektrechnung**  | Dieses schreibgeschützte Feld enthält das Rechnungsdatum der auf dieser Rechnung verwendeten Vorauszahlung oder des Vorschusses. Dieser Wert kann auf der Rechnung nicht geändert werden. Dieser Wert kann im Unterraster auf der Seite **Projektvertrag** aktualisiert werden. | Dieses Feld kann dem Kunden auf der gedruckten Rechnung angezeigt werden, um das Datum anzugeben, an dem die Vorauszahlung oder der Vorschuss dem Kunden zuerst in Rechnung gestellt wurde. |
| Betrag | Das Raster **Angewendete Vorauszahlungen und Vorschüsse** auf der Seite **Projektrechnung**  | Dieses schreibgeschützte Feld enthält den Betrag der auf dieser Rechnung verwendeten Vorauszahlung oder des Vorschusses. Dieser Wert kann auf der Rechnung nicht geändert werden. Dieser Wert kann im Unterraster auf der Seite **Projektvertrag** aktualisiert werden. | Dieses Feld kann dem Kunden auf der gedruckten Rechnung angezeigt werden, um den ursprünglichen Betrag der Vorauszahlung oder des Vorschusses anzugeben, der vom Kunden gezahlt wurde. |
| Verwendeter Betrag | Das Raster **Angewendete Vorauszahlungen und Vorschüsse** auf der Seite **Projektrechnung**  | Dieses schreibgeschützte Feld enthält den berechneten Wert, der zusammenfasst, wie viel der Vorauszahlung oder des Vorschusses verwendet wurde. | Dieses Feld kann dem Kunden auf der gedruckten Rechnung angezeigt werden, um den Betrag dieser Vorauszahlung oder des Vorschusses anzugeben, der bereits verwendet wurde. |
| Erweiterter Betrag | Das Raster **Angewendete Vorauszahlungen und Vorschüsse** auf der Seite **Projektrechnung**  | Dieses bearbeitbare Feld enthält den Betrag der auf dieser Projektrechnung verwendeten Vorauszahlung oder des Vorschusses. Dieser Betrag kann nicht höher sein als der im Vorschuss verfügbare Betrag. Das System berechnet dies automatisch als Differenz zwischen den Feldern **Menge** und **Verwendeter Betrag** im Raster. Sie können diesen Betrag verringern, um weniger zu verwenden als verfügbar ist, aber Sie können den Betrag nicht erhöhen, um mehr zu verwenden als verfügbar ist. | Dieses Feld kann dem Kunden auf der gedruckten Rechnung angezeigt werden, um den Betrag dieser Vorauszahlung oder des Vorschusses anzugeben, der in der Rechnung verwendet wurde. |
| Saldovorschussbetrag | Das Raster **Angewendete Vorauszahlungen und Vorschüsse** auf der Seite **Projektrechnung**  | Dieses schreibgeschützte Feld gibt den Wert an, der aussagt, wie viel von der Vorauszahlung oder des Vorschusses nach dem Bestätigen der Rechnung übrig bleibt. | Dieses Feld kann dem Kunden auf der gedruckten Rechnung angezeigt werden, um den Betrag anzugeben, der aus dieser Vorauszahlung oder aus diesem Vorschuss noch übrig bleibt, nachdem die Rechnung bestätigt und bezahlt wurde. |
