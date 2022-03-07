---
title: Kaufen von nicht vorrätigen Materialien mithilfe einer ausstehenden Lieferantenrechnung
description: In diesem Thema wird erläutert, wie ausstehende Lieferantenrechnungen erfasst werden.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e95f7dabe597968707fdd2dead40bfb93d7f1f95
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547288"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Kaufen von nicht vorrätigen Materialien mithilfe einer ausstehenden Lieferantenrechnung

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Wenn ein Unternehmen nicht vorrätige Materialien für ein Projekt beschafft, können die Kosten sofort gegen das Projekt erfasst werden. 

Contoso Robotics US führt beispielsweise ein Projekt zur Geräteerneuerung durch und benötigt Softwarelizenzen. Diese Lizenzen werden von einem Drittanbieter bezogen.  Mithilfe von Dynamics 365 Finance zeichnet der Kreditorenbuchhalter einen ausstehenden Lieferantenrechnungsbeleg auf und ordnet die Lizenzkosten direkt dem Projekt zur Geräteerneuerung zu. 

> [!IMPORTANT]
> Bevor Sie die in diesem Thema beschriebenen Funktionen verwenden, überprüfen Sie die erforderlichen Konfigurationen und wenden Sie sie an. Weitere Informationen finden Sie unter [Aktivieren von nicht vorrätigen Materialien und ausstehenden Lieferantenrechnungen](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Buchen Sie eine projektbezogene ausstehende Lieferantenrechnung 

Ausstehende Lieferantenrechnungen können auf der Seite **Ausstehende Lieferantenrechnungen** (**Kreditoren** > **Rechnungen** > **Ausstehende Lieferantenrechnungen**) erfasst werden. Führen Sie die folgenden Schritte aus, um eine projektbezogene ausstehende Lieferantenrechnung zu buchen:

1. Gehen Sie zu **Kreditoren** > **Rechnungen** und wählen Sie **Neu**. 
2. Wählen Sie im Feld **Rechnungskonto** einen Lieferanten aus und geben Sie im Feld **Nummer** die Lieferantenrechnungskennung ein.
3. Fügen Sie der Lieferantenrechnung eine Zeile hinzu und wählen Sie im Feld **Artikelnummer** den nicht vorrätigen Artikel aus, den Sie beim Lieferanten gekauft haben. 

    > [!NOTE]
    > Lieferantenrechnungsposten, die auf einer Beschaffungskategorie basieren, können nicht für das Projekt erfasst werden. 
    
5. Fügen Sie die gekaufte Menge hinzu. Das System füllt den Stückpreis basierend auf der nicht vorrätigen Artikelpreiskonfiguration auf. 
6. Überprüfen Sie den Gesamtbetrag und andere erforderliche Details in der Zeile.
7. Wählen Sie in den Zeilendetails, auf der Registerkarte **Projekt** die ID des Projekts aus, in dem dieses Element aufgezeichnet werden soll.
8. Wählen Sie optional die Aktivitätsnummer aus und aktualisieren Sie die Projektkategorie und die Zeileneigenschaft.
9. Ausstehende Kreditorenrechnung buchen Wenn die Rechnung gebucht wird, zeichnet das System Folgendes auf:
    
    - Saldobetrag des Lieferanten.
    - Der Umsatzsteuerbetrag
    - Die Kosten für das Projekt werden auf dem Konto für die Beschaffungsintegration erfasst.
    - Die Projekt-Ist-Kosten-Transaktion in Dataverse.  Diese Transaktion wird mithilfe des  [Project Operations-Integrationsjournals](../project-accounting/project-operations-integration-journal.md) verarbeitet. Durch das Buchen dieses Journals wird der Betrag vom Beschaffungsintegrationskonto auf das Projektkostenkonto verschoben. 
    - Einkäufe, die dem Projektkunden nach der Zeit- und Materialabrechnungsmethode fakturiert werden. Zusätzlich werden noch nicht fakturierte Verkaufstransaktionen für die Einkäufe in Dataverse erstellt. Die Produktpreisliste in Dataverse wird für die Verkaufspreise und -beträge für den nicht fakturierten Verkaufsvorgang verwendet.
