---
title: Nicht lagerhaltiges Material für ein Projekt über Projektbestellungen bestellen
description: In diesem Thema wird erklärt, wie Sie nicht lagerhaltiges Material für ein Projekt über Projektbestellungen bestellen.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563021"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Nicht lagerhaltiges Material für ein Projekt über Projektbestellungen bestellen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Die Beschaffungsabteilung in Ihrer Organisation verwendet möglicherweise [Bestellungen](/dynamics365/supply-chain/procurement/purchase-order-overview), um Waren- und Dienstleistungsaufträge zu verfolgen. Bestellungen für Nichtlagermaterialien können einem Projekt zugeordnet werden. Bei der Fakturierung dieser Bestellungen werden die Kosten für das Projekt erfasst.

## <a name="prerequisites"></a>Voraussetzungen
Führen Sie die folgenden Schritte aus, um die Funktion für Projektbestellungen zu aktivieren.

1. Navigieren Sie in Dynamics 365 Finance zum Arbeitsbereich **Funktionsverwaltung**.
2. Suchen Sie in der Funktionsliste die Funktion, und wählen Sie sie aus, **Projektbestellungen in Project Operations für ressourcenbasierte/nicht vorrätige Szenarien aktivieren**.
3. Wählen Sie **Aktivieren** aus.
4. Konfigurieren Sie nicht gelagerte Materialien und ausstehende Lieferantenrechnungen wie in [Nicht vorrätige Materialien und ausstehende Lieferantenrechnungen konfigurieren](configure-materials-nonstocked.md) beschrieben.

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Eine Projektbestellung aus der Projektbestellliste erstellen

1. Gehen Sie in Finance zu **Projektmanagement und Buchhaltung** > **Projekte** > **Alle Projekte** und wählen Sie ein Projekt aus.
2. Wählen Sie im Aktionsbereich auf der Registerkarte **Verwalten** in der Gruppe **Neu** die Option **Artikelaufgabe** > **Bestellung** aus.
3. Wählen Sie auf der Seite **Bestellung erstellen** den Lieferanten aus, bei dem Sie die Bestellung aufgeben möchten, geben Sie ggf. weitere Informationen ein und wählen Sie dann **OK**.
4. Wählen Sie auf der Seite **Bestellung** im Raster **Bestellpositionen** die Option **Position hinzufügen** aus.
5. Geben Sie nach Bedarf Artikelnummer, Menge, Einheit, Einheitspreis und andere Informationen ein.

    > [!NOTE]
    > Bei Projektbestellungen können nur nicht vorrätige Artikel und Dienstleistungen verwendet werden. Lagerartikel und Beschaffungskategorien werden nicht unterstützt.

6. Fügen Sie nach Bedarf weitere Artikel hinzu und bestätigen Sie die Bestellung.

    Wareneingangs- und Serviceerbringungseingänge können durch Anlegen und Buchen eines Produktzugangs erfasst werden.

    > [!NOTE]
    > Produkteingänge werden nicht in den Projekt-Istwerten in Microsoft Dataverse erfasst und wirken sich nicht auf das Nebenbuch des Projekts aus.

    Nachdem ein Lieferant die Rechnung für Artikel und Dienstleistungen in der Bestellung gesendet hat, kann die Beschaffungsabteilung eine Rechnung für die Bestellung erstellen, indem Sie auf **Rechnung** > **Generieren** > **Rechnung** im Aktionsbereich gehen. Weitere Informationen zu ausstehenden Kreditorenrechnungen finden Sie unter [Kaufen Sie nicht vorrätige Materialien mit einer ausstehenden Lieferantenrechnung](pending-vendor-invoices.md).
