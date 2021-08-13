---
title: Abrechnungsstau verwalten
description: Dieses Thema enthält Informationen zum Anzeigen und Bearbeiten des Rechnungsrückstandsprotokolls in Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2e839c1f32248fff6d97271796666b5031f66490ccd98574045b770100bf379f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991080"
---
# <a name="manage-billing-backlog"></a>Abrechnungsstau verwalten

_ **Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen

Dynamics 365 Project Operations verfügt über dedizierte Ansichten zur Verwaltung des Abrechnungsstaus. Um den Abrechnungsstau zu verwalten, wählen Sie die Links im Bereich **Vertrieb** unter **Abrechnung**. 

Die folgenden Ansichten stehen zur Verfügung:

- Vorschüsse und Vorauszahlungen
- Verfügbare Vorauszahlungen und Vorschüsse
- Festpreismeilensteine
- Rückstandsprotokoll über Zeit- und Materialberechnung

## <a name="retainers-and-advances"></a>Vorschüsse und Vorauszahlungen

Die Ansicht **Vorschüsse und Vorauszahlungen** listet alle Vorschüsse und Vorauszahlungen für alle Projektverträgen auf. Nachdem ein Vorbehalt oder Vorschuss in Rechnung gestellt wurde, steht der Betrag des Vorschusses zur Verwendung zur Verfügung.

## <a name="available-retainers-and-advances"></a>Verfügbare Vorauszahlungen und Vorschüsse

Die Ansicht **Verfügbare Vorschüsse und Vorauszahlungen** listet alle verfügbaren Vorschüsse und Vorauszahlungen für alle Projektverträgen auf. Nachdem ein Vorbehalt oder Vorschuss in Rechnung gestellt wurde, steht der Betrag des Vorschusses zur Verwendung zur Verfügung und wird zur Liste hinzugefügt. Nachdem der Betrag des Vorschusses oder der Vorauszahlung vollständig verwendet wurde, wird er aus der Liste entfernt.

## <a name="fixed-price-milestones"></a>Festpreismeilensteine

Die Ansicht **Festpreismeilensteine** listet alle Festpreismeilensteine für alle Projektvertragszeilen auf. In dieser Ansicht können einzelne oder mehrere Meilensteine als **Bereit für die Rechnungsstellung** oder **Nicht bereit für die Rechnungsstellung** markiert werden. Durch das Markieren eines Meilensteins als **Bereit für die Rechnungsstellung** kann er in einem Rechnungsentwurf verwendet werden.

Wenn Vertragszeilen mit mehreren Kunden eine Festpreisabrechnungsmethode haben, wird für jeden Kunden in der Vertragszeile ein Meilenstein erstellt. Ein Meilenstein kann erstellt und dann in einzelne kundenspezifische Meilensteindatensätze aufgeteilt werden. Diese Aufteilung erfolgt intern und entspricht der für jeden Kunden in der Vertragszeile definierten Aufteilung des Abrechnungsprozentsatzes. In der **Festpreismeilensteine**-Ansicht sehen Sie die einzelnen kundenspezifischen Meilensteindatensätze. Jeder dieser Meilensteindatensätze kann als **Bereit für die Rechnungsstellung** getrennt von dieser Ansicht markiert werden. Wenn einer oder mehrere der zugehörigen Meilensteinaufteilungen als **Bereit für die Rechnungsstellung** markiert sind, wird der Kopfzeilenstatus von **Nicht gestartet** auf **In Bearbeitung** gändert. Wenn alle Meilensteinaufteilungen in Rechnung gestellt wurden, wird der Kopfzeilenstatus des Meilensteins auf **Abgeschlossen** aktualisiert.

In dieser Ansicht wird ein Meilenstein auf einem Rechnungsentwurf mit dem Rechnungsstatus **Kundenrechnung erstellt** angezeigt. Wenn der Rechnungsentwurf bestätigt wird, wird der Rechnungsstatus im Datensatz auf **Gebuchte Kundenrechnung** aktualisiert. 

> [!NOTE] 
> Aktualisieren Sie diesen Statuswert nicht mit benutzerdefiniertem Code. Project Operations funktioniert nicht ordnungsgemäß, wenn diese Statuswerte mit benutzerdefiniertem Code aktualisiert werden.

## <a name="time-and-material-billing-backlog"></a>Rückstandsprotokoll über Zeit- und Materialberechnung

Die Ansicht **Rückstandsprotokoll über Zeit- und Materialberechnung** listet alle nicht in Rechnung gestellten Verkaufszahlen aller Projektverträge im System auf, die nicht in Rechnung gestellt wurden. Einzelne oder mehrere nicht fakturierte Umsatz-Istwerte können als **Bereit für die Rechnungsstellung** oder als **Nicht bereit für die Rechnungsstellung** über diese Ansicht markiert werden. Durch das Markieren eines nicht fakturierten Umsatz-Istwertes als **Bereit für die Rechnungsstellung** kann er in einem Rechnungsentwurf verwendet werden.

Nicht in Rechnung gestellte Vertriebs-Istwerte mit einem **Nicht zu überschreitender Grenzwert**-Status von **Fehler** können nicht als **Bereit für die Rechnungsstellung** markiert werden. Wenn die Istwerte als **Bereit für die Rechnungsstellung** gekennzeichnet werden müssen, setzen Sie den Status für andere Istdaten in der Vertragszeile zurück, die festgeschrieben wurden, und bewerten Sie dann den **den nicht zu überschreitenden Status** neu.

Wenn Vertragszeilen mit mehreren Kunden über eine Zeit- und Materialabrechnungsmethode verfügen und Zeit und Kosten genehmigt werden, wird für jeden Kunden in der Vertragszeile ein nicht abgerechneter tatsächlicher Umsatz gemäß der für jeden Kunden definierten Aufteilung des Abrechnungsprozentsatzes erstellt. In der Ansicht **Rückstandsprotokoll über Zeit- und Materialberechnung** sehen Sie diese einzelnen kundenspezifischen, nicht in Rechnung gestellten Verkaufsdaten. Jeder dieser Datensätze an nicht fakturierten Umsatz-Istwerten kann separat von dieser Ansicht als **Bereit für die Rechnungsstellung** markiert werden.

Ein nicht abgerechneter vertrieblicher Ist-Wert wird in dieser Ansicht mit einem Abrechnungsstatus **Erstellte Kundenrechnung** angezeigt. Wenn der Rechnungsentwurf bestätigt wird, wird der Abrechnungsstatus in diesem Datensatz auf **Kundenrechnung gebucht** aktualisiert. 

> [!NOTE] 
> Aktualisieren Sie diesen Statuswert nicht mit benutzerdefiniertem Code. Project Operations funktioniert nicht ordnungsgemäß, wenn diese Statuswerte mit benutzerdefiniertem Code aktualisiert werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
