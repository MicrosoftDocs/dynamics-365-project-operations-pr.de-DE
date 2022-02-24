---
title: Projektbudgets am Ende von Geschäftsjahr übertragen
description: Dieser Artikel enthält Informationen darüber, wie verbleibende Budgetbeträge auf zukünftige Jahre übertragen und Details zum Budgetregister erstellt werden können.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076657"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Projektbudgets am Ende von Geschäftsjahr übertragen

[!include [banner](../includes/banner.md)]

Wenn Sie an einem mehrjährigen Projekt arbeiten, haben Sie möglicherweise am Ende des Geschäftsjahr noch verbleibendes Budget. Sie können die verbleibenden Budgetbeträge in ein zukünftiges Jahr übertragen und Budgetregisterdetails für die Beträge in den zugehörigen Hauptbuchkonten erstellen. Bevor Sie die verbleibenden Beträge vortragen, überprüfen und analysieren Sie die verbleibenden Budgetbeträge.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Die verbleibenden Budgetbeträge überprüfen und analysieren

Führen Sie die folgenden Schritte aus, um die Budgetbeträge zum Jahresende für Projekte zu überprüfen, ohne die Beträge vorzutragen.

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Periodisch** > **Budgets** > **Budgets vortragen**. 
2. Überprüfen Sie auf der Seite **Projektbudgetvortrag-Prozess** auf der Registerkarte **Optionen zum Jahresende**, dass **Verbleibende Projektbudgetbeträge vortragen** nicht aktiviert ist.
3. Wählen Sie auf der Registerkarte **Parameter** im Feld **Projektbudgetjahr** das Geschäftsjahr aus, für das Sie den verbleibenden Budgetbetrag anzeigen möchten. 
4. Wählen Sie im Feld **Eröffnungsgeschäftsjahr** das Geschäftsjahr aus, für das Sie den verbleibenden Budgetbetrag anzeigen möchten. 
5. Wählen Sie im Feld **Von Planzahlenmodell** die Option **Übriges Budget** aus. 
6. Um Projekte einzuschließen, die Ihren Auswahlkriterien entsprechen, und die kein verbleibendes Budget haben, wählen Sie **Anzeigen bei Restbudget von null** aus.  
7. Wählen Sie auf der Registerkarte **Budgets auswählen** die Option **Alle Budgets abrufen** aus, um alle Budgets zu laden, die Ihren ausgewählten Kriterien entsprechen, und dann **Prozess**. 
8. Um eine Datenbankabfrage zu konzipieren, die einen speziellen Satz an Budgets in den Bereich lädt, wählen Sie **Ausgewählte Budgets abrufen** aus.

Um weitere Informationen zu einer bestimmten Zeile im Bereich zu erhalten, wählen Sie die Zeile und dann **Budgetdetails anzeigen** oder **Konten anzeigen** aus.

## <a name="carry-forward-remaining-budget-amounts"></a>Verbleibende Budgetbeträge vortragen 

Wenn Sie verbleibende Budgetbeträge verarbeiten, können Sie in der Finanzbuchhaltung Transaktionen für die Beträge erstellen, die Sie vortragen. Um Transaktionen in der Finanzbuchhaltung zu erstellen, schließen Sie die Schritte im Abschnitt [Budgetbeträge vortragen und Transaktionen in der Finanzbuchhaltung erstellen](#carry-forward) ab. 

> [!NOTE]
> Vorgetragene Budgetbeträge werden in das im Modell ausgewählte Prognosemodell übertragen, das auf der Seite **Prognosemodelle** als Prognosemodell für die Übertragung ausgewählt ist.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Budgetbeträge übertragen und Finanzbuchhaltungstransaktionen erstellen

1.  Wählen Sie **Projektmanagement und -buchhaltung** > **Periodisch** > **Budgets** > **Budgets vortragen** aus. 
2. Wählen Sie auf der Seite **Projektbudgetvortrag-Prozess** die Option **Jahresende** aus, und aktivieren Sie dann **Verbleibende Projektbudgetbeträge vortragen** und **Budgetregistereinträge im Hauptbuch erstellen**. 
3. Wählen Sie auf der Registerkarte **Parameter** in der Feldgruppe **Projektparameter** Folgendes aus:

   - **Projektbudgetjahr**: Wählen Sie den Anfang des Geschäftsjahres aus, für das Sie die verbleibenden Budgetbeträge anzeigen möchten. 
   - **Gewinn und Verlust**: Erstellen Sie Gewinn- und Verlusttransaktionen in der Finanzbuchhaltung. 
   -  **WIP**: Erstellen Sie WIP-Transaktionen in der Finanzbuchhaltung.
   -  **Lohnbuchhaltung**: Erstellen Sie Zuteilungstransaktionen für die Lohnbuchhaltung in der Finanzbuchhaltung. 

5. Geben Sie in der Feldgruppe **Finanzbuchhaltung** die folgenden Informationen ein: 

   - Wählen Sie im Feld **Eröffnungsgeschäftsjahr** das Geschäftsjahr aus, für das Sie die verbleibenden Budgetbeträge für das Projekt übertragen möchten. Der Standardwert liegt ein Jahr nach dem Wert im Feld **Projektbudgetjahr**.
   -  Wählen Sie im Feld **Vortragsperiode** die Periode aus, für die Sie die Budgetregisterdetails in der Finanzbuchhaltung erstellen möchten. Dies ist normalerweise die erste Periode im Eröffnungsgeschäftsjahr.

6. Geben Sie in die Feldgruppe **Kopieren von/nach** die folgenden Informationen ein:

   - Wählen Sie im Feld **Von Planzahlenmodell** das Projektbudget-Planzahlenmodell aus, das den verbleibenden Budgetbeträgen zugeordnet ist, die Sie für die Projekte übertragen möchten. 
   - Wählen Sie im Feld **Zu Sachkontobudgetmodell** das Sachkontobudgetmodell aus, das den verbleibenden Budgetbeträgen zugeordnet ist, die Sie in die Finanzbuchhaltung übertragen möchten. 
   -  Wählen Sie **Verkaufswährung übertragen** aus, um die Verkaufswährung des Projekts für Finanzbuchhaltungstransaktionen zu verwenden, die erstellt werden, wenn Sie die Budgetbeträge für Projekte übertragen. Wenn die Option nicht ausgewählt ist, verwenden Sie die Transaktionen der Buchhaltungswährung. 
   -  Wählen Sie **Anzeigen bei Restbudget von null** aus, um Projekte einzuschließen, die keine verbleibenden Budgetbeträge haben, aber die anderen Kriterien erfüllen, die Sie in den im unteren Bereich angezeigten Projekten auswählen.

7. Wählen Sie auf der Registerkarte **Budgets auswählen** die Option **Alle Budgets abrufen** aus, um alle Budgets zu laden, die Ihren ausgewählten Kriterien entsprechen. Wenn Sie es bevorzugen, eine Datenbankabfrage zu konzipieren, die einen speziellen Satz an Projektbudgets in den Bereich lädt, wählen Sie **Ausgewählte Budgets abrufen** aus.
8. Wählen Sie für jedes Projekt, das Sie verarbeiten möchten, die Option am Anfang der Zeile für das Projekt aus.

    > [!TIP]
    > Um alle oder die meisten Projekte auszuwählen, aktivieren Sie das Häkchen in der oberen linken Ecke. Deaktivieren Sie das Häkchen für dieses Projekt, um die Verarbeitung eines Projekts auszuschließen.

9. Um die verbleibenden Budgetbeträge für die ausgewählten Projekte in das ausgewählte Geschäftsjahr zu übertragen und Budgetregisterdetails in der Finanzbuchhaltung zu erstellen, wählen Sie **Prozess** aus.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Budgetbeträge übertragen ohne Finanzbuchhaltungstransaktionen zu erstellen

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Periodisch** > **Budgets** > **Budgets vortragen**.
2. Wählen Sie auf der Seite **Projektbudgetvortrag-Prozess** im Feld **Optionen zum Jahresende** die Option **Verbleibende Projektbudgetbeträge vortragen** aus.
3. Wählen Sie in der Gruppe **Parameter** im Feld **Projektbudgetjahr** das Geschäftsjahr aus, für das Sie die verbleibenden Budgetbeträge anzeigen möchten.
4. Geben Sie in die Gruppe **Kopieren von/nach** die folgenden Informationen ein:

   - Wählen Sie im Feld **Von Planzahlenmodell** das Projektbudget-Planzahlenmodell aus, das den verbleibenden Budgetbeträgen zugeordnet ist, die Sie für die Projekte übertragen möchten. 
   - Wählen Sie **Anzeigen bei Restbudget von null** aus, um Projekte einzuschließen, die keine verbleibenden Budgetbeträge haben, aber die anderen von Ihnen ausgewählten Kriterien erfüllen.
   - Wählen Sie in der Gruppe **Budgets auswählen** die Option **Alle Budgets abrufen** aus, um alle Budgets zu laden, die Ihren ausgewählten Kriterien entsprechen. Um eine Datenbankabfrage zu konzipieren, die einen speziellen Satz an Projektbudgets in den Bereich lädt, wählen Sie **Ausgewählte Budgets abrufen** aus.

5. Wählen Sie für jedes Projekt, das Sie verarbeiten möchten, die Option am Anfang der Zeile für das Projekt aus. 
6. Wählen Sie **Prozess** aus, um die verbleibenden Budgetbeträge für die ausgewählten Projekte an das ausgewählte Geschäftsjahr zu übertragen.

