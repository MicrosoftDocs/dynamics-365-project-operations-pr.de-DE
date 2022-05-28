---
title: Preislisten deaktivieren
description: In diesem Thema wird erläutert, wie nicht verwendete oder alte Preislisten deaktiviert oder entfernt werden.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ab790764f7a99118fd42bc76934105389173ff88
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596882"
---
# <a name="deactivate-price-lists"></a>Preislisten deaktivieren 

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Zum Entfernen von alten oder nicht verwendeten Preislisten aus Dynamics 365 Project Operations gibt es zwei Schritte, die Sie ausführen müssen. 

1. Entfernen oder löschen Sie die Preisliste von bestimmten Seiten.
2. Deaktivieren oder löschen Sie die Preisliste aus den aktiven Preislisten auf der **Preisliste**-Seite.

>[!IMPORTANT]
> Sie müssen beide Schritte ausführen, um eine Preisliste vollständig zu entfernen. Es reicht nicht aus, nur Schritt 2 auszuführen, bei dem die Preisliste direkt aus der Ansicht „Aktive Preislisten“ gelöscht oder deaktiviert wird. Sie müssen auch die Zuordnung dieser Preisliste von allen in Schritt 1 genannten Stellen löschen.

## <a name="delete-the-price-list-from-specific-pages"></a>Löschen Sie die Preisliste von bestimmten Seiten
1. Gehen Sie zu den folgenden Seiten, um eine Preisliste aus Project Operations zu löschen:  

      - **Projektparameter**-Seite > **Preislisten**-Registerkarte
      - **Organisationseinheit**-Seite> **Preisliste**-Raster
      - **Konto**-Seite > **Projektpreislisten**-Raster
      - **Projektangebote**-Seite > **Projektpreislisten**-Raster: Dies gilt für alle aktiven Projektangebote.
      - **Projektverträge**-Seite > **Projektpreislisten**-Raster: Dies gilt für alle aktiven Projektverträge.

 2. Für jede Seite müssen Sie die Preisliste auswählen, die Sie löschen möchten, und wählen Sie dann **Löschen**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Löschen oder deaktivieren Sie die Preisliste auf der Preisliste-Seite
 
1. Um eine Preisliste aus den aktiven Preislisten zu löschen, gehen Sie zu **Vertrieb** > **Kunden** > **Preisliste**. 
2. Wählen Sie die Preisliste aus, die Sie löschen möchten, und wählen Sie dann **Löschen**. Wenn bei vorhandenen Transaktionen auf die Preisliste verwiesen wird, können Sie sie nicht löschen. In diesem Fall können Sie die Preisliste deaktivieren, damit sie in keiner Ansicht angezeigt wird. 
3. Um die Preisliste zu deaktivieren, wählen Sie die Preisliste erneut aus und wählen Sie dann **Deaktivieren**.   
