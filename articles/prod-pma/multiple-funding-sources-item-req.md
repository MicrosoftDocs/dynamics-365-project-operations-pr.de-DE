---
title: Artikelanforderungen für Projektverträge mit mehreren Finanzierungsquellen
description: In diesem Artikel erfahren Sie, wie Sie Elementanforderungen mit mehreren Finanzierungsquellen konfigurieren und verwenden können.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a54ca1ec5e78d9d0af7b67914f6a63154c7347d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931191"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Artikelanforderungen für Projektverträge mit mehreren Finanzierungsquellen

_**Gilt für:** Project Operations für Szenarien basierend auf den vorrätigen Ressourcen/Fertigung_

Einige vertragliche Vereinbarungen für projektbasierte Leistungen erfordern möglicherweise mehrere Finanzierungsquellen. Dieser Artikel erklärt, wie Sie die gewünschten Finanzierungsquellen auswählen und konfigurieren, wenn mehrere Quellen für ein Projekt oder einen Projektvertrag erforderlich sind.

## <a name="terminology"></a>Terminologie

- **Finanzierungsquelle** – Die Entität, die die Projektvertragsarbeit finanziert. Diese Entität kann eine interne Organisation oder ein externes Rechnungskonto (Kunde oder Zuweisung) sein.
- **Projektkunde** – Die Entität, an die die Projektarbeit geliefert wird.
- **Rechnungskonto** – Die externe Entität, die die Projektarbeit bezahlt.

## <a name="example"></a>Beispiel

Contoso hat mit zwei seiner Kunden einen Vertrag zur Geräteerneuerung abgeschlossen: Adatum US und Adatum Corporate. Der Vertrag umfasst Hardware- und Installationsleistungen, die an Adatum US (den Projektkunden) geliefert werden. Die Hardware wird von Adatum Corporate (Rechnungskonto 1) und die Installationsarbeiten von Adatum US (Rechnungskonto 2) finanziert.

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Rechnungskonto-Standardregeln für Artikelanforderungen einrichten

### <a name="prerequisites"></a>Anforderungen

- Microsoft Dynamics 365 Finance and Operations **Version 10.0.27 oder höher** ist erforderlich, um Artikelanforderungen zu verwenden, die mehrere Rechnungskonten haben.
- Ihr Systemadministrator muss die Funktion **Artikelanforderungen mit mehreren Finanzierungsquellen für vorrats-/produktionsbasierte Project Operations-Szenarien zulassen** im Arbeitsbereich **Funktionsverwaltung** aktivieren.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Die Standardregeln für das Rechnungskonto einrichten

Um die Standardregeln für das Rechnungskonto einzurichten, führen Sie die folgenden Schritte aus.

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Einrichtung** \> **Projektmanagement- und Buchhaltungsparameter**.
1. Auf der **Allgemein**-Registerkarte, im **Verkaufsaufträge und Artikelanforderungen**-Abschnitt, stellen Sie die **Projekte mit mehreren Finanzierungsquellen zulassen**-Option auf **Ja**.
1. Geben Sie im Feld **Standardkunde** standardmäßig an, woher der Projektlieferungskunde für den Artikelbedarf kommt:

    - **Aus Finanzierungsquelle** – Der Standardkunde für die Projektlieferung stammt aus der Finanzierungsquelle. Wenn dem Projektvertrag mehrere Finanzierungsquellen zugeordnet sind, wird die erste Finanzierungsquelle in der Liste verwendet.
    - **Aus Projekt** – Der Standardkunde für die Projektlieferung stammt von dem Kunden, der im **Projektaufzeichnungskonto**-Feld ausgewählt ist.

1. Optional: Legen Sie das Standardrechnungskonto für Projektdatensätze fest oder ändern Sie es:

    1. Gehen Sie zu **Projektmanagement und Rechnungswesen** \> **Projekte** \> **Alle Projekte**, und öffnen Sie die Projektdatensatzdetails.
    2. Legen Sie auf der **Allgemein**-Registerkarte die **Standardrechnungskonto**-Feld fest oder aktualisieren Sie es. Das von Ihnen angegebene Konto wird als Standardrechnungskonto für neue Artikelanforderungen verwendet, die für das Projekt erstellt werden. Wenn Sie das Feld leer lassen, wird standardmäßig das Rechnungskonto der ersten Finanzierungsquelle des Projektvertrags verwendet. Benutzer können das Konto jedoch ändern, wenn sie den Datensatz speichern.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Das zu verwendende Rechnungskonto bei Erstellung eines Artikelbedarfs auswählen

Um das zu verwendende Rechnungskonto bei Erstellung eines Artikelbedarfs auszuwählen, führen Sie folgende Schritte aus.

1. Gehen Sie zu **Projektmanagement und Rechnungswesen** \> **Projekte** \> **Alle Projekte**, und wählen Sie den Projektdatensatz.
1. Auf der **Plan**-Registerkarte wählen Sie **Artikelanforderungen**.
1. Erstellen Sie einen neuen Artikelanforderungsdatensatz.

    - Standardmäßig ist das **Rechnungskonto**-Feld im Datensatz auf das Rechnungskonto eingestellt, das für das Projekt eingestellt ist. Sie können den Wert des **Rechnungskonto**-Felds ändern und dann den Datensatz speichern. Nachdem der Datensatz gespeichert wurde, können Sie den **Rechnungskonto**-Wert nicht mehr aktualisieren. Wenn Sie den **Rechnungskonto**-Wert für die Artikelanforderung aktualisieren müssen, löschen Sie die vorhandene Artikelanforderung und erstellen Sie dann eine neue mit dem gewünschten Wert.
    - Standardmäßig wird das **Kunde**-Feld für die Artikelanforderung basierend auf dem **Standardkunde**-Wert festgelegt, der auf der **Projektmanagement und Abrechnungsparameter**-Seite eingestellt ist.

    Wenn der Artikelbedarfsdatensatz gespeichert wird, ordnet ihn das System dem **Verkaufsauftrag für Artikelbedarf** Header-Datensatz zu. Wenn kein offener Kundenauftrags-Header das ausgewählte Rechnungskonto hat, erstellt das System eines und ordnet ihm die Artikelbedarfsposition zu.

> [!NOTE]
> Artikelanforderungen werden immer vollständig auf das im Datensatz hinterlegte Rechnungskonto fakturiert. Das System unterstützt derzeit keine Finanzierungszuweisungsregeln, die Artikelanforderungen haben, und es teilt die Buchung nicht basierend auf der Einrichtung von Finanzierungszuweisungsregeln auf.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Eine Artikelanforderung aus einem Artikelprognosedatensatz erstellen

Um eine Artikelanforderung aus einem Artikelprognosedatensatz zu erstellen, führen Sie folgende Schritte aus:

1. Gehen Sie zu **Projektmanagement und Rechnungswesen** \> **Projekte** \> **Alle Projekte**, und wählen Sie den Projektdatensatz.
1. Auf der **Plan**-Registerkarte wählen Sie **Artikelprognosen**.
1. Erstellen Sie einen neuen Artikelprognosedatensatz.
1. Optional: Auf der **Projekt**-Registerkarte wählen Sie im Feld **Finanzierungsquelle** das gewünschte Rechnungskonto aus.
1. Wählen Sie **Artikelanforderung erstellen** aus, und bestätigen Sie die Nachricht, die Sie erhalten.

    > [!NOTE]
    > Das System kopiert den **Finanzierungsquelle**-Wert aus dem Artikelprognosedatensatz in den neu erstellten Artikelanforderungsdatensatz.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Standardrechnungskonto, wenn das System automatisch eine Artikelanforderung aus einer Bestellposition erstellt

Wenn die **Artikelanforderung erstellen**-Option auf der **Projektmanagement und Abrechnungsparameter** Seite auf **Ja** eingestellt ist, erstellt das System automatisch eine Artikelanforderung, wenn eine neue Projektbestellposition gespeichert wird. Standardmäßig werden die Felder **Rechnungskonto** und **Artikelanforderung** auf den Wert des **Standardrechnungskonto**-Felds im Projektdatensatz gesetzt. Das System unterstützt derzeit keine Aktualisierung oder Änderung des Rechnungskontos für Datensätze dieses Typs.
