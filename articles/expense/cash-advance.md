---
title: Vorauskasse
description: In diesem Thema werden Vorauszahlungen erläutert.
author: suvaidya
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 58864790720824cecad8ce1ff7ff0a335a42cc03
ms.sourcegitcommit: 7aa0b7fb22213d8baa2d69efece9a636d9f62493
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098883"
---
# <a name="cash-advance"></a>Vorauskasse

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Mit einer Vorauszahlung können Mitarbeiter Geld von ihrem Unternehmen ausleihen, bevor sie Ausgaben verursachen. Wenn eine angeforderte Vorauszahlung genehmigt und ausgezahlt wird, kann der Mitarbeiter das Geld für die Geschäftsausgaben verwenden, die ihm möglicherweise entstehen. 

## <a name="create-and-submit-a-cash-advance-request"></a>Eine Vorauszahlungsanfrage erstellen und einreichen
Gehen Sie wie folgt vor, um einen neuen Vorschuss zu erstellen und einen Vorschussantrag zu stellen: 

1. Unter **Meine Ausgaben**, wählen Sie **Bargeldbezüge** > **Neu**. 
2. Auf der **Neue Vorauszahlungsanfrage**-Seite geben Sie den Ausgabenzweck ein und wählen Sie den Ort aus, an dem die Ausgaben anfallen.
3. Geben Sie den gewünschten Betrag und die gewünschte Währung ein und wählen Sie dann **Speichern**. 
4. Wenn Sie bereit sind, die Vorauszahlungsanforderung einzureichen, wählen Sie auf der **Vorauszahlungsanfrage**-Seite **Workflow** > **Einreichen** aus.

## <a name="modify-a-cash-advance-request"></a>Eine Vorauszahlungsanforderung ändern

Sie können eine Vorauszahlungsanforderung ändern, wenn sie nicht zur Genehmigung eingereicht wurde.

1. Unter **Meine Ausgaben: Barvorschüsse** Suchen Sie den Bargeldvorschuss, den Sie bearbeiten möchten, und wählen Sie ihn aus.
2. Wählen Sie **Bearbeiten** und nehmen Sie die erforderlichen Änderungen an der Vorauszahlungsanforderung vor. 
3. Wählen Sie **Speichern und schließen** aus.


## <a name="view-cash-advance-requests"></a>Vorauszahlungsanfragen anzeigen
Unter **Meine Ausgaben: Vorauszahlungen** können Sie die Liste aller Vorauszahlungen überprüfen, die sich im Entwurf befinden, eingereicht, überprüft oder gezahlt wurden. 

## <a name="approve-cash-advance-requests"></a>Vorauszahlungsanfragen genehmigen

Manager oder Benutzer, die im Workflow als Genehmigende konfiguriert sind, können die ihnen zur Überprüfung übermittelten Vorauszahlungen genehmigen. 

1. Um eine Vorauszahlung zu genehmigen, wählen Sie unter **Vorauszahlungen verarbeiten** die Option **Vorauszahlungen für meine Überprüfung**.
2. Wählen Sie die Vorauszahlung aus, die Sie überprüfen müssen, und wählen Sie **Genehmigen**.  

## <a name="pay-cash-advances"></a>Vorauszahlungen auszahlen 
Das folgende Verfahren wird normalerweise von einem Buchhalter oder einem Benutzer mit Buchhaltungsberechtigungen ausgeführt.

1. Wählen Sie **Genehmigte Vorauszahlungen** aus, um genehmigte Vorauszahlungen zu buchen, und dann wählen Sie **Auszahlen und überweisen**.  
2. Geben Sie die Erfassungsdetails für die Vorauszahlungen ein und wählen Sie dann **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Eine Ausgabenabrechnung für eine bezahlte Vorauszahlung einreichen 

Wenn Sie eine Ausgabenabrechnung für den bereits erhaltenen Vorschuss erstellen und übermitteln, werden die Ausgaben automatisch an diesen Vorschuss angepasst. Wenn Ihre Vorauszahlung höher ist als die Ausgaben, müssen Sie den Restbetrag über die **Bargeld zurückgeben**-Ausgabenkategorie an das Unternehmen zurückgeben. Wenn der vom Unternehmen bezahlte Vorschuss geringer ist als der Betrag, den Sie als Aufwand erfasst haben, muss das Unternehmen Ihnen den Restbetrag erstatten. 

### <a name="example"></a>Beispiel
Sie planen, für eine Konferenz von Seattle nach New York City zu reisen. Sie erstellen eine Vorauszahlungsanfrage für 3000.00 USD basierend auf den geschätzten Kosten für Konferenzticket, Flüge, Hotel, Mahlzeiten und Taxi. Sie werden erst bezahlt, wenn Ihr Manager diese Anfrage genehmigt. Nachdem Ihr Manager eine Genehmigung erteilt hat, wird der angeforderte Vorschuss als 3.000,00 USD auf Ihr Bankkonto gezahlt. Sie nehmen dann an der Konferenz teil. Nach Abschluss Ihrer Reise stellen Sie fest, dass die Gesamtausgaben nur 2.790,00 USD betrugen. Wählen Sie das Feld **Kasse** unter **Zahlungsmethode** und senden Sie Ihre Ausgaben für 2790.00 USD. Ihr übermittelter Ausgabenbetrag wird automatisch an der Vorauszahlung von 3.000,00 USD angepasst, der Ihnen verliehen wurde. Sie schulden jetzt einen Saldo von 210.00 USD (3000.00 – 2790.00), den Sie an das Unternehmen zurückgeben können mit der Ausgabenkategegorie **Bargeld zurückgeben**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]