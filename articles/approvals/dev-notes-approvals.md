---
title: Entwickleranmerkungen für Genehmigungen
description: Dieses Thema enthält zusätzliche Informationen für Entwickler zur Arbeit mit Genehmigungen.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991665"
---
# <a name="developer-notes-for-approvals"></a>Entwickleranmerkungen für Genehmigungen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations enthält eine Validierungslogik, die anhand der Genehmigungsphasen einen korrekten Datensatzübergang gewährleistet. Richtige Datensatzübergänge stellen sicher: 

  - Alle unterstützenden Zeilen werden in verwandten Tabellen wie Journalen und Istdaten erstellt.
  - Die genehmigende Person wird als **Projektgenehmiger** im Projekt gekennzeichnet, bevor Sie fortfahren.


[!INCLUDE[footer-include](../includes/footer-banner.md)]