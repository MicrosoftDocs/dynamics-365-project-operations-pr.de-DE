---
title: Neuigkeiten September 2022 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieser Artikel enthält Informationen zu den Qualitätsupdates, die in der Version vom September 2022 von Microsoft Dynamics 365 Project Operations für ressourcenbasierte/nicht vorratsbasierte Szenarien zur Verfügung stehen.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621244"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten September 2022 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Version 4.46.0.60
- Projektmanagement und -buchhaltung in einer Dynamics 365 Finance-Umgebungsversion 10.0.29

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

| Funktionsbereich | Funktionsname | Weitere Informationen |
| --- | --- | --- |
| Verkaufschancenmanagement | **Überarbeitung und Aktivierung von Angeboten**<br>Project Operations bringt die volle Unterstützung des Vertriebsprozesses mit ein. Projektangebote können aktiviert werden, um einen Status darzustellen, in dem das Angebot schreibgeschützt ist und überprüft wird. Aktivierte Angebote können überarbeitet werden, um neue Angebote zu erstellen, die eine erhöhte Revisionsnummer haben. Aktivierte Projektangebote oder Angebotsüberarbeitungen können als „gewonnen“ oder „verloren“ geschlossen werden. | [Projektangebot aktivieren und überarbeiten](/dynamics365/project-operations/sales/activation-and-revision) |
| Preise und Abrechnung | **Zeitzonenunabhängiger Standardpreis**<br>Project Operations hat das Konzept eines zeitzonenunabhängigen Datums für alle Ist-Werte des Projekts eingeführt. Ein neues Feld, **Transaktionsdatum**, ist jetzt für Erfassungspositionen und Ist-Werte verfügbar und wird verwendet, um das Datum zu speichern, an dem die Transaktion stattfand, jedoch ohne dieses Datum in die koordinierte Weltzeit umzuwandeln. Dieses Datum wird für nachgelagerte Prozesse wie Preisvorschlag und Rechnungserstellung verwendet. | <p>[Kostenraten für projektbasierte Schätzungen und tatsächliche Transaktionen bestimmen](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Vertriebspreise für projektbasierte Schätzungen und tatsächliche Transaktionen bestimmen](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Preise und Abrechnung | **Datumswirksame Preisüberschreibungen in Project Operations**<br>Datumswirksame Preisüberschreibungen bieten eine Möglichkeit, bestimmte Preise in der Preisliste zu überschreiben oder zu ändern. | [Preisüberschreibungen mit Gültigkeitsdatum](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Fremdarbeit | **Fremdarbeit und Kreditorenrechnungsabstimmung**<br>Mit dieser Funktion können Kunden Unterverträge erstellen, um Ressourcenzeit, Ausgabenkategorien und Materialien einzukaufen, die für die Projektarbeit verwendet werden. Kunden können dadurch auch in Finanz- und Betriebs-Apps Kreditorenrechnungen zu erfassen, die Projektmanagern in Dataverse zur Überprüfung zur Verfügung stehen. | <p>[Fremdarbeitsverwaltung](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Kreditorenrechnungen erstellen](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Zeit und Ausgaben | **Globaler Genehmiger**<br>Diese Funktion ermöglicht einen unabhängigen Softwareanbieter (ISV) und eine zentralisierte Genehmigung, unabhängig vom Status des Projekts oder Teammitglieds im Projekt. | [Sicherheit und Genehmigungen](/dynamics365/project-operations/approvals/approvals-security) |
| Ausgabenverwaltung | **Möglichkeit, Ausgabenverbindlichkeit in Kreditorenwährung zu buchen**<br>Mit dieser Funktion können Sie Ausgabenberichte in Kreditorenwährung für die Barzahlungsmethode buchen. | [Möglichkeit, Ausgabenverbindlichkeit in Kreditorenwährung zu buchen](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projektbeschaffung | **Pay-When-Paid-Kreditorenzahlungen**<br>Diese Funktion ermöglicht die Verwendung der Funktion „Zahlung bei Zahlungsempfang“ (PWP) mit nicht vorrätigen Umgebungen in Project Operations. Es ermöglicht das Sperren/Einbehaltung der Kreditorenzahlungen auf der Grundlage von Bedingungen für die Einbehaltung, bis die Zahlung vom Kunden eingegangen ist. | [Pay-When-Paid-Kreditorenzahlungen](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projektbeschaffung | **Projektbestellanforderungen**<br>Diese Funktion ermöglicht es Benutzern, projektbezogene Bestellungen in juristischen Personen zu erstellen, bei denen die Integration von Project Operations auf Dynamics 365 Customer Engagement aktiviert ist. Projektbestellungen können verwendet werden, um die Beschaffung von nicht vorrätigem Material für das Projekt durch Persona der Beschaffungsabteilung zu erfassen. Projektbestellungen werden nicht mit Dataverse synchronisiert. Sie können jedoch eine virtuelle Entität verwenden, um Projektbestellpositionen in Dataverse zur Information des Projektmanagers anzuzeigen. Projektbezogene Kreditorenrechnungskosten sind in die Entität „Projekt-Ist-Werte“ in Dataverse integriert. Projektkosten werden mithilfe der Project Operations-Integrationserfassung im untergeordneten Sachkonto des Projekts erfasst. | |

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Die folgende Tabelle zeigt die Zuordnungen für duales Schreiben, die in der Version vom September 2022 von Project Operations geändert oder hinzugefügt wurden.

| Entitätszuordnung | Aktualisierte Version | Anmerkungen |
| -------------- | ------------------- | ------------|
| Tatsächliche Werte der Project Operations-Integration (msdyn_actuals) | 1.0.0.15 | Diese Zuordnung unterstützt die Verarbeitung von Ist-Werten von Fremdaufträgen mit Project Operations für ressourcenbasierte Szenarien. |
| Project Operations-Integrationsprojektanbieter-Rechnungsexportentität (msdyn_projectvendorinvoices) | 1.0.0.2 | Diese Zuordnung unterstützt die Verarbeitung von Ist-Werten von Fremdaufträgen mit Project Operations für ressourcenbasierte Szenarien. |
| Project Operations-Integrationsprojektanbieter-Rechnungszeilenexportentität (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Diese Zuordnung unterstützt die Verarbeitung von Ist-Werten von Fremdaufträgen mit Project Operations für ressourcenbasierte Szenarien. |

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Einige Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Sie können die aktive Version der Zuordnung in der Spalte **Version** auf der Seite **Dual-Write** anzeigen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine vorkonfigurierte Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen im Abschnitt [Problem mit fehlenden Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) des Handbuchs zur Fehlerbehebung für duales Schreiben.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Preise und Abrechnung | 2754422 | Material- und Ausgabenkalkulationen fließen nicht in Finance ein, wenn Projekte in Dataverse kopiert werden. |
| Zeit und Ausgaben | 2787409 | Ein ungültiger Genehmiger kann einen Nicht-Projektzeiteintrag genehmigen. |
| Verkaufschancenmanagement | 2788907 | Aktualisierte Fehlermeldung zur Eindeutigkeitsprüfung für Auftragspositionen, die Kennzeichnungen enthalten. |
| Zeit und Ausgaben | 2842253 | Null-Ausnahmenbehandlung für die Zeitgenehmigung. |
| Preise und Abrechnung | 2844181 | Wird die Korrelations-ID nicht abgerufen, wird die Rechnungserstellung blockiert. |
| Preise und Abrechnung | 2876628 | QLD, CLD: Die Auflösung der Kalkulationspreisliste sollte ältere Datumsbereichsfelder der Preisliste verwenden. |
| Fremdarbeit | 2893222 | Wenn für eine Fremdarbeitsposition keine Rolle angegeben ist, sollte es möglich sein, diese Position für ein Teammitglied jeder Rolle auszuwählen. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmanagement und -buchhaltung in Finance

Melden Sie sich bei Microsoft Dynamics Lifecycle Services an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates enthalten sind und zeigen Sie die [Wissensdatenbankartikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559) an.

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Diese Features sind in der nächsten Version standardmäßig aktiviert.

Die folgende Tabelle listet die Features auf, die in Version 10.0.30 standardmäßig aktiviert sind. Die meisten Features, die automatisch aktiviert wurden, können in [Featureverwaltung](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) deaktiviert werden. In Zukunft könnten einige Features, die automatisch aktiviert wurden, aus der Featureverwaltung entfernt und obligatorisch werden. Diese Änderung stellt sicher, dass Kunden die aktuelle Funktionalität verwenden, sodass Erweiterungen auf der aktuellen Funktionalität aufbauen können, wenn sie hinzugefügt werden. Features werden niemals in weniger als einem Jahr automatisch aktiviert, es sei denn, sie gelten als wesentlich.

| Funktionsname | Datum aktivieren | Feature hinzugefügt | Featurezustand | Modul |
| --- | --- | --- |--- |--- |
| Asynchronen Vorgang aktivieren, wenn der Benutzer zwischen synchronen und asynchronen Vorgängen wechseln muss | 21. Oktober 2022 | 9. April 2021 | Standardmäßig aktiviert | Ausgabenverwaltung |
| Ausgabenrichtlinienüberprüfung für Belege erforderlich | 21. Oktober 2022 | 20. Dezember 2021 | Standardmäßig aktiviert | Ausgabenverwaltung |
| Listenansicht von Ausgabenberichte, die von delegierenden Mitarbeitern erstellt wurden | 21. Oktober 2022 | 19. Februar 2020 | Standardmäßig aktiviert | Ausgabenverwaltung |
| Gesamte Kilometerleistung nach Geschäftsjahr berechnen | 21. Oktober 2022 | 10. Mai 2022 | Standardmäßig aktiviert | Ausgabenverwaltung |
