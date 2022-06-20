---
title: Entwickleranmerkungen für Genehmigungen
description: Dieser Artikel enthält zusätzliche Informationen für Entwickler über die Arbeit mit Genehmigungen.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924751"
---
# <a name="developer-notes-for-approvals"></a>Entwickleranmerkungen für Genehmigungen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations enthält eine Validierungslogik, die anhand der Genehmigungsphasen einen korrekten Datensatzübergang gewährleistet. Richtige Datensatzübergänge stellen sicher: 

  - Alle unterstützenden Zeilen werden in verwandten Tabellen wie Journalen und Istdaten erstellt.
  - Die genehmigende Person wird als **Projektgenehmiger** im Projekt gekennzeichnet, bevor Sie fortfahren.


[!INCLUDE[footer-include](../includes/footer-banner.md)]