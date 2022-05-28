---
title: Ressourcennutzung – Übersicht
description: Dieses Thema enthält Informationen zur Ressourcennutzung in Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e24bbb33cdf34426d4e7fff21b68fcaea2fcef5e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587125"
---
# <a name="resource-utilization-overview"></a>Ressourcennutzung – Übersicht

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Ressourcen weisen für die abrechenbare Nutzung einen Zielwert auf. Dieser Zielwert für die Nutzung ist entweder als ein Attribut auf der Standardrolle einer Ressource definiert, oder er ist im Datensatz der einzelnen buchbaren Ressource festgelegt. Die Berechnung der Nutzung basiert auf den tatsächlichen Stunden, die Ressourcen in ihren genehmigten Zeiteinträgen angegeben haben.

Die folgenden Formeln werden zur Berechnung der Nutzung verwendet:

  - Fakturierbare Nutzung = Fakturierbare tatsächliche Stunden ÷ Ressourcenkapazität
  - Nicht fakturierbare Nutzung = Tatsächliche Zeit mit Fakturierungstyp-ID = Nicht fakturierbar, komplementär oder nicht verfügbar ÷ Ressourcenkapazität
  - Intern = Tatsächliche Zeit ohne Kaufvertrag ÷ Ressourcenkapazität
  - Ressourcenkapazität = Ressourcenarbeitsstunden – Abwesend – Arbeitsfreie Tage

Sie finden die Ansicht **Ressourcennutzung** im Bereich **Ressourcen**.

Jede Zelle im Raster steht für die abrechenbare Nutzung in Prozent der Ressource in einem Zeitraum, beispielsweise einem Tag, einer Woche oder einem Monat. Die folgenden Formeln werden für die Farbgebung der Zellen verwendet:

  - **Grün**: Verrechenbare Nutzung >= Ressourcen-Zielnutzung
  - **Gelb**: Zielnutzung – 20 <= Verrechenbare Nutzung < Zielnutzung
  - **Rot**: Verrechenbare Nutzung < Zielnutzung – 20

Da die Ansicht **Ressourcennutzung** auf der Zeitplanübersicht basiert, können Sie die Filterfunktionen der Zeitplanübersicht zum Filtern Ihrer Ergebnisse verwenden.

Das Raster erfordert das Festlegen einer Zielnutzung entweder für die Rolle oder die einzelne Ressource. Navigieren Sie hierfür zu **Ressourcen** > **Ressourcenrollen**.

Zusätzlich muss jeder buchbaren Ressource eine Standardrolle zugewiesen werden. Navigieren Sie zu **Ressourcen** > **Ressourcen**. Überprüfen Sie auf der Registerkarte **Project Service**, ob eine Ressourcenrolle definiert ist und das Feld **Ist Standard** für die Rolle auf **Ja** festgelegt ist. Sie können zusätzliche Rollen hinzufügen, für die **Ist Standard** = **Nein** gilt. Die Rolle mit **Ist Standard** = **Ja** wird zur Evaluierung der Ressourcennutzung anhand des Ziels für diese Rolle verwendet.

Auf der Registerkarte **Project Service** können Sie außerdem eine individuelle Zielnutzung für die Ressource festlegen. Die Nutzungsberechnung verwendet dann die Zielnutzung, um statt dem Ziel der Standardrolle der Ressource das Ziel der Ressource zu evaluieren.

Die Nutzung für eine Ressource wird nur dann angezeigt, wenn diese Ressource für den Zeitraum ihrer Anzeige im Raster über genehmigte, fakturierbare Zeit verfügt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]