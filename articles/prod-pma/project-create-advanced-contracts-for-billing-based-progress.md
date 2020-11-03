---
title: Erweiterte Verträge für die Abrechnung basierend auf dem Fortschritt erstellen
description: In diesem Thema wird erläutert, wie Sie Projektverträge erstellen, damit Sie Rechnungen für Kunden basierend auf einem Prozentsatz der abgeschlossenen Arbeit erstellen können.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: 1a83785a9db4dffc4585acf11ef971c08594f312
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076653"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Erweiterte Verträge für die Abrechnung basierend auf dem Fortschritt erstellen
[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Projektverträge erstellen, damit Sie Rechnungen für Kunden basierend auf einem Prozentsatz der abgeschlossenen Arbeit erstellen können. Rechnungsbeträge werden automatisch für die Budgetkategorien der Arbeit berechnet, die Sie für ein Projekt eingerichtet haben. Der Rechnungszeitpunkt wird festgelegt, wenn Sie den Projektvertrag mit dem Kunden aushandeln.

Verwenden Sie die Verfahren in diesem Thema, um einen Vertrag, ein zugehöriges Projekt und die Fakturierungsregeln einzurichten, mit denen Rechnungsbeträge für die Budgetkategorien der Arbeit berechnet werden, die Sie für das Projekt eingerichtet haben.

Nachdem Sie den Vertrag und das Projekt erstellt haben, können Sie die Details des Projekts einrichten. Sie können beispielsweise Aktivitäten definieren und dem Projekt Mitarbeiter zuweisen.

## <a name="example"></a>Beispiel

Ihre Organisation ist eine Softwareentwicklungsfirma. Sie erklären sich damit einverstanden, ein Lohnbuchhaltungspaket für einen Kunden für eine Gesamtgebühr von 20.000 US-Dollar (USD) zu entwickeln. Ihre Organisation erklärt sich damit einverstanden, dem Kunden eine Rechnung zu stellen, wenn Sie bestimmte Prozentsätze des Projekts abschließen. Sie richten die folgenden Projektkategorien für die Arbeit ein, damit Sie sie im Fakturierungsprozess verwenden können:

- Beratung
- Entwurf
- Installation

Sie richten auch Fakturierungsregeln ein, die automatisch die Rechnungsbeträge für den Prozentsatz der abgeschlossenen Projektarbeit in jeder Kategorie berechnen.

Der Budgetmanager erstellt ein Budget für die Projektkategorien. Die Menge der abgeschlossenen Arbeit wird automatisch als Prozentsatz der tatsächlichen Arbeit im Vergleich zu den budgetierten Beträgen berechnet.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie ein Projekt erstellen, das Fakturierungsregeln verwendet, müssen Sie die Nummernfolgen für Abrechnungsregeln und ein Gebührenjournal einrichten, mit dem statusbasierte Abrechnungen gebucht werden.

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Einrichtung** \> **Projektmanagement- und Buchhaltungsparameter**.
2. Richten Sie auf der Seite **Projektmanagement- und Buchhaltungsparameter** auf der Registerkarte **Nummernsequenzen** die Nummernsequenz ein, die Sie beim Erstellen von Fakturierungsregeln verwenden möchten.
3. Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Journale** \> **Gebühr**.
4. Wählen Sie auf der Seite **Gebührenjournal** die Option **Neu** aus, und geben Sie den Journalnamen ein.

## <a name="create-a-contract-for-progress-billings"></a>Einen Vertrag für statusbasierte Abrechnungen erstellen

Verwenden Sie dieses Verfahren, um einen Projektvertrag für ein Festpreisprojekt zu erstellen. Sie erstellen eine Projektrechnung, wenn die am Projekt abgeschlossene Arbeit einen bestimmten Prozentsatz erreicht.

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Projekte** \> **Projektverträge**.
2. Wählen Sie auf der Seite **Projektverträge** die Option **Neu** aus.
3. Legen Sie im Dialogfeld **Neuer Projektvertrag** die folgenden Felder fest:

    - **Name**
    - **Finanzierungstyp**
    - **Finanzierungsquelle**
    - **Verkaufswährung** – Standardmäßig wird diese Währung für Kundenrechnungen verwendet, die dem Projektvertrag zugeordnet sind. Sie können jedoch die Verkaufswährung auf einer bestimmten Kundenrechnung ändern.

4. Klicken Sie auf **OK**. Die Informationen werden in den Header der Seite **Projektverträge** kopiert.
5. Füllen Sie auf der Seite **Projektverträge** den Rest der erforderlichen Informationen für das Projekt ein.

## <a name="create-a-project-for-progress-billings"></a>Ein Projekt für statusbasierte Abrechnungen erstellen

Befolgen Sie diese Schritte, um ein Projekt und alle Teilprojekte zu erstellen, die einem Projektvertrag zugeordnet sind.

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Projekte** \> **Alle Projekte**.
2. Wählen Sie auf der Seite **Alle Projekte** die Option **Neu** aus.
3. Wählen Sie im Dialogfeld **Neues Projekt** im Feld **Projekttyp** **Zeit und Material** aus.
4. Wählen Sie eine Projektgruppe aus. Eine Projektgruppe definiert die Buchungsinformationen für die Projekte, die der Gruppe zugeordnet sind.
5. Wählen Sie **Projekt erstellen** aus.
6. Legen Sie nach dem Erstellen des Projekts die Projektphase auf **In Bearbeitung** fest.

## <a name="create-a-budget-for-a-project"></a>Ein Budget für ein Projekt erstellen

Budgetkategorien werden verwendet, um automatisch die Rechnungsbeträge für den Prozentsatz der abgeschlossenen Arbeit für jede Kategorie zu berechnen. Befolgen Sie diese Schritte, um Budgetkategorien für die vorkalkulierten Kosten zu erstellen.

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Projekte** \> **Alle Projekte**.
2. Wählen Sie auf der Seite **Alle Projekte** aus, und öffnen Sie das gewünschte Projekt.
3. Wählen Sie auf der Seite **Projekte** im Aktionsbereich auf der Registerkarte **Plan** in der Gruppe **Budget** die Option **Projektbudget** aus.
4. Geben Sie auf der Seite **Projektbudget** die vorkalkulierten Kosten für jede Kategorie im Projekt ein.

## <a name="create-billing-rules-for-progress-billings"></a>Fakturierungsregeln für statusbasierte Abrechnungen erstellen

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Projekte** \> **Projektverträge**.
2. Wählen Sie auf der Seite **Projektverträge** einen Projektvertrag aus, und öffnen Sie diesen.
3. Wählen Sie auf der Projektvertragsseite im Inforegister **Fakturierungsregeln** die Option **Hinzufügen** aus.
4. Wählen Sie auf der Seite **Fakturierungsregel** im Feld **Zeilentyp** die Option **Status** aus.
5. Geben Sie im Inforegister **Details der Fakturierungsregelpositionen** im Feld **Vertragswert** den Gesamtbetrag des Vertrags ein.
6. Wählen Sie im Feld **Kategorie** die Kategorie aus, in die die Gebührentransaktion gebucht werden soll.
7. Wählen Sie im Feld **Projekt** das Projekt aus, dass diese Fakturierungsregel verwendet.
8. Optional: Weisen Sie weiteren Projekten Fakturierungsregeln zu. Wählen Sie im Inforegister **Projekt** im Abschnitt **Verfügbare Projekte** ein Projekt aus. Wählen Sie dann die Schaltfläche mit dem Rechtspfeil aus, um das Projekt dem Abschnitt **Ausgewählte Projekte** hinzuzufügen.
9. Optional: Berechnen Sie den Prozentsatz, den der Kunde von Zahlungen auf einer Rechnung einbehält. Wählen Sie im Inforegister **Bedingungen für Einbehaltung der Zahlung** die Finanzierungsquelle aus, und geben Sie dann im Feld **Prozentsatz der Einbehaltung** den Prozentsatz der Einbehaltung ein.
10. Wiederholen Sie diese Schritte, um zusätzliche Fakturierungsregeln für den Projektvertrag zu erstellen.
