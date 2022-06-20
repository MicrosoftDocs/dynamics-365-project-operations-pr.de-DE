---
title: Untervertragsverwaltung in Project Operations
description: Dieser Artikel gibt einen Überblick über den gesamten Prozess der Verwaltung von Unteraufträgen in projektbasierten Unternehmen.
author: rumant
ms.date: 08/02/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f5e025b5f741935494349fb1bdfd3a19bacb5e1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911503"
---
# <a name="subcontract-management-in-project-operations"></a>Untervertragsverwaltung in Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieser Artikel gibt einen Überblick über den End-to-End-Prozess der Verwaltung von Unteraufträgen in projektbasierten Organisationen. Die Vergabe von Fremdarbeiten für Dienstleistungen folgt normalerweise dem Geschäftsprozessfluss, der im folgenden Diagramm gezeigt wird.

![Fremdarbeitsvergabeprozess-Flow](../media/SubcontractingProcessFlow.png)

Die folgende Liste bietet eine Schritt-für-Schritt-Beschreibung des Fremdarbeitsvergabeprozesses.

1. Der Projektmanager legt einen Fremdarbeitsvertrag mit einem Kreditor an. Standardmäßig werden die an den Kreditorendatensatz angehängten Preislisten für den Fremdarbeitsvertrag verwendet. Das Kreditorenkonten hat den Beziehungstyp **Kreditor** oder **Lieferant**.
2. Der Projektmanager kann alle Käufe als Positionen auf dem Fremdarbeitsvertrag auflisten. Fremdarbeitspositionen können Zeit, Ausgaben oder Produkte umfassen. Die Transaktionsklasse der Fremdarbeitsposition bestimmt, wofür die Position verwendet wird.
3. Der Konto-Manager des Zulieferers und der Projektmanager können den Fremdarbeitsvertrag durchlaufen. Die Preise können in den Einkaufspreislisten angepasst werden, die dem Fremdarbeitsvertrag angefügt sind.
4. An diesem Punkt oder später im Prozess ordnet der Konto-Manager des Zulieferers jeder Fremdarbeitsposition Lieferantenkontakte zu, wenn die Fremdarbeitsposition zeitlich begrenzt ist. Diese Assoziation stellt dem Projektmanager, der an dem Fremdarbeitsvertrag arbeitet, Informationen zur Verfügung. Wenn ein Lieferantenkontakt mit einer Fremdarbeitsposition verknüpft ist, erstellt das System automatisch eine buchbare Ressource aus dem Kontakt, falls noch keine buchbare Ressource vorhanden ist.
5. Die Fakturierungsmethode für jede Fremdarbeitsposition kann **Festpreis** oder **Zeit und Material** sein. Für Fremdarbeitspositionen mit Festpreisen wird ein meilensteinbasierter Rechnungsplan eingerichtet.
6.  Nachdem die Fremdarbeit eingerichtet und die Verhandlung abgeschlossen ist, wird er bestätigt. Bestätigte Fremdarbeiten können nicht bearbeitet werden, aber wenn Änderungen auftreten, kann eine Fremdarbeit 'zur Bearbeitung wieder geöffnet' werden, wodurch der Status von **Bestätigt** zurück zu **Entwurf** gesetzt wird, und Verhandlungen können wieder aufgenommen werden. 
7.  Beim Erstellen eines generischen Teammitglieds in einem Projekt kann das Teammitglied einer Fremdarbeitsposition zugeordnet werden. Dies weist auf die Notwendigkeit hin, das generische Teammitglied mit Subunternehmerkapazität zu besetzen.
8.  Benannte Teammitglieder können entweder direkt in einem Projekt erstellt werden, oder sie werden erstellt, indem sie mithilfe der Ressourcenplanungserfahrungen gebucht werden. Wenn ein benanntes Projektteammitglied ein Vertragsarbeiter ist, kann dies einer Fremdarbeitsposition zugeordnet werden. Dadurch wird die verfügbare Kapazität auf einer Fremdarbeitsposition in Anspruch genommen.
9.  Subunternehmer-Ressourcen können Zeit, Ausgaben und Materialverbrauch für Projekte und Projektaufgaben protokollieren und dann zur Genehmigung einreichen. Bei Mitarbeitern ist dies ähnlich. Bei der Zeiterfassung kann ein Vertragsarbeiter einer bestimmten Fremdarbeit und eine Fremdarbeitsposition auswählen.
10. Nach der Genehmigung erfasst die von Fremdarbeiten genehmigte Zeit die tatsächlichen Projektkosten basierend auf dem Kaufpreis des Vertragsarbeiters oder der Rolle, die er im Projekt übernommen hat.
11. Kreditorenrechnungen und Kreditorenrechnungszeilen können im System für die Arbeit erfasst werden, die von Kreditorenressourcen oder von den vom Kreditor gelieferten Produkten ausgeführt wird. Kreditorenrechnungszeilen müssen projektspezifisch und für eine Transaktionsklasse von Zeit, Aufwand, Produkt/Material, Meilenstein oder Gebühr sein. Optional können Kreditorenrechnungspositionen auf eine Fremdarbeitsposition verweisen.
12. Das System ordnet der Kreditorenrechnung automatisch alle Istkosten zu, die der Fremdauftragsposition und dem Projekt entsprechen. Dies erleichtert eine 3-Wege-Übereinstimmungs- und Verifizierungsprozess.
13. Der Projektmanager kann dann die automatisch abgeglichenen Projekt-Istwerte überprüfen, andere Projektkosten-Istwerte entfernen oder hinzufügen und den Verifizierungsprozess abschließen.
14. Wenn der Überprüfungsprozess in allen Zeilen abgeschlossen ist, wird die Kreditorenrechnung als **Bereit zur Zahlung** markiert. In dieser Phase können die Kreditorenrechnung und -zeilen an ein Buchhaltungs- oder Kreditorensystem übertragen werden, um die Zahlung an den Kreditor zu verarbeiten. Zuvor erfasste Projektkosten werden storniert und die tatsächlichen Kosten aus dem Kreditorenrechnungsposten werden im Projekt erfasst.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Mengenbasierte Fremdarbeitspositionen und arbeitsbasierte Lohnbearbeitungspositionen

Eine Fremdarbeitsposition kann mengen- oder arbeitsbasiert sein. 

Wenn eine Fremdarbeitsposition **mengenbasiert** ist, kann die Menge, die in der Fremdarbeitsposition für Zeit, Aufwand oder Material gekauft wird, für jedes Projekt verwendet werden.

Wenn eine Fremdarbeitsposition **arbeitsbasiert** ist, wird die Fremdarbeitsposition einem Arbeitskörper zugeordnet, der durch einen Knoten im Projektplan dargestellt wird. Der Wert der Fremdarbeitsposition ist die Summe aller Komponenten, die für die Erbringung dieser Arbeitsleistung erforderlich sind. Diese werden als Details zur Fremdarbeitsposition modelliert und können eine Sammlung von Zeit, Ausgaben oder Materialien sein. Bei einer arbeitsbasierten Fremdarbeitsposition ist die Fremdarbeitsposition ebenfalls einem einzelnen Projekt zugeordnet. Diese Arten von Unterverträgen werden derzeit nicht von Project Operations unterstützt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

