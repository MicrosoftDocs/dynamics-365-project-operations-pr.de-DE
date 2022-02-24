---
title: Einheiten und Einheitengruppen
description: Dieses Thema enthält Informationen zum Erstellen von Einheiten und Einheitengruppen in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f588e41d001befeac87bb6a4e28a83cf5cfa865
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131027"
---
# <a name="units-and-unit-groups"></a>Einheiten und Einheitengruppen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Einheiten sind die Mengen oder Maße, in denen Produkte oder Dienstleistungen verkauft werden. Wenn Sie z. B. Gartenarbeitszubehör verkaufen, bietet sich ein Verkauf in den Einheiten Paletten, Pakete, Kisten an. Eine Einheitengruppe ist eine Sammlung dieser verschiedenen Einheiten.

Stellen Sie zum Ausführen der Schritte in diesem Thema sicher, dass Sie der Systemrolle Administrator oder Sales Professional Manager zugewiesen wurden oder über entsprechende Berechtigungen verfügen.

## <a name="create-a-unit-group"></a>Erstellen einer Einheitengruppe

1. Wählen Sie in der Siteübersicht die Option **Einheiten** aus.
2. Wählen Sie **Neu** und geben Sie im Dialogfeld **Einheitengruppe erstellen** den Einheitennamen ein.
3. Geben Sie im Feld **Primäre Einheit** die niedrigste gebräuchliche Maßeinheit für die Einheitengruppe ein, in der das Produkt vertrieben wird. Beispielsweise können Sie "Stück" oder "Unze" eingeben.
4. Klicken Sie auf **OK**.

## <a name="add-units-to-a-unit-group"></a>Einheiten einer Einheitsgruppe hinzufügen

1. Öffnen Sie eine Einheitengruppe und klicken Sie auf die Registerkarte **verbunden** und wählen Sie **Einheiten**. Sie werden sehen, dass die primäre Einheit bereits hinzugefügt wurde.
2. Wählen Sie **Neue Einheit hinzufügen** und auf der Seite **Schnell erstellen: Einheit** im Feld **Name** geben Sie im Feld das Nanem der Einheit ein.
3. Geben Sie im Feld **Menge** die Menge ein, die die Einheit enthält. Wenn eine Kiste z. B. zwei Stück enthält, würden Sie 2 eingeben. 
4. In dem Feld **Grundeinheit** wählen Sie im Feld eine Basiseinheit aus, um die niedrigste Maßeinheit für die Einheit festzulegen. Zum Beispiel könnten Sie Stück auswählen.
5. Wählen Sie **Speichern**:
