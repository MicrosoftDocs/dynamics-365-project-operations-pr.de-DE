---
title: Genehmigte Zeit- oder Ausgabeneinträge zurückrufen
description: Dieses Thema enthält Informationen zum Zurückrufen einer zuvor genehmigten Zeit- oder -Ausgabentransaktion.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 74df6e196c9f060f957d79aebc9640a162fb2913
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722055"
---
# <a name="recall-approved-time-or-expense-entries"></a>Genehmigte Zeit- oder Ausgabeneinträge zurückrufen

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ein Projektteammitglied oder eine andere Person, die einen Zeit- oder Ausgabeneintrag übermittelt, kann selbigen nach der Genehmigung wieder zurückrufen. Das Zurückrufen eines genehmigten Zeit- oder Ausgabeneintrags umfasst zwei Schritte:

1. Ein Antragsteller fordert einen Rückruf an.
2. Eine genehmigende Person genehmigt den Rückruf.

## <a name="request-a-recall"></a>Anforderung eines Rückrufs

Führen Sie die folgenden Schritte aus, um den Rückruf eines zuvor genehmigten Zeit- bzw. Ausgabeneintrags anzufordern.

1. Navigieren Sie für Zeiteinträge zu **Projekte** \> **Meine Arbeit** \> **Zeiteintrag**.

    – oder –

    Navigieren Sie für Ausgabeneinträge zu **Projekte** \> **Meine Arbeit** \> **Ausgaben**.

2. Wählen Sie für Zeiteinträge alle Zeiteinträge für eine bestimmte Kombination aus Projekt und Aufgabe aus. Alternativ können Sie im Raster die einzelnen Zellen für die Zeit an einem bestimmten Datum für ein bestimmtes Projekt auswählen.

    – oder –

    Für Ausgabeneinträge wählen Sie die Zeile für den Ausgabeneintrag aus, der zurückgerufen werden soll.

3. Klicken Sie auf **Zurückrufen**. Ein Bestätigungsdialogfeld wird angezeigt. Falls die ausgewählten Zeit- und Ausgabeneinträge bereits genehmigt wurden, werden Sie aufgefordert, einen Grund für den Rückruf einzugeben.
4. Geben Sie einen Grund für den Rückruf ein und wählen Sie dann **OK** aus, um den Vorgang zu bestätigen. Das System sendet eine Anforderung an die Person, von der die Einträge genehmigt wurden, den Rückruf zu genehmigen.

> [!NOTE]
> Obwohl genehmigte Zeit- und Ausgabeneinträge zurückgerufen werden können, kann keine Rückrufanforderung erstellt werden, falls eine genehmigte Zeit oder Ausgabe dem Kunden bereits in Rechnung gestellt wurde. Ein Benutzer, der versucht, eine Rückrufanforderung zu erstellen, erhält eine Nachricht, die angibt, dass die Zeit oder Ausgabe nicht zurückgerufen werden kann, da sie bereits in Rechnung gestellt wurde.

## <a name="approve-or-reject-a-recall-request"></a>Genehmigen oder Ablehnen einer Rückrufanforderung

Führen Sie die folgenden Schritte aus, um eine Rückrufanforderung zu genehmigen oder abzulehnen.

1. Wechseln Sie zu **Projekte** \> **Meine Arbeit** \> **Genehmigungen**.
2. Ändern Sie auf der Listenseite **Genehmigungen** die Ansicht zu **Rückrufanforderungen zur Genehmigung**. Eine Liste der übermittelten Rückrufanforderungen wird angezeigt.
3. Wählen Sie einen oder mehrere Einträge aus und wählen Sie dann **Genehmigen** oder **Ablehnen** aus.
4. Wenn Sie **Genehmigen** ausgewählt haben, erhalten Sie eine Warnmeldung, in der die Auswirkungen der Genehmigung erläutert werden. Wählen Sie **OK** aus, um den Vorgang zu bestätigen. Die Rückrufanforderung wird genehmigt.

    – oder –

    Wenn Sie **Ablehnen** ausgewählt haben, wird die Rückrufanforderung abgelehnt.

> [!NOTE]
> Wie bei einer Rückrufanforderung prüft das System auch bei der Genehmigung eines Rückrufs, ob für die Zeit- oder Ausgabeneinträge bereits Rechnungen gestellt wurden. Wenn ein Eintrag bereits in Rechnung gestellt wurde oder sich auf einem Rechnungsentwurf befindet, erhält die genehmigende Person eine Fehlermeldung, dass für die Zeit oder Ausgabe kein Rückruf genehmigt werden können, da sie bereits in Rechnung gestellt wurde.

## <a name="impact-of-a-recall-request"></a>Auswirkungen einer Rückrufanforderung

Das Zurückrufen einer Genehmigung hat sowohl betriebliche als auch finanzielle Auswirkungen.

### <a name="operational-impact"></a>Betriebliche Auswirkungen

Wenn eine Rückrufanforderung genehmigt wird, wird der Genehmigungsdatensatz als **Abgelehnt** markiert. Der Status des Eintrags wird entweder in **Zurückgegeben** oder in **Abgelehnt** geändert, je nachdem, ob es sich um einen Zeiteintrag oder einen Ausgabeneintrag handelt.

Das Projektteammitglied kann Einträge anzeigen, bearbeiten, erneut senden oder vollständig löschen.

Wenn eine Rückrufanforderung abgelehnt wird, behält der Eintrag den Status **Genehmigt** und kann vom Projektteammitglied oder der genehmigenden Person für das Projekt nicht bearbeitet werden.

### <a name="financial-impact"></a>Finanzielle Auswirkungen

Wenn eine Rückrufanforderung genehmigt wird, werden zunächst die entsprechenden Istwerte für Kosten und Vertrieb folgendermaßen aktualisiert:

- Das Feld **Anpassungsstatus** wird zu **Angepasst** aktualisiert.
- Das Feld **Fakturierungsstatus** wird zu **Storniert** aktualisiert.

Als Nächstes werden Umkehrungseinträge in der Tabelle „Ist-Werte” erstellt. Zum Erstellen von Umkehrungseinträgen kopiert das System die Feldwerte aus den ursprünglichen Ist-Werten. Die einzigen Werte, die nicht übernommen werden, sind die Mengenwerte. Diese Werte werden stattdessen umgekehrt. Umgekehrte Ist-Werte werden sowohl für **Kosten** als auch für Ist-Werte von **Nicht fakturierten Umsätzen** erstellt. Das Feld **Anpassungsstatus** der umgekehrten Ist-Werte wird auf **Nicht anpassbar** festgelegt und das Feld **Fakturierungsstatus** auf **Storniert**. Aufgrund dieser Änderungen stellen die erfassten Ausgaben und das Umsatz-Rückstandsprotokoll des Projekts nicht länger die Ist-Werte dar.

Wenn eine Rückrufanforderung abgelehnt wird, hat dies keine finanziellen Auswirkungen auf das Projekt.

## <a name="changes-to-time-entry-records"></a>Änderungen an Zeiteintragsdatensätzen

Die folgende Abbildung zeigt die Änderungen, die für genehmigte Zeiteinträge auftreten, wenn sie zurückgerufen werden.

![Statusübergänge für Zeiteinträge](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Änderungen an Ausgabeneintragsdatensätzen

Die folgende Abbildung zeigt die Änderungen, die für genehmigte Ausgabeneinträge auftreten, wenn sie zurückgerufen werden.

![Statusübergänge für Ausgabeneinträge](media/ExpenseEntryStateTransitions.png)
