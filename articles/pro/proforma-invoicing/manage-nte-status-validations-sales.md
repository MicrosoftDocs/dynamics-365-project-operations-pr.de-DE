---
title: Status und Validierungen, die nicht überschritten werden dürfen, verwalten
description: Dieser Artikel informiert Sie über die Grenzwertprüfungen in Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d10a88305339a84b36d8606631ea9761806098a1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932755"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Status und Validierungen, die nicht überschritten werden dürfen, verwalten 

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

## <a name="not-to-exceed-on-approvals"></a>Nicht zu überschreitende Genehmigungen

Wenn Sie einen Zeit-, Kosten- oder Materialverbrauchseintrag senden, wird ein Genehmigungsdatensatz erstellt. Wenn die Genehmigung kostenpflichtig ist und einer Zeit- und Materialvertragszeile zugeordnet ist, führt das System eine nicht zu überschreitende Validierungsprüfung auf den folgenden Ebenen durch:

  - Prüfung anhand des für den Kunden festgelegten Limits in der Projektvertragszeile
  - Prüfung anhand des festgelegten Limits in der Vertragszeile
  - Prüfung anhand des festgelegten Limits für den Kunden
  - Prüfung anhand des festgelegten Limits im Vertrag

Bei den Überprüfungen auf jeder Ebene muss sichergestellt werden, dass der Verkaufswert dieser Genehmigung nicht gegen die auf dieser Ebene nicht zu überschreitende Grenze verstößt, nachdem der bereits erfasste Rechnungsbestand und der bisher auf dieser Ebene in Rechnung gestellte Betrag berücksichtigt wurden.

Wenn die Prüfung bestanden ist, erhält die Genehmigung den Validierungsstatus **Erfolg**.

Wenn die Prüfung fehlschlägt, erhält die Genehmigung den Validierungsstatus **Fehler**. Das nicht zu überschreitende Validierungsdetail informiert den Benutzer darüber, auf welcher Ebene die Validierung fehlgeschlagen ist.

Wenn der übermittelte Zeit-, Kosten- oder Materialverbrauchseintrag als nicht fakturierbar angesehen wird, wird der Validierungsstatus auf **Nicht zutreffend** und das Validierungsdetail auf **Nicht zutreffend** gesetzt.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Nicht zu überschreitende nicht fakturierte Umsatz-Istwerte

Wenn ein Zeit-, Kosten- oder Materialverbrauchseintrag genehmigt wird, werden Kosten- und nicht in Rechnung gestellte Umsatzdatensätze erstellt. Wenn die erstellten nicht fakturierten Umsatz-Istwerte fakturierbar und einer Zeit- und Materialvertragszeile zugeordnet sind, führt die Anwendung eine nicht zu überschreitende Validierungsprüfung auf den folgenden Ebenen durch:

  - Prüfung anhand des für den Kunden festgelegten Limits in der Projektvertragszeile
  - Prüfung anhand des festgelegten Limits in der Vertragszeile
  - Prüfung anhand des festgelegten Limits für den Kunden
  - Prüfung anhand des festgelegten Limits im Vertrag

Bei den Überprüfungen auf jeder Ebene wird sichergestellt, dass der Verkaufswert des Istwerts nicht gegen die auf dieser Ebene nicht zu überschreitende Grenze verstößt, nachdem der bereits erfasste Rechnungsbestand und der bisher auf dieser Ebene in Rechnung gestellte Betrag berücksichtigt wurden.

Wenn die Prüfung bestanden wird, erhält der nicht in Rechnung gestellte tatsächliche Umsatz einen Status „Nicht zu überschreiten“ von **Zugesagt**.

Wenn die Prüfung fehlschlägt, erhält der nicht in Rechnung gestellte tatsächliche Umsatz einen Status „Nicht zu überschreiten“ von **Fehler**. Das Validierungsdetail informiert den Benutzer darüber, auf welcher Ebene die Validierung fehlgeschlagen ist.

Wenn der nicht abgerechnete tatsächliche Umsatz als nicht fakturierbar oder fakturierbar angesehen wird, wenn auf keiner der vier Ebenen ein Grenzwert festgelegt wird, der nicht überschritten werden darf, oder wenn der tatsächlich erstellte Umsatz Kosten-, Aufbewahrungs-, Beschaffungseinheits- oder organisationsübergreifender Vertrieb ist, müssen die Felder **Nicht zu überschreitender Status** und **Informationen zur Prüfung „Nicht zu überschreiten“** auf **Nicht zutreffend** gesetzt sein.

## <a name="reset-the-not-to-exceed-status"></a>Nicht zu überschreitenden Status zurücksetzen

Sie können einen Massen-Reset des Status „Nicht zu überschreiten“ durchführen. Projektmanager können die nicht zu überschreitende Validierung anpassen, um die Abrechnung eines bestimmten Arbeits-, Zeit-, Kosten- oder Materialverbrauchs gegenüber anderen zu priorisieren, die bereits aus dem verfügbaren nicht zu überschreibenden Betrag gebunden sind.

Nachdem der Status „Nicht zu überschreiten“ bei nicht in Rechnung gestellten Verkaufszahlen zurückgesetzt wurde, wird der zugesagte Betrag reduziert. Der Projektmanager kann einen anderen Arbeits-, Zeit-, Kosten- oder Materialverbrauchseintrag auswählen, bei dem die nicht zu überschreitende Validierung zuvor nicht bestanden und neu bewertet wurde. Mit der Reduzierung des zugesagten Betrags bestehen diese Istwerte nun die Validierung, wodurch der Projektmanager einen größeren Einfluss und eine größere Kontrolle über die abrechnungsfähigen Transaktionen für diesen Zeitraum ausüben kann.

Um den Status „Nicht zu überschreiten“ zurückzusetzen, wählen Sie einen oder mehrere Istwerte aus der Ansicht **Rückstandsprotokoll über Zeit- und Materialberechnung** oder **Istwerte** und dann **Nicht zu überschreitenden Status zurücksetzen** aus.

Der Status „Nicht zu überschreiten“ wird bei allen relevanten ausgewählten Istwerten auf **Nicht bewertet** zurückgesetzt. Bei Istwerten, deren Status nicht überschritten werden darf, handelt es sich um nicht in Rechnung gestellte Verkaufsdaten, die nicht bereits in Rechnung gestellt wurden, nicht auf einem Rechnungsentwurf und als kostenpflichtig gekennzeichnet sind. Alle anderen ausgewählten Istwerte werden ignoriert.

## <a name="reevaluate-not-to-exceed-status"></a>Nicht zu überschreitenden Status erneut bewerten

Sie können eine Massen-Neubewertung des Status „Nicht zu überschreiten“ durchführen. Eine Neubewertung des Status „Nicht zu überschreiten“ ist nützlich, wenn:

  - Es gab eine Neuverhandlung von nicht zu überschreitenden Grenzwerten mit dem Kunden, und die tatsächlichen Werte müssen neu bewertet werden.
  - Der Projektmanager möchte die Rechnungsstellung für nicht in Rechnung gestellte Verkaufsbestände optimieren, indem er einen Arbeitsbereich einem anderen vorrangig behandelt.

Um den Status „Nicht zu überschreiten“ neu zu bewerten, wählen Sie einen oder mehrere Istwerte aus der Ansicht **Rückstandsprotokoll über Zeit- und Materialberechnung** oder **Istwerte** und dann **Nicht zu überschreitenden Status erneut bewerten** aus.

Alle relevanten ausgewählten Istwerte mit einem Grenzwert, der nicht überschritten werden darf, werden anhand der Einstellung des Grenzwerts bewertet, der nicht überschritten werden darf. Bei Istwerten, die relevant für die Neubewertung sind, handelt es sich um nicht in Rechnung gestellte Verkaufsdaten, die nicht bereits in Rechnung gestellt wurden, nicht auf einem Rechnungsentwurf und als kostenpflichtig gekennzeichnet sind. Alle anderen ausgewählten Istwerte.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
