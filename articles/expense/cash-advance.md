---
title: Vorauskasse
description: In diesem Thema werden Vorauszahlungen erläutert.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908136"
---
# <a name="cash-advance"></a>Vorauskasse

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Mit einer Vorauszahlung können Mitarbeiter Geld von ihrem Unternehmen ausleihen, bevor sie Ausgaben verursachen. Wenn eine angeforderte Vorauszahlung genehmigt und ausgezahlt wird, kann der Mitarbeiter das Geld für die Geschäftsausgaben verwenden, die ihm möglicherweise entstehen. 

## <a name="create-and-submit-a-cash-advance-request"></a>Eine Vorauszahlungsanfrage erstellen und einreichen

1. Wählen Sie unter **Meine Ausgaben** die Option **Vorauszahlungen** > **Neu**, um eine neue Vorauszahlung zu erstellen. 
2. Auf der **Neue Vorauszahlungsanfrage**-Seite geben Sie den Ausgabenzweck ein und wählen Sie den Ort aus, an dem die Ausgaben anfallen.
3. Geben Sie den gewünschten Betrag und die gewünschte Währung ein und wählen Sie dann **Speichern**. 
4. Wenn Sie bereit sind, die Vorauszahlungsanforderung einzureichen, wählen Sie auf der **Vorauszahlungsanfrage**-Seite **Workflow** > **Einreichen** aus.

## <a name="modify-a-cash-advance-request"></a>Eine Vorauszahlungsanforderung ändern

Sie können eine Vorauszahlungsanforderung ändern, wenn sie nicht zur Genehmigung eingereicht wurde.

1. Suchen Sie unter **Meine Ausgaben: Vorauszahlungen** den Vorauszahlungsbetrag, den Sie bearbeiten möchten, und wählen Sie ihn aus.
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

Wenn Sie eine Ausgabenabrechnung für die bereits erhaltene Vorauszahlung erstellen und übermitteln, werden die Ausgaben automatisch an diese Vorauszahlung angepasst. Wenn Ihre Vorauszahlung höher ist als die Ausgaben, müssen Sie den Restbetrag über die **Bargeld zurückgeben**-Ausgabenkategorie an das Unternehmen zurückgeben. Wenn die vom Unternehmen bezahlte Vorauszahlung geringer ist, als der von Ihnen als Ausgaben erfasste Betrag, muss das Unternehmen Ihnen den Restbetrag erstatten. 

### <a name="example"></a>Beispiel
Sie planen, von Seattle zu einer Konferenz in New York City zu reisen. Sie erstellen eine Vorauszahlungsanfrage für 3.000,00 USD, da Sie die Kosten für Konferenzticket, Flüge, Hotel, Mahlzeiten und Taxi auf ungefähr diesen Betrag geschätzt haben. Dies wird erst bezahlt, wenn Ihr Manager diese Anfrage genehmigt hat. Nachdem Ihr Manager eine Genehmigung erteilt hat, wird der angeforderte Vorschuss als 3.000,00 USD auf Ihr Bankkonto gezahlt. Sie nehmen dann an der Konferenz teil. Nach Abschluss Ihrer Reise stellen Sie fest, dass die Gesamtausgaben nur 2.790,00 USD betrugen. Wählen Sie **Kasse** in dem **Zahlungsmethode**-Feld und reichen Sie Ihre Ausgaben für 2.790,00 USD ein. Ihr übermittelter Ausgabenbetrag wird automatisch an der Vorauszahlung von 3.000,00 USD angepasst, der Ihnen verliehen wurde. Sie schulden dem Unternehmen jetzt einen Saldo von 210,00 USD (3.000,00-2.790,00), den Sie mit der **Bargeld zurückgeben**-Ausgabenkategorie zurückgeben. 
