---
title: Neuigkeiten oder Änderungen für März 2021 – Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigung
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version von Project Operations vom März 2021 für lager-/produktionsbasierte Szenarien verfügbar sind.
author: andchoi
manager: tfehr
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 804b5d1cc3392349fb6bcc81a91d69d0d9dc51da
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701933"
---
# <a name="whats-new-or-changed-in-project-operations-march-2021-for-stockedproduction-based-scenarios"></a>Neuigkeiten oder Änderungen für März 2021 – Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigung

_**Gilt für:** Project Operations für Szenarien basierend auf den vorrätigen Ressourcen/Fertigung_

Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:

- Projektmanagement und Buchhaltung in Dynamics 365 Finance, Umgebungsversion 10.0.17

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version
Die folgenden Funktionen sind in dieser Version enthalten:

  - [Leistung von Projektrechnungsvorschlägen](../project-invoice-proposal-performance.md)
 
### <a name="quality-updates"></a>Qualitätsupdates

| Funktionsbereich                        | Referenznummer | Qualitätsupdate                                                                                                                                                                                                                                                   |
|-------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektmanagement und -buchhaltung | [420064](https://fix.lcs.dynamics.com/Issue/Details/?bugId=420064) | Negativ gebuchte Projekttransaktionen werden nach der Neuberechnung des Inventars nicht aktualisiert.                                                                                                                      |
| Projektmanagement und -buchhaltung | [438692](https://fix.lcs.dynamics.com/Issue/Details/?bugId=438692) | Das Löschen einer Finanzierungsquelle sollte möglich sein, wenn der Finanzierungsquelle keine Transaktion oder Rechnung zugeordnet ist.                                                                                                           |
| Projektmanagement und -buchhaltung | [439470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=439470) | Bei tatsächlichen Schätzungstransaktionen werden keine Ausgaben- und Positionstransaktionen aus der Vorperiode angezeigt.                                                                                                       |
| Projektmanagement und -buchhaltung | [452710](https://fix.lcs.dynamics.com/Issue/Details/?bugId=452710) | Der Ledger-Beschreibungswert ist für den Packzettel der Projektartikelanforderungen falsch.                                                                                                              |
| Projektmanagement und -buchhaltung | [455602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=455602) | Wenn Journale für ein Projekt gebucht werden, werden die Finanzdimensionen nicht aus dem Mitarbeiter und dem Artikel im Gutschein ausgewählt.                                                                               |
| Projektmanagement und -buchhaltung | [472988](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472988) | Wenn der Nettobetrag der Zeile in der Projektrechnungssumme aktualisiert wird, wird der Verkaufsbetrag mit dem angepassten Betrag in der gebuchten Transaktion gefüllt.                                                                               |
| Projektmanagement und -buchhaltung | [477969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477969) | Die Rechnung wählt nicht die Projekt-ID-Referenz aus, wenn die Lieferantenrechnungsposten auf der **Pay-When-Paid-Kreditorenzahlungen**-Seite überprüft werden.                                                                                                   |
| Projektmanagement und -buchhaltung | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Der Vertragsbetrag auf der **Akonto**-Seite ist für ein Festpreisprojekt mit mehreren Finanzierungsquellen falsch.                                                                                                  |
| Projektmanagement und -buchhaltung | [481443](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481443) | Die aufgelaufenen Einnahmen aus einem Festpreisprojekt werden auch nach der Buchung der Eliminierung nicht angepasst.                                                                                                                                |
| Projektmanagement und -buchhaltung | [483209](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483209) | Der Kreditstatus wird nicht aktualisiert, wenn ein Projektauftrag über einen Rechnungsvorschlag in Rechnung gestellt wird.                                                                                                  |
| Projektmanagement und -buchhaltung | [484274](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484274) | Wenn die Bestellung in Rechnung gestellt wird und die Rechnung eine Beschaffungskategorie und einen Artikel enthält, erhält der Kunde die falschen Kontoinformationen.                                                                                              |
| Projektmanagement und -buchhaltung | [484817](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484817) | Projektrechnungsvorschläge, die durch wiederkehrende Stapelaufträge generiert werden, enthalten doppelte Transaktionen mit einem Betrag von null.                                                                                                  |
| Projektmanagement und -buchhaltung | [486817](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486817) | Entfernen Sie die Fehlergrenzwertprüfung, während Sie die Gewinn- und Verlustberichte des Projekts ausführen.                                                                                                                                  |
| Projektmanagement und -buchhaltung | [488076](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488076) | Ausgaben, die durch konzerninterne Aufladung gebucht werden, zeigen bei Verwendung der **Kosten buchen**-Funktionalität im **Projektcode für Zeit und Material** nicht die Gewinn- und Verlustbuchung.                                                         |
| Projektmanagement und -buchhaltung | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Der Filter **Rechnungsstatus** in gebuchten Projekttransaktionen für Festpreisprojekte funktioniert nicht.                                                                                                   |
| Projektmanagement und -buchhaltung | [488783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488783) | Arbeitszeittabelleneinträge werden aufgrund doppelter Delegatdatensätze dupliziert.                                                                                                                                           |
| Projektmanagement und -buchhaltung | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Die Eliminierung der umgekehrten Schätzung funktioniert in **Periodisch** nicht.                                                                                                                                                 |
| Projektmanagement und -buchhaltung | [498010](https://fix.lcs.dynamics.com/Issue/Details/?bugId=498010) | Die richtigen Daten können nicht aus der **Transaktionen anpassen**-Option im **Projektmanagement und Buchhaltung**-Modul ausgewählt werden, wenn ein zusätzlicher Bereich hinzugefügt wird. Der **Zusätzlich**-Filter wird ignoriert.                      |
| Projektmanagement und -buchhaltung | [508494](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508494) | Nachdem Sie einen Auftrag aufgezeichnet haben, können Sie den Status des Fertigungsauftrags nicht zurücksetzen.                                                                                                              |
| Projektmanagement und -buchhaltung | [509716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509716) | Artikel mit automatischer Reserve und Verfügbarkeitszusage (CTP), die aus einem Projekt stammen, werden nicht reserviert.                                                                                                                      |
| Projektmanagement und -buchhaltung | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Die **Bilanzierungsanpassung**-Funktion erstellt ein Problem mit Sachkonten, die **Manuelle Eingabe nicht zulassen** ausgewählt haben.                                                                     |
| Projektmanagement und -buchhaltung | [510079](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510079) | Im **Umsatz erzielen – Verkaufswert**-Feld auf Projektanweisungen sollte kein Wert angezeigt werden, wenn die Schätzung eliminiert wird.                                                                                 |
| Projektmanagement und -buchhaltung | [510607](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510607) | Die Kosten- und Verkaufspreise sind bei einer Projektanpassung mit Rollenpreisen falsch.                                                                                                                        |
| Projektmanagement und -buchhaltung | [10728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=10728) | In Project Operations funktioniert die Vorschuss-Korrekturrechnung nach einer teilweisen Vorschuss-Korrektur nicht.                                                                                                                   |
| Projektmanagement und -buchhaltung | [510743](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510743) | Die **Link entfernen**-Option sollte nur aktiviert werden, wenn Sie eine konzerninterne Bestellung stornieren.                                                                                                                                          |
| Projektmanagement und -buchhaltung | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | WIP – Buchung des Verkaufswerts in der konzerninternen Projektrechnung wählt ein unerwartetes Konto aus.                                                                                                                  |
| Projektmanagement und -buchhaltung | [514432](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514432) | Die Gebühr aus einer Abrechnungsregel wird nicht neu berechnet, wenn der Rechnungsvorschlag Zeilen enthält, die für Gutschriften ausgewählt wurden.                                                                                            |
| Projektmanagement und -buchhaltung | [515820](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515820) | Im Zeitplan für die Ausgaben der Federal Awards Inquiry werden die Belegbeträge angezeigt, wenn für eine Aufwandsbuchung kein Projektrechnungsvorschlag ausgeführt wurde.                                               |
| Projektmanagement und -buchhaltung | [516301](https://fix.lcs.dynamics.com/Issue/Details/?bugId=516301) | Die WIP-Kosten sind in der Projektaufstellung für einen Serviceartikel mit einer **Balance**-Projektgruppe falsch.                                                                                               |
| Projektmanagement und -buchhaltung | [516553](https://fix.lcs.dynamics.com/Issue/Details/?bugId=516553) | Eine Freitextrechnung, die einem Projekt zugeordnet ist, kann nicht korrigiert werden.                                                                                                                                                  |
| Projektmanagement und -buchhaltung | [517074](https://fix.lcs.dynamics.com/Issue/Details/?bugId=517074) | Wenn Sie eine Projekttransaktion auf einen Verkaufspreis von null einstellen, wird eine neue angepasste Transaktion mit dem Rechnungsstatus von **Nicht fakturierbar** geschaffen.                                                               |
| Projektmanagement und -buchhaltung | [517414](https://fix.lcs.dynamics.com/Issue/Details/?bugId=517414) | Beim Buchen einer Projektanpassung tritt ein Problem auf, wenn Sie mehrere Zeilen gleichzeitig anpassen.                                                                                                                               |
| Projektmanagement und -buchhaltung | [518001](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518001) | Eine Anpassung wird mit einem falschen Kostenbetrag gebucht, wenn sich der Produktkostenpreis und die Artikelbedarfsmenge nach dem Buchen des Packzettels ändern.                                                                   |
| Projektmanagement und -buchhaltung | [518092](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518092) | Die Finanzdimensionen einer Direktlieferungsbestellung sind falsch und wurden durch finanzielle Dimensionen des Kundenauftrags ersetzt.                                                              |
| Projektmanagement und -buchhaltung | [518605](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518605) | Die Erfassungsposition für das Projekt mit negativer Menge aktualisiert die Prognose nicht, wenn die Prognosemenge Null ist.                                                                                        |
| Projektmanagement und -buchhaltung | [518657](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518657) | Der Versuch, Artikelanforderungen mit Microsoft Excel zu importieren, führt zu einem Fehler beim Empfangsdatum.                                                                                                                                                    |
| Projektmanagement und -buchhaltung | [519200](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519200) | Der Projektpositionstransaktionsverweis auf eine Lieferantenrechnungstransaktion wird nicht aktualisiert, wenn die Rechnung gebucht wird.                                                                                               |
| Projektmanagement und -buchhaltung | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Wenn Sie einen Projektrechnungsvorschlag buchen, kann der folgende Fehler auftreten: „Die Transaktion wird nicht mit der Berichtswährung ausgeglichen, wenn die abgezogene Vorabrechnung hinzugefügt wird“.                                                                    |
| Projektmanagement und -buchhaltung | [520268](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520268) | Die Projekt-ID und der Projektname sind nicht im **Einbehaltung der Lieferantenzahlung**-Bericht aufgeführt, wenn Sie das Projektlayout verwenden.                                                                                              |
| Projektmanagement und -buchhaltung | [520872](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520872) | Wenn ein Projekt über eine Datenentität erstellt wird, ist die Sortierpriorität der Ledger-Buchung falsch.                                                                                                                      |
| Projektmanagement und -buchhaltung | [521150](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521150) | Der Kostenbetrag ist bei gebuchten Projekttransaktionen falsch, die auf der Grundlage einer Bestellung mit Lieferantenbindung generiert werden. Dies führt dazu, dass in Projektabrechnungen und in der Kostenkontrolle für Festpreisprojekte falsche Werte generiert werden. |
| Projektmanagement und -buchhaltung | [521374](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521374) | Das Projektverkaufsangebot aktualisiert den Stückpreis falsch, wenn der Header aktualisiert wird.                                                                                                                    |
| Projektmanagement und -buchhaltung | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Wenn Sie mit Retainern in Project Operations arbeiten, führt das Ändern des Standardprojekts im Vertrag nach Rechnungsstellung der Vorauszahlungen später zu Problemen mit eingehenden Abzügen.                                                                        |
| Projektmanagement und -buchhaltung | [521857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521857) | Die Aktualisierung des Rechnungsdatums für Lieferantenrechnungen und Projektverkaufspreise hat sich geändert.                                                                                                                                  |
| Projektmanagement und -buchhaltung | [522897](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520872) | Probleme treten auf, wenn Sie konzerninterne Transaktionen mit unterschiedlichen Wechselkursen anpassen.                                                                                                                |
| Projektmanagement und -buchhaltung | [522983](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522983) | Festgelegte Kosten mit einer Artikelanforderung und einer Bestellung sind im Bestellrechnungsprozess mit einem teilweisen Produktbeleg und einer teilweisen Rechnungsstellung nicht korrekt.                                                |
| Projektmanagement und -buchhaltung | [523960](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523960) | Falsche Werte treten auf, wenn eine Schätzung mit einem Wechselkurs umgekehrt wird.                                                                                                                                             |
| Projektmanagement und -buchhaltung | [524242](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524242) | Der Aufwand in Stunden wird auf Aufgabenebene automatisch in der Vorlage für die Projektstrukturplan gelöscht.                                                                                                                         |
| Projektmanagement und -buchhaltung | [524911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=524911) | Wenn Sie den Status eines Angebots auf **Verloren** aktualisieren, werden die Status aller von Ihnen gestarteten Anführungszeichen mit dem Status **Erstellt** oder **Gesendet** auch auf **Verloren** aktualisiert.                 |
| Projektmanagement und -buchhaltung | [525182](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525182) | Die Verkaufsrechnung ist auf dem Rechnungsvorschlag nicht sichtbar, wenn der Liefertermin in der Zukunft liegt.                                                                                                                  |
| Projektmanagement und -buchhaltung | [526180](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526180) | Es gibt eine Änderung in der Geschäftslogik für die **Projektartikel-Journalzeilen**-Entität.                                                                                                                                          |
| Projektmanagement und -buchhaltung | [526522](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526522) | Die aufgelaufenen Einnahmen auf einer konzerninternen Kundenrechnung stimmen nicht mit der Arbeitszeittabelle und der Neubewertung von Fremdwährungen überein.                                                                                 |
| Projektmanagement und -buchhaltung | [526650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526650) | Festgelegte Kosten werden falsch berechnet, nachdem die Liefererinnerung in der Projektbestellposition aus einer Projektbestellanforderung oder aus einem Projekt erstellt wurde.                    |
| Projektmanagement und -buchhaltung | [526812](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526812) | Wenn Sie ein Projekt anpassen, kann der folgende Fehler auftreten: „In der Inventareinheit werden keine Finanzdaten aktualisiert“.                                                                                                             |
| Projektmanagement und -buchhaltung | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Wenn Sie in Project Operations ein Projekt aus einem Vertrag entfernen, sollte das Standardprojekt des Vertrags bei Bedarf zurückgesetzt werden.                                                                                       |
| Projektmanagement und -buchhaltung | [527945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527945) | Der Verkaufspreis für einen Aufwand im Projekt ist falsch, wenn die Nutzungssteuer angewendet wird.                                                                                                                                         |
| Projektmanagement und -buchhaltung | [528020](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528020) | Die falsche Menge wird auf einer Projektartikelanforderung gebucht, wenn die Projektbestellposition mit zusätzlichen Rechnungen aktualisiert wird.                                                                                                 |
| Projektmanagement und -buchhaltung | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | In Project Operations werden die falschen Ausgabenzeilen in der **Zeile hinzufügen**-Liste auf der Intercompany-Rechnung angezeigt.                                                                                                |
| Projektmanagement und -buchhaltung | [529887](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529887) | Das **Kreditorenkonto**-Feld auf der **Projekt gebuchte Transaktion**-Seite ist leer, wenn Transaktionen über die Rechnungsregisterkarte und die Rechnungsgenehmigung gebucht werden.                                                                  |
| Projektmanagement und -buchhaltung | [530008](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530008) | Das ursprüngliche Projektdatum wird bei einer Anpassung nicht berücksichtigt, die einen Fehler verursacht, wenn **Anpassungsdatum als neues Projektdatum verwenden** auf **Nein** festgelegt ist.                                                                     |
| Projektmanagement und -buchhaltung | [530241](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530241) | Der projektbezogene Verkaufspreis im allgemeinen Journal und im Spesenjournal wird falsch berechnet, wenn die Transaktionswährung von der Unternehmenswährung abweicht.                                     |
| Projektmanagement und -buchhaltung | [530658](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530658) | Verkaufstransaktionen werden nicht auf Gutscheinen für die Teilrechnung einer Projektbestellung angezeigt.                                                                                                                          |
| Projektmanagement und -buchhaltung | [530883](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530883) | Die Rollen „Projektbuchhalter“ und „Projektmanager“ können keine Stundenjournale mit der Einrichtung der Genehmigungsgruppe erstellen.                                                                                                         |
| Projektmanagement und -buchhaltung | [531974](https://fix.lcs.dynamics.com/Issue/Details/?bugId=531974) | Es kann keine Spesenabrechnung gebucht werden, die mit Microsoft Excel importiert wurde.                                                                                                                                                              |
| Projektmanagement und -buchhaltung | [532106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532106) | Es kann keine Arbeitszeittabellenrichtlinie erstellt werden, da das **Nachricht**-Feld nicht aktiv ist.                                                                                                                               |
| Projektmanagement und -buchhaltung | [532548](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532548) | Es gibt ein Problem, bei dem die Stornierung von Lieferantentransaktionen in konzerninternen Szenarien zulässig ist. Dies gilt sowohl für Lieferantenrechnungen als auch für Spesenabrechnungen.                                                                                 |
| Projektmanagement und -buchhaltung | [532692](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532692) | Verteilungen auf einer genehmigten Arbeitszeittabelle können nicht zurückgesetzt werden.                                                                                                                                                     |
| Projektmanagement und -buchhaltung | [532843](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532843) | Bei der Stornierung einer Schätzung mit einem Wechselkurs für Stunden- und Artikeljournale treten falsche Werte auf.                                                                                                                  |
| Projektmanagement und -buchhaltung | [533426](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533426) | Die Projektanpassung aktualisiert den Verkaufsbetrag nicht korrekt mit indirekten Kosten.                                                                                                                              |
| Projektmanagement und -buchhaltung | [534597](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534597) | Wenn Sie das Stundenjournal buchen, wird die folgende Fehlermeldung angezeigt: „Der Dimensionswert ist nicht angegeben“.                                                                                                                                  |
| Projektmanagement und -buchhaltung | [535428](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535428) | Ein Projektvertrag mit einer anderen Währung berechnet die Buchungswährung auf dem Gutschein nicht korrekt.                                                                                              |
| Projektmanagement und -buchhaltung | [535652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535652) | Das falsche Verkaufs-WIP-Konto wird für die konzerninterne Arbeitszeittabellen-WIP-Buchung verwendet.                                                                                                                                     |
| Projektmanagement und -buchhaltung | [536536](https://fix.lcs.dynamics.com/Issue/Details/?bugId=536536) | Das Projektangebot berechnet die Preise falsch, wenn ein Rabatt angewendet und das Lager aktualisiert wird.                                                                                                       |
| Projektmanagement und -buchhaltung | [537905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537905) | Wenn Sie eine Neuberechnung ausführen, nachdem eine Artikelkostenanpassung in einer Projekttransaktion verwendet wurde, wird die folgende Fehlermeldung angezeigt: „Die Neuberechnung wird aufgrund eines Fehlers angehalten“.                                                               |
| Projektmanagement und -buchhaltung | [540622](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540622) | Es werden keine Hauptbucheinträge erstellt, wenn Transaktionen bei Rechnungsabgrenzung von „abrechnungsfähig“ auf „nicht abrechnungsfähig“ angepasst werden.                                                                                              |
| Projektmanagement und -buchhaltung | [540633](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540633) | Wenn die Funktion für die Aufbewahrung von Projektanbieterrechnungen **Aktivieren Sie die Kostenbetragsberechnung** aktiviert ist, wird **ProjTrans** nicht mit Pay-When-Paid erstellt.                                             |
| Projektmanagement und -buchhaltung | [541421](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541421) | Es gibt mehrere Probleme mit der **Rechnungsvorschlag erstellen**-Seite.                                                                                                                                                     |
| Projektmanagement und -buchhaltung | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | In Project Operations ist die **Kaufvertrag**-Seite in juristischen Personen des Finanzsektors, die in Project Operations integriert sind, nicht sichtbar.                                                                                             |
| Projektmanagement und -buchhaltung | [544132](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544132) | Erweiterte Journale können nicht mit einem Abrechnungsdatum in einem geschlossenen Zeitraum gebucht werden, selbst wenn die Option **Abrechnungsdatum automatisch auf die nächste offene Periode einstellen** aktiviert ist.                                                |
| Projektmanagement und -buchhaltung | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Aufgrund eines Dataverse-Integrationsfehlers können Sie ein Angebot nicht in Won in Project Operations konvertieren.                                                                                                                                       |
| Projektmanagement und -buchhaltung | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | In Project Operations tritt eine Fehlermeldung auf, wenn Sie versuchen, einer Projekt-ID eine Vertragszeile zuzuordnen, da überprüft wird, ob sich Vertragszeilen und Transaktionstypen überschneiden.                                                |
| Projektmanagement und -buchhaltung | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** kann die Rechnungsadresse der Finanzierungsquelle von einem anderen Kunden festlegen.                                                                                                             |
| Projektmanagement und -buchhaltung | [547606](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547606) | Die Standardsuche der Ressource auf Seiten ist nach dem 10.0.15-Update nicht verfügbar.                                                                                                                    |
| Projektmanagement und -buchhaltung | [547831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547831) | Das Sachkonto und die Buchungsart sind auf dem Hauptbuchbeleg falsch, und die Buchungsart ist auf dem Bestellbeleg für eine nicht auf Lager befindliche Serviceposition falsch, wenn die Projektgruppe auf **Saldo** gesetzt ist.                                 |
| Projektmanagement und -buchhaltung | [550030](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550030) | Die Aktivitätsnummer wird für eine ausstehende Lieferantenrechnung nicht angezeigt, obwohl **Auswahl der übergeordneten Aktivität blockieren** auf „Nein“ gesetzt ist.                                                                    |
| Projektmanagement und -buchhaltung | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | In Project Operations werden keine Dimensionen ausgewählt, wenn Sie eine Buchungsrechnung für eine Transaktion erstellen.                                                                                                                   |
| Projektmanagement und -buchhaltung | [442814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=442814) | Im Projektmanagement und in der Buchhaltung wird die Priorität des Transferpreises für konzerninterne Arbeitszeittabellen nicht genau wiedergegeben.                                                                            |
| Projektmanagement und -buchhaltung | [533530](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533530) | Die WBS-Klassenmethode (Legacy Work Breakdown Structure) **ProjWBSUpdateController::updateOutlineNumbersAndPublishInPreOrder** ist veraltet.                                                                                                   |

### <a name="regulatory-updates"></a>Aktualisierungen der Vorschriften
Informationen zu behördlichen Aktualisierungen für Finance and Operations-Apps, siehe [Aktualisierungen der Vorschriften](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Sie können sich auch bei LCS anmelden und die geplanten regulatorischen Aktualisierungen mit dem Problem-Suchwerkzeug anzeigen. Mit der Problemsuche können Sie nach Land, Art der Funktion und Version suchen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]