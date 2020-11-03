---
title: Projektzuschüsse
description: In diesem Thema wird erläutert, wie Sie einen Zuschuss erstellen oder ändern.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
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
ms.openlocfilehash: 89801696d6a2924d78c85f6e9b4281409222dbb0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076705"
---
# <a name="project-grants"></a>Projektzuschüsse

[!include [banner](../includes/banner.md)]

Ein Zuschuss ist ein Geldgeschenk für einen bestimmten Zweck oder ein bestimmtes Projekt. Normalerweise gibt es Einschränkungen, wie ein Zuschuss ausgegeben werden kann. In Projektmanagement und -buchhaltung können Sie Zuschüsse eingeben, verfolgen und deren Beziehungen für Projekte und Projektverträge definieren. Beispielsweise können Sie die folgenden Aufgaben durchführen:

- Ordnen Sie Zuschüsse Projekten und Finanzierungsquellen durch Links zu den Seiten **Projekt** und **Projektvertragsdetails** zu.
- Geben Sie Änderungen an einem Zuschuss ein und verfolgen Sie ihn, wenn dieser von einem Status in einen anderen wechselt.
- Geben Sie Kosten, angeforderte Beträge und gewährte Beträge ein, und verfolgen Sie sie.
- Erstellen Sie übergeordnete Zuschüsse und weisen Sie diesen untergeordnete Zuschüsse zu.

Sie können einen Zuschuss erstellen, indem Sie alle Details in einen neuen Datensatz eingeben, oder Sie können die Details aus einem vorhandenen Zuschuss kopieren und dann aktualisieren.

## <a name="create-a-new-grant"></a>Einen neuen Zuschuss erstellen

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Zuschüsse** \> **Zuschüsse**.
2. Wählen Sie **Neu** \> **Zuschuss** aus.
3. Geben Sie auf der Zuschussdetailseite im Inforegister **Allgemein** im Feld **Zuschusskennung** eine alphanumerische Kennung für den Zuschuss ein.
4. Geben Sie im Feld **Zuschussname** einen Namen für den Zuschuss ein.
5. Fügen Sie im Feld **Beschreibung** Details zum neuen Zuschuss hinzu.

    Die meisten anderen Felder auf der Seite sind optional, und Sie können so wenig oder so viele Informationen eingeben, wie Sie möchten.

    In der folgenden Liste werden die Informationen beschrieben, die in jedem Inforegister der Seite mit den Zuschussdetails angegeben sind:

    - **Allgemein** – Geben Sie den Namen, den Status, die Beschreibung, den Zweck und den Betrag des Zuschusses ein.
    - **Kontaktinformationen** – Geben Sie Details zu Mitarbeitern, der Abteilung, die den Zuschuss verwaltet, und der Quelle des Zuschusskunden oder der Organisation des Zuschusses ein. Sie können auch angeben, ob Ihre Organisation eine Durchlaufentität ist, die den Zuschuss erhält und ihn dann an einen anderen Empfänger weiterleitet. Wählen Sie **Hinzufügen** aus, um Kontaktinformationen wie Telefonnummern und E-Mail-Adressen für die Organisation hinzuzufügen, die den Zuschuss bereitstellt.
    - **Termine und Fristen** – Geben Sie Daten ein, die sich auf den Zuschuss und den Zuschussantrag beziehen. Beispiele hierfür sind das Fälligkeitsdatum des Antrags, das Einreichungsdatum und das Datum, an dem der Zuschuss genehmigt oder abgelehnt wird.
    - **Zugeordnete Projekte und Projektverträge** – Sie können Informationen zu diesem Inforegister nur eingeben, wenn das Feld **Zuschussstatus** im Inforegister **Allgemein** auf **Aktiv** oder **Bewilligt** festgelegt ist. Wählen Sie eine der folgenden Optionen aus, um die zugehörige Aufgabe abzuschließen:

        - **Finanzierungsquelle hinzufügen** – Fügen Sie eine neue Finanzierungsquelle für den Zuschuss hinzu. Sie können jetzt alle Details eingeben oder Standardinformationen verwenden und diese später aktualisieren.
        - **Projektvertrag hinzufügen** – Fügen Sie Projektvertragsinformationen hinzu oder aktualisieren Sie diese.
        - **Projekt hinzufügen** – Fügen Sie Projektdetails hinzu oder aktualisieren Sie diese.

    - **Konfiguration** – Geben Sie Details zu passenden Fonds ein, wenn diese Informationen erforderlich sind. Viele Organisationen, die Zuschüsse gewähren, verlangen, dass die Empfänger einen bestimmten Betrag ihres eigenen Geldes oder ihrer Ressourcen ausgeben, um dem Betrag zu entsprechen, der im Rahmen des Zuschusses gewährt wird. Im Feld **Kennung für lokales Projekt oder Überwachungskennung** können Sie eine Kennung eingeben, die sich von der Projektkennung unterscheidet.

        > [!NOTE]
        > Wenn ein Teil des Zuschusses an eine andere Organisation vergeben wird, legen Sie die Option **Untergeordneter Geber** auf **Ja** fest. Für Zuschüsse, die in den USA vergeben werden, können Sie angeben, ob ein Zuschuss im Rahmen eines staatlichen Mandats oder eines Bundesmandats gewährt wird.

    - **Details der Inanspruchnahme** – Fügen Sie Informationen dazu hinzu, wie häufig Zuschussmittel in Anspruch genommen, fakturiert oder ausgegeben werden können, und aktualisieren Sie diese Informationen.

## <a name="create-a-new-grant-from-a-copy"></a>Einen neuen Zuschuss aus einer Kopie erstellen

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Zuschüsse** \> **Zuschüsse**.
2. Wählen Sie **Neu** \> **Aus Zuschuss kopieren** aus.
3. Geben Sie eine alphanumerische Kennung und einen Namen für den neuen Zuschuss ein, und wählen Sie dann **OK** aus.
4. Überprüfen Sie auf der Seite mit den Zuschussdetails die Details des kopierten Zuschusses, und nehmen Sie die erforderlichen Änderungen vor. Die meisten Felder auf der Seite sind optional.

## <a name="view-or-modify-grant-details"></a>Zuschussdetails anzeigen oder ändern

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Zuschüsse** \> **Zuschüsse**.
2. Wählen Sie den zu ändernden Zuschuss aus.
3. Wählen Sie im Aktionsbereich auf der Registerkarte **Zuschuss** in der Gruppe **Verwalten** die Option **Bearbeiten** aus.
4. Überprüfen Sie die Zuschussdetails, und nehmen Sie die erforderlichen Änderungen vor.
