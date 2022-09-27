---
title: Spesenabrechnungen buchen
description: Dieser Artikel erklärt, wie Sie Spesenabrechnungen buchen können.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524868"
---
# <a name="post-expense-reports"></a>Spesenabrechnungen buchen

Nachdem eine Spesenabrechnung genehmigt und in das Fibu Buch.-Blatt übertragen wurde, kann sie gebucht werden. Wenn Sie eine Spesenabrechnung buchen, werden Ausgaben identifiziert, die zur Erstattung der Mehrwertsteuer berechtigt sind. Die Aufgabe der Überprüfung und Erstattung von Mehrwertsteuerzahlungen ist dem Mitarbeiter übertragen, der für die Überprüfung der Spesenabrechnung verantwortlich ist.

Wenn Ausgaben in einer Spesenabrechnung einem anderen Unternehmen als dem Unternehmen belastet werden, das den Mitarbeiter beschäftigt, müssen Sie sowohl das Unternehmen, dem diese Ausgaben geschuldet werden, als auch das Unternehmen, von dem sie geschuldet werden, überprüfen. Beispielsweise arbeitet der Mitarbeiter, der eine Spesenabrechnung eingereicht hat, für die DAT-Firma, belastet jedoch die DIR-Firma mit einer Spesenabrechnung. In diesem Fall ist DAT das Unternehmen, dem die Kosten geschuldet werden, und DIR ist das Unternehmen, von dem die Kosten geschuldet werden. Nachdem Sie diese Erfassungspositionen überprüft haben, können Sie die Ausgabenzeilen in die Finanzbuchhaltung buchen.

Um eine Spesenabrechnung zu erstellen, wählen Sie auf der Seite **Genehmigte Spesenabrechnungen** die Spesenanbrechnung und im Aktionsbereich **Buchen** aus.

Sie können auch alle Spesenabrechnungen gleichzeitig in der Liste buchen. Wählen Sie alle Spesenabrechnungen und dann **Buchen** aus.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Aktivieren Sie die Funktion Möglichkeit, Spesenverbindlichkeiten in Kreditorenwährung für Barzahlungsmethoden zu buchen

Die Funktion **Möglichkeit, Spesenverbindlichkeiten in Kreditorenwährung für Barzahlungsmethoden zu buchen** ermöglicht die Buchung von Spesenabrechnungen in einer Kreditorenwährung für die Barzahlungsmethode.

Wenn Sie Barauslagen einreichen, werden Spesenabrechnungen derzeit in der Buchhaltungswährung gebucht. Aufgrund der Betragsumrechnung zwischen Transaktionswährung, Buchhaltungswährung und Kreditorenwährung wird ein falscher Betrag an Kreditoren gezahlt, wenn das Transaktionsdatum der Ausgabe und das tatsächliche Zahlungsdatum unterschiedliche Wechselkurse haben.

Diese Funktion stellt sicher, dass der Kreditorensaldo in der Kreditorenwährung erfasst wird, wenn die Spesenabrechnung gebucht wird.

1. Gehen Sie zu **Arbeitsbereiche** \> **Funktionenverwaltung**.
2. In der Liste suchen und wählen Sie **Möglichkeit, Spesenverbindlichkeiten in Kreditorenwährung für Barzahlungsmethoden zu buchen**, und wählen Sie dann **Jetzt aktivieren**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
