---
title: Neuigkeiten für Februar 2022 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version vom Februar 2022 der Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 76ae00517c857415c89d7a03f421686dad28da93
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600833"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten für Februar 2022 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

*Gilt für: Project Operations für ressourcen-/nicht vorratsbasierte Szenarien*

Dieses Thema gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Version 4.28.0.120
- Projektmanagement und -buchhaltung in einer Dynamics 365 Finance-Umgebungsversion 10.0.24

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

- Ab dieser Version können Sie einem einzelnen Projekt bis zu 300 Teammitglieder hinzufügen. Bisher war die Anzahl der Teammitglieder auf 150 begrenzt. Weitere Informationen finden Sie unter [Projekt-Limits](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Project Operations – Zuordnungs-Updates für duales Schreiben

Die folgende Liste zeigt die Zuordnungen für duales Schreiben, die in der Project Operations-Version vom Februar 2022 geändert oder hinzugefügt wurden.

| Entitätszuordnung | Aktualisierte Version | Anmerkungen |
| --- | --- | --- |
| Exportentität für Projektkosten der Project Operations-Integration (msdyn\_expenses) | 1.0.0.3 | Erweitert für die Synchronisierung von Projektaktivitäten zu Dataverse. |

Die aktuelle Liste und Versionen der Zuordnungen für duales Schreiben von Project Operations finden Sie unter[Versionen der Zuordnungen für duales Schreiben von Project Operations](../environment/resource-dual-write-maps.md).

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Einige Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Sie können die aktive Version der Zuordnung in der Spalte **Version** auf der Seite **Dual-Write** anzeigen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine vorkonfigurierte Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen im Abschnitt [Problem mit fehlenden Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) des Handbuchs zur Fehlerbehebung für duales Schreiben.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Preise und Abrechnung | 2415109 | Der Standardwert im **Zahlungsbedingungen für Operationen**-Feld muss der Projektvertrags-Kundendatensatz und der Proforma-Rechnungsdatensatz sein. |
| Preise und Abrechnung | 2497369 | Die Materialkorrektur muss dem Datumswert im **Korrektur**-Parameter folgen. |
| Preise und Abrechnung | 2498697 | Verbesserte Sicherheitskonfiguration für **Rückruf des Zeiteintrags**. |
| Preise und Abrechnung | 2513824 | Bei ressourcenbasierten Szenarien darf die Transaktionskategorie-ID in Project Operations nicht länger als 28 Zeichen sein. |
| Preise und Abrechnung | 2517455 | Die **Rechnungspostenbuchungen aktualisieren**-Aktion darf nicht mehrfach gleichzeitig für dieselbe Rechnung ausgelöst werden. |
| Preise und Abrechnung | 2517465 | Die **Rechnungspostendetails deaktivieren**-Aktion ist blockiert, da sie nicht unterstützt wird. |
| Preise und Abrechnung | 2556660 | Die Datumsgültigkeitsprüfung, die für die Preisliste durchgeführt wird, die an einen Projektparameterdatensatz angehängt ist, wurde korrigiert. |
| Verkaufschancenmanagement | 2369202 | Die Geschäftslogik wurde korrigiert, die überprüft, ob Preislisten mit sich überschneidenden Gültigkeitsdaten demselben Projektvertrag angehängt werden können. |
| Verkaufschancenmanagement | 2385965 | Das Verhalten auf der **Kunden**-Registerkarte der **Projektvertrag**-Seite wurde korrigiert, wenn Sie **Speichern und schließen** auswählen. |
| Zeit und Ausgaben | 2538503 | Eine Projektaufgabe muss in der **Projekt-Ist-Werte**-Entität Unternehmen vorhanden sein, nachdem eine Spesenabrechnung gebucht wurde. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmanagement und -buchhaltung bei Dynamics 365 Finance

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Projektmanagement und -buchhaltung | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Beim Import von Kreditorengutschriften tritt ein Fehler auf. Die Fehlermeldung lautet: „Einbehaltungsbetrag darf nicht größer sein als der verbleibende Nettobetrag.“ |
| Projektmanagement und -buchhaltung | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Wenn ein Rechnungsvorschlag Gebührentransaktionen mit Nullbeträgen enthält, bei denen es sich um nicht fakturierte Verkaufs-Ist-Werte handelt, kann keine Rechnungsstellung erfolgen. |
| Projektmanagement und -buchhaltung | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Die gebuchten Kosten sind nicht korrekt, nachdem der Kaufpreis aktualisiert und **Änderungsmanagement aktivieren** aktiviert wurde.|
| Projektmanagement und -buchhaltung | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Die Buchungskalkulation für ein Festpreisprojekt verwendet die falsche Währung und den falschen Betrag im Kalkulationsbeleg, auch wenn die **Projektvertragswährung für Schätzungsberechnung aktivieren**-Funktion aktiviert ist. |
| Projektmanagement und -buchhaltung | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** sollte keinen Aufruf durchführen, um die Änderungsnachverfolgung zu aktivieren, ohne Ausnahmen für Entitäten abzufangen, die über nicht aktivierte Konfigurationsschlüssel verfügen. |
| Projektmanagement und -buchhaltung | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Der Batch-Auftrag wird behoben, wenn mehrere erweiterte Erfassungen gebucht werden und ein Fehler auftritt. |
| Reisekosten und Ausgaben | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Aufgrund eines Abrechnungsproblems im Zusammenhang mit Barvorschüssen auf Spesenabrechnungen wird der Steuerbetrag nicht als Teil des Barvorschusses gedeckt. |
| Reisekosten und Ausgaben | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Umsatzsteuerinformationen sind im Bereicht **Aufwand – Gebuchte Transaktionen** nicht enthalten. |
| Reisekosten und Ausgaben | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Die Spesenrichtlinienverletzung **Belege erforderlich** zeigt fälschlicherweise eine Warnung bei Spesenabrechnungen an. |
| Reisekosten und Ausgaben | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Eine Projekttransaktion enthält keine nicht erstattungsfähige Umsatzsteuer im Gesamtverkaufsbetrag, wenn die Transaktion das Ergebnis einer Fahrtkostenpauschale ist. |
| Reisekosten und Ausgaben | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Wenn eine Einzelposten Steuern enthält, können Sie das Einzelpostendatum nicht ändern, und es tritt ein Statusfehler des Quelldokuments auf. |

## <a name="removed-and-deprecated-features"></a>Entfernte und veraltete Funktionen

Das Thema [Entfernte oder veraltete Funktionen in Project Operations](removed-depreciated-features-project.md) beschreibt Funktionen, die aus Dynamics 365 Project Operations entfernt wurden oder veraltet sind.

- Eine entfernte Funktion ist im Produkt nicht mehr verfügbar.
- Eine veraltete Funktion wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

12 Monate vor dem Entfernen wird im Thema [Entfernte oder veraltete Funktionen in Project Operations](removed-depreciated-features-project.md) ein Verfallshinweis angezeigt.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Zeit für die Entfernung weniger als 12 Monate. In der Regel handelt es sich bei diesen Änderungen um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.
