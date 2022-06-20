---
title: Nicht lagerhaltiges Material für ein Projekt über Projektbestellungen bestellen
description: Dieser Artikel erklärt, wie Sie nicht vorrätige Materialien für ein Projekt mit Hilfe von Projektkäufen bestellen können.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929811"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Beschaffungskategorien oder nicht lagerhaltiges Material für ein Projekt über Projektbestellungen bestellen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Die Beschaffungsabteilung in Ihrer Organisation verwendet möglicherweise [Bestellungen](/dynamics365/supply-chain/procurement/purchase-order-overview), um Waren- und Dienstleistungsaufträge zu verfolgen. Bestellungen für Beschaffungskategorien oder nicht lagerhaltiges Material kann einem Projekt zugewiesen werden. Bei der Fakturierung dieser Bestellungen werden die Kosten für das Projekt erfasst.

## <a name="prerequisites"></a>Voraussetzungen
Führen Sie die folgenden Schritte aus, um die Funktion für Projektbestellungen zu aktivieren.

1. Wechseln Sie in Dynamics 365 Finance zum Arbeitsberiech **Funktionsverwaltung**.
2. Suchen Sie in der Funktionsliste die Funktion, und wählen Sie sie aus, **Projektbestellungen in Project Operations für ressourcenbasierte/nicht vorrätige Szenarien aktivieren**.
3. Wählen Sie **Aktivieren** aus.
4. Konfigurieren Sie nicht gelagerte Materialien und ausstehende Lieferantenrechnungen wie in [Nicht vorrätige Materialien und ausstehende Lieferantenrechnungen konfigurieren](configure-materials-nonstocked.md) beschrieben.
5. Konfigurieren Sie Beschaffungskategorien wie in [Beschaffungskategorien mit Projektbestellungen und ausstehenden Lieferantenrechnungen verwendet](configure-procurement-categories.md) beschrieben.

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Eine Projektbestellung aus der Projektbestellliste erstellen

1. Gehen Sie in Finance zu **Projektmanagement und Buchhaltung** > **Projekte** > **Alle Projekte** und wählen Sie ein Projekt aus.
2. Wählen Sie im Aktionsbereich auf der Registerkarte **Verwalten** in der Gruppe **Neu** die Option **Artikelaufgabe** > **Bestellung** aus.
3. Wählen Sie auf der Seite **Bestellung erstellen** den Lieferanten aus, bei dem Sie die Bestellung aufgeben möchten, geben Sie ggf. weitere Informationen ein und wählen Sie dann **OK**.
4. Wählen Sie auf der Seite **Bestellung** im Raster **Bestellpositionen** die Option **Position hinzufügen** aus.
5. Geben Sie nach Bedarf Artikelnummer oder Beschaffungskategorie, Menge, Einheit, Einheitspreis und andere Informationen ein.

    > [!NOTE]
    > Bei Beschaffungskategorien können nur nicht vorrätige Artikel und Dienstleistungen verwendet werden. Lagerartikel werden nicht unterstützt.

6. Fügen Sie nach Bedarf weitere Artikel oder Beschaffungskategorien hinzu und bestätigen Sie die Bestellung.

    Wareneingangs- und Serviceerbringungseingänge können durch Anlegen und Buchen eines Produktzugangs erfasst werden.

    > [!NOTE]
    > Produkteingänge werden nicht in den Projekt-Istwerten in Microsoft Dataverse erfasst und wirken sich nicht auf das Nebenbuch des Projekts aus.

    Nachdem ein Lieferant die Rechnung für Artikel und Dienstleistungen in der Bestellung gesendet hat, kann die Beschaffungsabteilung eine Rechnung für die Bestellung erstellen, indem Sie auf **Rechnung** > **Generieren** > **Rechnung** im Aktionsbereich gehen. Weitere Informationen zu ausstehenden Kreditorenrechnungen finden Sie unter [Kaufen Sie nicht vorrätige Materialien mit einer ausstehenden Lieferantenrechnung](pending-vendor-invoices.md).
