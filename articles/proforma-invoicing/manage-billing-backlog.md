---
title: Das Rechnungsrückstandsprotokoll verwalten
description: Dieses Thema enthält Informationen zum Anzeigen und Bearbeiten des Rechnungsrückstandsprotokolls in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bec6afe04a705d4f55ac3a7de93a64b47021fbb4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122342"
---
# <a name="manage-the-billing-backlog"></a>Das Rechnungsrückstandsprotokoll verwalten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations verfügt über zwei dedizierte Ansichten, mit denen Sie den Rechnungsrückstandsprotokoll bearbeiten und verwalten können. Sie lauten **Festpreismeilensteine** und **Rückstandsprotokoll über Zeit- und Materialberechnung**. Um eine Ansicht auszuwählen, klicken Sie im Bereich **Vertrieb** von Project Operations in der linken Navigationsseite auf **Abrechnung**. Dort werden die Links zu Rechnungsrückstandsprotokollen gespeichert.

## <a name="fixed-price-milestones"></a>Festpreismeilensteine

In dieser Ansicht werden alle Meilensteine des Festpreises in allen Projektvertragszeilen des Systems aufgelistet. Einzelne oder mehrere Meilensteine können als **Bereit für die Rechnungsstellung** oder als **Nicht bereit für die Rechnungsstellung** über diese Ansicht markiert werden. Wenn Sie einen Meilenstein als **Bereit für die Rechnungsstellung** markieren, wird der Meilenstein für einen Rechnungsentwurf verfügbar.

Wenn Vertragszeilen mit mehreren Kunden eine Festpreisfakturierungsmethode haben, wird für jeden Kunden in der Vertragszeile ein Meilenstein erstellt. Der Benutzer erstellt einen Meilenstein und dieser Meilenstein wird intern in kundenspezifische Meilensteindatensätze aufgeteilt, entsprechend der für jeden Kunden in der Vertragszeile definierten Aufteilung des Abrechnungsprozentsatzes. In der Ansicht **Festpreismeilensteine** sehen Sie einzelne kundenspezifische Meilensteindatensätze. Jeder dieser Meilensteindatensätze kann als **Bereit für die Rechnungsstellung** getrennt von dieser Ansicht markiert werden. Wenn einer oder mehrere der zugehörigen Meilensteinaufteilungen als **Bereit für die Rechnungsstellung** markiert sind, wird der Header vom Status **Nicht gestartet** in den Status **In Bearbeitung** gesetzt. Wenn alle Meilensteinaufteilungen in Rechnung gestellt wurden, wird der Header-Meilensteinstatus in **Abgeschlossen** geändert.

In dieser Ansicht wird ein Meilenstein auf einem Rechnungsentwurf mit dem Rechnungsstatus **Kundenrechnung erstellt** angezeigt. Wenn der Rechnungsentwurf bestätigt wird, wird der Abrechnungsstatus in diesem Datensatz auf **Rechnung gebucht** aktualisiert. Das Aktualisieren dieses Statuswerts mithilfe von benutzerdefiniertem Code wird nicht empfohlen. Project Operations funktioniert nicht ordnungsgemäß, wenn diese Statuswerte mit benutzerdefiniertem Code aktualisiert werden.

## <a name="time-and-material-billing-backlog"></a>Rückstandsprotokoll über Zeit- und Materialberechnung

In dieser Ansicht werden alle nicht fakturieren Umsatz-Istwerte aufgelistet, die nicht über alle Projektverträge im System in Rechnung gestellt wurden. Einzelne oder mehrere nicht fakturierte Umsatz-Istwerte können als **Bereit für die Rechnungsstellung** oder als **Nicht bereit für die Rechnungsstellung** über diese Ansicht markiert werden. Durch das Markieren eines nicht fakturierten Umsatz-Istwertes als **Bereit für die Rechnungsstellung** kann er in einem Rechnungsentwurf verwendet werden.

Nicht fakturierte Umsatz-Istwerte, die als Status für **Nicht zu überschreiten** die Angabe **Fehler** enthalten, können nicht als **Bereit für die Rechnungsstellung** markiert werden. Wenn diese Istwerte als solche gekennzeichnet werden müssen, setzen Sie den Status für andere Istwerte in der Vertragszeile zurück, die festgeschrieben wurden, und bewerten Sie dann den Status **Nicht zu überschreiten**.

Bei Vertragszeilen mit mehreren Kunden, die über eine Zeit- und Materialfakturierungsmethode verfügen, wird bei Genehmigung von Zeit und Kosten für jeden Kunden in der Vertragszeile ein nicht fakturierter tatsächlicher Umsatz-Istwert gemäß der für jeden Kunden in der Vertragszeile definierten Aufteilung des Abrechnungsprozentsatzes erstellt. In der Ansicht **Rückstandsprotokoll über Zeit- und Materialberechnung** sehen Sie diese einzelnen kundenspezifischen, nicht fakturierten Umsatz-Istwerte. Jeder dieser Datensätze an nicht fakturierten Umsatz-Istwerten kann separat von dieser Ansicht als **Bereit für die Rechnungsstellung** markiert werden.

Ein nicht fakturierter Umsatz-Istwert in einem Rechnungsentwurf wird in dieser Ansicht mit dem **Fakturierungsstatus** **Erstellte Kundenrechnung** angezeigt. Wenn der Rechnungsentwurf bestätigt wird, wird der Fakturierungsstatus in diesem Datensatz auf **Gebuchte Kundenrechnung** aktualisiert. Das Aktualisieren dieses Statuswerts in diesem Status mithilfe von benutzerdefiniertem Code wird nicht empfohlen. Project Operations funktioniert nicht ordnungsgemäß, wenn diese Statuswerte mit benutzerdefiniertem Code aktualisiert werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]