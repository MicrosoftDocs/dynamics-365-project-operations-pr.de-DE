---
title: Konzepte, die nur für projektbasierte Angebote gelten
description: Dieser Artikel enthält Informationen über Projektangebote in Microsoft Dynamics 365 Project Operations
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824326"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Konzepte, die nur für projektbasierte Angebote gelten

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Bevor Sie mit der Verwendung von Projektangeboten in Microsoft Dynamics 365 Project Operations beginnen, sollten Sie sich der folgenden Schlüsselkonzept bewusst sein.

## <a name="owning-company"></a>Zuständiges Unternehmen

Das besitzende Unternehmen stellt die juristische Person dar, die die Projektlieferung besitzt. Der Kunde im Angebot sollte ein gültiger Kunde dieser juristischen Person in Finanz- und Betriebs-Apps sein. Die Währung des Eigentümerunternehmens und die Währung der Vertragseinheit, die in einem projektbasierten Angebot ausgewählt wird, müssen übereinstimmen.

## <a name="contracting-unit"></a>Vertragsschlusseinheit

Eine Vertragseinheit repräsentiert die Abteilung oder Praxis, der die Projektbereitstellung gehört. Sie können für jede Vertragseinheit Ressourcenkosten einrichten. Wenn Sie Ressourcenkosten für eine Ressource in der Vertragseinheit angeben, können Sie unterschiedliche Kostensätze für Ressourcen festlegen, die die Vertragseinheit ausleiht, oder für andere Abteilungen oder Praktiken innerhalb des Unternehmens. Diese Kostensätze werden als Verrechnungspreise, Ausleihe von Ressourcen oder Wechselkurse bezeichnet. Wenn Sie die Kosten für das Ausleihen von Ressourcen aus anderen Geschäftsbereichen festlegen, können Sie die Kostensätze in der Währung der ausleihenden Abteilung festlegen.

## <a name="cost-currency"></a>Kostenwährung

Die Kostenwährung in Project Operations ist die Währung, in der die Kosten gemeldet werden. Diese Währung leitet sich von der Währung ab, die dem Feld **Vertragseinheit** im Angebot, Vertrag und Projekt beigefügt ist. Kosten können in jeder Währung gegen ein Projekt aufgezeichnet werden. Es erfolgt jedoch eine Währungsumrechnung von den Währungskosten, in denen erfasst wurde, in die Kostenwährung des Projekts.

Da Wechselkurse auf der Dataverse-Plattform nicht datumsabhängig sein können, können sich die auf dem Bildschirm angezeigten Kostensummen im Laufe der Zeit ändern, wenn Sie Wechselkurse aktualisieren. In der Datenbank erfasste Kosten bleiben jedoch unverändert, da die Beträge in der Währung gespeichert werden, in der sie angefallen sind.

## <a name="sales-currency"></a>Verkaufswährung

Die Verkaufswährung in Project Operations ist die Währung, in der die geschätzten und tatsächlichen Verkaufsbeträge erfasst und angezeigt werden. Es ist auch die Währung, in der dem Kunden das Geschäft in Rechnung gestellt wird. Bei einem Projektangebot wird die standardmäßige Verkaufswährung aus dem Kunden- oder Kontodatensatz übernommen und kann beim Erstellen des Angebots geändert werden. Die Verkaufswährung kann nach dem Speichern des Datensatzes jedoch nicht mehr geändert werden. Standardmäßige Produkt- und Projektpreislisten werden basierend auf der Verkaufswährung des Angebots festgelegt.

Im Gegensatz zu Kosten können Verkaufswerte **nur** in der Verkaufswährung erfasst werden.

## <a name="billing-method"></a>Abrechnungsmethode

Projekte haben in der Regel feste Gebühren- und verbrauchsabhängige Vertragsmodelle. In Project Operations wird das Vertragsmodell eines Projekts durch die Abrechnungsmethode dargestellt. Die Abrechnungsmethode hat zwei Werte: Zeit und Auwand und Festpreis.

- **Zeit und Material** – Ein verbrauchsabhängiges Vertragsmodell, bei dem alle angefallenen Kosten durch entsprechende Umsätze gedeckt sind. Wenn Sie mehr Kosten schätzen oder verursachen, steigt auch der entsprechende geschätzte und tatsächliche Umsatz. Sie können nicht zu überschreitende Grenzwerte in Angebotspositionen angeben, die diese Fakturierungsmethode aufweisen. So begrenzen Sie den tatsächlichen Umsatz. Der geschätzte Umsatz wird nicht durch nicht zu überschreitende Grenzwerte beeinflusst.
- **Festpreis**: Ein Vertragsmodell mit festen Gebühren, bei dem die Verkaufswerte unabhängig von den angefallenen Kosten sind. Der Verkaufswert ist fest und ändert sich nicht, wenn Sie weitere Kosten schätzen oder verursachen.

## <a name="project-price-lists"></a>Projektpreislisten

Projektpreislisten sind Preislisten, die als Standardpreise und nicht als Kostensätze für Zeit, Kosten und andere projektbezogene Komponenten verwendet werden. Es kann mehrere Preislisten geben, und jede Liste kann für jedes Projektangebot eine eigene Datumseffektivität haben. Project Operations unterstützt keine überlappende Datumseffektivität in Projektpreislisten.

## <a name="product-price-lists"></a>Produktpreislisten

Produktpreislisten sind Preislisten, die als Standardpreise und nicht als Kostensätze für produktbasierte Positionen in einem Angebot verwendet werden. Es gibt nur eine Produktpreisliste pro Angebot.

## <a name="transaction-classes"></a>Transaktionsklassen

Project Operations unterstützt vier Arten von Transaktionsklassen:

- Uhrzeit
- Ausgabe
- Material
- Gebühr

Kosten‑ und Verkaufswerte können geschätzt und den Transaktionsklassen **Zeit**, **Kosten** und **Material** zugeordnet werden. **Gebühr** ist eine Transaktionsklasse, die sich nur auf den Umsatz bezieht.

## <a name="work-entities-and-billing-entities"></a>Arbeits- und Fakturierungsentitäten

Projekte und Aufgaben sind Entitäten, die Arbeit darstellen. Entitäten, die die Fakturierung darstellen, sind Angebots- und Vertragszeilen. Sie können verschiedene Arbeitsentitäten mit Abrechnungsoptionen verknüpfen, indem Sie sie Angebots- oder Vertragszeilen zuordnen.

## <a name="multi-customer-deals"></a>Mehrkundenangebote

Geschäfte mit mehreren Kunden treten auf, wenn mehr als ein Kunde pro Rechnung gestellt werden muss. Im Folgenden finden Sie einige typische Beispiele:.

- **Original Equipment Manufacturer (OEM) Unternehmen und ihre Partner** – Partner und Wiederverkäufer verkaufen ein Produkt mit Mehrwertdiensten. Während eines Geschäfts mit einem Kunden bietet der OEM normalerweise die Finanzierung eines Teils des Projekts an.
- **Projekte des öffentlichen Sektors**: Mehrere Abteilungen einer lokalen Regierung vereinbaren die Finanzierung eines Projekts und werden gemäß einer zuvor vereinbarten Aufteilung in Rechnung gestellt. Beispielsweise vereinbaren ein Schulbezirk und die Stadt oder die lokale Regierungsabteilung, den Bau eines Schwimmbades zu finanzieren.

## <a name="invoice-schedules"></a>Rechnungszeitpläne

Rechnungszeitpläne sind für jede Angebotsposition spezifisch und optional. Rechnungszeitpläne werden basierend auf bestimmten Start‑ und Enddaten und der Rechnungshäufigkeit erstellt. Sie werden in der Vertragsphase verwendet, wenn der automatische Rechnungserstellungsprozess konfiguriert ist. Während der Angebotsphase sind die Rechnungszeitpläne optional. Wenn Sie in der Phase der Angebots erstellt werden, werden sie in den Projektvertrag kopiert, der erstellt wird, wenn ein Projektangebot gewonnen wird.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Unterschiede gegenüber dem Dynamics 365 Sales-Angeboten

Project Operations-Angebote basieren auf den Dynamics 365 Sales-Angeboten. Es gibt jedoch einige wichtige Unterschiede in der Funktionalität, die Sie beachten sollten:

- Project Operations-Angebote weisen zwei unterschiedliche Arten von Zeilen auf: eine für Projekte und eine für Produkte.
- Project Operations-Angebote haben ihre eigenen Seiten- und Benutzeroberflächenelemente, Geschäftsregeln, eine Geschäftslogik in Plug-Ins und clientseitige Skripte, die sie bei Verkaufsangeboten einzigartig machen.
- In Sales Angefügte können Sie mehrere Aufträge einem einzelnen Vertriebsangebot anfügen. In Project Operations können Sie nur einen Projektvertrag einem Projektangebot anfügen.
- Wenn Sie ein Angebot gewinnen, kann die zugehörige Verkaufschance offen bleiben. Wenn ein Projektangebot gewonnen wird, wird die verknüpfte Verkaufschance geschlossen.
- Ein Vertriebsangebot enthält einige Felder und Konzepte nicht, die in einem Projektangebot enthalten sind. Die Felder enthalten **Vertragseinheit**, **Kontomanager** und **Kontaktname für Rechnungsadresse**.
- Vertriebsangebote und Projektangebote werden ebenfalls über ein optionssatzbasiertes Feld namens **Typ** ermittelt. Für ein Verkaufsangebot hat dieses Feld den Wert **Elementbasiert**. Für ein Projektangebot ist der Wert **Arbeitsbasiert**.

Aufgrund dieser Unterschiede wird es nicht empfohlen, dass Sie Sales-Angebote und Project Operations Angebote austauschbar verwenden.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
