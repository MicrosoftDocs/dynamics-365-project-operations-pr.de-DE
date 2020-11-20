---
title: Ein Angebot schließen – Lite
description: Dieses Thema bietet Informationen zum Abschluss eines Angebots in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175710"
---
# <a name="close-a-quote---lite"></a>Ein Angebot schließen – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Ein Projektangebot kann als „Gewonnen“ oder „Verloren“ geschlossen werden. Die Vorgänge „Aktivieren“ und „Überarbeiten“ von Angeboten werden in Microsoft Dynamics 365 Project Operations nicht unterstützt, sodass ein Angebotsentwurf geschlossen werden kann.

## <a name="close-a-quote-as-won"></a>Ein Angebot als „Gewonnen“ schließen

Wenn Sie ein Projektangebot als „Gewonnen“ schließen, wird das Angebot in den Status „Geschlossen“ und der Statusgrund auf „Gewonnen“ gesetzt. Durch das Schließen des Angebots wird das Projektangebot schreibgeschützt, und es wird ein Entwurf eines Projektvertrags erstellt, der die Angebotsinformationen enthält. Ein Bestätigungs-Dialogfeld wird angezeigt, bevor die Änderungen vorgenommen werden, da ein geschlossenes Angebot nicht erneut geöffnet werden kann und die Änderungen nicht rückgängig gemacht werden können.

Wenn das Angebot an eine Verkaufschance angehängt ist, werden alle anderen Projektangebote für die Verkaufschance automatisch als „Verloren“ geschlossen.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finanzielle Auswirkungen des Abschlusses eines Angebots als „Gewonnen“

Wenn für ein Projekt tatsächliche Zeitangaben aufgezeichnet wurden, während es noch einem Angebotsentwurf beigefügt ist, werden nur die Kosten für die Zeit oder die Kosten erfasst. Nachdem ein Angebot als „Gewonnen“ geschlossen wurde, werden die Kosten von der Anwendung umgestaltet, indem die älteren tatsächlichen Kosten zurückgebucht und neue tatsächliche Kosten erneut erstellt werden. Die Anwendung verarbeitet diese Istkosten basierend auf der Abrechnungsmethode der zugehörigen Projektvertragszeile. Wenn sich die tatsächlichen Kosten auf eine Zeit- und Materialvertragszeile beziehen, erstellt das System automatisch die entsprechenden nicht in Rechnung gestellten Umsatz-Istwerte, wenn das Angebot geschlossen und der Projektvertrag erstellt wird. Wenn sich die tatsächlichen Kosten auf eine Festpreisvertragszeile beziehen, beendet die Anwendung die erneute Verabeitung der tatsächlichen Kosten basierend auf den Regeln für die getrennte Abrechnung für die Projektvertragskunden.

## <a name="closing-a-quote-as-lost"></a>Ein Angebot als „Verloren“ schließen:

Wenn Sie ein Projektangebot als „Verloren“ schließen, wird der Status auf „Geschlossen“ und der Statusgrund auf „Verloren“ gesetzt. Wenn Sie das Angebot schließen, ist das Projektangebot schreibgeschützt. Da ein geschlossenes Angebot nicht erneut geöffnet werden kann, werden Ihre Änderungen in einem Bestätigungsdialogfeld bestätigt, bevor Sie ein Angebot schließen.

Wenn für das als verloren geschlossene Projektangebot auf ein Projekt in einer seiner Zeilen verwiesen wird, wird dieses Projekt auch als geschlossen markiert und alle Ressourcenbuchungen ab diesem Tag werden storniert.

> [!NOTE]
> In Project Operations wirkt sich das Schließen eines Angebots als „Gewonnen“ oder „Verloren“ nicht auf den Status der Verkaufschance aus, die geöffnet bleibt, bis sie manuell geschlossen wird.
