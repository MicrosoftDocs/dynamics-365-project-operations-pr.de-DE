---
title: Genehmigungen – Übersicht
description: Dieser Artikel enthält Informationen über die Arbeit mit Genehmigungen in Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: d5b5c93dc948992505054ef7b17579aafcdf8f8d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924705"
---
# <a name="approvals-overview"></a>Genehmigungen – Übersicht

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Zeit-, Kosten- und Materialverbrauchsübermittlungen durchlaufen einen Genehmigungsworkflow. Nachdem die Einträge genehmigt wurden, werden Transaktionen in tatsächlichen Daten erfasst oder die Zeit wird im Zeitplan gebucht.

## <a name="approvals-workflow"></a>Genehmigungs-lWorkflow
Wenn Sie einen Zeit-, Kosten- oder Materialverbrauchseintrag erstellen und senden, wird ein Genehmigungsdatensatz erstellt. Der Projektgenehmiger oder Manager überprüft und genehmigt den Eintrag. Wenn sich der Eintrag auf ein Projekt bezieht, werden die Istdaten erstellt, wenn sie genehmigt werden. Dadurch können die Kosten und die Abrechnung nachverfolgt werden.

## <a name="approve-an-entry"></a>Einen Eintrag genehmigen
Auf der Seite **Genehmigungen** können Sie zwischen verschiedenen Ansichten wechseln, um die verschiedenen Arten von Genehmigungen anzuzeigen.
  
1. Gehen Sie zur Seite **Genehmigungen** und wählen Sie **Kosten**, **Zeit**, **Materialverbrauch** oder **Rückrufe** aus.
2. Überprüfen Sie jede Genehmigung und wählen Sie diejenigen aus, die Sie genehmigen möchten.
3. Wählen Sie **Genehmigen**, um die ausgewählten Einträge zu genehmigen.
Das System verarbeitet diese Einträge und erstellt Istwerte.

## <a name="reject-an-entry"></a>Einen Eintrag ablehnen
Als Projektgenehmiger müssen Sie möglicherweise einen Eintrag zur Korrektur an einen Benutzer zurücksenden.
  
1. Gehen Sie zur Seite **Genehmigungen** und wählen Sie den Eintrag aus, den Sie ablehnen möchten. 
2. Wählen **Ablehnen**.
3. Fügen Sie optional einen Kommentar in das Dialogfeld **Kommentare zur Ablehnung** ein, um den Benutzer darüber zu informieren, warum der Eintrag abgelehnt wird.
4. Klicken Sie auf **OK**. Der Eintrag wird an den Benutzer zurückgegeben.
  
## <a name="cancel-approval"></a>Genehmigung abbrechen
In einigen Fällen müssen Sie möglicherweise einen zuvor genehmigten Eintrag stornieren. Das Stornieren eines zuvor genehmigten Eintrags hat finanzielle Auswirkungen. 

## <a name="approving-recall-requests"></a>Rückrufanforderungen genehmigen
In einigen Fällen muss ein Berater möglicherweise einen zuvor genehmigten Eintrag zurückrufen. Das Stornieren eines zuvor genehmigten Eintrags hat finanzielle Auswirkungen. Der Projektgenehmiger muss den Rückruf genehmigen, um die Transaktion in den tatsächlichen Transaktionen rückgängig zu machen.

## <a name="specify-project-approvers"></a>Projektgenehmiger angeben
Jedes Projekt hat eine Reihe von Projektteammitgliedern. Sie können angeben, welche Teammitglieder auch Projektgenehmiger sind.

1. Gehen Sie zur Seite **Projekte** und öffnen Sie das Projekt aus der Liste.
2. Auf der **Team**-Registerkarte wählen Sie das Teammitglied aus, das als Projektgenehmiger fungieren soll, und wählen Sie dann aus **Bearbeiten**.
3. Legen Sie das Feld **Projektgenehmiger** auf **Ja** fest.
4. Wählen Sie **Speichern** aus.
5. Wiederholen Sie die Schritte 2 bis 4, um weitere Projektgenehmiger hinzuzufügen.

## <a name="configure-the-users-manager"></a>Den Manager des Benutzers konfigurieren

1. Gehen Sie zu **Einstellungen** > **Sicherheit** > **Benutzer**.
2. Wählen Sie den Benutzer, dem Sie einen Manager zuweisen, und im Bereich **Organisationsinformationen** wählen Sie den Manager aus der Liste aus. 
3. Wählen Sie **Speichern** aus.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
