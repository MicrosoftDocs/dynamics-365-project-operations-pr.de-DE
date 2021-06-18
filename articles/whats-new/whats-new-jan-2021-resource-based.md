---
title: Neuigkeiten für Januar 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version von Project Operations vom Januar 2021 für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen verfügbar sind.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c600c30acd5e07e6370459928e33033a6ba418d6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995755"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten für Januar 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_


Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:

  - Project Operations in Dataverse, Umgebungsversion 4.6.0.154
  - Projektmanagement und Buchhaltung in Dynamics 365 Finance, Umgebungsversion 10.0.16

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| **Bereitstellung und Konfiguration** | 2106818 | Die Umbenennung der Webresource wurde behoben, die Probleme beim Anpassen einer Seite verursachte. |
| **Preise und Abrechnung** | 2091908 | Die Sichtbarkeit der Optionen **Preise sperren** und **Verwenden Sie die aktuelle Preisgestaltung** auf der Seite **Rechnung** wurde behoben, wenn Project Operations zusammen mit Dynamics 365 Field Service installiert wird. |
| **Preise und Abrechnung** | 2103058 | **Projektsummen** aktualisiert, um Nullwerte für die tatsächlichen Kosten einer Aufgabe zu behandeln. |
| **Preise und Abrechnung** | 2116100 | Verbesserte Fehlermeldungen für die Funktionalität **Korrigieren Sie die tatsächlichen Einträge**. |
| **Preise und Abrechnung** | 2116129 | Verbesserte Sichtbarkeit der Kostenschätzungen auf der Registerkarte **Schätzungen** auf der Seite **Projekte**. |
| **Preise und Abrechnung** | 2119112 | Feste Aggregation von tatsächlichen Verkäufen und tatsächlichen Kosten bei Verwendung unterschiedlicher Wechselkurse. |
| **Preise und Abrechnung** | 2134705 | Der Fehler Eigenschaft **getResourceString** von undefiniert kann nicht gelesen werden, wenn die Seite **Rechnung** geöffnet und Field Service installiert ist, wurde behoben. |
| **Verkaufschancenmanagement** | 2022195 | Das aufgabenbasierte Abrechnungsraster auf der Seite **Projekt** enthält ein Symbol, das angibt, dass mit dieser Aufgabe ein Vertrag oder eine Angebotszeile verknüpft ist. |
| **Verkaufschancenmanagement** | 2029135 | Der Geschäftsprozessfehler wurde behoben, der auftritt, wenn ein Benutzer versucht, eine Rechnungsposition auf einer bestätigten Rechnung mit einem in Rechnung gestellten Vorschussbetrag zu öffnen. |
| **Verkaufschancenmanagement** | 2040713 | Der Skriptfehler, der beim Erstellen einer Rechnung aus einem Vertrag und beim Installieren von Field Service auftritt, wurde behoben. |
| **Projektplanung und -nachverfolgung** | 2090202 | Markierte Geschäftsregeln, die nicht mehr als **Veraltet** verwendet werden. |
| **Zeit und Ausgaben** | 2091249 | Engere Steuerung, so dass Benutzer die Aufgabe für einen Zeiteintrag nicht ändern können, der genehmigt oder übermittelt wurde. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmanagement und -buchhaltung in Dynamics 365 Finance

| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| **Projektmanagement und -buchhaltung** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Falscher Vertragsbetrag auf der Seite **Auf Rechnung** für ein Festpreisprojekt mit mehreren Finanzierungsquellen. |
| **Projektmanagement und -buchhaltung** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Der Platzhalter **Invoiceproposal.PSAnfRefProjId** zeigt die Projekt-ID für den Workflow nicht an. **Überprüfen Sie die Vorschläge für die Projektrechnung**. |
| **Projektmanagement und -buchhaltung** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Bei der Buchung von Projektrechnungsvorschlägen wird das falsche Skontodatum verwendet. |
| **Projektmanagement und -buchhaltung** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Durch das Entfernen und Lesen der Ressourcenzuweisung werden die Projektprognoseeinträge in Project Operations verdoppelt. |
| **Projektmanagement und -buchhaltung** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | In Project Operations können Sie keine Projektschätzungen in Dataverse erstellen, ohne eine Vertragslinie über das Projekt haben. |
| **Projektmanagement und -buchhaltung** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Die finanzielle Dimension einer Projektaufwandsbuchung wird nicht mit dem zugehörigen Beleg und der buchhalterischen Verteilung der Spesenabrechnung synchronisiert, wenn die Kosten in den Saldo gebucht werden. |
| **Projektmanagement und -buchhaltung** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Der Filter für den **Rechnungsstatus** in gebuchten Projekttransaktionen für Festpreisprojekte funktioniert nicht. |
| **Projektmanagement und -buchhaltung** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Die Eliminierung der umgekehrten Schätzung funktioniert im Abschnitt **Periodisch**. |
| **Projektmanagement und -buchhaltung** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Rechnungsvorschlagszeilen können in Project Operations gelöscht werden, wenn mit Dataverse integriert. |
| **Projektmanagement und -buchhaltung** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Vermeiden der Aktivierung der Funktion für mehrere Vertragszeilen ohne Dataverse-Integration. |
| **Projektmanagement und -buchhaltung** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Wenn die Rechnungsstellung auf dem Konto dem Gewinn und Verlust entspricht, wird der in Rechnung gestellte Umsatz auf dem Konto als Null aufgeführt auf der Seite Schätzungen. |
| **Projektmanagement und -buchhaltung** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Rechnungskorrekturen funktionieren in integrierten Umgebungen nicht. |
| **Projektmanagement und -buchhaltung** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Beim Buchen von WIP – Die Buchung des Verkaufswerts in der Intercompany-Projektrechnung wählt ein falsches Konto aus. |
| **Projektmanagement und -buchhaltung** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | In Project Operations können Abhängigkeiten von Schätzaufgaben in Dataverse nicht aktualisiert werden. |
| **Projektmanagement und -buchhaltung** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Das wiederholte Löschen von Project Operations-Integrationsjournalen in Finance führt zu Datenverlust. |
| **Projektmanagement und -buchhaltung** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Der folgende Fehler tritt auf, wenn ein Projektrechnungsvorschlag gebucht wird: Die Transaktion wird nicht mit der Berichtswährung ausgeglichen, wenn die abgezogene Vorabrechnung hinzugefügt wird. |
| **Projektmanagement und -buchhaltung** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Die falsche Projekt-ID ist in den Abzügen enthalten, nachdem der Standardprojektvertrag in Project Operations aktualisiert wurde. |
| **Projektmanagement und -buchhaltung** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Die Schätzung und Umsatzrealisierung kann nicht abgeschlossen werden, wenn Project Operations aktiviert ist. |
| **Projektmanagement und -buchhaltung** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Wenn Sie in Project Operations ein Projekt aus einem Vertrag entfernen, wird das Standardprojekt im Vertrag nicht zurückgesetzt. |
| **Projektmanagement und -buchhaltung** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | In Project Operations werden auf einer Intercompany-Rechnung die falschen Ausgabenzeilen in der Liste **Zeile hinzufügen** angezeigt. |
| **Reisekosten und Ausgaben** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Ausgabenzeilen können nicht gebucht werden, da die Stundeneinstellung in der Vertragszeile fehlt. |
| **Reisekosten und Ausgaben** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Wenn die Projekt-/Kategorievalidierung obligatorisch ist, werden die mit dem Projekt verknüpften Ausgabenkategorien in der Ausgabenabrechnung nicht angezeigt. |
| **Reisekosten und Ausgaben** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Der Vorauszahlungssaldo wird nicht aktualisiert, wenn eine Ausgabenabrechnung zeilenweise gebucht wird. |
| **Reisekosten und Ausgaben** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Der Auftrag **Zahlungsinformationen aktualisieren** schlägt fehl, nachdem Abrechnungen storniert wurden, bei denen eine Rechnung mit zwei oder mehr Zahlungsvorgängen beglichen wurde. |
| **Reisekosten und Ausgaben** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Es besteht ein Problem mit der Berechnung der Reduzierung der Mahlzeiten am letzten Tag für die Tagessatzkategorie. |
| **Reisekosten und Ausgaben** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Der Bericht **Aufwandsart pro Mitarbeiter** zeigt keine Einzelkosten an, wenn die erste Verbindung eines Benutzers in der Sprache es-MX bestand. |
| **Reisekosten und Ausgaben** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Die Lieferantenzahlung für einen Ausgabenabrechnungsbericht verwendet das falsche Zusammenfassungskonto für die Abrechnungsbuchung. |
| **Reisekosten und Ausgaben** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Wenn ein Ausgabenbericht mit **Gruppierung von Transaktionen basierend auf dem Gegenzahlungskonto zulassen** und **Abrechnungsdatum bei Buchung korrigieren** gebucht wird, werden die Buchungsdaten nicht in der Tabelle **Buchhaltungsverteilung** gruppiert, die sich auf die Umsatzsteueraufzeichnungen auswirken. |
| **Reisekosten und Ausgaben** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Die Zuordnung der Ausgabenunterkategorien wird entfernt, wenn das Kontrollkästchen Ausgaben verwenden deaktiviert und dann erneut aktiviert wird. |
| **Reisekosten und Ausgaben** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Ein konzerninterner Ausgabenbericht kann nicht erstellt werden, wenn die Projekt-ID auf Kopfzeilenebene hinzugefügt wird. |
| **Reisekosten und Ausgaben** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Es besteht ein Problem mit Ausgabenzahlungen, wenn der Ausgabenbetrag höher ist als der Vorauszahlungsbetrag. |
| **Reisekosten und Ausgaben** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Das Feld **Projekt-ID** auf einem konzerninternen Ausgabenbericht ist leer, wenn die Benutzerrolle einer bestimmten Organisation zugewiesen ist. |
| **Reisekosten und Ausgaben** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Die Ausgabenkategorie wird beim Hinzufügen einer neuen Ausgabenzeile gesperrt. |
| **Reisekosten und Ausgaben** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Die Aufteilung der bereits geteilten Ausgabenabrechnungszeilen führt zu einem unvollständigen gebuchten Kreditorenbuchhaltungsbeleg \ Hauptbuchbeleg. Wegen der Vervielfältigung von **TRVEXPTRANS.SOURCEDOCUMENTLINE** ist der Buchhaltungsquellexplorer ebenfalls fehlerhaft. |
| **Reisekosten und Ausgaben** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Der Index, der auf der Tabelle **TRVREQUISITIONLINE** hinzugefügt wird, für die der Kunde Duplikate hat, führt beim Upgrade zu einem Fehler. |
| **Reisekosten und Ausgaben** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | In Project Operations kann die Zeit mit konzerninternen Aufgaben in Dataverse nicht erstellt oder genehmigt werden. |

## <a name="regulatory-updates"></a>Aktualisierungen der Vorschriften

Informationen zu behördlichen Aktualisierungen für Finance and Operations-Apps, siehe [Aktualisierungen der Vorschriften](/dynamics365/finance/localizations/regulatory-updates). Sie können sich auch bei LCS anmelden und die geplanten regulatorischen Aktualisierungen mit dem Problem-Suchwerkzeug anzeigen. Mit der Problemsuche können Sie nach Land, Art der Funktion und Version suchen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]