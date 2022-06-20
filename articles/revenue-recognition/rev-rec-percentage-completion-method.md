---
title: Projektvorkalkulation (Festpreis) des Umsatzes
description: Dieser Artikel enthält Informationen über Festpreisumsätze in Projekten.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928385"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projektvorkalkulation (Festpreis) des Umsatzes 

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Wenn Sie eine Projektvertragszeile mit den folgenden Attributen in Dynamics 365 Project Operations auf Microsoft Dataverse erstellen, erstellt das System automatisch ein Projekt zur Schätzung des Festpreisumsatzes. Die Informationen in diesem Projekt basieren auf Folgendem:

  - Eine Abrechnungsmethode zum Festpreis.
  - Ein zugeordnetes Projekt.
  - Mindestens ein Meilenstein, der auf der **Rechnungsplan**-Registerkarte auf der **Projektvertragszeile**-Seite definiert ist.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Projektvorkalkulationen (Festpreis) des Umsatzes überprüfen
Führen Sie die folgenden Schritte aus, um Projekte zur Schätzung von Festpreiseinnahmen zu überprüfen:

1. Gehen Sie in der Dynamics 365 Finance-Umgebung zu **Projektmanagement und -buchhaltung** > **Projekte** > **Projektvorkalkulation (Festpreis) des Umsatzes**.
2. Wählen Sie das Projekt aus, das Sie anzeigen möchten, und doppelklicken Sie auf **Projekt-ID schätzen**, um den Datensatz zu öffnen und die Details des Projekts zu überprüfen.
3. Erweitern Sie die **Projekt**-Registerkarte. Sie sehen ein Projekt im **Ausgewählte Projekte**-Raster. Das System verwendet dies als Standardprojekt, da es sich um das Projekt handelt, das der Projektvertragszeile zugeordnet ist. 
4. Um die Zuordnung zu ändern, wählen Sie zusätzliche Projekte aus und fügen Sie sie dem **Ausgewählte Projekte**-Raster hinzu. Wenn in diesem Raster mehrere Projekte ausgewählt sind, werden die prozentualen Projektabschluss- und Umsatzschätzungen für alle ausgewählten Projekte zusammen berechnet.

  Projektkosten, Umsatzprofil, Kostenvorlage und der Periodencode können manuell festgelegt werden. Wenn sie nicht manuell festgelegt werden, werden die Werte bei der ersten Schätzungsberechnung für das Projekt standardmäßig unter Verwendung der für Projektkosten- und Ertragsprofile konfigurierten Regeln verwendet.



[!INCLUDE[footer-include](../includes/footer-banner.md)]