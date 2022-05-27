---
title: Entwickleranmerkungen für Genehmigungen
description: Dieses Thema enthält zusätzliche Informationen für Entwickler zur Arbeit mit Genehmigungen.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579719"
---
# <a name="developer-notes-for-approvals"></a>Entwickleranmerkungen für Genehmigungen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations enthält eine Validierungslogik, die anhand der Genehmigungsphasen einen korrekten Datensatzübergang gewährleistet. Richtige Datensatzübergänge stellen sicher: 

  - Alle unterstützenden Zeilen werden in verwandten Tabellen wie Journalen und Istdaten erstellt.
  - Die genehmigende Person wird als **Projektgenehmiger** im Projekt gekennzeichnet, bevor Sie fortfahren.


[!INCLUDE[footer-include](../includes/footer-banner.md)]