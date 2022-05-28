---
title: Kreditorenabrechnung – Konzept und Erstellung
description: Dieses Thema beschreibt das Konzept von Kreditorenrechnungen, Anwendungsszenarien und wie Sie Kreditorenrechnungen in Microsoft Dynamics 365 Project Operations erstellen.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc9b3954b237294f52aa0bb74f8008a5dfdf78fd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580547"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Kreditorenabrechnung – Konzept und Erstellung

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Die Kreditorenrechnungsstellung in Microsoft Dynamics 365 Project Operations kann verwendet werden, um Kosten aus Lieferungen von Dienstleistungen und/oder Materialien für ein Projekt durch Kreditoren zu erfassen.

Wenn Dienstleistungen und/oder Materialien an einen Kreditor vergeben werden, stellt eine Fremdarbeit die vertragliche Vereinbarung mit diesem Lieferanten dar. Wenn der Kreditor die Dienstleistungen erbringt oder die Materialien empfangen und für Projektaufgaben verwendet werden, werden die Kosten für das Projekt erfasst. Der Kreditor sendet regelmäßig Rechnungen, die geprüft und mit den im Projekt erfassten Kosten abgeglichen werden. Nach Abschluss des Verifizierungsprozesses wird die Kreditorenrechnung bestätigt und zur Zahlung freigegeben.

## <a name="scenarios-for-use"></a>Anwendungsszenarien

Kreditorenrechnungen in Project Operations können verwendet werden, um zwei unterschiedliche Szenarien zu unterstützen.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Kunden nutzen die vollständigen Fremdarbeitserfahrung

Erfahrungen mit Kreditorenrechnungen bieten eine Möglichkeit zum Überprüfen und Abgleichen von Zeiteinträgen, Materialverbrauch und Ausgabeneinträgen, die auf fremdvergebene Komponenten mit Kreditorenrechnungspositionen verweisen. Dieser Prozess kann verwendet werden, um die Genauigkeit der Kreditorenrechnungspositionen zu überprüfen. Nachdem der Überprüfungsprozess abgeschlossen und die Kreditorenrechnung bestätigt wurde, storniert die Anwendung die Ist-Werte, die durch genehmigte Zeit-, Ausgaben- und Materialverwendungsprotokolle erfasst wurden, und erstellt mithilfe der Kreditorenrechnungspositionen neue Ist-Kosten.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Kunden nutzen nicht die vollständigen Fremdvergabeerfahrungen, möchten aber eine einheitliche Ansicht der Kosten für Projekte in Project Operations haben

Wenn Sie den Fremdarbeitsprozess in einem Drittsystem verfolgen, können Sie Kosten aus diesem Drittsystem in Project Operations erfassen, indem Sie Kreditorenrechnungen erstellen, die nicht auf Fremdarbeit verweisen. Auf diese Weise haben Ihre Projektmanager einen einzigen, einheitlichen Überblick über alle Kosten eines bestimmten Projekts.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Erstellung von Kreditorenrechnungen in Project Operations

Kreditorenrechnungen können auf zwei Arten erstellt werden:

- Auf der Listenseite der Kreditorenrechnung oder der Detailseite für eine einzelne Kreditorenrechnung
- Auf der Listenseite für Fremdarbeit oder der Detailseite für eine einzelne Fremdarbeit

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Erstellung über die Listenseite der Kreditorenrechnung oder die Detailseite

1. Gehen Sie zu **Einkauf** \> **Kreditorenrechnungen**.
2. Wählen Sie auf der Listenseite der Kreditorenrechnung oder der Detailseite für eine einzelne Kreditorenrechnung **Neu** aus, um eine neue Kreditorenrechnung zu erstellen.

Auf diese Weise erstellte Kreditorenrechnungen können auch auf eine Fremdarbeit verweisen.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Erstellung über die Listenseite für Fremdarbeit oder die Detailseite

1. Gehen Sie zu **Einkauf** \> **Fremdarbeit**.
2. Wählen Sie mindestens eine Fremdarbeit aus.
3. Wählen Sie auf der Listenseite der Fremdarbeit oder der Detailseite für eine einzelne Fremdarbeit **Kreditorenrechnung erstellen** aus, um eine neue Kreditorenrechnung zu erstellen.

Eine neue Kreditorenrechnung im **Entwurf**-Status wird für jede von Ihnen ausgewählte Fremdarbeit erstellt.

Kreditorenrechnungen, die Sie auf diese Weise erstellen, verweisen immer auf die Fremdarbeit in der Kopfzeile der Kreditorenrechnung. Jede Position bei der Fremdarbeit, die eine Zeit- und Materialabrechnungsmethode hat, führt dazu, dass eine Position auf der Kreditorenrechnung erstellt wird. Jede Position bei der Fremdarbeit, die eine Festpreis-Fakturierungsmethode hat, bewirkt, dass eine Position auf der Kreditorenrechnung für jeden Meilenstein der Untervertragsposition mit dem Status **Bereit zur Fakturierung** erstellt wird.

Die folgenden Felder und zugehörigen Datensätze werden aus dem Untervertrag in die Kopfzeile der Kreditorenrechnung kopiert:

- Kreditor.
- Zugehörige Preislisten werden als Preislisten in die Kreditorenrechnung kopiert.
- Währung.
- Vertragsschlusseinheit.
- Zahlungsbedingungen.

Für Zeit- und Material-Untervertragspositionen werden die folgenden Felder und zugehörigen Datensätze aus der Untervertragsposition in die Kreditorenrechnungsposition kopiert:

- Untervertrag und Untervertragspositionsreferenzen
- Transaktionsklasse
- Role
- Transaktionskategorie
- Produktfelder
- Project
- Task
- Buchbare Ressource

Für Festpreis-Untervertragspositionen werden die folgenden Felder aus der Untervertragsposition und dem Untervertragsmeilenstein in die Kreditorenrechnungsposition kopiert:

- Untervertrag und Untervertragspositionsreferenzen.
- Transaktionsklasse. Standardmäßig ist der Wert **Meilenstein**.
- Name und Betrag des Meilensteins werden aus dem zugehörigen Meilenstein der Unterauftragsposition kopiert.
- Der Benutzer kann ein Projekt und eine Aufgabe in der Kreditorenrechnungsposition auswählen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
