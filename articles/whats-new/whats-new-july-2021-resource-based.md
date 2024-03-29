---
title: Was ist neu Juli 2021 - Project Operations für ressourcen-/nicht vorrätig-basierte Szenarien
description: Dieser Artikel informiert über die Qualitätsupdates, die in der Version von Project Operations vom Juli 2021 für ressourcenbasierte/nicht vorrätige Szenarien zur Verfügung stehen.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c004a6adc265f8f02fc557700d9b88a174c221c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931697"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Was ist neu Juli 2021 - Project Operations für ressourcen-/nicht vorrätig-basierte Szenarien

*Gilt für: Project Operations für ressourcen-/nicht vorratsbasierte Szenarien*

Dieser Artikel bezieht sich auf die folgenden Dynamics 365 Project Operations-Komponenten und Versionen:

   - Project Operations in Microsoft Dataverse-Umgebung Version 4.12.0.148 oder 4.12.0.152.
   - Projektmanagement und -buchhaltung in Dynamics 365 Finance-Umgebungsversion 10.0.20.

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

Die folgenden Funktionen sind in dieser Version enthalten:

- Möglichkeit für Administratoren, die PSS-Protokolle und die Protokolle der festgelegten Vorgänge über das Einstellungsmenü einzusehen. Die Protokolle werden 90 Tage lang gespeichert.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Es gibt keine Updates für Project Operations Dual-Write Zuordnungen in dieser Version.

Eine aktuelle Liste und Versionen von Project Operations dual-write Zuordnungen finden Sie unter [Versionen von Project Operations dual-write Zuordnungen](../environment/resource-dual-write-maps.md).

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Bestimmte Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Die aktive Version der Zuordnung können Sie auf der Seite **Dual-write** in der Spalte **Version** sehen. Aktivieren Sie eine neue Version der Zuordnung, indem Sie **Kartenversionen zuordnen** wählen, die neueste Version auswählen und dann die ausgewählte Version speichern. Wenn Sie eine sofort einsatzbereite Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn ein Problem beim Starten der Zuordnung auftritt, befolgen Sie die Anweisungen im Abschnitt [Fehlende Tabellenspalten bei Zuordnungen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) in der Anleitung zur Fehlerbehebung für Dual-Write.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Funktionsbereich**              | **Referenznummer** | **Qualitätsupdate**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Preise und Abrechnung           | 2224046              | Das Feld **Transaktionsklasse** kann auf der Registerkarte **Angebotszeile Details** bearbeitet werden, ist aber gesperrt, wenn Sie auf der Seite **Angebotszeile Details** arbeiten.                                                                     |
| Preise und Abrechnung           | 2224400              | Die Aktion **Angebot als gewonnen schließen** schlägt fehl, wenn ein Angebot keine Datums-Meilensteine hat.                                                                                                                                    |
| Preise und Abrechnung           | 2234089              | Wenn Sie eine Produktbeschreibung manuell eingeben, wird sie gelöscht, nachdem Sie eine Menge für eine Materialschätzung eingegeben haben.                                                                                                                         |
| Preise und Abrechnung           | 2234100              | Das Raster **Auftragsabrechnung einrichten** enthält nicht die Spalte **Material** und ihren Wert auf der Registerkarte **Auftragsabrechnung** des Projekts.                                                                                                       |
| Preise und Abrechnung           | 2277409              | Die Produkt-ID ist in den Details der Vertragszeile für eine Materialartzeile nicht verfügbar.                                                                                                                                        |
| Preise und Abrechnung           | 2281728              | Das Erstellen einer Vertragszeile führt unnötigerweise zu einer Neubewertung der Istwerte und damit zu einem erheblichen Anstieg des Datenvolumens, was die Leistung beeinträchtigt.                                                                                |
| Preise und Abrechnung           | 2298668              | Erfassungszeilen, die mit einer zurückgerufenen und gelöschten Ausgabe verbunden sind, werden nicht entfernt.                                                                                                                                     |
| Preise und Abrechnung           | 2300192              | Wenn mehrere Benutzer eine Rechnung bearbeiten, ist es möglich, dass ein neues Rechnungszeilendetail auf einer bestätigten Rechnung erstellt wird.                                                                                   |
| Preise und Abrechnung           | 2301569              | Rechnungen können nicht korrigiert werden, wenn ein Betragseinbehalt von \$0 angewendet wurde.                                                                                                                                        |
| Preise und Abrechnung           | 2307965              | Es tritt ein Fehler auf, wenn ein Kategoriepreis mit fehlenden Werten erstellt wird.                                                                                                                           |
| Preise und Abrechnung           | 2326870              | Es tritt ein Fehler in **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** auf, wenn **Producttypecode** null ist.                                                                            |
| Preise und Abrechnung           | 2332732              | Ein Fehler tritt auf, wenn ein Meilenstein für eine Vertragszeile ohne eine Auftragszeile erstellt wird.                                                                                                                |
| Projektplanung und -nachverfolgung | 2181094              | Die Projektplanungs-API unterstützt jetzt PSS-Protokolle und Vorgangs-Set-Protokolle, die für 90 Tage gespeichert werden.                                                                                                                  |
| Projektplanung und -nachverfolgung | 2254201              | Das Label **Geplanter Modus** wurde mit Details aktualisiert, die die Vorgabe-Logik beschreiben.                                                                                                                                      |
| Projektplanung und -nachverfolgung | 2300252              | Der **openProject** Antwort-Cache wird aktualisiert und enthält den Token-Besitzer im Cache-Schlüssel, **Basis-Url** und **Segment-Url**, sodass **Request-Url** immer neu erstellt werden kann, wenn sich die **Basis-Url** ändert. |
| Projektplanung und -nachverfolgung | 2301312              | **msdyn_membershipstatus** wurde aus der Ansicht **Projektteam-Mitglied** entfernt.                                                                                                                                        |
| Projektplanung und -nachverfolgung | 2302759              | Auf den Registerkarten **Ressourcenzuweisungen**, **Schätzungen** und **Aufwandsschätzungen** werden unnötigerweise Produkte geholt.                                                                                                        |
| Projektplanung und -nachverfolgung | 2308050              | **CopyProject** schlägt mit der Fehlermeldung „Fehler beim Abrufen von Token für die Kommunikation mit dem Remotedienst“ fehl.                                                                                                                           |
| Projektplanung und -nachverfolgung | 2322650              | Die Ansicht **Projektaufgabenliste** wurde aktualisiert und zeigt jetzt standardmäßig das Datum der Aufgabe an.                                                                                                            |
| Projektplanung und -nachverfolgung | 2327266              | **CopyProject** erzeugt beim Kopieren von Schätzungen den Fehler „Schlüssel nicht im Wörterbuch gefunden“.                                                                                                      |
| Projektplanung und -nachverfolgung | 2328123              | **CopyProject** erzeugt den Fehler, „Fehler beim Abrufen von Token für die Kommunikation mit dem Remotedienst“.                                                                                                                          |
| Projektplanung und -nachverfolgung | 2336258              | **CopyProject** kopiert fälschlicherweise die Positionsnamen von Ressourcen.                                                                                                                                                 |
| Preise und Abrechnung           | 2224476              | Das Feld **Buchbare Ressource** zeigt auf der Seite **Materialverwendung** nicht korrekt den angemeldeten Benutzer an.                                                                                                            |
| Ressourcenverwaltung           | 2277249              | Es tritt ein Fehler auf, wenn eine nicht projektbasierte Ressourcenanforderung aktualisiert wird.                                                                                                            |
| Ressourcenverwaltung           | 2323869              | Die Ressourcenauslastung erkennt gefilterte Ressourcen nicht korrekt.                                                                                                                                             |
| Zeit und Ausgaben              | 2176538              | Auf das Steuerelement **Zeiteintrag** werden falsche Filtervorgänge angewendet.                                                                                                                                                   |
| Zeit und Ausgaben              | 2177462              | Das Löschen eines Zeiteintrags im Raster aktualisiert den Status der Schaltflächen **Senden**, **Aufrufen**, **Löschen** und **Eintrag bearbeiten** nicht wie erwartet.                                                                                        |
| Zeit und Ausgaben              | 2299985              | **TimeEntriesImportFromResourceAssignment** erhält nicht die Start-/Endzeit aus den Zuweisungskonturen.                                                                                                  |
| Zeit und Ausgaben              | 2318426              | Nachdem ein Zeiteintrag gesendet wurde, können gesperrte Felder noch bearbeitet werden.                                                                                                                                   |
| Zeit und Ausgaben              | 2323749              | Ein Fehler tritt auf, wenn eine Leistung aus dem **Bezogen**-Register einer buchbaren Ressource erstellt wird.                                                                                                      |
| Zeit und Ausgaben              | 2327678              | Wenn Sie einen Zeiteintrag von der Registerkarte **Bezogen** einer buchbaren Ressource erstellen, wird die übergeordnete Ressource nicht an das Steuerelement für den Zeiteintrag übergeben.                                                                            |
| Allgemein                       | 2296857              | Fortschrittsverfolgung für lang ausgeführte Jobs.                                                                                                                                                                        |
| Allgemein                       | 2253682              | Die Project Operations Dual-Write-Lösung sollte nicht installiert werden, wenn Dual-Write Core in einer Umgebung ohne die Dual-Write-Orchestrierungslösung installiert ist.                                                |
| Allgemein                       | 2316420              | Die Bereitstellung von Project Service Core schlägt fehl, wenn die Einheit des Anwendungsbenutzers geändert wird.                                                                                                                     |
| Allgemein                       | 2376405              | Problem mit vom Herausgeber gesteuerten Updates behoben (Qualitätsupdate ist in Version 4.12.0.152 verfügbar)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmanagement und -buchhaltung bei Dynamics 365 Finance

| Funktionsbereich                      | Referenznummer | Qualitätsupdate                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektmanagement und -buchhaltung | 4620267          | Formulare können nicht personalisiert werden, um ein **Zweck**-Feld auf den Seiten **Projekt gebuchte Transaktion**, **Rechnungsvorschlagserstellung** und **Rechnungsvorschlag** hinzuzufügen.                                                                                                                                                                                         |
| Projektmanagement und -buchhaltung | 4613449          | Wenn Sie in Finance eine Projektvertrags-ID auswählen, öffnet die integrierte Umgebung von Project Operations die Seite zum Erstellen eines neuen Datensatzes, statt der Seite für bereits erstellte Projektverträge.                                                                                                                                           |
| Projektmanagement und -buchhaltung | 4614445          | Beim Bereitstellen des integrierten Szenarios Project Operations können Sie das Feld **Element Mehrwertsteuergruppe** auf dem Rechnungsvorschlag, der aus Staging importiert wird, nicht bearbeiten. Die Mehrwertsteuergruppe sollte für einen offenen Rechnungsvorschlag für alle Transaktionstypen, einschließlich Transaktion auf Rechnung, Stunden, Spesen, Gebühren und Artikel, bearbeitbar sein. |
| Projektmanagement und -buchhaltung |                  | Ein Rechnungsvorschlag, der aus einer Korrektur einer negativen Zeittransaktion resultiert, kann nicht gepostet werden.                                                                                                                                                                                                                                              |
| Projektmanagement und -buchhaltung |                  | Zeilen des Rechnungsvorschlags werden dupliziert, weil mehrere **Import aus Staging** periodische Prozesse gleichzeitig ausgeführt werden.                                                                                                                                                                                                                |

