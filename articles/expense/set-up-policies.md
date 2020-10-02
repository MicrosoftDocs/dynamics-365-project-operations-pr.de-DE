---
title: Kostenrichtlinien definieren
description: Sie können Ausgabenrichtlinien definieren, die Ihre Mitarbeiter beim Eingeben und Senden von Ausgabeabrechnungen und Reiseanforderungen befolgen müssen.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fbab7fd94fa429876216ee82b716da8d847fb01a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896640"
---
# <a name="define-expense-policies"></a>Kostenrichtlinien definieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Sie können Ausgabenrichtlinien definieren, denen Ihre Mitarbeiter beim Eingeben und Senden von Ausgabeabrechnungen und Reiseanforderungen folgen müssen.         
Durch die Implementierung von Ausgabenrichtlinien können Sie Ausgaben effektiv verwalten.         

Sie können beispielsweise eine Richtlinie für Hotelkosten in New York City festlegen, die besagt, dass die Kosten pro Nacht USD 250 nicht überschreiten dürfen.       
Wenn ein Mitarbeiter eine Ausgabenabrechnung oder eine Reiseanforderung einreicht, bei der der Zimmerpreis diesen Betrag überschreitet, benachrichtigt das System den         
Arbeitnehmer, dass der Richtlinienbetrag für die Ausgabe überschritten wurde. Sie können die Nachricht konfigurieren, die der Worker erhält        
definieren der Richtlinie.      
        
Sie können drei Arten von Richtlinien definieren:         
        
- **Warnung**: Ermöglicht dem Mitarbeiter, eine Ausgabenabrechnung oder Reiseanforderung einzureichen, die Ausgaben werden jedoch für alle Genehmigenden markiert und         
  für die spätere Berichterstattung.        

- **Fehler**: Fordert den Arbeitnehmer auf, die Ausgaben zu überarbeiten, um die Richtlinien einzuhalten, bevor er die Spesenabrechnung oder die Reiseanforderung einreicht.        
 
 - **Rechtfertigung**: Fordert den Arbeitnehmer oder einen Manager auf, vor dem Einreichen der Ausgabenabrechnung oder der Reiseanforderung eine Begründung für die Überschreitung des Richtlinienbetrags einzugeben.        

## <a name="policy-tips"></a>Richtlinienhinweise
Im Folgenden finden Sie einige Vorschläge, die Sie beim Erstellen neuer Richtlinien für das Ausgabenmanagement unterstützen können: 

- Richtlinien haben das Datum des Inkrafttretens. Dies bedeutet, dass eine Richtlinie nicht wirksam wird, wenn sie mit einem Datum nach dem Datum erstellt wird, an dem die Ausgabe entstanden sind. Beispielsweise erstellen Sie heute eine neue Richtlinie, um eine maximale Essensausgabe von $50 durchzusetzen. Bestehende Ausgaben, die ab gestern eingegeben wurden, werden nicht mit dieser Richtlinie verglichen.
- Wenn Sie eine Richtlinie für eine Ausgabenkategorie erstellen, die aufgelistet werden kann, sollten Sie eine Bedingung für den Ausgabenzeilentyp hinzufügen. Einige Richtlinien, z. B. das Erfordernis einer Quittung, sind für einzelne Zeilen möglicherweise nicht sinnvoll. In dieser Situation wird die Richtlinie nur auf die Kopfzeile oder eine nicht aufgeschlüsselte Zeile angewendet. 
- Ausgabenverwaltungsrichtlinien werden standardmäßig anhand der Quellenentität bewertet. Für konzerninterne Szenarien können Sie stattdessen festlegen, dass die Richtlinie anhand der Zielentität (Kreditinstanz) bewertet wird. Aktivieren Sie die Funktion **Bewerten Sie die Ausgabenpolitik gegen die Aufnahme einer juristischen Person** im Arbeitsbereich **Funktionsverwaltung**, um die Richtlinien für die Zielentität auszuführen.

## <a name="when-to-evaluate-policies"></a>Wann müssen die Richtlinien bewertet werden

In den Ausgabenmanagementparametern können Sie auswählen, ob die Ausgabenmanagementrichtlinien ausgewertet werden sollen, wenn eine Zeile gespeichert wird oder wenn eine Ausgabenabrechnung gesendet wird. Wenn Sie auswerten möchten, wann eine Zeile gespeichert wird, haben Benutzer früher einen Überblick darüber, was sie tun müssen, um ihre Ausgabenabrechnung auf einmal zu vervollständigen. Andernfalls können Sie die Richtlinienbewertung verzögern und Zeit sparen, indem Sie am Ende während der Übermittlung an den Workflow validieren.