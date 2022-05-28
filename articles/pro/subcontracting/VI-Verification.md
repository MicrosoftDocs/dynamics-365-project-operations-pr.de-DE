---
title: Überprüfung von Kreditorenrechnungen mit genehmigten Ist-Werten
description: Dieses Thema erklärt, wie Microsoft Dynamics 365 Project Operations es Projektmanagern ermöglicht, Kreditorenrechnungen mit den Ist-Werten zu überprüfen, die genehmigt wurden, als die Auftragnehmer Arbeiten durchgeführt und Zeit erfasst haben, sowie die Ausgaben und Materialien, die von den Projektteammitgliedern verwendet wurden.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3350a51bde2872036b79a789fae23ea6790fb21a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585469"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Überprüfung von Kreditorenrechnungen mit genehmigten Ist-Werten

[!include [banner](../../includes/dataverse-preview.md)]

_ **Gilt für**: Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung

Microsoft Dynamics 365 Project Operations ermöglicht es Projektmanagern, Kreditorenrechnungspositionen auf folgende Weise zu überprüfen:

- Verwenden Sie das Feld **Überprüfungsstatus** in den Kreditorenrechnungspositionen.
- Wenn die Kreditorenrechnungspositionen auf eine Unterauftragsposition verweisen, verknüpfen Sie Ist-Kosten aus der Auftragsnehmeraktivität mit diesen Kreditorenrechnungspositionen. Die Verknüpfung wird erstellt, indem Ist-Kosten mit den Kreditorenrechnungspositionen abgeglichen werden.

    > [!NOTE]
    > Obwohl der Verifizierungsstatus für Kreditorenrechnungspositionen nachverfolgt werden kann, die nicht auf einen Untervertrag verweisen, können tatsächliche Kosten nicht mit diesen Kreditorenrechnungspositionen verknüpft werden.

## <a name="verification-status"></a>Überprüfungsstatus

Das **Überprüfungsstatus** Feld in einer Kreditorenrechnungsposition gibt diesen Status der Überprüfung an. Die folgenden Status werden unterstützt:

1. Nicht begonnen
2. In Bearbeitung
3. Abgeschlossen

Kreditorenrechnungspositionen mit dem Überprüfungsstatus **Nicht gestartet** können bearbeitet werden.

Kreditorenrechnungspositionen mit dem Überprüfungsstatus **In Bearbeitung** können nicht mehr bearbeitet werden. Für eine Kreditorenrechnungsposition, die auf einen Untervertrag verweist, wird der Überprüfungsstatus automatisch auf **In Bearbeitung** gesetzt, sobald die ersten Ist-Kosten mit der Kreditorenrechnungsposition abgeglichen sind.

Kreditorenrechnungspositionen mit dem Überprüfungsstatus **Abgeschlossen** können nicht mehr bearbeitet werden. Wenn alle Zeilen einer Kreditorenrechnung diesen Überprüfungsstatus haben, kann die Kreditorenrechnung bestätigt werden.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Kosten-Ist-Werte mit Kreditorenrechnungspositionen abgleichen

Der Abgleich der Ist-Kosten hilft beim Überprüfungsprozess einer Kreditorenrechnungsposition. Führen Sie die folgenden Schritte aus, um Ist-Kosten mit einer Kreditorenrechnungsposition abzugleichen.

1. Öffnen Sie die Kreditorenrechnungsposition, und wählen Sie die Registerkarte **Nicht zugeordnete Kosten-Ist-Werte**. Ein Raster zeigt eine Liste der Ist-Kosten, die auf dieselbe Untervertragsposition wie die Kreditorenrechnungsposition verweisen.
2. Wählen Sie eine oder mehrere der tatsächlichen Kosten aus, und wählen Sie dann **Abgleichen** auf der Symbolleiste über dem Raster aus. Das System validiert, dass die ausgewählten Ist-Kosten abgeglichen werden können. Nachdem die Validierung bestanden wurde, werden die Ist-Kosten mit der Kreditorenrechnungsposition verknüpft.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Validierungskriterien, die verwendet werden, um Ist-Kosten mit Kreditorenrechnungspositionen zu verknüpfen

Während des Abgleichprozesses kann eine Verknüpfung zwischen Ist-Kosten und einer Kreditorenrechnungsposition nur hergestellt werden, wenn die beiden folgenden Bedingungen erfüllt sind:

- Das **Anpassungsstatus**-Feld für alle ausgewählten Ist-Kosten muss leer sein. Mit anderen Worten, die Ist-Kosten dürfen nicht während eines Rückruf-, Genehmigungsstornierungs- oder Korrekturerfassungsprozesses durch andere Ist-Kosten ersetzt worden sein.
- Die Werte der folgenden Felder werden zwischen der Kreditorenrechnungsposition und den ausgewählten Ist-Kosten abgeglichen. Wenn ein Feld in der Kreditorenrechnungsposition nicht festgelegt ist, wird es nicht für den Abgleich berücksichtigt.

    - Projektvertrag
    - Projektvertragszeile
    - Transaktionsklasse
    - Project
    - Task
    - Ressourcenkategorie
    - Transaktionskategorie
    - Produkt
    - Fremdarbeitsposition
    - Buchbare Ressource

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Die Zuordnung von Kosten-Ist-Werten zu einer Kreditorenrechnungsposition aufheben

Das Aufheben der Zuordnung von Ist-Kosten kann auch beim Überprüfungsprozess auf einer Kreditorenrechnung helfen, indem zuvor erstellte Verknüpfungen entfernt werden können. Die Zuordnung von Kosten-Ist-Werten kann nur von Kreditorenrechnungspositionen mit dem Überprüfungsstatus **In Bearbeitung** aufgehoben werden. Führen Sie die folgenden Schritte aus, um die Zuordnung von Ist-Kosten zu einer Kreditorenrechnungsposition aufzuheben.

1. Öffnen Sie die Kreditorenrechnungsposition, und wählen Sie die Registerkarte **Zugeordnete Kosten-Ist-Werte**. Ein Raster zeigt eine Liste der Kosten-Ist-Werte, die auf dieselbe Untervertragsposition verweisen.
2. Wählen Sie eine oder mehrere der tatsächlichen Kosten aus, und wählen Sie dann **Zuordnung aufheben** auf der Symbolleiste über dem Raster aus.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
