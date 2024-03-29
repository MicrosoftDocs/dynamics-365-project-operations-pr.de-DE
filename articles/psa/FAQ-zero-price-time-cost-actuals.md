---
title: Warum ist der Standardpreis bei tatsächlichen Werten für Zeitkosten null?
description: Fehlerbehebung warum der Standardpreis bei tatsächlichen Werten für Zeitkosten null ist.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 1421f83458cf0aee4e70858e83d4c54179ff87e3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588229"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Warum ist der Standardpreis bei tatsächlichen Werten für Zeitkosten null?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dieses FAQ gilt für Ist-Werte, bei denen die Transaktionsklasse auf „Zeit“ und der Transaktionstyp auf „Kosten“ festgelegt wird. Die folgenden drei Überprüfungen helfen bei der Problembehebung, warum der Preis bei Zeitkosten-Ist-Werten 0 ist.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Überprüfung 1: Ermitteln Sie die Kostenpreisliste für das Projekt

Suchen Sie des Projekt im Projektfeld des Ist-Werts und rufen Sie dann die Projektseite auf. Klicken Sie im Vertragseinheitenlink in das Feld. Prüfen Sie auf der Vertragseinheitsseite, ob die Vertragseinheit eine Preisliste im Raster der Einstandspreisliste aufweist.

Bei mehr als einer Preisliste haben Sie das Problem isoliert. Project Service unterstützt nur eine Preisliste pro Organisationseinheit. Entfernen Sie alle Preislisten aus dieser Entität, bis nur eine Preisliste am Einstandspreislistenraster der Organisationseinheit angefügt ist.

Wenn der Organisationseinheit keine Preislisten angefügt sind, notieren Sie die Währung der Organisationseinheit. Wechseln Sie zu „Project Service“ und dann zu „Parameter“ und öffnen Sie die Registerkarte „Preislisten“. Überprüfen Sie, ob es Preislisten mit einem Kontext gibt, der auf „Kosten“ festgelegt ist, und der Währung der Organisationseinheit entspricht.
 
Wenn keine Preislisten vorhanden sind, die diesen Kriterien entsprechen, haben Sie das Problem isoliert. Stellen Sie sicher, dass Sie mindestens über eine Preisliste verfügen, deren Kontext auf „Kosten“ gesetzt ist und deren Währung der Währung der Organisationseinheit entspricht.

Bei mehr als einer Preisliste, die den Kriterien entsprechen, lesen Sie dieses Dokument weiter, um mehr Überprüfungen durchzuführen.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Überprüfung 2: Gelten irgendwelche der oben identifizierten Preislisten für ein bestimmtes Datum des Zeitkosten-Ist-Werts?

Damit Project Service eine Preisliste als Standardpreis annimmt muss diese Preisliste für das Datum des vertrieblichen Zeitkosten-Ist-Werts gelten. Überprüfen Sie Folgendes, um zu überprüfen, ob die oben identifizierten Preisliste(n) anwendbar sind:

- Überprüfen Sie, ob die Start- und Enddaten auf der Registerkarte „Allgemein“ für die angefügten Preisliste nicht leer sind. Wenn die Start- und Enddaten auf den oben identifizierten Preislisten leer sind, haben Sie das Problem isoliert. 
- Notieren Sie das Startdatumfeld auf Ihrem vertrieblichen Zeitkosten-Ist-Wert und überprüfen Sie, ob eine der identifizierten Preislisten für das Datum gilt. Beispielsweise sollte das Datum des Zeitkosten-Ist-Werts innerhalb eines Startdatums und des Enddatums auf der Preisliste liegen. 
    - Wenn keine Preisliste für das Datum im Zeitkosten-Ist-Wert vorhanden ist, haben Sie das Problem isoliert. Ändern Sie die Start- und Enddaten der Preisliste, um sicherzustellen, dass die Preisliste für das Datum des Zeitkosten-Ist-Werts gilt. 
    - Wenn mehr als eine Preisliste für das Datum im Zeitkosten-Ist-Wert vorhanden ist, haben Sie das Problem isoliert. Sie können dies beheben, indem Sie die Start- und Enddaten der Preisliste(n) bearbeiten, sodass nur eine Preisliste vorhanden ist, die für das Datum des Zeitkosten-Ist-Werts gilt. 
    - Bei nur einer Preisliste, die den Datums- und Zeitkosten-Ist-Wert abdeckt, machen Sie bei der nächsten Überprüfung im Dokument weiter.
Wenn Sie die erforderlichen Fehlerbehebungen vorgenommen haben, erstellen Sie erneut einen Zeiteintrag, genehmigen Sie ihn und stellen Sie sicher, dass der Zeitkosten-Ist-Wert einen gültigen Preis anzeigt.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Überprüfung 3: Gibt es einen Preis in der Preisliste für die Preisberechnungsdimensionen auf dem Zeitkosten-Ist-Wert?

Wenn Sie Überprüfung 1 und 2 erfolgreich abgeschlossen haben, sollte nur eine Preisliste für das Datum des Zeitkosten-Ist-Werts vorhanden sein. Öffnen Sie diese Preisliste und wechseln Sie zur Registerkarte „Rollenpreise“. Stellen Sie sicher, dass im Raster eine Zeile für die Preisberechnungsdimensionen auf dem Zeitkosten-Ist-Wert vorhanden ist.

Wenn keine Zeile im Rollenpreisraster für die Preisberechnungsdimensionen auf dem Zeitkosten-Ist-Wert vorhanden ist, haben Sie das Problem isoliert. Erstellen Sie eine Zeile im Rollenpreisraster für die Preisberechnungsdimensionen auf dem Zeitkosten-Ist-Wert. Wenn dies durchgeführt ist, erstellen Sie erneut einen Zeiteintrag, genehmigen Sie ihn und stellen Sie sicher, dass der nicht Zeitkosten-Ist-Wert einen gültigen Preis anzeigt.
 
Wird weiterhin keine gültiger Preis auf Ihrem Zeitkosten-Ist-Wert angezeigt, nachdem alle drei oben genannten Überprüfungen durchgeführt wurden, reichen Sie ein Support-Ticket ein.





[!INCLUDE[footer-include](../includes/footer-banner.md)]
