---
title: Status und Validierungen, die nicht überschritten werden dürfen, verwalten
description: Dieses Thema enthält Informationen zu den in Project Operations durchgeführten Grenzwertprüfungen, die nicht überschritten werden dürfen.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129992"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Status und Validierungen, die nicht überschritten werden dürfen, verwalten 

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

## <a name="not-to-exceed-on-approvals"></a>Nicht zu überschreitende Genehmigungen

Wenn ein Zeit- oder Kosteneintrag übermittelt wird, wird ein Genehmigungsdatensatz erstellt. Wenn die Genehmigung kostenpflichtig ist und einer Zeit- und Materialvertragszeile zugeordnet ist, führt das System eine nicht zu überschreitende Validierungsprüfung auf den folgenden Ebenen durch:

  - Prüfung anhand des für den Kunden festgelegten Limits in der Projektvertragszeile
  - Prüfung anhand des festgelegten Limits in der Vertragszeile
  - Prüfung anhand des festgelegten Limits für den Kunden
  - Prüfung anhand des festgelegten Limits im Vertrag

Bei den Überprüfungen auf jeder Ebene muss sichergestellt werden, dass der Verkaufswert dieser Genehmigung nicht gegen die auf dieser Ebene nicht zu überschreitende Grenze verstößt, nachdem der bereits erfasste Rechnungsbestand und der bisher auf dieser Ebene in Rechnung gestellte Betrag berücksichtigt wurden.

Wenn die Prüfung bestanden ist, erhält die Genehmigung den Validierungsstatus **Erfolg**.

Wenn die Prüfung fehlschlägt, erhält die Genehmigung den Validierungsstatus **Fehler**. Das nicht zu überschreitende Validierungsdetail informiert den Benutzer darüber, auf welcher Ebene die Validierung fehlgeschlagen ist.

Wenn der übermittelte Zeit- oder Kosteneintrag als nicht kostenpflichtig angesehen wird, wird der Validierungsstatus „Nicht zu überschreiten“ auf **Nicht zutreffend** mit dem Validierungsdetail **Nicht zutreffend** gesetzt.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Nicht zu überschreitende nicht fakturierte Umsatz-Istwerte

Wenn eine Zeit- oder Kostenbuchung genehmigt wird, werden Kosten- und nicht abgerechnete Verkaufsdaten erstellt. Wenn die erstellten nicht fakturierten Umsatz-Istwerte fakturierbar und einer Zeit- und Materialvertragszeile zugeordnet sind, führt die Anwendung eine nicht zu überschreitende Validierungsprüfung auf den folgenden Ebenen durch:

  - Prüfung anhand des für den Kunden festgelegten Limits in der Projektvertragszeile
  - Prüfung anhand des festgelegten Limits in der Vertragszeile
  - Prüfung anhand des festgelegten Limits für den Kunden
  - Prüfung anhand des festgelegten Limits im Vertrag

Bei den Überprüfungen auf jeder Ebene wird sichergestellt, dass der Verkaufswert des Istwerts nicht gegen die auf dieser Ebene nicht zu überschreitende Grenze verstößt, nachdem der bereits erfasste Rechnungsbestand und der bisher auf dieser Ebene in Rechnung gestellte Betrag berücksichtigt wurden.

Wenn die Prüfung bestanden wird, erhält der nicht in Rechnung gestellte tatsächliche Umsatz einen Status „Nicht zu überschreiten“ von **Zugesagt**.

Wenn die Prüfung fehlschlägt, erhält der nicht in Rechnung gestellte tatsächliche Umsatz einen Status „Nicht zu überschreiten“ von **Fehler**. Das Validierungsdetail informiert den Benutzer darüber, auf welcher Ebene die Validierung fehlgeschlagen ist.

Wenn der nicht abgerechnete tatsächliche Umsatz als nicht fakturierbar oder fakturierbar angesehen wird, wenn auf keiner der vier Ebenen ein Grenzwert festgelegt wird, der nicht überschritten werden darf, oder wenn der tatsächlich erstellte Umsatz Kosten-, Aufbewahrungs-, Beschaffungseinheits- oder organisationsübergreifender Vertrieb ist, müssen die Felder **Nicht zu überschreitender Status** und **Informationen zur Prüfung „Nicht zu überschreiten“** auf **Nicht zutreffend** gesetzt sein.

## <a name="reset-the-not-to-exceed-status"></a>Nicht zu überschreitenden Status zurücksetzen

Sie können einen Massen-Reset des Status „Nicht zu überschreiten“ durchführen. Auf diese Weise können Projektmanager die nicht zu überschreitende Validierung anpassen, um die Abrechnung eines bestimmten Arbeits-, Zeit- oder Kostenaufwands gegenüber anderen zu priorisieren, die bereits aus dem verfügbaren nicht zu überschreitenden Betrag gebunden sind.

Nachdem der Status „Nicht zu überschreiten“ bei nicht in Rechnung gestellten Verkaufszahlen zurückgesetzt wurde, wird der zugesagte Betrag reduziert. Der Projektmanager kann einen anderen Teil der Arbeit, Zeit oder Kosten auswählen, bei denen die nicht zu überschreitende Validierung zuvor nicht bestanden wurde, und diese neu bewerten. Mit der Reduzierung des zugesagten Betrags bestehen diese Istwerte nun die Validierung. Dies hilft dem Projektmanager, mehr Einfluss und Kontrolle über die abrechnungsfähigen Transaktionen für diesen Zeitraum auszuüben.

Um den Status „Nicht zu überschreiten“ zurückzusetzen, wählen Sie einen oder mehrere Istwerte aus der Ansicht **Rückstandsprotokoll über Zeit- und Materialberechnung** oder **Istwerte** und dann **Nicht zu überschreitenden Status zurücksetzen** aus.

Der Status „Nicht zu überschreiten“ wird bei allen relevanten ausgewählten Istwerten auf **Nicht bewertet** zurückgesetzt. Bei Istwerten, deren Status nicht überschritten werden darf, handelt es sich um nicht in Rechnung gestellte Verkaufsdaten, die nicht bereits in Rechnung gestellt wurden, nicht auf einem Rechnungsentwurf und als kostenpflichtig gekennzeichnet sind. Alle anderen ausgewählten Istwerte werden ignoriert.

## <a name="reevaluate-not-to-exceed-status"></a>Nicht zu überschreitenden Status erneut bewerten

Sie können eine Massen-Neubewertung des Status „Nicht zu überschreiten“ durchführen. Eine Neubewertung des Status „Nicht zu überschreiten“ ist nützlich, wenn:

  - Es gab eine Neuverhandlung von nicht zu überschreitenden Grenzwerten mit dem Kunden, und die tatsächlichen Werte müssen neu bewertet werden.
  - Der Projektmanager möchte die Rechnungsstellung für nicht in Rechnung gestellte Verkaufsbestände optimieren, indem er einen Arbeitsbereich einem anderen vorrangig behandelt.

Um den Status „Nicht zu überschreiten“ neu zu bewerten, wählen Sie einen oder mehrere Istwerte aus der Ansicht **Rückstandsprotokoll über Zeit- und Materialberechnung** oder **Istwerte** und dann **Nicht zu überschreitenden Status erneut bewerten** aus.

Alle relevanten ausgewählten Istwerte mit einem Grenzwert, der nicht überschritten werden darf, werden anhand der Einstellung des Grenzwerts bewertet, der nicht überschritten werden darf. Bei Istwerten, die relevant für die Neubewertung sind, handelt es sich um nicht in Rechnung gestellte Verkaufsdaten, die nicht bereits in Rechnung gestellt wurden, nicht auf einem Rechnungsentwurf und als kostenpflichtig gekennzeichnet sind. Alle anderen ausgewählten Istwerte.
