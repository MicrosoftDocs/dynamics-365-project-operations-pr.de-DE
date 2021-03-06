---
title: Rechnungsverarbeitung, Vorschau
description: Dieses Thema bietet einen Prozessüberblick über die Rechnungsstellung in Project Operations für ressourcen-/nicht vorrätige Szenarien.
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 0eab33c8640f665555cf5ec5b0f188e5af65a493
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369015"
---
# <a name="invoicing-process-overview"></a>Rechnungsverarbeitung, Vorschau

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Project Operations für ressourcen-/nicht vorrätige Szenarien bietet umfassende Funktionen, die auf die Anforderungen des Projektmanagers und des Debitorenbuchhalters/Projektbuchhalters zugeschnitten sind. Für den Rechnungsstellungsprozess verwaltet der Projektmanager den Projektabrechnungsstau und der Debitorenbuchhalter/Projektbuchhalter erstellt einen konformen und genauen kundenorientierten Rechnungsbeleg.

![Rechnungsflussdiagramm](./media/invoicing-flow.png)

Die Projektvertragszeile definiert die Abrechnungsmethode für zugehörige Projekttransaktionen. Wenn der Projektmanager Zeit- und Kostentransaktionen genehmigt, zeichnet das System die Transaktionen in der Entität **Projekt-Istwerte** auf und sendet die Informationen an die Module **Projektmanagement und Buchhaltung** in Dynamics 365 Finance. Der Projektbuchhalter überprüft und veröffentlicht die Aufzeichnungen dann mit dem [Project Operations Integration-Journal](../project-accounting/project-operations-integration-journal.md). Dieses Journal enthält wichtige Buchhaltungsdetails für Projektdaten, wie z. B. Abrechnung, Umsatzsteuergruppe, Umsatzsteuergruppe für Abrechnungsposten und finanzielle Dimensionen.

Der Projektmanager kann nicht abgerechnete Verkaufstransaktionen anhand der Zeit- und Materialabrechnungsmethode in [Zeit- und Materialabrechnungsstau](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) und Festpreisabrechnung in [Festpreismeilensteine](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones) überprüfen. In diesen Ansichten können Sie Transaktionen filtern, auswählen, die in den nächsten Abrechnungszyklus aufgenommen werden müssen, und diese dann als **Rechnungsfertig** markieren.

Sie können [manuell eine Proforma-Rechnung erstellen](../proforma-invoicing/create-manual-proforma-invoice.md) oder einen [periodischer Prozess](../proforma-invoicing/configure-automated-invoice-creation.md) verwenden. Der Projektmanager kann [einen Entwurf einer Proforma-Rechnung anpassen](../proforma-invoicing/manage-proforma-invoice.md) nach Bedarf und ihn dann bestätigen.

Die bestätigte Proforma-Rechnung wird an das Modul **Projektmanagement und Buchhaltung** in Finance senden. Der Projektbuchhalter formatiert und aktualisiert den Projektrechnungsvorschlag und veröffentlicht und druckt das Dokument. Gebuchte Projektrechnungen werden in der Finanzbuchhaltung sowie in den untergeordneten Sachkonten für Kunden und Projekt erfasst.


[!INCLUDE[footer-include](../includes/footer-banner.md)]