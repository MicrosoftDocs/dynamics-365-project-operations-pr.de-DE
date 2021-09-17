---
title: Fremdarbeit in der Vorabzugangsversion für Oktober 2021
description: Dieses Thema bietet einen Überblick über die Fremdarbeitsfunktionen in Project Operations, die Teil der Vorabzugangsversion vom Oktober 2021 sind.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383694"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Fremdarbeit in der Vorabzugangsversion für Oktober 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieses Thema bietet einen Überblick über die Fremdarbeitsfunktionen in Dynamics 365 Project Operations, die Teil der Vorabzugangsversion vom Oktober 2021 sind. Dieser Funktionssatz ist noch nicht für Produktions- oder Live-Umgebungen bereit, daher bleiben diese Funktionen in der Vorabzugangsversion, bis das vollständige Feature-Set veröffentlicht wird. Es wird dringend empfohlen, den Funktionssatz für die Fremdarbeit nicht für Live-Produktionsszenarien zu verwenden, bis das Vorschaubanner entfernt wurde. 

Die folgende Liste bietet einen Überblick darüber, was derzeit in der Vorabzugangsversion vom Oktober 2021 verfügbar ist:

1. Der Projektmanager legt einen Fremdarbeitsvertrag mit einem Kreditor an. Standardmäßig werden die an den Kreditorendatensatz angehängten Preislisten für den Fremdarbeitsvertrag verwendet. Das Kreditorenkonten hat den Beziehungstyp **Kreditor** oder **Lieferant**.

2. Der Projektmanager kann alle Käufe als Positionen auf dem Fremdarbeitsvertrag auflisten. Fremdarbeitspositionen können Zeit, Ausgaben oder Produkte umfassen. Die Transaktionsklasse der Fremdarbeitsposition bestimmt, wofür die Position verwendet wird.

3. Der Konto-Manager des Zulieferers und der Projektmanager können den Fremdarbeitsvertrag durchlaufen. Die Preise können in den Einkaufspreislisten angepasst werden, die dem Fremdarbeitsvertrag angefügt sind.

4. An diesem Punkt oder später im Prozess ordnet der Konto-Manager des Zulieferers jeder Fremdarbeitsposition Lieferantenkontakte zu, wenn die Fremdarbeitsposition zeitlich begrenzt ist. Diese Assoziation stellt dem Projektmanager, der an dem Fremdarbeitsvertrag arbeitet, Informationen zur Verfügung. Wenn ein Lieferantenkontakt mit einer Fremdarbeitsposition verknüpft ist, erstellt das System automatisch eine buchbare Ressource aus dem Kontakt, falls noch keine buchbare Ressource vorhanden ist.

5. Die Fakturierungsmethode für jede Fremdarbeitsposition kann **Festpreis** oder **Zeit und Material** sein. Für Fremdarbeitspositionen mit Festpreisen wird ein meilensteinbasierter Rechnungsplan eingerichtet.

Die verbleibenden Schritte im Geschäftsprozessfluss für die Fremdarbeitsvergabe, die in der Übersicht beschrieben sind, sind derzeit nicht verfügbar. Wenn neue Funktionen hinzugefügt werden, wird diese Thema aktualisiert. 

Die folgende Abbildung stellt die Vorabzugangsversion für die Vergabe von Fremdarbeit im Gegensatz zum End-to-End-Geschäftsprozess dar.

![Fremdarbeitsvergabeprozess-Flow](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Mengenbasierte und arbeitsbasierte Fremdarbeitspositionen in der Vorabzugangsversion
In der Vorabzugangsversion vom Oktober 2021 werden nur mengenbasierte Fremdarbeitspositionen unterstützt. Dies bedeutet, dass eine Fremdarbeitsposition verwendet werden kann, um Zeit, Ausgaben oder Materialien von einem Lieferanten zu kaufen, aber nicht eine ganze Arbeitsmenge. Dies bedeutet auch, dass die eingekaufte Menge (Zeiteinheiten, Ausgaben oder Materialmenge) auf einer Fremdarbeitsposition für jedes Projekt im System verwendet werden kann.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
