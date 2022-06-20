---
title: Was ist neu August 2021 - Project Operations Lite-Bereitstellung
description: Dieser Artikel enthält Informationen über die Qualitätsupdates, die in der Lite-Bereitstellung von Project Operations im August 2021 verfügbar sind.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 84318a26d97355fe56794e1d1532576cde4af661
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922037"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Was ist neu August 2021 - Project Operations Lite-Bereitstellung

_Gilt für: Lite Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieser Artikel bezieht sich auf die folgenden Dynamics 365 Project Operations-Komponenten und Versionen:

  - Project Operations in Dataverse, Umgebungsversion 4.13.0.152

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

Die folgenden Funktionen sind in dieser Version enthalten:

- **Zulassungssätze**: Genehmigungssets gruppieren Genehmigungsanfragen für Zeit, Ausgaben oder Materialverbrauch in kleinere Vorgangsteilmengen. Diese Gruppierung ermöglicht die Bearbeitung von Genehmigungen nach Projekt in einer bestimmten Reihenfolge und ermöglicht Wiederholungsversuche und Sequenzierung. Das Gruppieren der Anfragen verbessert die Zuverlässigkeit und Nachvollziehbarkeit der Genehmigungsverarbeitung bei großen Genehmigungsmengen. Weitere Informationen finden Sie unter [Genehmigungssätze](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| Preise und Abrechnung | 2295625 | Der Meilensteinname muss aus dem Rechnungsplan in das Rechnungspostendetail kopiert werden. |
| Preise und Abrechnung | 2316323 | Der Rabatt sollte auf einer Proforma-Rechnung in Project Operations für ressourcenbasierte Szenarien nicht bearbeitet werden können. |
| Verkaufschancenmanagement | 2338619 | Die Geschäftsregeln **Verkaufschance** und **Angebot** dürfen nur auf Seiten aufgerufen werden. |
| Ressourcenverwaltung | 2316523 | Das Verwenden von **Anfrage senden** aus einer Ressourcenanforderung, der eine Rolle zugeordnet ist, sollte keinen Fehler anzeigen. |
| Ressourcenverwaltung | 2326885 | Beim Erstellen einer Ressourcenanforderung mittels eines Projekts sollte kein Fehler angezeigt werden. |
| Zeit und Ausgaben | 2335584 | Veraltete Aufgabenflüsse in der Zeiterfassung. |
| Zeit und Ausgaben | 2336884 | Die Zeiteingabeschaltfläche **Woche kopieren** muss für mehr als nur für den aktuellen Benutzer funktionieren. |
