---
title: Warum ist der Standardpreis bei Zeitvertriebs-Ist-Werten null?
description: Fehlerbehebung warum der Standardpreis bei Zeitvertrieb-Ist-Werten null ist.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 5106e8c1a059bbb0efbeb73dc63e03e8bc9e4b7b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125942"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Warum ist der Standardpreis bei Zeitvertriebs-Ist-Werten null?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dieses FAQ gilt für Ist-Werte, bei denen die Transaktionsklasse auf „Zeit” und der Transaktionstyp auf „Nicht fakturierte Umsätze” festgelegt wird. Die folgenden drei Überprüfungen helfen bei der Problembehebung, warum der Preis (Fakturierungsrate) bei vertrieblichen Zeit-Ist-Werten 0 ist.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Überprüfung 1: Ermitteln Sie die Vertriebspreisliste für das Projekt

Suchen Sie des Projekt im Projektfeld des Ist-Werts und rufen Sie die Projektseite auf. Wechseln Sie dann zur Registerkarte „Verbrieb” und klicken Sie auf dem Projektvertragszeilengitter auf den Link im Projektvertragsfeld. Die Projektvertragsseite wird geöffnet. Wechseln Sie auf der Projektvertragsseite zur Registerkarte „Projektpreisliste”. Überprüfen Sie, ob hier mindestens eine Preisliste angefügt ist. Wenn keine Preisliste im Projektpreislistenraster des Projektvertrags angefügt ist, haben Sie das Problem isoliert: Eine Preisliste am Projektpreislistenraster anfügen. Bei den Preislisten, die hier angefügt werden können, sollte das Kontextfeld auf „Vertrieb” gesetzt werden und das Währungsfeld sollte dem Währungsfeld des Projektvertrags entsprechen. Wenn Sie die erforderlichen Fehlerbehebungen vorgenommen haben, erstellen Sie erneut einen Zeiteintrag, genehmigen Sie ihn und stellen Sie sicher, dass der nicht in Rechnung gestellte vertriebliche Ist-Wert einen gültigen Preis anzeigt. 

Wenn im Projektpreislistenraster des Projektvertrags mindestens eine Preisliste angefügt ist, machen Sie bei der nächsten Überprüfung in dem Dokument weiter.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Überprüfung 2: Gelten irgendwelche der oben identifizierten Preislisten für ein bestimmtes Datum des vertrieblichen Zeitkosten-Ist-Werts?

Damit Project Service eine Preisliste als Standardpreis annimmt muss diese Preisliste für das Datum des vertrieblichen Zeit-Ist-Werts gelten. Überprüfen Sie Folgendes, um zu überprüfen, ob die oben identifizierten Preisliste(n) anwendbar sind:
- Überprüfen Sie, ob die Start- und Enddaten auf der Registerkarte „Allgemein” für die angefügten Preisliste nicht leer sind. Wenn die Start- und Enddaten auf den oben identifizierten Preislisten leer sind, haben Sie das Problem isoliert. 
- Notieren Sie das Startdatumfeld auf Ihrem vertrieblichen Zeit-Ist-Wert und überprüfen Sie, ob eine der identifizierten Preislisten für das Datum gilt. Beispielsweise sollte das Datum des vertrieblichen Zeit-Ist-Werts innerhalb eines Startdatums und des Enddatums auf der Preisliste liegen. 
    - Wenn keine Preisliste für das Datum im vertrieblichen Zeit-Ist-Wert vorhanden ist, haben Sie das Problem isoliert. Ändern Sie die Start- und Enddaten der Preisliste, um sicherzustellen, dass die Preisliste für das Datum des vertrieblichen Zeit-Ist-Werts gilt. 
    - Wenn mehr als eine Preisliste für das Datum im vertrieblichen Zeit-Ist-Wert vorhanden ist, haben Sie das Problem isoliert. Sie können dies beheben, indem Sie die Start- und Enddaten der Preisliste(n) bearbeiten, sodass nur eine Preisliste vorhanden ist, die für das Datum des vertrieblichen Zeitkosten-Ist-Werts gilt. 
    - Liegt nur eine Preisliste für das Datum des vertrieblichen Zeit-Ist-Werts vor, machen Sie bei Überprüfung 3 weiter.
Wenn Sie die erforderlichen Fehlerbehebungen vorgenommen haben, erstellen Sie erneut einen Zeiteintrag, genehmigen Sie ihn und stellen Sie sicher, dass der vertriebliche Zeit-Ist-Wert einen gültigen Preis anzeigt.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Überprüfung 3: Gibt es einen Preis in der Preisliste für die Preisberechnungsdimensionen auf dem vertrieblichen Zeit-Ist-Wert?

Wenn Sie Überprüfung 1 und 2 erfolgreich abgeschlossen haben, sollte nur eine Preisliste für das Datum des vertrieblichen Zeit-Ist-Werts vorhanden sein. Öffnen Sie diese Preisliste und navigieren Sie zur Registerkarte „Rollenpreise”. Stellen Sie sicher, dass im Raster eine Zeile für die Preisberechnungsdimensionen auf dem vertrieblichen Zeit-Ist-Wert vorhanden ist.

Wenn keine Zeile im Rollenpreisraster für die Preisberechnungsdimensionen auf dem vertrieblichen Zeit-Ist-Wert vorhanden ist, haben Sie das Problem isoliert. Erstellen Sie eine Zeile im Rollenpreisraster für die Preisberechnungsdimensionen auf dem vertrieblichen Zeit-Ist-Wert. Wenn dies durchgeführt ist, erstellen Sie erneut einen Zeiteintrag, genehmigen Sie ihn und stellen Sie sicher, dass der nicht vertrieblichen Zeit-Ist-Wert einen gültigen Preis anzeigt.

Wird weiterhin keine gültiger Preis auf Ihrem vertrieblichen Zeit-Ist-Wert angezeigt, nachdem alle drei oben genannten Überprüfungen befolgt wurden, reichen Sie ein Support-Ticket ein. 

