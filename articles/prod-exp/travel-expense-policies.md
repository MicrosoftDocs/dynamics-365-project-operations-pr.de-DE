---
title: Ausgabenrichtlinien einrichten
description: Sie können die Ausgabenrichtlinien einrichten, die Ihre Mitarbeiter beim Eingeben und Senden von Spesenabrechnungen und Reiseanforderungen in Microsoft Dynamics 365 Finance befolgen müssen.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076671"
---
# <a name="set-up-expense-policies"></a>Ausgabenrichtlinien einrichten

[!include [banner](../includes/banner.md)]

Sie können Ausgabenrichtlinien definieren, denen Ihre Mitarbeiter beim Eingeben und Senden von Ausgabeabrechnungen und Reiseanforderungen folgen müssen.         
Durch die Implementierung von Ausgabenrichtlinien können Sie Ausgaben effektiv verwalten.         

Sie können beispielsweise eine Richtlinie für Hotelkosten in New York City festlegen, die besagt, dass die Kosten pro Nacht USD 250 nicht überschreiten dürfen.       
Wenn ein Mitarbeiter eine Spesenabrechnung oder eine Reiseanforderung einreicht, bei der der Zimmerpreis diesen Betrag überschreitet, benachrichtigt das System den        
Arbeitnehmer, dass der Richtlinienbetrag für die Ausgabe überschritten wurde. Sie können die Nachricht konfigurieren, die der Worker erhält        
definieren der Richtlinie.      
        
Sie können drei Arten von Richtlinien definieren:         
        
- Warnung – Ermöglicht dem Mitarbeiter, eine Spesenabrechnung oder Reiseanforderung einzureichen, die Ausgaben werden jedoch für alle Genehmigenden markiert und        
  für die spätere Berichterstattung.        

- Fehler – Fordert den Arbeitnehmer auf, die Ausgaben zu überarbeiten, um die Richtlinien einzuhalten, bevor er die Spesenabrechnung oder die Reiseanforderung einreicht       
 
 - Rechtfertigung – Fordert den Arbeitnehmer oder einen Manager auf, vor dem Einreichen der Spesenabrechnung oder der Reiseanforderung eine Begründung für die Überschreitung des Richtlinienbetrags einzugeben.        

## <a name="policy-tips"></a>Richtlinienhinweise
Im Folgenden finden Sie einige Vorschläge, die Sie beim Erstellen neuer Richtlinien für das Ausgabenmanagement unterstützen können. 
* Richtlinien haben das Datum des Inkrafttretens. Eine Richtlinie wird nicht wirksam, wenn sie mit einem Datum nach dem Datum erstellt wird, an dem die Ausgaben entstanden sind. Wenn Sie beispielsweise heute eine neue Richtlinie erstellen, um maximale Mahlzeitkosten von 50 USD durchzusetzen, werden alle ab gestern eingegebenen Ausgaben nicht mit dieser Richtlinie verglichen.
* Wenn Sie eine Richtlinie für eine Ausgabenkategorie erstellen, die aufgelistet werden kann, sollten Sie eine Bedingung für den Ausgabenzeilentyp hinzufügen. Einige Richtlinien, z. B. die Erfordernis einer Quittung, sind für Einzelposten möglicherweise nicht sinnvoll und sollten nur auf die Kopfzeile oder eine nicht Einzelpostenzeile angewendet werden. 
* Ausgabenverwaltungsrichtlinien werden standardmäßig anhand der Quellenentität bewertet. Für konzerninterne Szenarien können Sie stattdessen festlegen, dass die Richtlinie anhand der Zielentität (Kreditinstanz) bewertet wird. Um die Richtlinien für die Zielentität auszuführen, aktivieren Sie die Funktion „Bewerten Sie die Ausgabenpolitik gegen die Aufnahme einer juristischen Person“ im Arbeitsbereich **Funktionsverwaltung**.

## <a name="when-to-evaluate-policies"></a>Wann müssen die Richtlinien bewertet werden

In den Ausgabenverwaltungsparametern können Sie auswählen, ob die Ausgabenverwaltungsrichtlinien ausgewertet werden sollen, wenn eine Zeile gespeichert wird oder wenn eine Spesenabrechnung gesendet wird. Wenn Sie auswerten, wann eine Zeile gespeichert wird, stellt dies sicher, dass Benutzer früher einen Überblick darüber erhalten, was sie tun müssen, um ihre Spesenabrechnung auf einmal zu vervollständigen. Andernfalls können Sie die Richtlinienbewertung verzögern und Zeit sparen, wenn am Ende während der Übermittlung an den Workflow eine Überprüfung ansteht.
