---
title: Neuigkeiten September 2022 – Project Operations lite-Bereitstellung
description: Dieser Artikel enthält Informationen über die Qualitätsupdates, die in der Lite-Bereitstellung von Microsoft Dynamics 365 Project Operations im September 2022 zur Verfügung stehen.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621257"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Neuigkeiten September 2022 – Project Operations lite-Bereitstellung

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Version 4.46.0.60

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

| Funktionsbereich | Funktionsname | Weitere Informationen |
| --- | --- | --- |
| Verkaufschancenmanagement | **Überarbeitung und Aktivierung von Angeboten**<br>Project Operations bringt die volle Unterstützung des Vertriebsprozesses mit ein. Projektangebote können aktiviert werden, um einen Status darzustellen, in dem das Angebot schreibgeschützt ist und überprüft wird. Aktivierte Angebote können überarbeitet werden, um neue Angebote zu erstellen, die eine erhöhte Revisionsnummer haben. Aktivierte Projektangebote oder Angebotsüberarbeitungen können als „gewonnen“ oder „verloren“ geschlossen werden. | [Projektangebot aktivieren und überarbeiten](/dynamics365/project-operations/sales/activation-and-revision) |
| Preise und Abrechnung | **Zeitzonenunabhängiger Standardpreis**<br>Project Operations hat das Konzept eines zeitzonenunabhängigen Datums für alle Ist-Werte des Projekts eingeführt. Ein neues Feld, **Transaktionsdatum**, ist jetzt für Erfassungspositionen und Ist-Werte verfügbar und wird verwendet, um das Datum zu speichern, an dem die Transaktion stattfand, jedoch ohne dieses Datum in die koordinierte Weltzeit umzuwandeln. Dieses Datum wird für nachgelagerte Prozesse wie Preisvorschlag und Rechnungserstellung verwendet. | <p>[Kostenraten für projektbasierte Schätzungen und tatsächliche Transaktionen bestimmen](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Vertriebspreise für projektbasierte Schätzungen und tatsächliche Transaktionen bestimmen](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Preise und Abrechnung | **Datumswirksame Preisüberschreibungen in Project Operations**<br>Datumswirksame Preisüberschreibungen bieten eine Möglichkeit, bestimmte Preise in der Preisliste zu überschreiben oder zu ändern. | [Preisüberschreibungen mit Gültigkeitsdatum](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Zeit und Ausgaben | **Globaler Genehmiger**<br>Diese Funktion ermöglicht einen unabhängigen Softwareanbieter (ISV) und eine zentralisierte Genehmigung, unabhängig vom Status des Projekts oder Teammitglieds im Projekt. | [Sicherheit und Genehmigungen](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Qualitätsupdates

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Preise und Abrechnung | 2754422 | Material- und Ausgabenkalkulationen fließen nicht in Dynamics 365 Finance ein, wenn Projekte in Dataverse kopiert werden. |
| Zeit und Ausgaben | 2787409 | Ein ungültiger Genehmiger kann einen Nicht-Projektzeiteintrag genehmigen. |
| Verkaufschancenmanagement | 2788907 | Aktualisierte Fehlermeldung zur Eindeutigkeitsprüfung für Auftragspositionen, die Kennzeichnungen enthalten. |
| Zeit und Ausgaben | 2842253 | Null-Ausnahmenbehandlung für die Zeitgenehmigung. |
| Preise und Abrechnung | 2844181 | Wird die Korrelations-ID nicht abgerufen, wird die Rechnungserstellung blockiert. |
| Preise und Abrechnung | 2876628 | QLD, CLD: Die Auflösung der Kalkulationspreisliste sollte ältere Datumsbereichsfelder der Preisliste verwenden. |
| Fremdarbeit | 2893222 | Wenn für eine Fremdarbeitsposition keine Rolle angegeben ist, sollte es möglich sein, diese Position für ein Teammitglied jeder Rolle auszuwählen. |
