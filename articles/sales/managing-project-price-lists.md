---
title: Projektpreislisten in einem Angebot verwalten
description: Dieser Artikel enthält Informationen über die Entität Projektpreisliste.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8439a03e6557ec531405048ec4149344e283242e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933148"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Projektpreislisten in einem Angebot verwalten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations erweitert die Preislistenentität in Dynamics 365 Sales. 

## <a name="key-entities"></a>Schlüsselentitäten

Eine Preisliste enthält Informationen, die von vier verschiedenen Entitäten bereitgestellt werden:

- **Preisliste**: Diese Entität speichert Informationen zum Kontext, zur Währung, zur Datumsgültigkeit und zur Preisgestaltungszeit. Kontext zeigt, ob die Preisliste Kosten- oder Vertriebsraten enthält. 
- **Währung**: Diese Entität speichert die Währung von Preisen auf der Preisliste. 
- **Datum**: Diese Entität wird verwendet, wenn das System versucht, einen Preis standardmäßig für eine Transaktion einzugeben. Es wird eine Preisliste ausgewählt, bei der eine Datumsgültigkeit vorliegt, die das Datum der Transaktion enthält. Wenn mehr als eine Preisliste gefunden wird, die für das Transaktionsdatum gültig ist und dem entsprechenden Angebot, Vertrag oder der Organisationseinheit angefügt ist, wird kein Preis standardmäßig festgelegt. 
- **Zeit**: Diese Entität speichert die Zeiteinheit, für die Preise ausgedrückt werden, beispielsweise Tages- oder Stundenraten. 

Mit der Preislistenentität sind drei Tabellen verbunden, bei denen Preise gespeichert werden:

  - **Rollenpreis**: Diese Tabelle enthält eine Rate für eine Kombination aus Rollen- und Organisationseinheitswerten und wird verwendet, um rollenbasierte Preise für Mitarbeiter festzulegen.
  - **Transaktionskategoriepreis**: Diese Tabelle enthält Preise nach Transaktionskategorie und wird verwendet, um Ausgabenkategoriepreise einzurichten.
  - **Preislistenelemente**: Diese Tabelle enthält Preise für Katalogprodukte.
 
Die Preisliste ist eine Gebührenkarte. Eine Gebührenkarte ist eine Kombination aus der Preislistenentität und verknüpften Zeilen bei den Tabellen Rollenpreis, Transaktionskategoriepreis und Preislistenelemente.

## <a name="resource-roles"></a>Ressourcenrollen

Der Begriff *Ressourcenrolle* bezieht sich auf eine Reihe von Fähigkeiten, Kompetenzen und Zertifizierungen, die eine Person haben muss, um eine bestimmte Gruppe von Aufgaben bei einem Projekt durchzuführen.

Die Personalzeit wird normalerweise basierend auf der Rolle angeboten, die eine Ressource für ein bestimmtes Projekt erfüllt. Für die Personalzeit basiert die Kostenberechnung und Abrechnung basierend auf der Ressourcenrolle. Bei der Zeit kann der Preis für alle Einheiten in der Einheitengruppe **Zeit** berechnet werden.

Die Einheitengruppe **Zeit** wird bei der Installation von Project Operations erstellt. Es hat die Standardeinheit **Stunde**. Sie können die Attribute für die Einheitengruppe **Zeit** oder **Stunde** nicht löschen, umbenennen oder bearbeiten. Sie können der Einheitengruppe **Zeit** jedoch andere Einheiten hinzufügen. Wenn Sie versuchen, entweder die Einheitengruppe **Zeit** oder **Stunde** zu löschen, kann dies unter Umständen zu Fehlern in der Geschäftslogik führen.
 
## <a name="transaction-categories-and-expense-categories"></a>Transaktions- und Ausgabenkategorien

Reise- und andere Ausgaben, die Projektberater verursachen, werden in der Regel dem Kunden in Rechnung gestellt. Preisgestaltung von Ausgabenkategorien werden durch die Verwendung von Preislisten abgeschlossen. Flugpreise, Hotel und Automiete sind Beispiele für Ausgabenkategorien. Jede Preislistenzeile für Ausgaben gibt die Preisgestaltung für eine bestimmte Ausgabenkategorie an. Die folgenden drei Methoden werden verwendet, um Ausgabenkategorien zu bewerten:

- **Einstandswert**: Die Ausgabenkosten werden dem Kunden in Rechnung gestellt und es wird kein Aufschlag angewendet.
- **Aufschlagsprozentsatz**: Den Prozentsatz für die tatsächlichen Kosten wird dem Kunden in Rechnung gestellt. 
- **Einzelpreis**: Ein Abrechnungspreis wird für jede Einheit der Ausgabenkategorie festgelegt. Der Betrag, der dem Kunden berechnet wird, wird basierend auf der Anzahl der Ausgabeneinheiten berechnet, die der Berater meldet. Bei der Kilometerangabe wird die Preis-pro-Einheit-Preisberechnungsmethode verwendet. Beispielsweise kann die Kilometerangaben-Ausgabenkategorie mit 30 US-Dollar (USD) pro Tag oder 2 USD pro Meile konfiguriert werden. Wenn ein Berater die Kilometerangabe bei einem Projekt meldet, wird der Abrechnungsbetrag basierend auf der Anzahl der Meilen berechnet, die der Berater gemeldet hat.
 
## <a name="project-sales-pricing-and-overrides"></a>Projektvertriebspreisberechnung und -Außerkraftsetzungen

Für Projektangebote und -verträge enthält eine Projektpreisliste ein anderes Preisaußerkraftsetzungsmuster als eine Produktpreisliste. Bei einer produktkatalogbasierten Angebotszeile können Sie den Preis für Rollen und Kategorien direkt in der Angebotszeile überschreiben, da jede Angebotszeile genau auf ein Katalogelement verweist. Allerdings können Sie bei einer projektbasierten Angebotszeile den Preis für Rollen und Kategorien nicht direkt in der Angebotszeile überschreiben. Sie können die Projektpreisliste verwenden, um die beiden unterschiedlichen Überschreibungsmustern zu unterstützen.

> [!NOTE]
> Wir empfehlen Ihnen, dass Sie aufgrund der Verhaltensunterschiede zwischen den zwei beim Überschreiben der Preisgestaltung eine separate Preisliste für Ihre Projektressourcen und Ihre Katalogelemente einrichten.

Jeder der folgenden Entitäten kann eine oder mehrere Vertriebspreislisten für die Projektpreisberechnung zugewiesen werden:

- Kunde (Konto) 
- Verkaufschance 
- Angebot 
- Projektvertrag

Die Zuordnung dieser Entitäten mit einer Preisliste wird anhand der Projektpreislisten angegeben. Sie können eine oder mehrere Preislisten den Vertriebsentitäten Kunde, Verkaufschance, Angebot und Projekt zuordnen.

Eine Standardprojektpreisliste wird nicht automatisch in einen Kundendatensatz eingegeben. Sie können jedoch eine Projektpreisliste manuell dem Kundendatensatz anfügen. Dennoch sollten Sie eine Projektpreisliste nur manuell anfügen, wenn Sie eine benutzerdefinierte Preisvereinbarung mit dem Kunden haben. 

Wenn eine Projektpreisliste einer Vertriebsentität angefügt ist, werden die folgenden Informationen überprüft:

- Die Preisliste hat einen Kontext **Vertrieb**. 
- Die Währung der Preisliste stimmt mit der Währung des Kunden überein. 

Bei einem Projektvertrag wird die folgende Rangfolge verwendet, um verwandte Projektpreislisten automatisch festzulegen:

1. Angebot
2. Verkaufschance
3. Kunde 
4. Globale Einstellungen 

Wenn eine Projektpreisliste standardmäßig angegeben ist, prüft das System, dass die Währung mit der Währung des Kunden übereinstimmt, und dass die Standardpreislisten, die eingegeben wurden, den Kontext **Vertrieb** haben.

Sie können mehrere Projektpreislisten den Entitäten Kunde, Verkaufschance, Angebot und Projektvertrag zuordnen. Diese Funktion unterstützt datumsspezifische Standardpreise für einen Projektvertrag mit langer Laufzeit, bei dem mehr als eine Preisliste erforderlich ist, um Preisaktualisierungen zu berücksichtigen, die aufgrund von Inflation auftreten. Wenn die Preislisten, die Sie der Entität Kunden, Verkaufschance, Angebot oder Projektvertrag zuordnen, eine überlappende Datumsgültigkeit haben, sind die Standardpreise unter Umständen falsch. Sie sollten deshalb sicherstellen, dass Projektpreislisten, die eine überlappende Datumsgültigkeit haben, nicht diesen Entitäten zugewiesen sind.

### <a name="deal-specific-price-overrides"></a>Angebotsspezifische Preisaußerkraftsetzungen

Sie können angebotsspezifische Außerkraftsetzungen für ausgewählte Preise auf Projektpreislisten erstellen, die standardmäßig in einem Angebot oder Projektvertrag eingegeben werden.

Standardmäßig erhält ein Projektvertrag immer eine Kopie der Mastervertriebspreisliste statt eines direkten Links zur Liste. Mithilfe dieses Verhaltens kann garantiert werden, dass Preisvereinbarungen mit einem Kunden über eine Leistungsbeschreibung (SOW) nicht geändert werden, wenn die Masterpreisliste geändert wird.

Bei einem Angebot können Sie jedoch eine Masterpreisliste verwenden. Sie können auch eine Masterpreisliste kopieren und sie bearbeiten, um eine benutzerdefinierte Preisliste zu erstellen, die nur für dieses Angebot gilt. Um eine neue Preisliste zu erstellen, die nur für ein bestimmtes Angebot gilt, wählen Sie auf der Seite **Angebot** die Option **Benutzerdefinierte Preisberechnung erstellen** aus. Sie können nur über das Angebot auf die angebotsspezifische Projektpreisliste zugreifen. 

Wenn Sie eine benutzerdefinierte Projektpreisliste erstellen, werden nur die Projektkomponenten der Preisliste kopiert. Das bedeutet, eine neue Preisliste, die als Kopie der vorhandenen Projektpreisliste erstellt wurde, wird dem Angebot angefügt, und diese neue Preisliste hat nur verknüpfte Rollenpreise und Transaktionskategoriepreise.
  
## <a name="tracking-costs"></a>Nachverfolgung von Kosten

Project Operations verfolgt die Kosten für die Nutzung der Personalzeit bei Projekten. Darüber hinaus werden auch die Kosten für andere wiederkehrende Ausgaben nachverfolgt, die während des Projekts auflaufen, wie z. B. Reisekosten.

Wie Rechnungssätze werden auch Kostensätze für Personal mithilfe von Preislisten eingerichtet. Hier finden Sie die Hauptunterschiede im Verhalten der Einstandspreisliste und der Vertriebspreisliste:

- Der Kostensatz einer Ressource darf bei einem bestimmten Projekt, Vertrag oder Angebot nicht überschrieben werden. Rechnungssätze können jedoch auf der Grundlage einzelner Angebote überschrieben werden, wenn Änderungen vorgenommen werden, die nur für die Art des Angebots gelten. 

- Die folgende Reihenfolge wird verwendet, um eine Einstandspreisliste abzuschließen:

    1. Die Einstandspreisliste, die der Organisationseinheit angefügt wird.
    2. Die Einstandspreisliste, die den Project Operations Parametern angefügt wird. Da Einstandspreislisten in vielen verschiedenen Währungen den Project Service-Parametern angefügt werden können, wird eine Währungsabstimmung zwischen der Währung der Vertragsorganisationseinheit des Projekts, Vertrags oder Angebots und der Währung der Einstandspreisliste durchgeführt.
    3. Bei Ausgaben gelten die Preisberechnungsmethoden „Zum Einstandswert“ und „Aufschlag auf Kosten“ nicht für Einstandspreislisten. Selbst wenn diese Preisberechnungsmethoden bei Einstandspreislistenzeilen verwendet werden, um Transaktionskategoriekosten einzurichten, werden diese vom System ignoriert, und es wird kein Standardeinstandspreis angegeben.


[!INCLUDE[footer-include](../includes/footer-banner.md)]