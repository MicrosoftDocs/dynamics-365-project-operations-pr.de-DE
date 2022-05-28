---
title: Bedingungen für die Einbehaltung von Kreditorenzahlungen erstellen und anwenden
description: Dieses Thema enthält Informationen zum Einrichten und Verwalten von Bedingungen für die Einbehaltung von Kreditorenzahlungen.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3961d18fcd53381ad43a1d3e598ac61652ba9843
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685101"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Bedingungen für die Einbehaltung von Kreditorenzahlungen erstellen und anwenden

[!include [banner](../includes/banner.md)] 

Das Einrichten von Bedingungen für die Einbehaltung von Kreditorenzahlungen für ein Projekt ist nützlich, wenn Ihre Organisation einen Teil der an einen Kreditor geleisteten Zahlungen einbehalten möchte. Wenn Sie die Zahlung an einen Kreditor beispielsweise so lange einbehalten möchten, bis die gelieferten Produkte, Ihren Erwartungen entsprechen. Bedingungen für die Einbehaltung von Kreditorenzahlungen können angegeben werden, wenn Sie einen Kreditorenvertrag aushandeln.

## <a name="create-vendor-payment-retention-terms"></a>Bedingungen für die Einbehaltung von Kreditorenzahlungen erstellen

Sie können den Prozentsatz der Kreditorenzahlung für die Einbehaltung und den Prozentsatz der zuvor einbehaltenden Beträge eingeben, die freigegeben werden sollen. Beträge werden automatisch auf Kreditorenrechnungen einbehalten, bis der Vertrag den angegebenen Fertigstellungsstatus erreicht. Nachdem Sie die Bedingungen für die Einbehaltung eingerichtet haben, können Sie sie auf jedes Projekt für diesen Kreditor anwenden.

Führen Sie die folgenden Schritte aus, um Bedingungen für die Einbehaltung von Kreditorenzahlungen einzurichten und zu verwalten. 

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Einbehaltung** > **Bedingungen für einbehaltene Kreditorenzahlungen**.
2. Wählen Sie **Neu** aus, um eine neue Bedingung für die Einbehaltung von Kreditorenzahlungen hinzuzufügen. Der Wert **Regel-ID** für die neue Bedingung wird automatisch eingegeben. 
3. Geben Sie eine kurze Beschreibung in das Feld **Beschreibung** ein, und wählen Sie im Inforegister **Bedingungen** die Option **Zeile hinzufügen** aus, um Werte für die Bedingung für folgende Optionen einzugeben:

   - **Prozentsatz der gelieferten Einheiten**: Geben Sie einen Prozentsatz für die Fertigstellung für die Bedingung ein. Beträge werden automatisch auf Kreditorenrechnungen einbehalten, bis der Projektstatus des Abschlusses dem angegebenen Prozentsatz entspricht. Wenn Sie beispielsweise 50,00 eingeben, werden die Beträge einbehalten, bis das Projekt zu 50 Prozent abgeschlossen ist.
   - **Einzubehaltender Prozentsatz** : Geben Sie einen Prozentsatz des Kreditorenrechnungsbetrags ein, der einbehalten werden soll. Wenn Sie beispielsweise 10,00 eingeben, werden 10 Prozent des Betrags auf einer Kreditorenrechnung einbehalten, bis das Projekt den im Abschnitt festgelegten Prozentsatz des Abschlusses, wie in **Prozentsatz der gelieferten Einheiten** festgelegt, erreicht.
   - **Freizugebender Prozentsatz**: Wählen Sie **Zeile hinzufügen** aus, um einen Prozentsatz aller zuvor einbehaltenen Beträge einzugeben, die für die ausgewählte Stufe des Projektabschlusses freigegeben werden sollen.

> [!NOTE]
> Wenn Sie mehr als einen Meilenstein für verschiedene Stufen des Projektabschlusses haben, geben Sie für jede Einbehaltungsregel eine separate Zeile für die Bedingung zum Einbehalt der Kreditorenrechnung ein. Jede Zeile kann für jede festgelegte Projektabschlussstufe einen anderen Prozentsatz für die Einbehaltung und einen anderen Prozentsatz für die Freigabe angeben.

Nachdem Sie Bedingungen für die Einbehaltung von Kreditorenzahlungen für einen Kreditor eingegeben haben, können Sie die Bedingungen auf ein Projekt anwenden.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Bedingungen für die Einbehaltung von Kreditorenzahlungen auf ein Projekt anwenden

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Projekte** > **Alle Projekte**, und öffnen Sie ein Projekt aus der Projektlistenseite aus.
2. Wählen Sie im Inforegister **Kreditorenvereinbarungen** die Option **Zeile hinzufügen** aus.
3. Wählen Sie im Feld **Kontocode** eine der folgenden Optionen aus: 

   - **Tabelle**: Die Bedingungen für die Einbehaltung von Kreditorenzahlungen gelten für einen einzelnen Kreditor.
   - **Gruppe** : Die Bedingungen für die Einbehaltung von Kreditorenzahlungen gelten für alle Kreditoren in einer Kreditorengruppe.
   - **Alle**: Die Bedingungen für die Einbehaltung von Kreditorenzahlungen gelten für alle Kreditoren.

4. Wählen Sie im Feld **Kreditor/Kreditorengruppe** den Kreditor oder die Kreditorengruppe aus, für die die Bedingungen für die Einbehaltung von Kreditorenzahlungen gelten soll. Wenn Sie im vorherigen Schritt **Alle** ausgewählt haben, ist dieses Feld nicht verfügbar.
5. Wählen Sie im Feld **Bedingungen für einbehaltene Kreditorenbeträge** die Bedingungen für die Einbehaltung aus, die Sie im vorherigen Verfahren erstellt haben.
6. Wenn für das Projekt auch Bedingungen zur Zahlung bei Zahlungsempfang für den Kreditor eingerichtet wurden, geben Sie den Schwellenwertprozentsatz für das Projekt im Feld **Pay When Paid - Schwellenwertprozentsatz** ein.

Die Bedingungen für die Einbehaltung von Kreditorenzahlungen werden auch in Bestellungen angezeigt, die Sie für den Kreditor erstellen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]