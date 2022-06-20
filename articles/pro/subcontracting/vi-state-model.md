---
title: Statusübergänge auf einer Kreditorenrechnung
description: Dieser Artikel erklärt die Statusübergänge bei einer Lieferantenrechnung in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 58b07322fb6480fdeb07eb867a7aabc0eff7b955
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934319"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Statusübergänge auf einer Kreditorenrechnung

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieser Artikel erklärt die Statusübergänge bei einer Lieferantenrechnung in Microsoft Dynamics 365 Project Operations. Folgende Zustände werden verwendet: **Entwurf**, **In Überprüfung**, **Bestätigt**, **In Wartestellung** und **Storniert**.

Die folgende Abbildungen zeigen diese Statusübergänge:

![Statusübergangsmodell bei Fremdarbeit.](../media/VI_State_Model.jpg)

Die folgende Tabelle erklärt, was die einzelnen Status im Lebenszyklus einer Kreditorenrechnung in Project Operations darstellen.

| Bundesstaat | Beschreibung des Dataflows | Zulässige Übergänge |
| --- | --- | --- |
| Entwurf | Dieser Status ist der Anfangsstatus einer Kreditorenrechnung. Die Positionen und Preise können sich ändern. Eine Kreditorenrechnung mit diesem Status kann nicht bearbeitet und gelöscht werden. | In Bearbeitung |
| In Überprüfung | Dieser Status stellt den Bearbeitungsstatus einer Kreditorenrechnung dar. Mindestens eine Kreditorenrechnungsposition hat einen Überprüfungsstatus von **In Bearbeitung**. | Bestätigt, in Wartestellung |
| Bestätigt | Dieser Status stellt die Phase einer Kreditorenrechnung dar, in der die Anwendung tatsächliche Kosten für jede Kreditorenrechnungsposition erstellt hat. Alle verknüpften Ist-Kosten, die mit den Kreditorenrechnungspositionen abgeglichen wurden, wurden storniert und durch die Ist-Kosten aus diesen Kreditorenrechnungspositionen ersetzt. Eine Kreditorenrechnung mit diesem Status kann nicht bearbeitet oder gelöscht werden. Sie können mit der **Stornieren**-Schaltfläche eine bestätigte Kreditorenrechnung stornieren. Die Aktion „Abbrechen“ kehrt die Auswirkung der Aktion „Bestätigen“ um. | Abgesagt |
| Zurückgestellt | <p>Dieser Status stellt eine Phase einer Kreditorenrechnung dar, in der die Kreditorenrechnung aufgrund eines Problems mit der Rechnung oder dem Status des Kreditors nicht verschoben werden kann. Eine Kreditorenrechnung mit diesem Status kann nicht bestätigt, storniert, bearbeitet oder gelöscht werden.</p><p>Sie können die Aktion „Erneut öffnen“ verwenden, um die Kreditorenrechnung in den Status **Entwurf** oder **In Überprüfung** zu verschieben. Wenn mindestens eine Position auf der Kreditorenrechnung den Überprüfungsstatus **In Bearbeitung** oder **Abgeschlossen** hat, wird die Kreditorenrechnung erneut im Status **In Überprüfung** geöffnet. Wenn alle Zeilen auf der Kreditorenrechnung einen Überprüfungsstatus von **Nicht angefangen** haben, wird die Kreditorenrechnung erneut im Status **Entwurf** geöffnet.</p> | Entwurf, In Überprüfung |
| Abgesagt | Dieser Status stellt die Phase einer Fremdarbeit dar, bei dem die tatsächliche Lieferung von Materialien und/oder Arbeiten durch Fremdarbeitsressourcen nicht mehr erforderlich ist. Eine Fremdarbeit in diesem Status kann nicht verwendet werden, um den Projektbedarf für Ressourcen und Materialien zu schätzen und zu besetzen, noch kann auf Zeit, Kosten und Materialverbrauch für ein Projekt verwiesen werden. Eine Fremdarbeit in diesem Status kann nicht bearbeitet oder gelöscht werden. | Nein |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
