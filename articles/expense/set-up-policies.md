---
title: Kostenrichtlinien definieren
description: Sie können Ausgabenrichtlinien definieren, die Ihre Mitarbeiter beim Eingeben und Senden von Ausgabeabrechnungen und Reiseanforderungen befolgen müssen.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8ae6de664fc18a00fd6d3d6c8177daa95da5754d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576913"
---
# <a name="define-expense-policies"></a>Kostenrichtlinien definieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Sie können Ausgabenrichtlinien definieren, denen Ihre Mitarbeiter beim Eingeben und Senden von Ausgabeabrechnungen und Reiseanforderungen folgen müssen.         
Durch die Implementierung von Spesenrichtlinien können Sie Spesen effektiv verwalten.         

Sie können beispielsweise eine Richtlinie für Hotelkosten in New York City festlegen, die besagt, dass die Spesen pro Nacht 250 USD nicht überschreiten dürfen.       
Wenn ein Mitarbeiter eine Ausgabenabrechnung oder eine Reiseanforderung einreicht, bei der der Zimmerpreis diesen Betrag überschreitet, benachrichtigt das System den         
Arbeitnehmer, dass der Richtlinienbetrag für die Ausgabe überschritten wurde. Sie können die Nachricht konfigurieren, die der Worker erhält        
definieren der Richtlinie.      
        
Sie können drei Arten von Richtlinien definieren:         
        
- **Warnung**: Ermöglicht dem Mitarbeiter, eine Ausgabenabrechnung oder Reiseanforderung einzureichen, die Ausgaben werden jedoch für alle Genehmigenden markiert und         
  für die spätere Berichterstattung.        

- **Fehler**: Fordert den Arbeitnehmer auf, die Ausgaben zu überarbeiten, um die Richtlinien einzuhalten, bevor er die Spesenabrechnung oder die Reiseanforderung einreicht.        
 
 - **Rechtfertigung**: Fordert den Arbeitnehmer oder einen Manager auf, vor dem Einreichen der Ausgabenabrechnung oder der Reiseanforderung eine Begründung für die Überschreitung des Richtlinienbetrags einzugeben.        

## <a name="policy-tips"></a>Richtlinientipps
Im Folgenden finden Sie einige Vorschläge, die Sie beim Erstellen neuer Richtlinien für die Spesenverwaltung unterstützen können: 

- Für Richtlinien gilt das Datum des Inkrafttretens. Dies bedeutet, dass eine Richtlinie nicht wirksam wird, wenn sie mit einem Datum nach dem Datum erstellt wird, an dem die Spesen entstanden sind. Beispielsweise erstellen Sie heute eine neue Richtlinie, um maximale Essenskosten von 50 USD durchzusetzen. Bestehende Spesen, die ab gestern eingegeben wurden, werden nicht mit dieser Richtlinie verglichen.
- Wenn Sie eine Richtlinie für eine Spesenkategorie erstellen, die aufgelistet werden kann, sollten Sie eine Bedingung für den Spesenzeilentyp hinzufügen. Einige Richtlinien, z. B. das Erfordernis eines Beleges, sind für einzelne Zeilen möglicherweise nicht sinnvoll. In dieser Situation wird die Richtlinie nur auf die Kopfzeile oder eine nicht aufgeschlüsselte Zeile angewendet. 
- Spesenverwaltungsrichtlinien werden standardmäßig anhand der Quellenentität ausgewertet. Für konzerninterne Szenarien können Sie stattdessen festlegen, dass die Richtlinie für die Zielentität (Kreditinstanz) ausgewertet wird. Aktivieren Sie die Funktion **Bewerten Sie die Ausgabenpolitik gegen die Aufnahme einer juristischen Person** im Arbeitsbereich **Funktionsverwaltung**, um die Richtlinien für die Zielentität auszuführen.

## <a name="when-to-evaluate-policies"></a>Wann müssen die Richtlinien bewertet werden

In den Ausgabenmanagementparametern können Sie auswählen, ob die Ausgabenmanagementrichtlinien ausgewertet werden sollen, wenn eine Zeile gespeichert wird oder wenn eine Ausgabenabrechnung gesendet wird. Wenn Sie auswerten möchten, wann eine Zeile gespeichert wird, haben Benutzer früher einen Überblick darüber, was sie tun müssen, um ihre Ausgabenabrechnung auf einmal zu vervollständigen. Andernfalls können Sie die Richtlinienbewertung verzögern und Zeit sparen, indem Sie am Ende während der Übermittlung an den Workflow validieren.


[!INCLUDE[footer-include](../includes/footer-banner.md)]