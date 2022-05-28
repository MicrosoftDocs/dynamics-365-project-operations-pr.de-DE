---
title: Stornieren zuvor genehmigter Zeit- bzw. Ausgabeneinträge
description: Dieses Thema enthält Informationen zum Stornieren einer genehmigten Projektzeit- und -Ausgabentransaktion.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9e3bc94b626b88a2167e3a61472b768e2fb5c731
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590759"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Stornieren zuvor genehmigter Zeit- bzw. Ausgabeneinträge

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In der aktuellen Version von Dynamics 365 Project Service Automation können Genehmiger Zeit- bzw. Ausgabeneinträge stornieren, die sie zuvor genehmigt haben.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Stornieren eines zuvor genehmigten Zeit- bzw. Ausgabeneintrags

Führen Sie die folgenden Schritte aus, um einen zuvor genehmigten Zeit- bzw. Ausgabeneintrag zu stornieren.

1. Wechseln Sie zu **Projekte** \> **Meine Arbeit** \> **Genehmigungen**.
2. Ändern Sie auf der Listenseite **Genehmigungen** die Ansicht in **Meine letzten Genehmigungen**. Eine Liste der zuvor genehmigten Zeit- und Ausgabeneinträge wird angezeigt.
3. Wählen Sie einen oder mehrere Einträge aus, und wählen Sie dann **Genehmigung stornieren** aus. Sie erhalten eine Warnmeldung.
4. Wählen Sie **OK** aus, um die Genehmigung zu stornieren.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Grundlegendes zum Stornierens einer Genehmigung für Zeit- oder Ausgabeneinträge

Das Stornieren einer Genehmigung hat sowohl betriebliche als auch finanzielle Auswirkungen.

### <a name="operational-impact"></a>Betriebliche Auswirkungen

Auf der betrieblichen Seite wird der Status des Datensatzes beim Stornieren einer Genehmigung auf **Entwurf** zurückgesetzt, und die Genehmigung wird in der Ansicht **Meine letzten Genehmigungen** nicht mehr angezeigt. Stattdessen wird die stornierte Genehmigung entweder in der Ansicht **Zeiteinträge zur Genehmigung** oder in der Ansicht **Ausgabeneinträge zur Genehmigung** angezeigt, je nachdem, ob es sich um einen Zeit- oder einen Ausgabeneintrag handelte. Darüber hinaus wird der Status des zugehörigen Zeit- bzw. Ausgabeneintrags in **Gesendet** geändert, sodass der zugehörige Eintrag mit Genehmigungen im Status **Entwurf** konsistent ist.

Als Genehmiger können Sie einige Felder einer Genehmigung bearbeiten, die den Status **Entwurf** aufweist. Diese Felder sind **Fakturierungstyp** und **Abrechenbare Stunden für Zeiteinträge**. Nachdem Sie Änderungen vorgenommen haben, können Sie den Datensatz erneut genehmigen. Alternativ können Sie den Eintrag ablehnen. Wenn Sie die Genehmigung eines Zeiteintrags ablehnen, wird der Status des Eintrags in **Zurückgegeben** geändert. Wenn Sie die Genehmigung eines Ausgabeneintrags ablehnen, wird der Status des Eintrags in **Abgelehnt** geändert. In Bezug auf ihre Funktion verhalten sich sowohl zurückgegebene als auch abgelehnte Einträge wie ein Eintrag mit dem Status **Entwurf**. Ein Projektteammitglied kann entweder die erforderlichen Änderungen am Eintrag vornehmen und ihn dann erneut zur Genehmigung einreichen oder den Eintrag vollständig löschen.

### <a name="financial-impact"></a>Finanzielle Auswirkungen

Das Stornieren einer Genehmigung wirkt sich auch finanziell auf das Projekt aus. Zunächst werden die entsprechenden Istwerte für Kosten und Vertrieb folgendermaßen aktualisiert:

- Der Anpassungsstatus wird auf **Angepasst** festgelegt.
- Der Fakturierungsstatus wird auf **Storniert** festgelegt.

Als Nächstes werden Umkehrungseinträge in der Tabelle „Ist-Werte“ erstellt. Zum Erstellen von Umkehrungseinträgen kopiert das System die Feldwerte aus den ursprünglichen Ist-Werten. Die einzigen Werte, die nicht übernommen werden, sind die Mengenwerte. Diese Werte werden stattdessen umgekehrt. Umgekehrte Ist-Werte werden sowohl für **Kosten** als auch für Ist-Werte von **Nicht fakturierten Umsätzen** erstellt. Das Feld **Anpassungsstatus** des umgekehrten Ist-Werts wird auf **Nicht anpassbar** festgelegt, und der Fakturierungsstatus wird auf **Storniert** festgelegt.

Nachdem diese Änderungen vorgenommen wurden, stellen der Betrag, der als für das Projekt ausgegeben erfasst wurde, und das Umsatz-Rückstandsprotokoll des Projekts nicht mehr die Ist-Werte dar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
