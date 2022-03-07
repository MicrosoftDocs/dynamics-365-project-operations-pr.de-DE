---
title: Angebote – Wichtige Konzepte – Lite
description: Dieses Thema bietet Informationen zur Verwendung von Projektangeboten in Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 279e7dd47d3d61b02227b307a5833ca0bac66f4a774b5ff23cb69aac417e2f0e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009440"
---
# <a name="concepts-unique-to-project-quotes"></a>Konzepte, die nur für Projektangebote gelten

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_


Nachfolgend finden Sie die wichtigsten Konzepte, die Sie kennen sollten, bevor Sie mit der Verwendung von Projektangeboten in Dynamics 365 Project Operations beginnen:

## <a name="contracting-unit"></a>Vertragsschlusseinheit

Die Vertragseinheit repräsentiert die Abteilung oder Praxis, der die Projektbereitstellung gehört. Sie können Ressourcenkosten für jede Vertragseinheit einrichten. Wenn Sie Ressourcenkosten für eine Ressource in der Vertragseinheit angeben, können Sie auch unterschiedliche Kostensätze für Ressourcen festlegen, die diese Vertragseinheit ausleiht, oder für andere Abteilungen oder Praktiken innerhalb des Unternehmens. Diese werden als Verrechnungspreise, Ausleihe von Ressourcen oder Wechselkurse bezeichnet. Wenn Sie die Kosten für das Ausleihen von Ressourcen aus anderen Geschäftsbereichen festlegen, können Sie diese Kostensätze auch in der Währung der ausleihenden Abteilung festlegen.

## <a name="cost-currency"></a>Kostenwährung

Die Kostenwährung in Project Operations ist die Währung, in der die Kosten gemeldet werden. Diese Währung leitet sich von der Währung ab, die dem Feld **Vertragseinheit** im Angebot, Vertrag und Projekt beigefügt ist. Kosten können in jeder Währung für ein Projekt protokolliert werden. Es erfolgt jedoch eine Währungsumrechnung von den Währungskosten, in denen erfasst wurde, in die Kostenwährung des Projekts.

Da die Wechselkurse auf der CDS-Plattform nicht datumsabhängig sein können, können sich die auf dem Bildschirm angezeigten Kostensummen im Laufe der Zeit ändern, wenn Sie die Wechselkurse aktualisieren. Die in der Datenbank erfassten Kosten bleiben jedoch unverändert, da die Beträge in der Währung gespeichert werden, in der sie angefallen sind.

## <a name="sales-currency"></a>Verkaufswährung

Die Verkaufswährung in Project Operations ist die Währung, in der die geschätzten und tatsächlichen Verkaufsbeträge erfasst und angezeigt werden. Es ist auch die Währung, in der dem Kunden das Geschäft in Rechnung gestellt wird. Bei einem Projektangebot wird die Verkaufswährung standardmäßig aus dem Kunden- oder Kontodatensatz übernommen und kann beim Erstellen des Angebots geändert werden. Die Verkaufswährung kann nach dem Speichern des Datensatzes nicht mehr geändert werden. Produkt- und Projektpreislisten basieren standardmäßig auf der Verkaufswährung des Angebots.

Im Gegensatz zu Kosten können Verkaufswerte nur in der Verkaufswährung erfasst werden.

## <a name="billing-method"></a>Fakturierungsmethode

Projekte haben in der Regel feste Gebühren- und verbrauchsabhängige Vertragsmodelle. Dies wird in Project Operations als **Fakturierungsmethode** dargestellt und weist zwei Werte, Zeit und Material und Festpreis auf.

- **Zeit und Material:** Hierbei handelt es sich um ein verbrauchsabhängiges Vertragsmodell, bei dem alle angefallenen Kosten durch entsprechende Umsätze gedeckt sind. Wenn Sie mehr Kosten schätzen oder verursachen, steigt auch der entsprechende geschätzte und tatsächliche Umsatz. Sie können nicht zu überschreitende Grenzwerte in Angebotspositionen angeben, die diese Fakturierungsmethode aufweisen. Dadurch wird der tatsächliche Umsatz begrenzt. Der geschätzte Umsatz wird nicht durch nicht zu überschreitende Grenzwerte beeinflusst.
- **Festpreis:** Dies ist ein Vertragsmodell mit festen Gebühren, das angibt, dass die Verkaufswerte unabhängig von den angefallenen Kosten sind. Der Verkaufswert ist fest und ändert sich nicht, wenn Sie weitere Kosten schätzen oder verursachen.

## <a name="project-price-lists"></a>Projektpreislisten

Projektpreislisten sind Preislisten, die als Standardpreise und nicht als Kostensätze für Zeit, Kosten und andere projektbezogene Komponenten verwendet werden. Es kann mehrere Preislisten geben, und jede Liste kann für jedes Projektangebot eine eigene Datumseffektivität haben. Die überlappende Datumseffektivität wird in Projektpreislisten in Project Operations nicht unterstützt.

## <a name="product-price-lists"></a>Produktpreislisten

Produktpreislisten sind Preislisten, die als Standardpreise und nicht als Kostensätze für produktbasierte Positionen in einem Angebot verwendet werden. Es gibt nur eine Produktpreisliste pro Angebot.

## <a name="transaction-classes"></a>Transaktionsklassen

Project Operations unterstützt vier Arten von Transaktionsklassen:

- Uhrzeit
- Ausgabe
- Material
- Gebühr

Kosten- und Verkaufswerte können für die Transaktionsklassen Zeit, Kosten und Material geschätzt werden und anfallen. Die Gebühr ist eine reine Umsatzklasse.

## <a name="work-entities-and-billing-entities"></a>Arbeits- und Fakturierungsentitäten

Entitäten, die Arbeit darstellen, sind Projekte und Aufgaben. Entitäten, die die Fakturierung darstellen, sind Angebots- und Vertragszeilen. Sie können verschiedene Arbeitsentitäten mit Abrechnungsoptionen verknüpfen, indem Sie sie Angebots- oder Vertragszeilen zuordnen.

## <a name="multi-customer-deals"></a>Geschäfte mit mehreren Kunden

Geschäfte mit mehreren Kunden treten auf, wenn mehr als ein Kunde in Rechnung gestellt werden muss. Hierzu zählen folgende gängige Beispiele:

- **OEM-Unternehmen und ihre Partner:** Partner und Wiederverkäufer verkaufen ein Produkt mit Mehrwertdiensten. Dies ist normalerweise ein Szenario, in dem der OEM während eines bestimmten Geschäfts mit einem Kunden anbietet, einen Teil des Projekts zu finanzieren. 

- **Projekte des öffentlichen Sektors:** Mehrere Abteilungen einer lokalen Regierung vereinbaren die Finanzierung eines Projekts und werden gemäß einer zuvor vereinbarten Aufteilung in Rechnung gestellt. Beispielsweise vereinbaren ein Schulbezirk und die Stadt oder die lokale Regierungsabteilung, den Bau eines Schwimmbades zu finanzieren.

## <a name="invoice-schedules"></a>Rechnungszeitpläne

Rechnungszeitpläne sind für jede Angebotsposition spezifisch und optional. Rechnungszeitpläne werden basierend auf bestimmten Start- und Enddaten und der Rechnungshäufigkeit erstellt. Rechnungszeitpläne werden in der Vertragsphase verwendet, wenn der automatische Rechnungserstellungsprozess konfiguriert ist. In der Angebotsphase sind die Zeitpläne optional. Wenn Rechnungspläne in der Phase des **Angebots** erstellt werden, werden sie in den Projektvertrag kopiert, der erstellt wird, wenn ein Projektangebot gewonnen wird.

## <a name="changes-from-dynamics-365-sales-quote"></a>Änderungen gegenüber dem Dynamics 365 Sales-Angebot:

Project Operations-Angebote basieren auf den Dynamics 365 Sales-Angeboten. Es gibt jedoch einige wichtige Unterschiede in der Funktionalität, die Sie beachten sollten:

- Die Aktionen **Überarbeiten** und **Aktivieren** werden nicht unterstützt.
- Project Operations-Angebote haben zwei verschiedene Arten von Positionen. Eine ist für Projekte und die andere für Produkte.
- Project Operations-Angebote haben ihre eigenen Formular- und Benutzeroberflächenelemente, Geschäftsregeln, eine Geschäftslogik in Plug-Ins und clientseitige Skripte, die sie bei Verkaufsangeboten einzigartig machen.

Aus diesen Gründen wird nicht empfohlen, ein Verkaufsangebot und ein Project Operations-Angebot variabel zu verwenden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
