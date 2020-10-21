---
title: Ein Angebot abschließen
description: Dieses Thema bietet Informationen zum Abschluss von Angeboten in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c429fa14b4b95420c67a91a6a59af7db2660f68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898890"
---
# <a name="close-a-quote"></a>Ein Angebot abschließen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Ein Projektangebot kann als „Gewonnen“ oder „Verloren“ geschlossen werden. Da die Funktionen „Aktivieren“ und „Überarbeiten“ in Angeboten in Microsoft Dynamics 365 Project Operations nicht unterstützt werden, können Sie den Angebotsentwurf schließen.

## <a name="close-a-quote-as-won"></a>Ein Angebot als „Gewonnen“ schließen

Wenn Sie ein Projektangebot als „Gewonnen“ schließen, wird der Status des Angebots auf **Geschlossen** und der Statusgrund auf **Gewonnen** gesetzt. Durch das Schließen der Angebote wird das Projektangebot schreibgeschützt, und es wird ein Entwurf eines Projektvertrags erstellt, der alle Angebotsinformationen enthält. Da ein geschlossenes Angebot nicht erneut geöffnet werden kann, werden Ihre Änderungen in einem Bestätigungsdialogfeld bestätigt, bevor Sie ein Angebot schließen.

Der aus einem Projektangebot erstellte Projektvertrag wird auch im Modul „Projektmanagement und -buchhaltung“ von Project Operations zur Verfügung gestellt. Wenn ein Projektvertrag keinem Projekt in einer seiner Zeilen zugeordnet ist, wird dieser Projektvertrag als inaktiver Projektvertrag zur Verfügung gestellt. Er wird aktiv, sobald ein Projekt mindestens einer seiner Vertragszeilen zugeordnet wird.

Wenn das Angebot an eine Verkaufschance angehängt ist, werden alle anderen Projektangebote für die Verkaufschance automatisch als „Verloren“ geschlossen.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finanzielle Auswirkungen des Abschlusses eines Angebots als „Gewonnen“

Wenn für ein Projekt tatsächliche Zeitangaben aufgezeichnet wurden, während es noch einem Angebotsentwurf beigefügt ist, werden nur die Kosten für die Zeit oder die Kosten erfasst. Nachdem ein Angebot als „Gewonnen“ geschlossen wurde, werden die Kosten von der Anwendung umgestaltet, indem die älteren tatsächlichen Kosten zurückgebucht und neue tatsächliche Kosten erneut erstellt werden. Die Anwendung verarbeitet diese Istkosten basierend auf der Abrechnungsmethode der zugehörigen Projektvertragszeile. Wenn sich die tatsächlichen Kosten auf eine Zeit- und Materialvertragszeile beziehen, erstellt das System automatisch die entsprechenden nicht in Rechnung gestellten Umsatz-Istwerte, wenn das Angebot geschlossen und der Projektvertrag erstellt wird. Wenn sich die tatsächlichen Kosten auf eine Festpreisvertragszeile beziehen, beendet die Anwendung die erneute Verabeitung der tatsächlichen Kosten basierend auf den Regeln für die getrennte Abrechnung für die Projektvertragskunden.

Alle erneut verarbeiteten Istdaten stehen im Modul „Projektmanagement und -buchhaltung“ zur Verfügung, damit der Projektbuchhalter sie überprüfen, aktualisieren und in die Finanzbuchhaltung buchen kann. 

## <a name="close-a-quote-as-lost"></a>Ein Angebot als „Verloren“ schließen

Wenn Sie ein Projektangebot als „Verloren“ schließen, wird der Status auf **Geschlossen** und der Statusgrund auf **Verloren** gesetzt. Wenn Sie das Angebot schließen, ist es schreibgeschützt. Da ein geschlossenes Angebot nicht erneut geöffnet werden kann, werden Ihre Änderungen in einem Bestätigungsdialogfeld bestätigt, bevor Sie ein Angebot schließen.

Wenn für das als verloren geschlossene Projektangebot auf ein Projekt in einer seiner Zeilen verwiesen wird, wird dieses Projekt auch als geschlossen markiert und alle Ressourcenbuchungen ab diesem Tag werden storniert.

> [!NOTE]
> In Project Operations wirkt sich das Schließen eines Angebots als „Gewonnen“ oder „Verloren“ nicht auf den Status der Verkaufschance aus, die geöffnet bleibt, bis sie manuell geschlossen wird.
