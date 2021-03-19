---
title: Entwickleranmerkungen für Genehmigungen
description: Dieses Thema enthält zusätzliche Informationen für Entwickler zur Arbeit mit Genehmigungen.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290268"
---
# <a name="developer-notes-for-approvals"></a>Entwickleranmerkungen für Genehmigungen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations enthält eine Validierungslogik, die anhand der Genehmigungsphasen einen korrekten Datensatzübergang gewährleistet. Richtige Datensatzübergänge stellen sicher: 

  - Alle unterstützenden Zeilen werden in verwandten Tabellen wie Journalen und Istdaten erstellt.
  - Die genehmigende Person wird als **Projektgenehmiger** im Projekt gekennzeichnet, bevor Sie fortfahren.


[!INCLUDE[footer-include](../includes/footer-banner.md)]