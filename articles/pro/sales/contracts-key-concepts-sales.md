---
title: Projektverträge – Wichtige Konzepte – Lite
description: Dieses Thema enthält Informationen zu den wichtigen Konzepten von Projektverträgen.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75c4b90e47c0b90ed3fea8dce1533057aa6137b9
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663773"
---
# <a name="concepts-unique-to-project-contracts"></a>Konzepte, die nur für Projektverträge gelten

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dieses Thema enthält die wichtigsten Konzepte, die Sie kennen sollten, bevor Sie mit der Verwendung von Projektverträgen in Dynamics 365 Project Operations beginnen:

## <a name="contracting-unit"></a>Vertragseinheit

Die Vertragseinheit repräsentiert die Abteilung oder Praxis, der die Projektbereitstellung gehört. Sie können für jede Vertragseinheit Ressourcenkosten einrichten. Wenn Sie die Ressourcenkosten für eine Ressource angeben, können Sie auch unterschiedliche Kostensätze für Ressourcen einrichten. Diese Vertragseinheit leiht diese Ressourcen von anderen Abteilungen oder Verfahren innerhalb des Unternehmens. Die Kostensätze für die Ressourcen werden als Verrechnungspreise, Ausleihe von Ressourcen oder Wechselkurse bezeichnet. Wenn Sie die Kostensätze für das Ausleihen von Ressourcen aus anderen Geschäftsbereichen festlegen, verwenden Sie die Währung der ausleihenden Abteilung.

## <a name="cost-currency"></a>Kostenwährung

Die Kostenwährung ist die Währung, in der die Kosten auf dem Bildschirm gemeldet werden. Diese Währung leitet sich von der Währung ab, die dem Feld **Vertragseinheit** im Vertrag und Projekt beigefügt ist. Kosten können in jeder Währung gegen ein Projekt protokolliert werden. Es erfolgt jedoch eine Währungsumrechnung aus der Währung, in der die Kosten erfasst wurden, in die Kostenwährung des Projekts, wenn dies auf dem Bildschirm angezeigt wird.

Da die Wechselkurse auf der Common Data Service-(CDS-)Plattform nicht datumsabhängig sein können, können sich die auf dem Bildschirm angezeigten Kostensummen im Laufe der Zeit ändern, wenn Sie die Wechselkurse aktualisieren. Die in der Datenbank erfassten Kosten bleiben jedoch unverändert, da die Beträge in der Währung gespeichert werden, in der sie angefallen sind.

## <a name="sales-currency"></a>Verkaufswährung

Die Verkaufswährung in Project Operations ist die Währung, in der die geschätzten und tatsächlichen Verkaufsbeträge erfasst und angezeigt werden. Die Verkaufswährung ist auch die Währung, in der dem Kunden das Geschäft in Rechnung gestellt wird. Bei einem Projektvertrag wird die Verkaufswährung standardmäßig aus dem Kunden- oder Kontodatensatz übernommen und kann beim Erstellen des Vertrags geändert werden. Wenn ein Vertrag durch Schließen eines Angebots als gewonnen erstellt wird, ist die Währung im Vertrag standardmäßig die Währung aus dem Angebot.

Wenn Sie einen Projektvertrag von Grund auf neu erstellen, kann das Feld **Verkaufswährung** nicht bearbeitet werden. Produkt- und Projektpreislisten basieren standardmäßig auf dieser Währung im Vertrag.

Im Gegensatz zu Kosten können Verkaufswerte nur in der Verkaufswährung erfasst werden.

## <a name="billing-method"></a>Fakturierungsmethode

Es gibt in der Regel zwei Arten von Vertragsmodellen für Projekte, feste Gebühren und verbrauchsabhängige Kosten. Diese Modelle werden in Project Operations als Fakturierungsmethoden mit zwei möglichen Werten dargestellt:

- Zeit und Material: Ein verbrauchsabhängiges Vertragsmodell, bei dem alle angefallenen Kosten durch entsprechende Umsätze gedeckt sind. Wenn Sie mehr Kosten schätzen oder verursachen, steigt auch der entsprechende geschätzte und tatsächliche Umsatz. Geben Sie nicht zu überschreitende Grenzwerte in Vertragszeilen ein, die diese Fakturierungsmethode aufweisen, bei der der tatsächliche Umsatz begrenzt wird. Der geschätzte Umsatz wird nicht durch nicht zu überschreitende Grenzwerte beeinflusst.
- Festpreis: Ein Vertragsmodell mit festen Gebühren, das angibt, dass die Verkaufswerte unabhängig von den angefallenen Kosten sind. Der Verkaufswert ist fest und ändert sich nicht, wenn Sie weitere Kosten schätzen oder verursachen.

## <a name="project-price-lists"></a>Projektpreislisten

Projektpreislisten werden als Standardpreise und nicht als Kostensätze für Zeit, Kosten und andere projektbezogene Komponenten verwendet. Es kann mehrere Preislisten geben. Jede Preisliste hat für jeden Projektvertrag ein eigenes Datum. Die überlappende Datumseffektivität wird in Projektpreislisten in Project Operations nicht unterstützt.

Wenn ein Projektvertrag durch den Gewinn eines Projektangebots erstellt wird, werden Projektpreislisten mit dem Vertragsnamen und dem darin enthaltenen Datum kopiert. Das Kopieren dieser Informationen stellt eine benutzerdefinierte Preisgestaltung für Projektkomponenten in diesem Projektvertrag dar.

## <a name="product-price-lists"></a>Produktpreislisten

Produktpreislisten werden als Standardpreise und nicht als Kostensätze für produktbasierte Positionen in einem Vertrag verwendet. Pro Vertrag gibt es nur eine Produktpreisliste.

## <a name="transaction-classes"></a>Transaktionsklassen

Project Operations unterstützt vier Arten von Transaktionsklassen:

- Uhrzeit
- Ausgabe
- Material
- Gebühr

Kosten- und Verkaufswerte können für die Transaktionsklassen Zeit, Kosten und Material geschätzt werden und anfallen. Eine Gebühr ist eine reine Umsatzklasse.

## <a name="work-entities-and-billing-entities"></a>Arbeits- und Fakturierungsentitäten

Entitäten, die Arbeit darstellen, sind Projekte und Aufgaben. Entitäten, die Abrechnungsaspekte darstellen, sind Vertragszeilen. Sie können verschiedene Arbeitseinheiten mit Abrechnungsoptionen verknüpfen, indem Sie sie an Vertragszeilen binden.

## <a name="multi-customer-deals"></a>Mehrkundenangebote

Bei Geschäften mit mehreren Kunden gibt es mehr als einen Kunden, dem bei einem Geschäft eine Rechnung gestellt werden muss. Hierzu zählen folgende gängige Beispiele:

- OEM-Unternehmen und ihre Partner: Partner und Wiederverkäufer verkaufen ein Produkt mit einigen Mehrwertdiensten, die in der Regel einen bestimmten Vertrag mit einem Kunden beinhalten. Der OEM bietet an, einen Teil des Projekts zu finanzieren. 

- Projekte des öffentlichen Sektors: Mehrere Abteilungen einer lokalen Regierung vereinbaren die Finanzierung eines Projekts und werden gemäß einer zuvor vereinbarten Aufteilung in Rechnung gestellt. Beispielsweise vereinbaren ein Schulbezirk oder die lokale Regierungsabteilung, den Bau eines Schwimmbades zu finanzieren.

## <a name="invoice-schedules"></a>Rechnungszeitpläne

Rechnungszeitpläne sind für jede Vertragszeile spezifisch und erforderlich, damit die automatische Rechnungsstellung funktioniert. Rechnungszeitpläne werden basierend auf bestimmten Start‑ und Enddaten und der Rechnungshäufigkeit erstellt. Die Zeitpläne werden in der Vertragsphase verwendet, wenn der automatische Rechnungserstellungsprozess konfiguriert ist. Wenn aus einem Angebot ein Projektvertrag erstellt wird, wird der Rechnungszeitplan aus dem Angebot in den Projektvertrag kopiert.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Änderungen aus dem Dynamics 365 Sales-Vertrag

Project Operations-Verträge basieren auf Dynamics 365 Sales-Verträge. Es gibt jedoch einige wichtige Abweichungen und Unterschiede in der Funktionalität, die Sie beachten sollten:

- Project Operations-Verträge weisen zwei unterschiedliche Arten von Zeilen auf, eine für Projekte und eine für Produkte.
- Project Operations-Verträge haben ihre eigenen Formular- und Benutzeroberflächenelemente, Geschäftsregeln, eine Geschäftslogik in Plug-Ins und clientseitige Skripte, die sie bei Verkaufsverträgen einzigartig machen.

Aus diesen Gründen sollten Sie einen Verkaufsauftrag nicht gegen einen Project Operations-Vertrag austauschen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
