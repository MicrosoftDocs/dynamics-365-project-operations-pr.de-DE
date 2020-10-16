---
title: Genehmigungen – Übersicht
description: Dieses Thema bietet Informationen zur Arbeit mit Genehmigungen in Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961165"
---
# <a name="approvals-overview"></a>Genehmigungen – Übersicht

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Zeit- und Kostenübermittlungen durchlaufen einen Genehmigungs-Workflow. Nachdem die Einträge genehmigt wurden, werden Transaktionen in tatsächlichen Daten erfasst oder die Zeit wird im Zeitplan gebucht.

## <a name="approvals-workflow"></a>Genehmigungs-lWorkflow
Wenn Sie einen Zeit- oder Kosteneintrag erstellen und senden, wird ein Genehmigungseintrag erstellt. Der Projektgenehmiger oder Ihr Manager überprüft und genehmigt Ihren Eintrag. Wenn sich der Eintrag auf ein Projekt bezieht und dessen Genehmigung vorliegt, werden die Ist-Daten erstellt. Dadurch können die Kosten und die Abrechnung nachverfolgt werden. 

## <a name="approve-an-entry"></a>Einen Eintrag genehmigen
Mit dem **Genehmigungen**-Formular können Sie zwischen verschiedenen Ansichten wechseln, um die verschiedenen Arten von Genehmigungen anzuzeigen.
  
1. Wechseln Sie zum **Genehmigungen**-Formular und wählen Sie **Ausgaben**, **Zeit** oder **Rückrufe**.
2. Überprüfen Sie jede Genehmigung und wählen Sie diejenigen aus, die Sie genehmigen möchten.
3. Wählen Sie **Genehmigen**, um die ausgewählten Einträge zu genehmigen.
Das System verarbeitet diese Einträge und erstellt Ist-Daten oder eine Buchung.

## <a name="reject-an-entry"></a>Einen Eintrag ablehnen
Als Projektgenehmiger müssen Sie möglicherweise einen Eintrag zur Korrektur an einen Benutzer zurücksenden.
  
1. Wechseln Sie zum **Genehmigungen**-Formular und wählen Sie den Eintrag aus, den Sie ablehnen möchten. 
2. Wählen **Ablehnen**.
3. Optional – Fügen Sie einen Kommentar in den **Ablehnungskommentare**-Dialog ein, um den Benutzer darüber zu informieren, warum der Eintrag abgelehnt wird.
4. Klicken Sie auf **OK**. Der Eintrag wird an den Benutzer zurückgegeben.
  
## <a name="recall-entries"></a>Einträge zurückrufen
Irgendwann müssen Sie möglicherweise einen übermittelten Eintrag zurückrufen. Wenn der Eintrag nicht genehmigt wurde, wird er sofort zurückgesandt. Ein genehmigter Eintrag kann jedoch wesentliche Auswirkungen haben. Der Projektgenehmiger muss den Rückruf genehmigen, um die Transaktion in Ist-Daten zu stornieren.

## <a name="specify-project-approvers"></a>Projektgenehmiger angeben
Jedes Projekt hat eine Reihe von Projektteammitgliedern. Sie können angeben, welche Teammitglieder auch Projektgenehmiger sind.

1. Wechseln Sie zum **Projekte**-Formular und öffnen Sie das Projekt aus der Liste.
2. Auf der **Team**-Registerkarte wählen Sie das Teammitglied aus, das als Projektgenehmiger fungieren soll, und wählen Sie dann aus **Bearbeiten**.
3. Legen Sie das Feld **Projektgenehmiger** auf **Ja** fest.
4. Wählen Sie **Speichern** aus.
5. Wiederholen Sie die Schritte 2 bis 4, um weitere Projektgenehmiger hinzuzufügen.

## <a name="configure-the-users-manager"></a>Den Manager des Benutzers konfigurieren

1. Gehen Sie zu **Einstellungen** > **Sicherheit** > **Benutzer**.
2. Wählen Sie den Benutzer, dem Sie einen Manager zuweisen, und im Bereich **Organisationsinformationen** wählen Sie den Manager aus der Liste aus. 
3. Wählen Sie **Speichern** aus.


