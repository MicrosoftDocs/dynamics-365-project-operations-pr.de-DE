---
title: Preislisten einrichten
description: Dieses Thema bietet Informationen zum Einrichten von Kosten- und Verkaufspreislisten.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 227e9a6f0ce6fd3fa1c2b0bd9afa014a3ec4f9758ead0dfb408156535692575c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009485"
---
# <a name="set-up-price-lists"></a>Preislisten einrichten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

In Dynamics 365 Project Operations stellen Preislisten einen Katalog von Preisen dar. Die Preise drücken Kosten-, Umsatz- und Rechnungssätze aus. Abhängig davon, ob die Preisliste Kostensätze oder Verkaufs- und Rechnungssätze ausdrückt, lautet der Kontext der Preisliste **Umsatz** oder **Kosten**.

Die folgenden Erweiterungen gelten speziell für Project Operations und werden auf Preislisten von Dynamics 365 Sales angewendet.

- **Kontext**: Dieses Feld enthält die unterstützten Werte **Kosten** und **Umsatz**. Der Wert **Kauf** wird nicht unterstützt. Legen Sie den Kontext auf **Kosten** fest, um eine Einstandspreisliste zu erstellen, oder den Kontext für eine Verkaufspreisliste auf **Verkauf** festzulegen. Einstandspreislisten lösen Sie den Preis für die Kostenart anhand von Kostenvoranschlägen und Datensätze für Istwerte auf. Verkaufspreislisten lösen den Preis für Datensätze zu Kostenvoranschlägen und Istwerten von nicht fakturierte und fakturierten Umsatztypen auf.
- **Zeiteinheit**: Dies ist die Standardzeiteinheit, für die der Preis in der entsprechenden Tabelle **Rollenpreis** für diese Preisliste eingerichtet ist.
- **Preislistenentität**: Dieses ausgeblendete Feld wird von Project Operations verwendet, um Preislisten, die angebots- oder vertragsspezifisch sind, von Standardlisten zu unterscheiden, die standardmäßig und global anwendbar sind.

## <a name="price-list-header"></a>Preislisten-Header

Die folgende Tabelle enthält die Felder auf der Registerkarte **Allgemein** einer Preisliste, die nur für Project Operations gilt oder wesentliche Verhaltensänderungen gegenüber Preislisten im Vertrieb aufweist.

| Feld | Position | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| Name des Dataflows | Die Registerkarte **Allgemein** und **Schnellerfassungs**-Formulare | Die Identität der Preisliste. | Die Preisliste wird mit diesem Wert auf allen Listenseiten und Dropdownoptionen angezeigt.|
| Kontext | Die Registerkarte **Allgemein** und **Schnellerfassungs**-Formulare | Dieses Feld kann auf **Kosten** oder **Verkauf** festgelegt sein. | Eine Preisliste, die auf **Kosten** festgelegt ist, wird verwendet, um den Preis für Kostenvoranschläge und tatsächliche Kosten zu suchen. Eine Preisliste, die auf **Verkauf** festgelegt ist, wird verwendet, um den Preis für Verkaufskostenvoranschläge und tatsächliche Umsatz-Istwerte zu suchen. Nur Preislisten, für die der Kontext auf **Umsatz** festgelegt ist, können an eine Projektpreisliste für Kunden, Projektangebote und Projektverträge angehängt werden. |
| Startdatum | Die Registerkarte **Allgemein** und **Schnellerfassungs**-Formulare | Das Startdatum des Zeitraums, in dem sich die Preisliste befindet, ist wirksam. | Zusammen mit dem Feld **Enddatum** wird dieses Feld verwendet, um festzulegen, welche Preisliste für einen bestimmten Kostenvoranschlag oder eine tatsächliche Zeile gilt. |
| Enddatum | Die Registerkarte **Allgemein** und **Schnellerfassungs**-Formulare | Das Enddatum des Zeitraums, in dem sich die Preisliste befindet, ist wirksam. | Zusammen mit dem Feld **Startdatum** wird dieses Feld verwendet, um festzulegen, welche Preisliste für einen bestimmten Kostenvoranschlag oder eine tatsächliche Zeile gilt. |
| Währung | Die Registerkarte **Allgemein** und **Schnellerfassungs**-Formulare | In diesem Feld wird die Währung für jede Rollen-, Kategorie- oder Preislisten-Artikelzeile festgelegt, die sich auf diese Preisliste bezieht. | In den Preislisten **Verkauf** können Zeilen für Preislisten, Rollen, Kategorien oder Preislistenelemente nicht in einer anderen Währung als in dieser Währung erstellt werden. In den Preislisten **Kosten** können Sie eine Rollenpreislinie in jeder Währung erstellen. Die hier definierte Währung wird standardmäßig verwendet. Das Benutzer-Setup, das sich auf die Rollenpreise bezieht, kann diesen Wert überschreiben, um das Einrichten des Arbeitskostensatzes in jeder Währung zu ermöglichen. Kategoriekostensätze und Preislistenelementkosten können nur in der hier definierten Währung eingerichtet werden. |
| Zeiteinheit | Die Registerkarte **Allgemein** und **Schnellerfassungs**-Formulare | In diesem Feld wird die Zeiteinheit für jede Rollenzeile verwendet, die sich auf diese Preisliste bezieht. | Dieser Feldwert wird nur für die Einrichtung des zugehörigen Rollenpreises verwendet. In den Preislisten **Kosten** und **Verkauf** können Sie eine Rollenpreiszeile in jeder Zeiteinheit erstellen. Die hier definierte Zeiteinheit wird standardmäßig verwendet. Das Benutzer-Setup, das sich auf die Rollenpreise bezieht, kann diesen Wert überschreiben, um das Einrichten des Arbeitskosten- und Abrechnungssatzes in jeder Zeiteinheit zu ermöglichen. |
| Beschreibung des Dataflows | Die Registerkarte **Allgemein** und **Schnellerfassungs**-Formulare | In diesem Textfeld können Sie eine mehrzeilige Beschreibung der Preisliste bereitstellen. | Dieses Feld wird in den Ansichten **Zugeordnet** in der Preisliste in verschiedenen Entitäten angezeigt, die zugehörige Preislisten haben. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]