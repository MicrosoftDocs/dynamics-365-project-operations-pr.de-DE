---
title: Vorauszahlungen oder auf dem Vorbehalt basierende Verträge
description: Dieser Artikel enthält Informationen über Retainer-basierte Vertragsmodelle und Fortschritte in Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 201dd1651b12614930f6a2c294156b31deceab0b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932479"
---
# <a name="advances-and-retainer-based-contracts"></a>Vorauszahlungen oder auf dem Vorbehalt basierende Verträge


_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations unterstützt auf Vorbehalt basierende Verträge. Ein auf Vorauszahlungen basierender Vertrag ist ein ausgehandelter Satz gleichmäßig verteilter Zahlungen, die dem Kunden während der gesamten Projektdauer in Rechnung gestellt werden. Diese Art von Vertrag wird normalerweise für Zeit- und Material- oder verbrauchsabhängige Abrechnungsmodelle verwendet, bei denen dem Kunden ein vorhersehbarer Rechnungs- und Zahlungsplan vorgelegt werden muss. In jeder Periode aufgelaufene tatsächliche Umsatzerlöse werden mit der Zahlung abgeglichen, die der Kunde zu Beginn der Periode erhalten hat. Gemäß dem Konzept des Zeit- und Materialfakturierungsmodells können die in jeder Periode aufgelaufenen Umsatzwerte mit den angefallenen Kosten variieren. Wenn die aufgelaufenen Umsätze höher sind als der zu Beginn des Zeitraums erhaltene Betrag, könnte das Unternehmen der Projektbereitstellung:

- Dem Debitor nur den Überschuss in Rechnung stellen 
- Die Abstimmung des Umsatzes auf die nächste Rechnungsperiode verschieben und am Ende des Projekts eine endgültige Rechnung für verbleibende nicht abgestimmte Umsätze erstellen

Der Hauptunterschied zwischen einem auf Vorauszahlungen basierenden Vertragsmodell und einem Festpreisvertragsmodell in Project Operations besteht darin, dass im Festpreisvertragsmodell der Rechnungsbetrag nicht an angefallene Kosten geknüpft oder gebunden ist. Die Rechnungsstellung folgt einem Meilenstein-basierten Ansatz, der an den für diesen Zeitraum angefallenen Kosten ausgerichtet ist. In einem auf Vorauszahlungen basierenden Vertrag werden Umsätze, die in Rechnung gestellt werden können, basierend auf der Abrechnungsmethode in der Vertragszeile erfasst. Wenn die Fakturierungsmethode Zeit und Material beinhaltet, sind die fakturierbaren Umsätze an die Kosten gebunden, die in einem bestimmten Zeitraum anfallen, und können von Zeitraum zu Zeitraum variieren. Dem Kunden wird jedoch nur der Betrag in der periodischen Vorauszahlung in Rechnung gestellt. Das System verwendet am Ende des Zeitraums eine andere Rechnung, um die während des Zeitraums erfassten fakturierbaren Umsätze mit dem Betrag abzugleichen, den der Kunde zu Beginn des Zeitraums in Rechnung gestellt hatte.

Der Vorteil dieser Methode besteht darin, dass die Kosten des Kunden im Gegensatz zu einem typischen Zeit- und Materialmodell im Vorauszahlungszeitplan vorhersehbar werden. Die Organisation, die das Projekt bereitstellt, hat auch einen gewissen Spielraum, um das Risiko zum Abdecken der Kosten zu sichern, die durch eine Erhöhung des Umfangs entstehen, die ein Festpreismodell ihnen nicht ermöglicht hätte.

Zusätzlich zu einem regelmäßigen, auf Vorauszahlungen basierenden Zeitplan kann Project Operations einen einmaligen Vorschuss eines Kunden erfassen und diesen mit den verschiedenen Projektkostenkomponenten abgleichen.

Die Vorauszahlung in Project Operations kann erst verwendet werden, wenn sie dem Kunden in Rechnung gestellt wird. Dies wird durch die folgenden Felder im Unterraster für Vorschüsse und Vorauszahlungen angezeigt.

| Feld | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- |
| Verfügbarer Betrag | Der Betrag, der zur Verwendung im Vorauszahlungs- oder Vorschussdatensatz verfügbar ist. | Bis der Vorschuss oder die Vorauszahlung in Rechnung gestellt wird, kann sie nicht verwendet werden, was bedeutet, dass der verfügbare Betrag null ist. |
| Verwendeter Betrag | Der Betrag, der zur Verwendung im Vorauszahlungs- oder Vorschussdatensatz bereits verwendet wird. | Ein Vorschuss oder eine Vorauszahlung kann teilweise auf einer Rechnung mit den tatsächlichen Kosten abgeglichen werden, wobei ein Teil als bereits verwendet oder verbraucht gekennzeichnet ist. Der Rest des Vorschuss- oder Vorauszahlungsbetrags steht zur Verfügung, um eine zukünftige Rechnung mit den tatsächlichen Kosten abzustimmen. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]