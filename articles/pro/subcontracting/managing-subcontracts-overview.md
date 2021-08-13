---
title: Fremdarbeitsmanagement in Project Operations
description: Dieses Thema bietet einen Überblick über den End-to-End-Fremdarbeitsverwaltungsprozess in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994230"
---
# <a name="subcontract-management-in-project-operations"></a>Fremdarbeitsmanagement in Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Fremdarbeitsauftragsvergabe bei Microsoft Dynamics 365 Project Operations unterstützt die folgenden Geschäftsprozessflows.

![Fremdarbeitsvergabeprozess-Flow](../media/SubcontractingProcessFlow.png)

Hier ist eine Schritt-für-Schritt-Beschreibung des Fremdarbeitsvergabeprozesses.

1. Der Projektmanager legt einen Fremdarbeitsvertrag mit einem Kreditor an. Standardmäßig werden die an den Kreditorendatensatz angehängten Preislisten für den Fremdarbeitsvertrag verwendet. Das Kreditorenkonten hat den Beziehungstyp **Kreditor** oder **Lieferant**.
2. Der Projektmanager kann alle Käufe als Positionen auf dem Fremdarbeitsvertrag auflisten. Fremdarbeitspositionen können Zeit, Ausgaben oder Produkte umfassen. Die Transaktionsklasse, die in jeder Fremdarbeitsposition ausgewählt wird, bestimmt, wofür die Position verwendet wird.
3. Der Konto-Manager des Zulieferers und der Projektmanager können den Fremdarbeitsvertrag durchlaufen. Die Preise können in den Einkaufspreislisten angepasst werden, die dem Fremdarbeitsvertrag angefügt sind.
4. An diesem Punkt oder später im Prozess ordnet der Konto-Manager des Zulieferers jeder Fremdarbeitsposition Kontakte zu, wenn die Fremdarbeitsposition zeitlich begrenzt ist. Diese Assoziation stellt dem Projektmanager, der an dem Fremdarbeitsvertrag arbeitet, Informationen zur Verfügung. Wenn ein Kontakt mit einer Fremdarbeitsposition verknüpft ist, erstellt das System automatisch eine buchbare Ressource aus dem Kontakt, falls noch keine buchbare Ressource vorhanden ist.
5. Die Fakturierungsmethode für jede Fremdarbeitsposition kann **Festpreis** oder **Zeit und Material** sein. Für Fremdarbeitspositionen mit Festpreisen können Sie einen meilensteinbasierten Rechnungsplan einrichten.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
