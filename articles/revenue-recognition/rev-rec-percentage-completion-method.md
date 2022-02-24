---
title: Projektvorkalkulation (Festpreis) des Umsatzes
description: Dieses Thema enthält Informationen zum Festpreisumsatz in Projekten.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531432"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projektvorkalkulation (Festpreis) des Umsatzes 

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Wenn Sie eine Projektvertragszeile mit den folgenden Attributen in Dynamics 365 Project Operations auf Microsoft Dataverse erstellen, erstellt das System automatisch ein Projekt zur Schätzung des Festpreisumsatzes. Die Informationen in diesem Projekt basieren auf Folgendem:

  - Eine Abrechnungsmethode zum Festpreis.
  - Ein zugeordnetes Projekt.
  - Mindestens ein Meilenstein, der auf der **Rechnungsplan**-Registerkarte auf der **Projektvertragszeile**-Seite definiert ist.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Projektvorkalkulationen (Festpreis) des Umsatzes überprüfen
Führen Sie die folgenden Schritte aus, um Projekte zur Schätzung von Festpreiseinnahmen zu überprüfen:

1. Gehen Sie in der Dynamics 365 Finance-Umgebung zu **Projektmanagement und Buchhaltung** > **Projekte** > **Projektvorkalkulation (Festpreis) des Umsatzes**.
2. Wählen Sie das Projekt aus, das Sie anzeigen möchten, und doppelklicken Sie auf **Projekt-ID schätzen**, um den Datensatz zu öffnen und die Details des Projekts zu überprüfen.
3. Erweitern Sie die **Projekt**-Registerkarte. Sie sehen ein Projekt im **Ausgewählte Projekte**-Raster. Das System verwendet dies als Standardprojekt, da es sich um das Projekt handelt, das der Projektvertragszeile zugeordnet ist. 
4. Um die Zuordnung zu ändern, wählen Sie zusätzliche Projekte aus und fügen Sie sie dem **Ausgewählte Projekte**-Raster hinzu. Wenn in diesem Raster mehrere Projekte ausgewählt sind, werden die prozentualen Projektabschluss- und Umsatzschätzungen für alle ausgewählten Projekte zusammen berechnet.

  Projektkosten, Umsatzprofil, Kostenvorlage und der Periodencode können manuell festgelegt werden. Wenn sie nicht manuell festgelegt werden, werden die Werte bei der ersten Schätzungsberechnung für das Projekt standardmäßig unter Verwendung der für Projektkosten- und Ertragsprofile konfigurierten Regeln verwendet.

