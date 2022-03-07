---
title: Warum ist der Standardpreis bei vertrieblichen Ausgaben-Ist-Werten null?
description: Die folgenden drei Überprüfungen helfen bei der Problembehebung, warum der Preis bei vertrieblichen Ausgaben-Ist-Werten 0 ist.
author: rumant
ms.prod: ''
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
ms.openlocfilehash: 6e477b7d5973398d50c6be03469d1c0a792b1b3323522329bc33cba755104968
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000800"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Warum ist der Standardpreis bei vertrieblichen Ausgaben-Ist-Werten null?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dieses FAQ gilt für tatsächliche Ausgabenwerte, bei denen die Transaktionsklasse auf „Ausgabe“ und der Transaktionstyp auf „Nicht fakturierte Umsätze“ festgelegt wird. Die folgenden drei Überprüfungen helfen bei der Problembehebung, warum der Preis (Fakturierungsrate) bei vertrieblichen Ausgaben-Ist-Werten 0 ist.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Überprüfung 1: Ermitteln Sie die Vertriebspreisliste für das Projekt

Suchen Sie des Projekt im Projektfeld des Ist-Werts und rufen Sie die Projektseite auf. Wechseln Sie dann zur Registerkarte „Verbrieb“. Klicken Sie auf dem Projektvertragszeilengitter auf den Link im Projektvertragsfeld. Die Projektvertragsseite wird geöffnet. Wechseln Sie auf der Projektvertragsseite zur Registerkarte „Projektpreisliste“. Überprüfen Sie, ob hier mindestens eine Preisliste angefügt ist.

Wenn keine Preisliste im Projektpreislistenraster des Projektvertrags angefügt ist, gehen Sie folgendermaßen vor:

- Eine Preisliste am Projektpreislistenraster anfügen. Bei den Preislisten, die hier angefügt werden können, sollte das Kontextfeld auf „Vertrieb“ gesetzt werden und das Währungsfeld sollte dem Währungsfeld des Projektvertrags entsprechen. Wenn Sie die erforderlichen Fehlerbehebungen vorgenommen haben, erstellen Sie erneut einen Ausgabeneintrag, genehmigen Sie ihn und stellen Sie sicher, dass der nicht in Rechnung gestellte vertriebliche Ist-Wert einen gültigen Preis anzeigt.
- Wenn im Projektpreislistenraster des Projektvertrags mindestens eine Preisliste angefügt ist, machen Sie bei Überprüfung 2 weiter.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Überprüfung 2: Gelten irgendwelche der oben identifizierten Preislisten für ein bestimmtes Datum des Ausgaben-Ist-Werts?

Damit Project Service eine Preisliste als Standardpreis annimmt muss diese Preisliste für das Datum des vertrieblichen Ausgaben-Ist-Werts gelten. Überprüfen Sie Folgendes, um zu überprüfen, ob die oben identifizierten Preisliste(n) anwendbar sind:

- Beginen Sie damit, zu überprüfen, ob die Start- und Enddaten auf der Registerkarte „Allgemein“ für die angefügten Preisliste nicht leer sind. Wenn die Start- und Enddaten auf den oben identifizierten Preislisten leer sind, haben Sie das Problem isoliert. 
- Notieren Sie das Startdatumfeld auf Ihrem vertrieblichen Ausgaben-Ist-Wert und überprüfen Sie, ob eine der identifizierten Preislisten für das Datum gilt. Beispielsweise sollte das Datum des Ausgaben-Ist-Werts innerhalb eines Startdatums und des Enddatums auf der Preisliste liegen. 
    - Wenn keine Preisliste für das Datum im Ausgaben-Ist-Wert vorhanden ist, haben Sie das Problem isoliert. Ändern Sie die Start- und Enddaten der Preisliste, um sicherzustellen, dass die Preisliste für das Datum des Ausgaben-Ist-Werts gilt. 
    - Wenn mehr als eine Preisliste für das Datum im Ausgaben-Ist-Wert vorhanden ist, haben Sie das Problem isoliert. Sie können das beheben, indem Sie die Start- und Enddaten der Preisliste(n) bearbeiten, sodass nur eine Preisliste vorhanden ist, die für das Datum des Ausgaben-Ist-Werts gilt. 
    - Liegt nur eine Preisliste für das Datum des Ausgaben-Ist-Werts vor, machen Sie bei Überprüfung 3 weiter.
Wenn Sie die erforderlichen Fehlerbehebungen vorgenommen haben, erstellen Sie erneut einen Ausgabeneintrag, genehmigen Sie ihn und stellen Sie sicher, dass der nicht in Rechnung gestellte vertriebliche Ist-Wert einen gültigen Preis anzeigt.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Überprüfung 3: Ist ein gültiger Preis für die Ausgabenkategorie in der anwendbaren Projektpreisliste vorhanden? 

Wenn Sie Überprüfung 1 und 2 erfolgreich abgeschlossen haben, sollte nur eine Projektpreisliste für das Datum des vertrieblichen Ausgaben-Ist-Werts vorhanden sein. Öffnen Sie diese Projektpreisliste und wechseln Sie zur Registerkarte „Kategoriepreise“. Stellen Sie sicher, dass im Raster eine Zeile für die bestimmte Ausgabenkategorie auf dem Ausgaben-Ist-Wert vorhanden ist.
 
- Wenn keine Zeile vorhanden ist, haben Sie das Problem isoliert. Erstellen Sie eine Zeile im Kategoriepreisraster für die Kategorie auf dem Ausgaben-Ist-Wert. Wenn dies durchgeführt ist, erstellen Sie erneut einen Ausgabeneintrag, genehmigen Sie ihn und stellen Sie sicher, dass der nicht in Rechnung gestellte Ist-Wert einen gültigen Preis anzeigt. 
- Wenn eine Zeile für die Ausgabenkategorie im Kategoriepreisraster vorhanden ist, überprüfen Sie, ob ein gültiger Preis darin angegeben ist.

Wenn Sie verstehen möchten, was ein gültiger Preis ist, verwenden Sie diese Methoden:

- Wenn das Feld für die Preisberechnungsmethode auf der Kategoriepreisposition auf „Selbstkostenpreis“ festgelegt ist, wird die Einheitenrate auf dem vertrieblichen Ausgaben-Ist-Wert standardmäßig auf den Wert im Ausgabeneintrag festgelegt.
- Wenn das Feld für die Preisberechnungsmethode auf der Kategoriepreisposition auf „Aufschlagsprozentsatz“ festgelegt ist, überprüfen Sie, ob das Prozentfeld auf einen gültigen Wert festgelegt ist. Die Einheitsrate auf Ihrem vertrieblichen Ausgaben-Ist-Wert wird zum Standard, indem Sie diesen Aufschlagsprozent im Ausgabeneintrag auf den Preis anwenden.
- Wenn das Feld für die Preisberechnungsmethode auf der Kategoriepreisposition auf „Preis pro Einheit“ festgelegt ist, überprüfen Sie, ob das Preisfeld auf einen gültigen Wert festgelegt ist. Die Einheitsrate auf Ihrem vertrieblichen Ausgaben-Ist-Wert wird standardmäßig auf den Währungsbetrag festgelegt, der im Preisfeld angegeben ist.

Wenn der Preis, der für die Ausgabenkategorie eingerichtet wird, nicht gültig ist, dann haben Sie das Problem isoliert. Zur Lösung bearbeiten Sie die Kategoriepreisposition mit einem gültigen Preis für die Ausgabenkategorie laut den oben genannten Regeln. Wenn Sie dies durchgeführt ist, erstellen Sie erneut einen Ausgabeneintrag, überprüfen Sie ihn dann und stellen Sie sicher, dass der nicht in Rechnung gestellte vertriebliche Ist-Wert einen gültigen Preis erhält.

Wird weiterhin keine gültiger Preis auf Ihrem Ausgaben-Ist-Wert angezeigt, nachdem alle drei oben genannten Überprüfungen durchgeführt wurden, reichen Sie ein Support-Ticket ein.




[!INCLUDE[footer-include](../includes/footer-banner.md)]