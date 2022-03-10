---
title: Ein Angebot schließen – Lite
description: Dieses Thema bietet Informationen zum Abschluss eines Angebots in Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8ae5e14220ffecab5bcfa016d8d18e6ccfbc5b04be9a4e66cee26f8885125d31
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994320"
---
# <a name="close-a-quote---lite"></a>Ein Angebot schließen – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Ein Projektangebot kann als „Gewonnen“ oder „Verloren“ geschlossen werden. Ein Angebotsentwurf kann geschlossen werden, da die Vorgänge Aktivieren und Überarbeiten von Angeboten in Microsoft Dynamics 365 Project Operations nicht unterstützt werden.

## <a name="close-a-quote-as-won"></a>Ein Angebot als „Gewonnen“ schließen

Wenn Sie ein Projektangebot als gewonnen schließen, wird der Status auf geschlossen gesetzt und Statusgrund lautet gewonnen. Durch das Schließen des Angebots wird das Projektangebot schreibgeschützt, und es wird ein Entwurf eines Projektvertrags erstellt, der die Angebotsinformationen enthält. Da ein geschlossenes Angebot nicht erneut geöffnet werden kann, werden Ihre Änderungen in einem Bestätigungsdialogfeld bestätigt.

Wenn das Angebot an eine Verkaufschance angehängt ist, werden alle anderen Projektangebote für die Verkaufschance automatisch als „Verloren“ geschlossen.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finanzielle Auswirkungen des Abschlusses eines Angebots als „Gewonnen“

Wenn ein Projekt tatsächlich Zeit enthält, während es noch einem Angebotsentwurf beigefügt ist, werden nur die Kosten für die Zeit oder die Kosten erfasst. Nachdem ein Angebot als „Gewonnen“ geschlossen wurde, werden die Kosten von der Anwendung umgestaltet, indem die älteren tatsächlichen Kosten zurückgebucht und neue tatsächliche Kosten erneut erstellt werden. Die Anwendung verarbeitet diese Istkosten basierend auf der Abrechnungsmethode der zugehörigen Projektvertragszeile. Wenn sich die tatsächlichen Kosten auf eine Zeit- und Materialvertragszeile beziehen, werden entsprechende nicht in Rechnung gestellte Verkaufszahlen erstellt, wenn das Angebot geschlossen und der Projektvertrag erstellt wird. Wenn sich die tatsächlichen Kosten auf eine Festpreisvertragszeile beziehen, beendet die Anwendung die Wiederaufbereitung der tatsächlichen Kosten, die auf den Regeln für die getrennte Abrechnung für die Projektvertragskunden basieren.

## <a name="closing-a-quote-as-lost"></a>Ein Angebot als „Verloren“ schließen:

Wenn Sie ein Projektangebot als verloren schließen, wird der Status auf geschlossen gesetzt und Statusgrund lautet verloren. Wenn Sie das Angebot schließen, ist das Projektangebot schreibgeschützt. Da ein geschlossenes Angebot nicht erneut geöffnet werden kann, werden Ihre Änderungen in einem Bestätigungsdialogfeld bestätigt, bevor Sie ein Angebot schließen.

Wenn das als verloren geschlossene Projektangebot in einer seiner Zeilen auf ein Projekt verweist, wird dieses Projekt auch als geschlossen markiert. Alle Ressourcenbuchungen ab diesem Tag werden storniert.

> [!NOTE]
> In Project Operations wirkt sich das Schließen eines Angebots als „Gewonnen“ oder „Verloren“ nicht auf den Status der Verkaufschance aus, die geöffnet bleibt, bis sie manuell geschlossen wird.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]