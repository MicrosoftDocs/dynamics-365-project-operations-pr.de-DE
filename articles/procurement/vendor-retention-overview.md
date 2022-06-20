---
title: Übersicht zur Lieferantenbindung
description: Dieser Artikel gibt Ihnen einen Überblick über die Funktionalitäten der Anbieterbindung.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 680786f239125905f3b8746cb8318732aa74d9e0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916839"
---
# <a name="vendor-retention-overview"></a>Übersicht zur Lieferantenbindung

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Ihre Organisation möchte möglicherweise einen Teil der Zahlungen an Lieferanten einbehalten, die an Projekten für Ihre Organisation arbeiten. Bevor Sie beispielsweise Ihren Lieferanten bezahlen, möchten Sie möglicherweise sicherstellen, dass die von ihm bereitgestellten Artikel und Dienstleistungen Ihren Erwartungen entsprechen.

Wenn Sie Einkäufe für Projekte mit Kreditoren aushandeln, können Sie die Bedingungen für die Kreditorenbindung angeben, die den einzubehaltenden Prozentsatz oder Betrag enthalten. Wenn der Lieferant Artikel und Dienstleistungen liefert, ziehen Sie den angegebenen Einbehaltungsprozentsatz oder -betrag von Ihrer Zahlung an den Lieferanten ab. Wenn das Projekt abgeschlossen ist oder eine im Lieferantenvertrag festgelegte Zwischenstufe erreicht ist, geben Sie den einbehaltenen Betrag frei und erstellen eine Zahlung an den Lieferanten.

## <a name="vendor-retention-example"></a>Beispiel zur Lieferantenbindung

Das folgende Beispiel zeigt, wie ein Prozentsatz eines Kreditorenrechnungsbetrags basierend auf dem für ein Projekt abgeschlossenen Prozentsatz einbehalten wird.

Contoso Robotics USA hat mit dem Anbieter Fabrikam einen Vertrag über die Bereitstellung von 100 Schulungsstunden für das Projekt zur Ausrüstungserneuerung abgeschlossen. Der Gesamtauftragswert beträgt USD 30.000 mit einem vereinbarten Kaufpreis von USD 300 pro Stunde.

Die Ausbildung erfolgt in drei Phasen mit folgendem Zeitplan:

- Phase 1: 50 Stunden oder 50 Prozent des Projekts
- Phase 2: 30 Stunden oder 80 Prozent des Projekts im Ganzen
- Phase 3: 20 Stunden oder 100 Prozent des Projekts

In der folgenden Tabelle sind die Aufbewahrungsbedingungen aufgeführt.

| **Prozentsatz der gelieferten Einheiten** | **Zu behaltender Prozentsatz** | **Freizugebender Prozentsatz** |
| --- | --- | --- |
| 50 % | 20 % | 0 % |
| 80 % | 10 % | 10 % |
| 100% | 0 % | 100% |

Aus den Transaktionen ergeben sich folgende Beträge:

- Phase 1:
  - Der zu zahlende Betrag beträgt 50 x 300 oder 15.000.
  - 20 Prozent des Betrags oder 3.000 werden einbehalten und zu einem späteren Zeitpunkt freigegeben.
  - Der an den Kreditor gezahlte Betrag liegt jedoch bei 12.000.
- Phase 2:
  - Der zu zahlende Betrag beträgt 30 x 300 oder 9.000.
  - 10 Prozent des Betrags oder 900 werden einbehalten.
  - 10 Prozent der 3.000, die in Phase 1 zurückbehalten wurden, oder 300, werden freigegeben.
  - Der an den Kreditor gezahlte Betrag liegt jedoch bei 8.400. Dieser Betrag beträgt 9.000 abzüglich der 900er Einbehalte zuzüglich der 300, die aus der Phase-1-Einbehaltung freigegeben wurden.
- Phase 3:
  - Der zu zahlende Betrag beträgt 20 x 300 oder 6.000.
  - Es wird kein Betrag einbehalten.
  - Der freigegebene Betrag beträgt 3.600. Dieser Betrag setzt sich zusammen aus den 3.000, die in Phase 1 zurückbehalten wurden, abzüglich der 300 aus Phase 1, die in Phase 2 freigegeben wurden, plus den 900, die in Phase 2 zurückbehalten wurden.
  - Der an den Kreditor gezahlte Betrag liegt jedoch bei 9.600. Dieser Betrag setzt sich zusammen aus dem einbehaltenen Betrag von 3.600 plus den 6.000 für den Abschluss von Phase 3.

Der an den Lieferanten nach Abschluss der drei Phasen gezahlte Gesamtbetrag beträgt 30.000, was dem Gesamtbetrag der Bestellung (15.000 + 9.000 + 6.000) entspricht.
