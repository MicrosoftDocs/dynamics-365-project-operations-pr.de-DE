---
title: Die Genehmigung zuvor genehmigter Zeit- oder Einträge stornieren
description: Dieser Artikel erklärt, wie ein Projekt Manager die Genehmigung von zuvor genehmigten Zeit-, Spesen- oder Materialverbrauchsbuchungen rückgängig machen kann.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930455"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Die Genehmigung zuvor genehmigter Zeit- oder Einträge stornieren

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Ein Projektmanager oder eine genehmigende Person, die zuvor Zeit-, Ausgaben- oder Materialnutzungseinträge genehmigt hat, kann die Genehmigung dieser Einträge stornieren. 

Führen Sie die folgenden Schritte aus, um die Genehmigung eines zuvor genehmigten Zeit-, Ausgaben- oder Materialverbrauchseintrags zu stornieren.

1. Wechseln Sie zu **Projekte** \> **Meine Arbeit** \> **Genehmigungen**.
2. Die Listenseite **Genehmigungen** zeigt alle Zeiteinträge, die auf Genehmigung warten. Ändern Sie die Ansicht in **Meine vergangenen Genehmigungen**.
3. Wählen Sie die zu stornierenden Zeit-, Ausgaben- oder Materialgenehmigungen aus. Wählen Sie im Aktionsbereich dann die Option **Genehmigung stornieren** aus.
4. Wählen Sie im angezeigten Bestätigungsmeldungsfeld **OK**, um den Vorgang zu bestätigen.

> [!IMPORTANT]
> Sie können keine Genehmigung für einen zuvor genehmigten Zeit-, Ausgaben- und Materialverbrauchseintrag stornieren, der dem Kunden bereits in Rechnung gestellt wurde. Wenn Sie dies versuchen, erhalten Sie eine Nachricht, die angibt, dass die Genehmigung nicht storniert werden kann, da sie bereits in Rechnung gestellt wurde. In diesem Fall können Sie nur dann eine Genehmigung stornieren, wenn eine Korrekturrechnung verwendet wird, um dem Kunden eine vollständige Gutschrift oder Rückerstattung auf die ursprüngliche Rechnung zu erteilen.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Auswirkung der Stornierung der Genehmigung eines zuvor genehmigten Eintrags

Das Stornieren einer Genehmigung hat sowohl betriebliche als auch finanzielle Auswirkungen.

### <a name="operational-impact"></a>Betriebliche Auswirkungen

Wenn die Genehmigung eines Eintrags storniert wird, wird der Genehmigungsdatensatz als **Eingereicht** markiert. Der Eintragsstatus wird in **Eingereicht** geändert. In dieser Phase kann ein Projektteammitglied den Eintrag zurückrufen, ohne einen Rückrufantrag zu stellen.

Die genehmigende Person kann die Werte für **Fakturierbare Menge** und die **Fakturierungstyp** ändern und den Eintrag dann erneut genehmigen.

### <a name="financial-impact"></a>Finanzielle Auswirkungen

Wenn die Genehmigung eines Eintrags storniert wird, werden zunächst die entsprechenden Ist-Werte für Kosten und Vertrieb folgendermaßen aktualisiert:

- Das Feld **Anpassungsstatus** wird zu **Angepasst** aktualisiert.
- Das Feld **Fakturierungsstatus** wird zu **Storniert** aktualisiert.

Als Nächstes werden Umkehrungseinträge in der Tabelle „Ist-Werte“ erstellt. Zum Erstellen von Umkehrungseinträgen kopiert das System die Feldwerte aus den ursprünglichen Ist-Werten. Die einzigen Werte, die nicht übernommen werden, sind die Mengenwerte. Diese Werte werden stattdessen umgekehrt. Umgekehrte Ist-Werte werden sowohl für **Kosten** als auch für Ist-Werte von **Nicht fakturierten Umsätzen** erstellt. Das Feld **Anpassungsstatus** der umgekehrten Ist-Werte wird auf **Nicht anpassbar** festgelegt und das Feld **Fakturierungsstatus** auf **Storniert**. Aufgrund dieser Änderungen stellen die erfassten Ausgaben und das Umsatz-Rückstandsprotokoll des Projekts nicht länger die Ist-Werte dar.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
