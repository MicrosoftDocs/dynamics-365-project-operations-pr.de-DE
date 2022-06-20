---
title: Nicht vorrätige Materialien oder Beschaffungskategorien mithilfe einer ausstehender Kreditorenrechnung kaufen
description: Dieser Artikel erklärt, wie Sie ausstehende Lieferantenrechnungen erfassen.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921991"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Nicht vorrätige Materialien oder Beschaffungskategorien mithilfe einer ausstehender Kreditorenrechnung kaufen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Wenn ein Unternehmen nicht lagerhaltige Materialien oder Beschaffungskategorien für ein Projekt beschafft, können die Kosten sofort gegen das Projekt gebucht werden. 

Contoso Robotics US führt beispielsweise ein Projekt zur Geräteerneuerung durch und benötigt Softwarelizenzen. Diese Lizenzen werden von einem Drittanbieter bezogen.  Unter Verwendung von Dynamics 365 Finance erfasst der Kreditorenbuchhalter ein ausstehendes Kreditorenrechnungsdokument und ordnet die Lizenzkosten direkt dem Arbeitsgeräteerungsprojekt zu. 

> [!IMPORTANT]
> Bevor Sie die in diesem Artikel beschriebenen Funktionen nutzen, sollten Sie die erforderlichen Konfigurationen überprüfen und anwenden. Weitere Informationen finden Sie unter [Nicht vorrätige Materialien und ausstehende Kreditorenrechnungen aktivieren](configure-materials-nonstocked.md) und [Beschaffungskategorien mit Projektbestellungen und ausstehenden Kreditorenrechnungen verwenden](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Buchen Sie eine projektbezogene ausstehende Lieferantenrechnung 

Ausstehende Lieferantenrechnungen können auf der Seite **Ausstehende Lieferantenrechnungen** (**Kreditoren** > **Rechnungen** > **Ausstehende Lieferantenrechnungen**) erfasst werden. Führen Sie die folgenden Schritte aus, um eine projektbezogene ausstehende Lieferantenrechnung zu buchen:

1. Gehen Sie zu **Kreditoren** > **Rechnungen**, und wählen Sie **Neu**. 
1. Wählen Sie im Feld **Rechnungskonto** einen Anbieter aus, und geben Sie dann im Feld **Nummer** die Kreditorenrechnungsidentifikation ein.
1. Fügen Sie der Kreditorenrechnung eine Zeile hinzu und wählen Sie dann im Feld **Artikelnummer** den nicht auf Lager befindlichen Artikel aus, der beim Kreditor gekauft wurde. Wählen Sie alternativ im Feld **Beschaffungskategorie** die Beschaffungskategorie aus, die vom Kreditor gekauft wurde.   
1. Fügen Sie die gekaufte Menge hinzu. Das System füllt den Stückpreis basierend auf der Preiskonfiguration für nicht vorrätige Artikel aus. 
1. Überprüfen Sie den Gesamtbetrag und andere erforderliche Details in der Zeile.
1. Wählen Sie in den Zeilendetails auf der Registerkarte **Projekt** die ID des Projekts aus, in dem dieses Element aufgezeichnet wird.
1. Optional: Wählen Sie die Aktivitätsnummer aus und aktualisieren Sie die Projektkategorie und die Positionseigenschaft.
1. Ausstehende Kreditorenrechnung buchen Beim Buchen der Rechnung erfasst das System folgende Informationen:
    
    - Saldobetrag des Lieferanten.
    - Der Umsatzsteuerbetrag
    - Die Kosten für das Projekt werden auf dem Konto für die Beschaffungsintegration erfasst.
    - Die Projekt-Ist-Kosten-Transaktion in Dataverse.  Diese Transaktion wird mithilfe des  [Project Operations-Integrationsjournals](../project-accounting/project-operations-integration-journal.md) verarbeitet. Durch das Buchen dieses Journals wird der Betrag vom Beschaffungsintegrationskonto auf das Projektkostenkonto verschoben. 
    - Einkäufe, die dem Projektkunden nach der Zeit- und Materialabrechnungsmethode fakturiert werden. Zusätzlich werden noch nicht fakturierte Verkaufstransaktionen für die Einkäufe in Dataverse erstellt. Die Produktpreisliste in Dataverse wird für die Verkaufspreise und -beträge für den nicht fakturierten Verkaufsvorgang verwendet.
