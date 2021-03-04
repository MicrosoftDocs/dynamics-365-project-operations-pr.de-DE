---
title: Rechnungsverarbeitung, Vorschau
description: Dieses Thema bietet einen Prozessüberblick über die Rechnungsstellung in Project Operations für ressourcen-/nicht vorrätige Szenarien.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fbc1519b6cbcf231cfa89df8b7843d11a8904e49
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089241"
---
# <a name="invoicing-process-overview"></a>Rechnungsverarbeitung, Vorschau

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Project Operations für ressourcen-/nicht vorrätige Szenarien bietet umfassende Funktionen, die auf die Anforderungen des Projektmanagers und des Debitorenbuchhalters/Projektbuchhalters zugeschnitten sind. Für den Rechnungsstellungsprozess verwaltet der Projektmanager den Projektabrechnungsstau und der Debitorenbuchhalter/Projektbuchhalter erstellt einen konformen und genauen kundenorientierten Rechnungsbeleg.

![Rechnungsflussdiagramm](./media/invoicing-flow.png)

Die Projektvertragszeile definiert die Abrechnungsmethode für zugehörige Projekttransaktionen. Wenn der Projektmanager Zeit- und Kostentransaktionen genehmigt, zeichnet das System die Transaktionen in der Entität **Projekt-Istwerte** auf und sendet die Informationen an die Module **Projektmanagement und Buchhaltung** in Dynamics 365 Finance. Der Projektbuchhalter überprüft und veröffentlicht die Aufzeichnungen dann mit dem [Project Operations Integration-Journal](../project-accounting/project-operations-integration-journal.md). Dieses Journal enthält wichtige Buchhaltungsdetails für Projektdaten, wie z. B. Abrechnung, Umsatzsteuergruppe, Umsatzsteuergruppe für Abrechnungsposten und finanzielle Dimensionen.

Der Projektmanager kann nicht abgerechnete Verkaufstransaktionen anhand der Zeit- und Materialabrechnungsmethode in [Zeit- und Materialabrechnungsstau](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) und Festpreisabrechnung in [Festpreismeilensteine](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones) überprüfen. In diesen Ansichten können Sie Transaktionen filtern, jene auswählen, die in den nächsten Abrechnungszyklus aufgenommen werden müssen, und diese dann als **Bereit zur Rechnungsstellung** markieren.

Sie können [manuell eine Proforma-Rechnung erstellen](../proforma-invoicing/create-manual-proforma-invoice.md) oder einen [periodischer Prozess](../proforma-invoicing/configure-automated-invoice-creation.md) verwenden. Der Projektmanager kann [einen Entwurf einer Proforma-Rechnung anpassen](../proforma-invoicing/manage-proforma-invoice.md) nach Bedarf und ihn dann bestätigen.

Die bestätigte Proforma-Rechnung wird an das Modul **Projektmanagement und Buchhaltung** in Finance senden. Der Projektbuchhalter formatiert und aktualisiert den Projektrechnungsvorschlag und veröffentlicht und druckt das Dokument. Gebuchte Projektrechnungen werden im Hauptbuch sowie in den Nebenbüchern Kunden und Projekt erfasst.
