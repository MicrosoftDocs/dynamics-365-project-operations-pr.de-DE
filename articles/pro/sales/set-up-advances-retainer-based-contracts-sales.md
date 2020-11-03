---
title: Vorschüsse und vorauszahlungsbasierte Verträge
description: Dieses Thema enthält Informationen über vorauszahlungsbasierte Vertragsmodell und Vorschüsse in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ccf8ff4fa52fa6ff9fe534dfbe6736afc24ffba
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087916"
---
# <a name="advances-and-retainer-based-contracts"></a>Vorschüsse und vorauszahlungsbasierte Verträge 


_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dynamics 365 Project Operations unterstützt auf Vorauszahlungen basierende Verträge. Ein auf Vorauszahlungen basierender Vertrag ist ein ausgehandelter Satz gleichmäßig verteilter Zahlungen, die dem Kunden während der gesamten Projektdauer in Rechnung gestellt werden. Diese Art von Vertrag wird normalerweise für Zeit- und Material- oder verbrauchsabhängige Abrechnungsmodelle verwendet, bei denen dem Kunden ein vorhersehbarer Rechnungs- und Zahlungsplan vorgelegt werden muss. In jeder Periode aufgelaufene tatsächliche Umsatzerlöse werden mit der Zahlung abgeglichen, die der Kunde zu Beginn der Periode erhalten hat. Gemäß dem Konzept des Zeit- und Materialfakturierungsmodells können die in jeder Periode aufgelaufenen Umsatzwerte mit den angefallenen Kosten variieren. Wenn die aufgelaufenen Umsätze höher sind als der zu Beginn des Zeitraums erhaltene Betrag, könnte das Unternehmen der Projektbereitstellung:

- Dem Debitor nur den Überschuss in Rechnung stellen 
- Die Abstimmung des Umsatzes auf die nächste Rechnungsperiode verschieben und am Ende des Projekts eine endgültige Rechnung für verbleibende nicht abgestimmte Umsätze erstellen

Der Hauptunterschied zwischen einem auf Vorauszahlungen basierenden Vertragsmodell und einem Festpreisvertragsmodell in Project Operations besteht darin, dass im Festpreisvertragsmodell der Rechnungsbetrag nicht an angefallene Kosten geknüpft oder gebunden ist. Die Rechnungsstellung folgt einem Meilenstein-basierten Ansatz, der an den für diesen Zeitraum angefallenen Kosten ausgerichtet ist. In einem auf Vorauszahlungen basierenden Vertrag werden Umsätze, die in Rechnung gestellt werden können, basierend auf der Abrechnungsmethode in der Vertragszeile erfasst. Wenn die Fakturierungsmethode Zeit und Material beinhaltet, sind die fakturierbaren Umsätze an die Kosten gebunden, die in einem bestimmten Zeitraum anfallen, und können von Zeitraum zu Zeitraum variieren. Dem Kunden wird jedoch nur der Betrag in der periodischen Vorauszahlung in Rechnung gestellt. Das System verwendet am Ende des Zeitraums eine andere Rechnung, um die während des Zeitraums erfassten fakturierbaren Umsätze mit dem Betrag abzugleichen, den der Kunde zu Beginn des Zeitraums in Rechnung gestellt hatte.

Der Vorteil dieser Methode besteht darin, dass die Kosten des Kunden im Gegensatz zu einem typischen Zeit- und Materialmodell im Vorauszahlungszeitplan vorhersehbar werden. Die Organisation, die das Projekt bereitstellt, hat auch einen gewissen Spielraum, um das Risiko zum Abdecken der Kosten zu sichern, die durch eine Erhöhung des Umfangs entstehen, die ein Festpreismodell ihnen nicht ermöglicht hätte.

Zusätzlich zu einem regelmäßigen, auf Vorauszahlungen basierenden Zeitplan kann Project Operations einen einmaligen Vorschuss eines Kunden erfassen und diesen mit den verschiedenen Projektkostenkomponenten abgleichen.

Die Vorauszahlung in Project Operations kann erst verwendet werden, wenn sie dem Kunden in Rechnung gestellt wird. Dies wird durch die folgenden Felder im Unterraster für Vorschüsse und Vorauszahlungen angezeigt.

| Feld | Relevanz, Zweck und Anleitung | Nachgelagerte Auswirkungen |
| --- | --- | --- |
| Verfügbarer Betrag | Der Betrag, der zur Verwendung im Vorauszahlungs- oder Vorschussdatensatz verfügbar ist. | Bis der Vorschuss oder die Vorauszahlung in Rechnung gestellt wird, kann sie nicht verwendet werden, was bedeutet, dass der verfügbare Betrag null ist. |
| Verwendeter Betrag | Der Betrag, der zur Verwendung im Vorauszahlungs- oder Vorschussdatensatz bereits verwendet wird. | Ein Vorschuss oder eine Vorauszahlung kann teilweise auf einer Rechnung mit den tatsächlichen Kosten abgeglichen werden, wobei ein Teil als bereits verwendet oder verbraucht gekennzeichnet ist. Der Rest des Vorschuss- oder Vorauszahlungsbetrags steht zur Verfügung, um eine zukünftige Rechnung mit den tatsächlichen Kosten abzustimmen. |
