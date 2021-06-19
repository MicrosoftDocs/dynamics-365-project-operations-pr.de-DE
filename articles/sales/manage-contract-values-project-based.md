---
title: Mit projektbasierten Vertragszeilen arbeiten
description: Dieses Thema enthält Informationen zu projektbasierten Vertragszeilen.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2072692296308a08756ec3e0f381c792745dd3e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011505"
---
# <a name="work-with-projectbased-contract-lines"></a>Mit projektbasierten Vertragszeilen arbeiten

Projektbasierte Vertragszeilen in Dynamics 365 Project Operations dienen dazu, die Kostenvoranschlags- und Abrechnungsvereinbarungen für bestimmte Komponenten der Projektarbeit an einem Auftrag zu speichern. Die Struktur einer projektbasierten Vertragszeile wird für Projektschätzungen und Abrechnungsszenarien um folgende Konzepte erweitert:

- Abrechnungsmethode
- Projekt‑ und Aufgabenzuordnung
- Eingeschlossene Transaktionsklassen
- Nicht zu überschreitender Grenzwert
- Fakturierbarkeitseinrichtung
- Schätzungen unter Verwendung von Vertragszeilendetails
- Vertragszeilenkunden

Die folgenden Felder sind in der **Allgemein**-Registerkarte der projektbasierten Vertragszeilen enthalten. Diese Felder helfen dabei, die Grundlage für eine detaillierte, grundlegende Schätzung und die Abrechnungsmodalitäten für projektbasierte Arbeiten zu schaffen.

| Feld | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- |
| **Name** | Der Name der Vertragszeile, die die diskrete Komponente des Vertrags identifiziert, der geschätzt wird. Bei einem aus einem Angebot erstellten Projektvertrag wird dieser Wert aus einem entsprechenden Wert der projektbasierten Angebotszeile kopiert. | Der Feldwert wird die Projektrechnungszeile kopiert, die aus dieser Vertragszeile erstellt wird, wenn die Rechnung erstellt wird. |
| **Fakturierungsmethode** | Bei einem aus einem Angebot erstellten Projektvertrag wird dieser Wert aus einem entsprechenden Feld der Angebotszeile kopiert. Dies ist ein Optionssatz, der die beiden wichtigsten Vertragsmodelle darstellt, die von Project Operations unterstützt werden:</br>- **Festpreis**</br>- **Zeit und Materialien** | Basierend auf der Abrechnungsmethode der referenzierten Vertragszeile wird die eigentliche Transaktion verarbeitet. Wenn die Vertragszeile, auf die sich der Istwert bezieht, über eine Zeit- und Materialabrechnungsmethode verfügt, werden Kosten- und nicht abgerechnete Umsatzdatensätze erstellt. Wenn die Vertragszeile, auf die der Istwert verweist, eine Abrechnungsmethode zum Festpreis hat, wird nur ein Istpreis erstellt. |
| **Project** | Verwenden Sie dieses Feld, um das Projekt zu identifizieren, mit dem die Arbeit an diesem Auftrag ausgeführt wird. | Der Wert in diesem Feld wird in Verbindung mit den Feldern **Eingeschlossene Aufgaben** und **Eingeschlossene Transaktionsklassen** verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder einem geschätzten Zeilendatensatz aufzulösen. |
| **Zeit einschließen** | Ein Flag zeigt an, ob Zeittransaktionen oder Arbeitskosten für das ausgewählte Projekt in dieser Vertragszeile enthalten sind. Ein **Nein**-Wert zeigt an, dass die Zeittransaktionen oder Arbeitskosten in dieser Vertragszeile enthalten sind. Ein **Ja**-Wert gibt an, dass sie enthalten sind | Dieser Feldwert wird in Verbindung mit Projekt verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder einem geschätzten Zeilendatensatz aufzulösen. |
| **Ausgaben einschließen** | Ein Flag zeigt an, ob Ausgabenkosten für das ausgewählte Projekt in dieser Vertragszeile enthalten sind. Ein **Nein**-Wert zeigt an, dass die Ausgabenkosten in dieser Vertragszeile nicht enthalten sind. Ein **Ja**-Wert gibt an, dass sie enthalten sind | Dieser Feldwert wird in Verbindung mit dem Projekt verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder einem geschätzten Zeilendatensatz aufzulösen. |
| **Gebühr einschließen** | Ein Flag zeigt an, ob Gebühren für das ausgewählte Projekt in dieser Vertragszeile enthalten sind. Ein **Nein**-Wert zeigt an, dass Gebühren in dieser Vertragszeile nicht enthalten sind. Ein **Ja**-Wert gibt an, dass sie enthalten sind | Dieser Feldwert wird in Verbindung mit dem Projekt verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder einem geschätzten Zeilendatensatz aufzulösen. |
| **Vertraglicher Betrag** | Bei einer Festpreisvertragszeile ist dies der vereinbarte Wert, der dem Kunden für alle mit dieser Vertragszeile verbundenen Arbeitskomponenten in Rechnung gestellt wird. Bei einer Zeit- und Materialtransaktionenvertragszeile ist dieser Betrag ein geschätzter Wert, der dem Kunden für alle mit dieser Vertragszeile verbundenen Arbeitskomponenten in Rechnung gestellt wird. Bei einem aus einem Angebot erstellten Projektvertrag wird dieser Wert aus einem entsprechenden Feld der Angebotszeile kopiert. Wenn eine projektbasierte Vertragszeile Zeilendetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Betrag in den Vertragszeilendetails zusammengefasst. | Wenn die Vertragszeile Zeilendetails enthält, kann dieser Wert durch Ändern der Beträge in den Zeilendetails geändert werden. In einer Festpreisvertragszeile wird dieser Wert verwendet, um den Betrag vor Steuern für periodische Abrechnungsmeilensteine zu generieren. |
| **Geschätzte Steuer** | Der Benutzer kann dieses Feld bearbeiten, um den geschätzten Steuerbetrag in die Vertragszeile einzugeben. Wenn eine projektbasierte Vertragszeile Zeilendetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Steuerbetrag in den Vertragszeilendetails zusammengefasst. | Wenn die Vertragszeile Zeilendetails enthält, kann dieser Wert durch Ändern der Steuerbeträge in den Zeilendetails geändert werden. In einer Festpreisvertragszeile wird dieser Wert verwendet, um die Steuern für periodische Abrechnungsmeilensteine zu generieren. |
| **Vertraglicher Nettobetrag** | Der vertragliche Nettobetrag. Dieses Feld ist schreibgeschützt und wird berechnet als **Vertraglicher Betrag + Steuer**. | In einer Festpreisvertragszeile wird dieser Wert verwendet, um die periodische Abrechnungsmeilensteine zu generieren. |
| **Nicht zu überschreitender Grenzwert** | Der Benutzer kann dieses Feld bearbeiten und es ist nur in projektbasierten Vertragszeilen verfügbar, für die die Abrechnungsmethode als Zeit und Material festgelegt ist. | Der Benutzer kann dieses Feld bearbeiten. Wenn ein Istwert für Zeit oder Ausgaben auf diese Vertragszeile für Zeit und Material verweist, wird der Betrag auf dem Istwert anhand der nicht zu überschreitenden Grenze in der Vertragszeile bewertet, nachdem die bereits ausgegebenen und übermittelten Beträge verbucht wurden. |
| **Kundenbudget** | Dieses Feld kann bearbeitet werden und wird aus dem entsprechenden Feld der Angebotszeile kopiert, wenn der Vertrag aus einem Angebot erstellt wurde. | Dieses Feld wird nur zur Information verwendet und hat keine nachgelagerte Bedeutung. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Validierungsregel für die Optionen auf der Registerkarte „Allgemein“ der projektbasierten Vertragszeilen

Regel: Ein Projekt und eine bestimmte Transaktionsklasse können nur in einer projektbasierten Vertragszeile in einem Vertrag enthalten sein.

| Vertrag | Vertragszeile | Project | Zeit einbeziehen | Ausgabe einbeziehen | Gebühr einschließen | Gültig/Nicht gültig | Ursache                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Ja          | Ja             | Ja         | Nicht gültig       | Verstößt gegen die Regel. Zeit, Kosten und Gebühren für Projekt P1 sind in beiden Vertragszeilen CL1 und CL2 enthalten.                                                                                       |
| C1       | CL2           | P1      | Ja          | Ja             | Ja         | Nicht gültig       | Verstößt gegen die Regel. Zeit, Kosten und Gebühren für Projekt P1 sind in beiden Vertragszeilen CL1 und CL2 enthalten.                                                                                       |
| C1       | CL1           | P1      | Ja          | Nr.              | Ja         | Nicht gültig       | Verstößt gegen die Regel. Zeit und Gebühren für Projekt P1 sind in beiden Vertragszeilen CL1 und CL2 enthalten.                                                                                                   |
| C1       | CL2           | P1      | Ja          | Ja             | Ja         | Nicht gültig       | Verstößt gegen die Regel. Zeit und Gebühren für Projekt P1 sind in beiden Vertragszeilen CL1 und CL2 enthalten.                                                                                                   |
| C1       | CL1           | P1      | Ja          | Nr.              | Ja         | Gültig           | Zeit und Gebühren für Projekt P1 sind im CL1 enthalten. Die Kosten für das P1-Projekt sind in CL2 enthalten. </br>   Es gibt keine Überschneidungen in dem, was in jeder Vertragszeile enthalten ist, und ist daher gültig.  |
| C1       | CL2           | P1      | Nr.           | Ja             | Nr.          | Gültig           | Zeit und Gebühren für Projekt P1 sind im CL1 enthalten. Die Kosten für das P1-Projekt sind in CL2 enthalten. </br>   Es gibt keine Überschneidungen in dem, was in jeder Vertragszeile enthalten ist, und ist daher gültig.  |
| C1       | CL1           | P1      | Ja          | Ja             | Ja         | Nicht gültig       | Verstößt gegen die Regel. Zeit, Kosten und Gebühren für Projekt P1 sind in den Zeilen von zwei Verträgen enthalten.                                                                                               |
| CL2      | CL2           | P1      | Ja          | Ja             | Ja         | Nicht gültig       | Verstößt gegen die Regel. Zeit, Kosten und Gebühren für Projekt P1 sind in den Zeilen von zwei Verträgen enthalten.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]