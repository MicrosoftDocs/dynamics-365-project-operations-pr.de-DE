---
title: Richten Sie die Währungsumrechnung ein, um Verkaufspreise aus Kostensätzen zu berechnen
description: In diesem Artikel wird erläutert, wie das Währungsumrechnungsverhalten konfiguriert wird, das in Microsoft Dynamics 365 Project Operations verwendet wird, wenn Verkaufstransaktionen aus Kostentransaktionen generiert werden.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816666"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Richten Sie die Währungsumrechnung ein, um Verkaufspreise aus Kostensätzen zu berechnen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

In Microsoft Dynamics 365 Project Operations können Verkaufspreise für Ausgabenkategorien als numerische Werte eingerichtet werden, oder sie können so eingerichtet werden, dass sie basierend auf den angefallenen Kosten berechnet werden.

Wenn sie so eingerichtet sind, dass sie basierend auf den angefallenen Kosten berechnet werden, sind die folgenden Optionen verfügbar:

- Zum Einstandswert
- Markieren Sie den Prozentsatz über den Kosten

In Szenarien, in denen die Aufwandskosten in einer Währung anfallen, die sich von der Verkaufswährung für den Projektvertrag unterscheidet, ist eine Währungsumrechnung erforderlich, um den Verkaufspreis basierend auf den Kosten zu berechnen.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Währungsumrechnungsverhalten, das native Dataverse Wechselkurse verwendet

Standardmäßig verwendet Project Operations die Wechselkurse, die in der Währungstabelle in Dataverse gespeichert sind. Führen Sie die folgenden Schritte aus, um Project Operations so zu konfigurieren, dass native Wechselkurse zur Berechnung der Verkaufspreise aus den Kosten verwendet werden.

1. Gehen Sie zu **Project Operations \> Einstellungen \> Parameter**.
1. Öffnen Sie die Detailseite **Projektparameter**.
1. Setzen Sie das Feld **Währungsumrechnungslogik** auf einen leeren Wert.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Währungsumrechnungsverhalten, das Wechselkurse aus Finanz- und Betriebs-Apps verwendet

Die Wechselkurse in der Währungstabelle, die nativ verfügbar ist in Dataverse , sind nicht gültig. Daher sind sie möglicherweise nicht immer auf die Anforderungen skaliert, die Sie für die Berechnung von Verkaufspreisen aus Einstandssätzen haben.

Sie können Wechselkurse aus der Finanz- und Betriebsumgebung verwenden, um den Verkaufspreis in der Verkaufswährung aus einem Einstandssatz in der Einstandswährung zu berechnen. Gehen Sie folgendermaßen vor, um dieses Währungsumrechnungsverhalten zu konfigurieren.

1. Fügen Sie auf der Seite **Projektparameter** das Feld **Währungsumrechnungslogik** hinzu. Speichern und veröffentlichen Sie dann die Anpassung.
1. Gehen Sie zu **Project Operations \> Einstellungen \> Parameter**.
1. Öffnen Sie die Detailseite **Projektparameter**. 
1. Setzen Sie das Feld **Währungsumrechnungsverhalten** auf **Erweitert mit Fallback auf Standard**.
1. Erteilen Sie dem **Dual-Write-App-Benutzer** Sicherheitsrolle **Global Read** die Berechtigung für die folgenden Tabellen:

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. Führen Sie in Ihrer Finanz- und Betriebsumgebung die folgenden Dual-Write-Maps mit anfänglicher Synchronisierung aus:

    - Wechselkurstyp (msdyn\_exchangeratetypes)
    - Währungspaar für Wechselkurs (msdyn\_currencyexchangeratepairs)
    - CDS Wechselkurse (msdyn\_currencyexchangerates)

Nachdem diese Änderungen abgeschlossen sind, stellt Dual-Write die Wechselkurse aus der Finanz- und Betriebsumgebung in Dataverse zur Verfügung. Project Operations verwendet dann diese Wechselkurse, um die Kostensätze in die Verkaufswährung des Vertrags umzurechnen.

> [!NOTE]
> Dieses Währungsumrechnungsverhalten gilt nur für die Berechnung von Verkaufspreisen aus Kostensätzen. Es wird nicht zur allgemeinen Berechnung von Basiswährungswerten verwendet. Basiswährungswerte verwenden immer native Dataverse Wechselkurse, unabhängig davon, ob Sie dieses Verfahren durchführen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
