---
title: Projektabrechnungsrückstand verwalten
description: Dieser Artikel informiert Sie über die verschiedenen Ansichten, die Sie bei der Verwaltung des Rechnungsrückstands für Projekte verwenden können.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f2e68449a8f1a0da62850454fb8ae56daffbab0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930087"
---
# <a name="manage-project-billing-backlog"></a>Projektabrechnungsrückstand verwalten 

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dynamics 365 Project Operations verfügt über dedizierte Ansichten zur Verwaltung des Abrechnungsstaus. Um den Abrechnungsstau zu verwalten, wählen Sie die Links im Bereich **Vertrieb** unter **Abrechnung**. 

Die folgenden Ansichten stehen zur Verfügung:

- Vorschüsse und Vorauszahlungen
- Verfügbare Vorauszahlungen und Vorschüsse
- Festpreismeilensteine
- Rechnungsrückstandsprotokoll zu Produkten
- Rückstandsprotokoll über Zeit- und Materialberechnung

## <a name="retainers-and-advances"></a>Vorschüsse und Vorauszahlungen

Die Ansicht **Vorschüsse und Vorauszahlungen** listet alle Vorschüsse und Vorauszahlungen aller Projektverträge im System auf. Nachdem ein Vorbehalt oder Vorschuss in Rechnung gestellt wurde, steht der Betrag des Vorschusses zur Verwendung zur Verfügung.

## <a name="available-retainers-and-advances"></a>Verfügbare Vorauszahlungen und Vorschüsse

Die Ansicht **Verfügbare Vorschüsse und Vorauszahlungen** listet alle verfügbaren Vorschüsse und Vorauszahlungen aller Projektverträge im System auf. Nachdem ein Vorbehalt oder Vorschuss in Rechnung gestellt wurde, steht der Betrag des Vorschusses zur Verwendung zur Verfügung und wird zur Liste hinzugefügt. Nachdem der Betrag des Vorschusses oder der Vorauszahlung vollständig verbraucht ist, wird er aus der Liste entfernt.

## <a name="fixed-price-milestones"></a>Festpreismeilensteine

Die Ansicht **Festpreismeilensteine** listet alle Meilensteine des Festpreises über alle Projektvertragslinien im System auf. Einzelne oder mehrere Meilensteine können über diese Ansicht als **Bereit für die Rechnungsstellung** oder **Nicht bereit für die Rechnungsstellung** markiert werden. Durch die Markierung eines Meilensteins als **Bereit für die Rechnungsstellung** kann dieser in einem Rechnungsentwurf verwendet werden.

Wenn Vertragszeilen mit mehreren Kunden eine Festpreisabrechnungsmethode haben, wird für jeden Kunden in der Vertragszeile ein Meilenstein erstellt. Ein Meilenstein kann erstellt und dann in einzelne kundenspezifische Meilensteindatensätze aufgeteilt werden. Diese Aufteilung erfolgt intern und entspricht der für jeden Kunden in der Vertragszeile definierten Aufteilung des Abrechnungsprozentsatzes. In der **Festpreismeilensteine**-Ansicht sehen Sie die einzelnen kundenspezifischen Meilensteindatensätze. Jeder dieser Meilensteindatensätze kann als **Bereit für die Rechnungsstellung** getrennt von dieser Ansicht markiert werden. Wenn eine oder mehrere der zugehörigen Meilensteinaufteilungen als **Bereit für die Rechnungsstellung** markiert sind, wird der Header-Status von **Nicht gestartet** auf **In Bearbeitung** aktualisiert. Wenn alle Meilensteinaufteilungen in Rechnung gestellt wurden, wird der Status des Header-Meilensteins auf **Abgeschlossen** aktualisiert.

In dieser Ansicht wird ein Meilenstein auf einem Rechnungsentwurf mit dem Rechnungsstatus **Kundenrechnung erstellt** angezeigt. Wenn der Rechnungsentwurf bestätigt wird, wird der Rechnungsstatus im Datensatz auf **Gebuchte Kundenrechnung** aktualisiert. Aktualisieren Sie diesen Statuswert nicht mithilfe von benutzerdefiniertem Code. Project Operations funktioniert nicht ordnungsgemäß, wenn diese Statuswerte mit benutzerdefiniertem Code aktualisiert werden.

## <a name="product-billing-backlog"></a>Rechnungsrückstandsprotokoll zu Produkten

Die Ansicht **Rechnungsrückstandsprotokoll zu Produkten** listet alle produktbasierten Vertragszeilen über alle Projektverträge im System auf. Einzelne oder mehrere produktbasierte Vertragszeilen können über diese Ansicht als **Bereit für die Rechnungsstellung** oder **Nicht bereit für die Rechnungsstellung** markiert werden. Durch das Markieren einer produktbasierten Vertragszeile als **Bereit für die Rechnungsstellung** kann sie in einem Rechnungsentwurf verwendet werden.

In dieser Ansicht wird eine produktbasierte Vertragszeile, die sich in einem Rechnungsentwurf befindet, mit dem Abrechnungsstatus **Erstellte Kundenrechnung** angezeigt. Wenn der Rechnungsentwurf bestätigt wird, wird der Fakturierungsstatus in diesem Datensatz auf **Gebuchte Kundenrechnung** aktualisiert. Aktualisieren Sie diesen Statuswert nicht mithilfe von benutzerdefiniertem Code. Project Operations funktioniert nicht ordnungsgemäß, wenn diese Statuswerte mit benutzerdefiniertem Code aktualisiert werden.

## <a name="time-and-material-billing-backlog"></a>Rückstandsprotokoll über Zeit- und Materialberechnung

Die Ansicht **Rückstandsprotokoll über Zeit- und Materialberechnung** listet alle nicht in Rechnung gestellten Verkaufszahlen aller Projektverträge im System auf, die nicht in Rechnung gestellt wurden. Einzelne oder mehrere nicht fakturierte Umsatz-Istwerte können als **Bereit für die Rechnungsstellung** oder als **Nicht bereit für die Rechnungsstellung** über diese Ansicht markiert werden. Durch das Markieren eines nicht fakturierten Umsatz-Istwertes als **Bereit für die Rechnungsstellung** kann er in einem Rechnungsentwurf verwendet werden.

Nicht in Rechnung gestellte Vertriebs-Istwerte mit einem **Nicht zu überschreitender Grenzwert**-Status von **Fehler** können nicht als **Bereit für die Rechnungsstellung** markiert werden. Wenn die Istwerte als **Bereit für die Rechnungsstellung** gekennzeichnet werden müssen, setzen Sie den Status für andere Istdaten in der Vertragszeile zurück, die festgeschrieben wurden. und bewerten Sie den **Nicht zu überschreitender Grenzwert**-Status erneut.

Wenn Vertragszeilen mit mehreren Kunden über eine Zeit- und Materialabrechnungsmethode verfügen und Zeit und Kosten genehmigt werden, wird für jeden Kunden in der Vertragszeile ein nicht abgerechneter tatsächlicher Umsatz gemäß der für jeden Kunden definierten Aufteilung des Abrechnungsprozentsatzes erstellt. In der Ansicht **Rückstandsprotokoll über Zeit- und Materialberechnung** sehen Sie diese einzelnen kundenspezifischen, nicht in Rechnung gestellten Verkaufsdaten. Jeder dieser Datensätze an nicht fakturierten Umsatz-Istwerten kann separat von dieser Ansicht als **Bereit für die Rechnungsstellung** markiert werden.

In dieser Ansicht wird ein nicht abgerechneter vertrieblicher Ist-Wert mit dem Abrechnungsstatus **Erstellte Kundenrechnung** angezeigt, der sich in einem Rechnungsentwurf befindet. Wenn der Rechnungsentwurf bestätigt wird, wird der Fakturierungsstatus in diesem Datensatz auf **Gebuchte Kundenrechnung** aktualisiert. Aktualisieren Sie diesen Statuswert nicht mithilfe von benutzerdefiniertem Code. Project Operations funktioniert nicht ordnungsgemäß, wenn diese Statuswerte mit benutzerdefiniertem Code aktualisiert werden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
