---
title: Rückruf zuvor genehmigter Einträge
description: Dieses Thema erklärt, wie ein Projektteammitglied den Rückruf von zuvor eingereichten und genehmigten Zeit-, Ausgaben- und Materialverbrauchsdatensätzen beantragen kann und wie ein Projektmanager Rückrufanträge genehmigen oder ablehnen kann.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586573"
---
# <a name="recall-previously-approved-entries"></a>Rückruf zuvor genehmigter Einträge

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Ein Projektteammitglied, sas einen Zeit- oder Ausgaben- oder Materialnutzungseintrag übermittelt, kann selbigen nach der Genehmigung wieder zurückrufen. Der Rückrufvorgang besteht aus zwei Hauptschritten:

1. Ein Antragsteller fordert einen Rückruf an.
2. Eine genehmigende Person genehmigt die Rückrufanfrage.

## <a name="request-a-recall"></a>Anforderung eines Rückrufs

Führen Sie die folgenden Schritte aus, um den Rückruf eines zuvor genehmigten Zeit-, Ausgaben oder Materialnutzungseintrags anzufordern.

1. Führen Sie diese Schritte aus, je nachdem, welche Art von Eintrag Sie zurücjrufen möchten:

    - Gehen Sie für Zeiteinträge zu **Eigenschaften** \> **Meine Arbeit** \> **Zeiteintrag** und wählen Sie alle Zeiteinträge für eine bestimmte Kombination aus Projekt und Aufgabe aus. Alternativ können Sie im Raster die einzelnen Zellen für die Zeit an einem bestimmten Datum für ein bestimmtes Projekt auswählen.
    - Für Ausgabeneinträge gehen Sie zu **Projekte** \> **Meine Arbeit** \> **Ausgaben**, und wählen Sie die Zeile für den Ausgabeneintrag aus, der zurückgerufen werden soll.
    - Für Materialnutzungseinträge gehen Sie zu **Projekte** \> **Meine Arbeit** \> **Materialnutzungsprotokoll**, und wählen Sie die Zeile für den Ausgabeneintrag aus, der zurückgerufen werden soll.

2. Wählen Sie **Zurückrufen** aus. Ein Bestätigungsdialogfeld wird angezeigt. Falls die ausgewählten Zeit-, Ausgaben- oder Materialnutzungseinträge bereits genehmigt wurden, werden Sie aufgefordert, einen Grund für den Rückruf einzugeben.
3. Geben Sie einen Grund für den Rückruf ein und wählen Sie dann **OK** aus, um den Vorgang zu bestätigen. Das System sendet eine Anforderung an die Person, von der die Einträge genehmigt wurden, den Rückruf zu genehmigen.

> [!IMPORTANT]
> Sie können keine Rückrufanforderung für einen genehmigten Zeit-, Ausgaben- oder Materialverbrauchseintrag erstellen, der dem Kunden bereits in Rechnung gestellt wurde. Wenn Sie dies versuchen, erhalten Sie eine Nachricht, die angibt, dass der Zeit-, Ausgaben- oder Materialverbrauchseintrag nicht zurückgerufen werden kann, da sie bereits in Rechnung gestellt wurde. In diesem Fall können Sie nur dann einen Rückruf der Buchung anfordern, wenn eine Korrekturrechnung verwendet wird, um dem Kunden eine vollständige Gutschrift oder Rückerstattung auf die ursprüngliche Rechnung zu erteilen.

## <a name="approve-or-reject-a-recall-request"></a>Genehmigen oder Ablehnen einer Rückrufanforderung

Führen Sie die folgenden Schritte aus, um eine Rückrufanforderung zu genehmigen oder abzulehnen.

1. Wechseln Sie zu **Projekte** \> **Meine Arbeit** \> **Genehmigungen**.
2. Ändern Sie auf der Listenseite **Genehmigungen** die Ansicht zu **Rückrufanforderungen zur Genehmigung**. Eine Liste der übermittelten Rückrufanforderungen wird angezeigt.
3. Wählen Sie einen oder mehrere Einträge aus und wählen Sie dann **Genehmigen** oder **Ablehnen** aus.
4. Wenn Sie **Genehmigen** ausgewählt haben, erhalten Sie eine Warnmeldung, in der die Auswirkungen der Genehmigung erläutert werden. Wählen Sie **OK** aus, um den Vorgang zu bestätigen. Die Rückrufanforderung wird genehmigt.

    – oder –

    Wenn Sie **Ablehnen** ausgewählt haben, wird die Rückrufanforderung abgelehnt.

> [!IMPORTANT]
> Wenn ein Rückruf gehemigt wurde, prüft das System, wie bei der Anforderung, ob für die Zeit-, Ausgaben- oder Materialverbrauchseinträge bereits Rechnungen gestellt wurden. Wenn ein Eintrag bereits in Rechnung gestellt wurde oder sich auf einem Rechnungsentwurf befindet, erhält die genehmigende Person eine Fehlermeldung, dass für die Zeit oder Ausgabe kein Rückruf genehmigt werden können, da sie bereits in Rechnung gestellt wurde. In diesem Fall kann die genehmigende Person den Rückruf nur genehmigen, wenn eine Korrekturrechnung verwendet wird, um dem Kunden eine vollständige Gutschrift oder Rückerstattung auf die ursprüngliche Rechnung zu erteilen.

## <a name="impact-of-a-recall-request"></a>Auswirkungen einer Rückrufanforderung

Das Zurückrufen einer Genehmigung hat sowohl betriebliche als auch finanzielle Auswirkungen.

### <a name="operational-impact"></a>Betriebliche Auswirkungen

Wenn eine Rückrufanforderung genehmigt wird, wird der Genehmigungsdatensatz als **Abgelehnt** markiert. Der Status des Eintrags wird entweder in **Zurückgegeben** oder in **Abgelehnt** geändert, je nachdem, ob es sich um einen Zeit-, Ausgaben- oder Materialverbrauchseintrag handelt.

Das Projektteammitglied kann Einträge anzeigen, bearbeiten, erneut senden oder vollständig löschen.

Wenn eine Rückrufanforderung abgelehnt wird, behält der Eintrag den Status **Genehmigt** und kann vom Projektteammitglied oder der genehmigenden Person für das Projekt nicht bearbeitet werden.

### <a name="financial-impact"></a>Finanzielle Auswirkungen

Wenn eine Rückrufanforderung genehmigt wird, werden zunächst die entsprechenden Istwerte für Kosten und Vertrieb folgendermaßen aktualisiert:

- Das Feld **Anpassungsstatus** wird zu **Angepasst** aktualisiert.
- Das Feld **Fakturierungsstatus** wird zu **Storniert** aktualisiert.

Als Nächstes werden Umkehrungseinträge in der Tabelle „Ist-Werte“ erstellt. Zum Erstellen von Umkehrungseinträgen kopiert das System die Feldwerte aus den ursprünglichen Ist-Werten. Die einzigen Werte, die nicht übernommen werden, sind die Mengenwerte. Diese Werte werden stattdessen umgekehrt. Umgekehrte Ist-Werte werden sowohl für **Kosten** als auch für Ist-Werte von **Nicht fakturierten Umsätzen** erstellt. Das Feld **Anpassungsstatus** der umgekehrten Ist-Werte wird auf **Nicht anpassbar** festgelegt und das Feld **Fakturierungsstatus** auf **Storniert**. Aufgrund dieser Änderungen stellen die erfassten Ausgaben und das Umsatz-Rückstandsprotokoll des Projekts nicht länger die Ist-Werte dar.

Wenn eine Rückrufanforderung abgelehnt wird, hat dies keine finanziellen Auswirkungen auf das Projekt.

## <a name="changes-to-time-entry-records"></a>Änderungen an Zeiteintragsdatensätzen

Die folgende Abbildung zeigt die Änderungen, die für genehmigte Zeiteinträge auftreten und die entsprechenden Genehmigungsdatensätze, wenn sie zurückgerufen werden.

![Statusübergänge für Zeiteinträge.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Änderungen an Ausgaben- ind Materialverbrauchseintragsdatensätzen

Die folgende Abbildung zeigt die Änderungen, die für genehmigte Ausgaben- und Materialverbrauchseinträge auftreten und die entsprechenden Genehmigungsdatensätze, wenn sie zurückgerufen werden.

![Statusübergänge für Ausgabeneinträge.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
