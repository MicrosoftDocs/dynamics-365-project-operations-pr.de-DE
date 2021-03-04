---
title: Ausgabenverwaltung konfigurieren
description: Dieser Artikel beschreibt die Überlegungen und Entscheidungen, die Sie während des Planungsprozesses treffen müssen, bevor Sie die Ausgabenverwaltung in Microsoft Dynamics 365 Finance konfigurieren können.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960336"
---
# <a name="configure-expense-management"></a>Ausgabenverwaltung konfigurieren

Dieses Thema beschreibt die Überlegungen und Entscheidungen, die Sie während des Planungsprozesses treffen müssen, bevor Sie Ihre Ausgabenverwaltung konfigurieren können. In der Ausgabenverwaltung können Sie Informationen zu Zahlungsmethoden, Reiseanforderungen, Spesenabrechnungen, Richtlinien usw. speichern.

Da viele der Entscheidungen, die Sie bei der Planung Ihrer Konfiguration für die Ausgabenverwaltung treffen, auf der Hierarchie und Finanzstruktur Ihres Unternehmens basieren, müssen Sie sich auf die Planungsdokumente für diese Bereiche beziehen.

## <a name="intercompany-expenses"></a>Intercompany-Ausgaben

Wenn Sie konzerninterne Ausgaben aktivieren, können juristische Personen und Mitarbeiter im Namen einer anderen juristischen Person Kosten verursachen und Zahlungen von der juristischen Person der Beschäftigung in Ihrer Organisation einziehen. Beispielsweise schließt ein Mitarbeiter der juristischen Person A ein Projekt für die juristische Person B ab, und für das Projekt fallen reisebezogene Kosten an. Wenn konzerninterne Ausgaben aktiviert sind, kann der Mitarbeiter eine Spesenabrechnung einreichen, in der die Ausgaben an die juristische Person B gebucht werden. Die Ausgaben müssen dann von der juristischen Person A bezahlt werden. Wenn Ihre Organisation nicht über mehrere juristische Personen verfügt, müssen Sie dies nicht tun. Es müssen keine konzerninternen Ausgaben aktiviert werden.

**Entscheidung:** Möchten Sie konzerninterne Ausgaben aktivieren?

## <a name="financial-management"></a>Finanzverwaltung

Die Ausgabenverwaltung ist eng in die Finanzverwaltung Ihrer Organisation integriert. Ein Großteil Ihrer Konfiguration für die Ausgabenverwaltung basiert auf den Entscheidungen, die Sie über die Finanzen Ihres Unternehmens getroffen haben. In den folgenden Abschnitten werden die verschiedenen Bereiche beschrieben, die Planung und Entscheidungen erfordern, basierend auf den finanziellen Entscheidungen Ihres Unternehmens und den Anweisungen Ihres Führungsteams.

### <a name="per-diems"></a>Pro Tag

Sie müssen die von Ihrer Organisation bereitgestellten Mitarbeiter-Tagessätze definieren. Da Tagessätze normalerweise zur Deckung von Ausgaben wie Mahlzeiten, Unterkunft und anderen Nebenkosten verwendet werden, können Sie Regeln für die Tagessätze erstellen, die Ihre Organisation anbietet. Die Tagessätze können auf der Jahreszeit, dem Reiseort oder beiden basieren. Wenn Sie eine Tagessatzregel definieren, können Sie festlegen, dass ein Prozentsatz des Tagessatzes einbehalten wird, wenn ein Mitarbeiter kostenlose Mahlzeiten oder Dienstleistungen erhält. Sie können auch Tagessatzstufen definieren, um eine minimale und maximale Anzahl von Stunden festzulegen, für die der Tagessatz für die Reise eines Arbeitnehmers gelten kann.

**Entscheidungen:**

- Standard-Tagessatzregeln für den ersten und letzten Tag:

    - Wie viele Stunden kann ein Mitarbeiter mindestens für einen Tag beanspruchen und trotzdem einen Tagessatz erhalten?
    - Gibt es eine Reduzierung des Betrags, der für Mahlzeiten am ersten und letzten Tag angeboten wird? Wenn es eine Reduzierung gibt, wie hoch ist der Prozentsatz der Reduzierung?
    - Gibt es eine Reduzierung des Betrags, der für ein Hotel am ersten und letzten Tag angeboten wird? Wenn es eine Reduzierung gibt, wie hoch ist der Prozentsatz der Reduzierung?
    - Gibt es eine Reduzierung des Betrags, der für andere Ausgaben angeboten wird, die am ersten und am letzten Tag anfallen? Wenn es eine Reduzierung gibt, wie hoch ist der Prozentsatz der Reduzierung?

- Standard-Tagessatzregeln:

    - Gibt es eine prozentuale Reduzierung des Tagessatzes für jede Mahlzeit, wenn beispielsweise die Mahlzeit kostenlos ist? Wenn es eine Reduzierung gibt, wie hoch ist der Prozentsatz der Reduzierung für jede Mahlzeit?
    - Wird die Reduzierung der Mahlzeiten pro Tag, pro Reise oder anhand der Anzahl der Mahlzeiten pro Tag berechnet?
    - Sollten die Beträge der Tagessätze regelmäßig gerundet oder aufgerundet werden?
    - Werden Tagessätze für einen Zeitraum von 24 Stunden oder an einem Kalendertag berechnet?

- Tagessatzregeln, die auf dem Standort basieren:

    - Variieren die Tagessätze je nach Standort? Welche Standorte sind enthalten?
    - Wenn die Tagessätze je nach Standort variieren, wird für jeden Standort der prozentuale Betrag für die folgenden Arten von Ausgaben bereitgestellt:

        - Mahlzeiten
        - Hotel
        - Andere Ausgaben

### <a name="expense-management-journals-and-accounts"></a>Ausgabenverwaltungs-Journale und -Konten

Für die Ausgabenverwaltung müssen Sie mehrere Journale und Konten verwenden. Sie müssen beispielsweise entscheiden, ob dasselbe Konto für Bargeldvorschüsse und Kreditkartenstreitigkeiten verwendet wird.

**Entscheidungen:**

- In welche Sachkontoerfassung werden genehmigte Spesenabrechnungen gebucht?
- Welches Konto wird für Bargeldvorschüsse verwendet?
- Sollten Bargeldvorschüsse sofort gebucht werden?

### <a name="payment-methods"></a>Zahlungsmethoden

Wenn Sie Mitarbeitern erlauben, im Namen Ihres Unternehmens Kosten zu verursachen, müssen Sie die Zahlungsmethoden definieren, die Mitarbeiter verwenden dürfen. Beispielsweise können Sie Mitarbeitern erlauben, Bargeld oder eine Firmenkreditkarte zu verwenden. Sie können Mitarbeitern auch erlauben, persönliche Kreditkarten zu verwenden, und die Kosten den Mitarbeitern anschließend erstatten. Sie müssen die folgenden Entscheidungen für jede Zahlungsmethode treffen, die Sie zulassen.

**Entscheidungen:**

- Welche Zahlungsmethoden sind erlaubt?
- Wer ist für die Kosten der Zahlungsmethode verantwortlich?
- Gibt es einen Gegenkontotyp? Wenn es einen Gegenkontotyp gibt, um welchen handelt es sich?
- Wenn es einen Gegenkontotyp gibt, wie lautet das Konto?
- Wenn es sich bei der Zahlungsmethode um eine Kreditkarte handelt, sollte die Zahlungsmethode nur bei importierten Transaktionen verwendet werden?

### <a name="expense-categories-and-shared-categories"></a>Ausgabenkategorien und gemeinsame Kategorien

Wenn Mitarbeiter eine Spesenabrechnung erstellen, muss jede von ihnen erfasste Ausgabe einer Ausgabenkategorie zugeordnet werden. Ausgabenkategorien werden aus gemeinsam genutzten Kategorien abgeleitet, die von den juristischen Personen in Ihrer Organisation gemeinsam genutzt werden können. Diese Kategorien können auch im Projektmanagement und in der Projektbuchhaltung verwendet werden, abhängig von der Art und Weise, wie Ihre Organisation definiert ist. Legen Sie basierend auf der Definition Ihrer Organisation und den Anweisungen des Implementierungsteams fest, ob die in der Ausgabenverwaltung verwendeten Kategorien nur in der Ausgabenverwaltung verwendet werden oder zwischen dem Projektmanagement, der Buchhaltung und der Ausgabenverwaltung gemeinsam genutzt werden sollten. Beachten Sie, dass diese Kategorien zwischen Projekt und Ausgaben oder Projekt und Produktion gemeinsam genutzt werden können, jedoch nicht zwischen Ausgaben und Produktion. Sie müssen für jede Ausgabenkategorie die folgenden Entscheidungen treffen.

**Entscheidungen:**

- Was ist die Ausgabenkategorie? Beispiele sind Kategorien für Flüge, Hotel oder Kilometerstand.
- Kann die Ausgabenkategorie auch im Projektmanagement und in der Buchhaltung verwendet werden?
- Was ist der Ausgabentyp?
- Was ist die Standardzahlungsmethode für die Ausgabenkategorie?
- Müssen Ausgaben in der Ausgabenkategorie aufgelistet werden?
- Was ist das Haupt-Standardkonto für die Ausgabenkategorie?
- Was ist die Standard-Artikel-Mehrwertsteuergruppe für die Ausgabenkategorie?
- Sind zusätzliche Zahlungsmethoden für die Ausgabenkategorie zulässig? Welche zusätzlichen Zahlungsmethoden sind zulässig?
- Gibt es Unterkategorien in dieser Ausgabenkategorie? Falls es Unterkategorien gibt, müssen Sie auch die folgenden Entscheidungen treffen:

    - Sind einige der Unterkategorien von der Steuerrückerstattung ausgeschlossen?
    - Was ist die Artikel-Mehrwertsteuergruppe der Unterkategorien?

Wenn die Ausgabenkategorie auch im Projektmanagement und in der Buchhaltung verwendet wird, beantworten Sie die verbleibenden Fragen. Andernfalls können Sie mit dem nächsten Abschnitt fortfahren.

- Welche Kostenkonten werden für die folgenden Ausgaben verwendet?

    - Kosten
    - Lohnzuweisung
    - WIP-Einstandswert
    - Kostenelement
    - WIP-Einstandswertelement
    - Antizipierter Verlust
    - WIP - Antizipierter Verlust

- Welche Umsatzkonten werden für Folgendes verwendet?

    - Rechnungsumsatz
    - Antizipierter Umsatzerlös - Verkaufswert
    - RIF – Verkaufswert
    - Antizipierter Umsatzerlös – Produktion
    - RIF – Fertigung
    - Antizipierter Umsatzerlös – Gewinn
    - WIP - Gewinn
    - Antizipierter Umsatz - Dauerauftrag
    - WIP - Dauerauftrag

### <a name="taxes"></a>Steuern

Für kostenbezogene Steuern müssen Sie festlegen, was in den Spesenabrechnungen enthalten oder aktiviert ist.

**Entscheidungen:**

- Ist die Umsatzsteuer in den Aufwandsbeträgen enthalten?
- Sollte die Steuerrückerstattung für Ausgaben ermöglicht werden?

    > [!NOTE]
    > Wenn Sie bei der Planung der Finanzbuchhaltung beschlossen haben, die US-Umsatzsteuer und Steuerregeln anzuwenden, können Sie die Steuerrückerstattung für Ausgaben nicht aktivieren. (Um die US-Umsatzsteuer und Steuervorschriften zu verwenden, legen Sie die Option **Mehrwertsteuerregeln anwenden** auf **Ja** fest.)

## <a name="policies"></a>Richtlinien

Durch das Erstellen von Richtlinien für Spesenabrechnungen können Sie Ihrem Unternehmen helfen, Zeit und Geld zu sparen, wenn Mitarbeiter im Namen des Unternehmens Ausgaben tätigen. Richtlinien tragen dazu bei, dass die Mitarbeiter im Budget bleiben, alle erforderlichen Informationen bereitstellen und Geld nur dann ausgeben, wenn sie es benötigen. Sie müssen die folgenden Entscheidungen für jede Spesenabrechnungsrichtlinie und jede von Ihnen erstellte Spesenabrechnungsgenehmigungsrichtlinie treffen.

**Entscheidungen:**

- Wie lautet der Name der Richtlinie?
- Wofür gilt die Ausgabenrichtlinie?
- Wenn Sie zuvor beschlossen haben, konzerninterne Ausgaben zu aktivieren, für welche Unternehmen in Ihrer Organisation gilt diese Richtlinie?
- Wann tritt die Richtlinie in Kraft?
- Wann läuft die Richtlinie ab?
- Wie lautet die Richtlinienregel?
- Was ist das Ergebnis der Richtlinienregel?


[!INCLUDE[footer-include](../includes/footer-banner.md)]