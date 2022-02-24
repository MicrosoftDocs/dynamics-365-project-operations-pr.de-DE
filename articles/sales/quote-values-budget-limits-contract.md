---
title: Projektangebotseinstellungen
description: Dieses Thema enthält Informationen zu den Informationen und Einstellungen, die für Projektangebote gelten und sich auf diese auswirken.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5b1b88596ddac48ab8adce00c25c3ccd83cdd727
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663638"
---
# <a name="header-details-for-project-based-quotes"></a>Kopfzeilendetails für projektbasierte Angebote

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_


In diesem Artikel werden die Informationen erläutert, die für ein Projektangebot gelten. Dies umfasst die Einstellungen, die sich auf alle Angebotspositionen auswirken, sowie Informationen zum Angebot, die in allen Positionen zusammengefasst sind, um die KPIs des Projektangebots zu steuern.

In der folgenden Tabelle sind die Felder mit den zusammenfassenden Informationen zu einem Projektvertrag aufgeführt, die nur in Dynamics 365 Project Operations vorhanden sind oder einige wichtige Änderungen im Verhalten hinsichtlich Angeboten in Dynamics 365 Sales aufweisen.

| **Feld** | **Ort** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- | --- |
| Art | Registerkarte „Zusammenfassung“ (ausgeblendet) | Dieses Optionssatzfeld enthält die folgenden Optionen:</br>- Arbeitsbasiert (nur bei Installation von Project Operations verfügbar)</br>- Positionsbasiert (nur verfügbar, wenn Project Operations und Sales installiert sind)</br>- Servicewartungsbasiert (verfügbar, wenn Dynamics 365 Field Service installiert ist) | Wenn Sie die Project Operations-Anwendung verwenden, wird der Wert dieses Felds automatisch auf **Arbeitsbasiert** festgelegt. Dadurch wird das Angebot als projektbasiertes Angebot klassifiziert. Ein Angebot sollte projektbasiert sein, um alle projektspezifischen Erweiterungen und Funktionen zu aktivieren. |
| Zuständiges Unternehmen | Übersicht | Die juristische Person, die die Kosten und Einnahmen aus diesem Projekt oder den mit diesem Angebot verbundenen Projekten berücksichtigt. Bei einem aus einer Verkaufschance erstellten Angebot wird dieses Feld aus dem entsprechenden Feld in der Verkaufschance kopiert. | Das zuständige Unternehmen entspricht dem Konzept der juristischen Person im Modul **Projektmanagement und -buchhaltung** von Project Operations. Alle Kosten und Umsätze aus diesem Projekt werden in der Finanzbuchhaltung des zuständigen Unternehmens ausgewiesen. |
| Potenz. Kunde | Registerkarte „Zusammenfassung“ | Verweis auf die Firma oder den Kontodatensatz des Kunden. Ein gültiger Kunde, auf den im Projektangebot verwiesen werden kann, muss als Kunde im zuständigen Unternehmen des Angebots eingerichtet sein. Das zuständige Unternehmen zeigt die Liste der juristischen Personen an. Diese werden im Modul **Projektmanagement und -buchhaltung** von Project Operations eingerichtet. Bei einem aus einer Verkaufschance erstellten Angebot wird dieses Feld aus dem entsprechenden Feld in der Verkaufschance kopiert. | Die Währung im Projektangebot basiert auf der Währung des Kunden. Diese kann jedoch vor dem Speichern des Angebots gespeichert werden. |
| Konto-Manager | Registerkarte „Zusammenfassung“ | Der Name des Account Managers für dieses Geschäft. Bei einem aus einer Verkaufschance erstellten Angebot wird dieses Feld aus dem entsprechenden Feld in der Verkaufschance kopiert. | Der Account Manager ist verantwortlich für die Verwaltung der Beziehung zum Kunden bis zum Abschluss dieses Projekts. Basierend auf dem buchbaren Ressourceneintrag, der an den Account Manager gebunden ist, ist die Vertragseinheit im Projektangebot voreingestellt.|
| Vertragseinheit | Registerkarte „Zusammenfassung“ | Die Organisationseinheit, die für die Bereitstellung des Projekts oder der mit diesem Angebot verbundenen Projekte verantwortlich ist. Bei einem aus einer Verkaufschance erstellten Angebot wird dieses Feld aus dem entsprechenden Feld in der Verkaufschance kopiert. | Die Vertragseinheit ist die Abteilung des Unternehmens, die die Projekte nach Abschluss des Geschäfts abschließt. Jede Vertragseinheit hat eine Währung, und diese Währung wird verwendet, um geschätzte und tatsächliche Kosten zu melden, die während der Ausführung des Projekts anfallen. |
| Produktpreisliste | Registerkarte „Zusammenfassung“ | Dies ist die Preisliste, die verwendet wird, um die Preise in den produktbasierten Angebotspositionen als Standard festzulegen. Die Liste der Optionen für dieses Feld enthält eine Liste der Preislisten, bei denen die Preislistenwährung mit der Währung im Angebot übereinstimmt. Bei einem aus einer Verkaufschance erstellten Angebot wird dieses Feld aus dem entsprechenden Feld in der Verkaufschance kopiert. Dieses Feld für die Verkaufschance wird standardmäßig aus dem Firmendatensatz übernommen, kann jedoch geändert werden. | Wenn ein Angebot gewonnn wurde, wird der Feldwert in den erstellten Projektvertrag kopiert. |
| Währung | Registerkarte „Zusammenfassung“ | Dies gibt die Währung an, die für die Meldung des Werts dieses Geschäfts verwendet wird. Dies ist auch die Währung, in der dem Kunden eine Rechnung gestellt wird, wenn das Geschäft gewonnen wurde. Bei einem aus einer Verkaufschance erstellten Angebot wird dieses Feld aus dem entsprechenden Feld in der Verkaufschance kopiert. Dieses Feld für die Verkaufschance wird standardmäßig aus dem Firmendatensatz übernommen, kann jedoch vom Benutzer geändert werden.  | Nachdem ein Angebot gespeichert wurde, kann dieses Feld nicht mehr bearbeitet werden. Dies wird verwendet, um die Produkt- und Projektpreislisten im Angebot standardmäßig anzugeben. Die Währung im Angebot wird verwendet, um die Währung in der Preisliste abzustimmen. |
| Nicht zu überschreitender Grenzwert | Registerkarte „Zusammenfassung“ | Dies zeigt die ausgehandelte Obergrenze für den Endwert an, dem der Kunde für dieses Geschäft zustimmt. | Diese Obergrenze wird während der Ausführung bewertet und gilt für alle mit diesem Geschäft verbundenen Positionen und Projekte. |
| Angefordertes Bereitstellungsdatum | Registerkarte „Zusammenfassung“ | Bei einem aus einer Verkaufschance erstellten Angebot wird dieses Feld aus dem entsprechenden Feld in der Verkaufschance kopiert. | Dieses Datum wird als Enddatum für die Erstellung von Rechnungsplänen verwendet. |

Im Folgenden finden Sie die Registerkarten und KPIs, die in einem Projektangebot verfügbar sind, die nur für Project Operations gelten oder einige wichtige Verhaltensänderungen gegenüber Verkaufsangeboten aufweisen:

| **Feld** | **Ort** | **Beschreibung** |
| --- | --- | --- |
| Rentabilitätsanalyse | Registerkarte im Angebot | Die Registerkarte zeigt die folgenden Metriken an:</br>- Fakturierbare Gesamtkosten</br></br>- Nicht fakturierbare Gesamtkosten</br>- Gesamtumsatz</br>- Gesamtumsatz (Basis)</br>- Bruttogewinn</br>- Angepasster Bruttogewinn|
| Vergleich mit Kundenerwartungen | Registerkarte im Angebot | Diese Registerkarte zeigt die folgenden Metriken an:</br>- Geschätzter Abschluss</br>- Angeforderter Abschluss</br>- Kundenbudget</br>- Angebotswert |
| Angebotsanalyse | Registerkarte im Angebot | Diese Registerkarte fasst die folgenden Top-KPIs für ein Projektangebot zusammen</br>- Vergleich der Kundenerwartungen hinsichtlich Budget und Zeitplan</br>- Bruttogewinn</br>- Angepasster Bruttogewinn |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
