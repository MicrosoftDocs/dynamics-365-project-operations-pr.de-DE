---
title: Projektpreise
description: Dieses Thema enthält Informationen zu den Preisen in Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 010fe834-c449-46ee-9d45-7c91cd8e262a
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fec4f24688a00cd019577460e948bef6b918f1b5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722000"
---
# <a name="project-pricing"></a>Projektpreise 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation erweitert die Preislistenentität in Dynamics 365 Sales. 

## <a name="key-entities"></a>Schlüsselentitäten

Eine Preisliste enthält Informationen, die von vier verschiedenen Entitäten bereitgestellt werden:

- **Preisliste** – Diese Entität speichert Informationen zum Kontext, zur Währung, zur Datumsgültigkeit und zur Preisgestaltungszeit. Der Kontext zeigt, ob die Preisliste Kosten- oder Vertriebsraten enthält. 
- **Währung** – Diese Entität speichert die Währung von Preisen auf der Preisliste. 
- **Datum** – Diese Entität wird verwendet, wenn das System versucht, einen Preis standardmäßig für eine Transaktion einzugeben. Bei der Preisgestaltung in PSA wird die Preisliste ausgewählt, bei der eine Datumsgültigkeit vorliegt, die das Datum der Transaktion enthält. Wenn bei der PSA-Preisberechnung festgestellt wird, dass mehr als eine Preisliste, die für das Transaktionsdatum gültig ist, dem entsprechenden Angebot, Vertrag oder der Organisationseinheit angefügt ist, wird kein Preis standardmäßig festgelegt. 
- **Zeit** – Diese Entität speichert die Zeiteinheit, für die Preise ausgedrückt werden, beispielsweise Tages- oder Stundenraten. 

Mit der Preislistenentität sind drei Tabellen verbunden, bei denen Preise gespeichert werden:

  - **Rollenpreis** – Diese Tabelle enthält eine Rate für eine Kombination aus Rollen- und Organisationseinheitswerten und wird verwendet, um rollenbasierte Preise für Mitarbeiter festzulegen.
  - **Transaktionskategoriepreis** – Diese Tabelle enthält Preise nach Transaktionskategorie und wird verwendet, um Ausgabenkategoriepreise einzurichten.
  - **Preislistenelemente** – Diese Tabelle enthält Preise für Katalogprodukte.

> ![Konfigurieren von Preisen mithilfe einer Preisliste](media/basic-guide-12.png)
 
Die Preisliste ist eine Gebührenkarte. Eine Gebührenkarte ist eine Kombination aus der Preislistenentität und verknüpften Zeilen bei den Tabellen Rollenpreis, Transaktionskategoriepreis und Preislistenelemente.

## <a name="resource-roles"></a>Ressourcenrollen

Der Begriff *Ressourcenrolle* bezieht sich auf eine Reihe von Fähigkeiten, Kompetenzen und Zertifizierungen, die eine Person haben muss, um eine bestimmte Gruppe von Aufgaben bei einem Projekt durchzuführen.

Die Personalzeit wird normalerweise basierend auf der Rolle angeboten, die eine Ressource bei einem bestimmten Projekt erfüllt. Für die Personalzeit unterstützt PSA die Kostenberechnung und Abrechnung basierend auf der Ressourcenrolle. Bei der Zeit kann der Preis für alle Einheiten in der Einheitengruppe **Zeit** berechnet werden.

Die Einheitengruppe **Zeit** wird erstellt, wenn PSA installiert ist. Es hat die Standardeinheit **Stunde**. Sie können die Attribute für die Einheitengruppe **Zeit** oder die Einheit **Stunde** nicht löschen, umbenennen oder bearbeiten. Sie können der Einheitengruppe **Zeit** jedoch andere Einheiten hinzufügen. Wenn Sie versuchen, entweder die Einheitengruppe **Zeit** oder die Einheit **Stunde** zu löschen, kann dies unter Umständen zu Fehlern in der PSA-Geschäftslogik führen.

> ![Konfigurieren von Preisen nach Rolle](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Transaktions- und Ausgabenkategorien

Reise- und sonstige Ausgaben, die Projektberater verursachen, werden in der Regel dem Kunden in Rechnung gestellt. PSA unterstützt die Preisgestaltung von Ausgabenkategorien durch die Verwendung von Preislisten. Flugpreise, Hotel und Automiete sind Beispiele für Ausgabenkategorien. Jede Preislistenzeile für Ausgaben gibt die Preisgestaltung für eine bestimmte Ausgabenkategorie an. Für die Preisgestaltung von Ausgabenkategorien unterstützt PSA die folgenden drei Preisberechnungsmethoden:

- **Zum Einstandswert** – Die Ausgabenkosten werden dem Kunden in Rechnung gestellt und es wird kein Aufschlag angewendet.
- **Aufschlagsprozentsatz** – Den Prozentsatz für die tatsächlichen Kosten wird dem Kunden in Rechnung gestellt. 
- **Einzelpreis** – Ein Abrechnungspreis wird für jede Einheit der Ausgabenkategorie festgelegt. Der Betrag, der dem Kunden berechnet wird, wird basierend auf der Anzahl der Ausgabeneinheiten berechnet, die der Berater meldet. Bei der Kilometerangabe wird die Preis-pro-Einheit-Preisberechnungsmethode verwendet. Beispielsweise kann die Kilometerangaben-Ausgabenkategorie mit 30 US-Dollar (USD) pro Tag oder 2 USD pro Meile konfiguriert werden. Wenn ein Berater die Kilometerangabe bei einem Projekt meldet, wird der Abrechnungsbetrag basierend auf der Anzahl der Meilen berechnet, die der Berater gemeldet hat.

> ![Konfigurieren der Preisberechnung für Ausgabenkategorien](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Projektvertriebspreisberechnung und -Außerkraftsetzungen

Für Projektangebote und -verträge enthält eine Projektpreisliste ein anderes Preisaußerkraftsetzungsmuster als eine Produktpreisliste. Bei einer produktkatalogbasierten Angebotszeile können Sie den Preis für Rollen und Kategorien direkt in der Angebotszeile überschreiben, da jede Angebotszeile genau auf ein Katalogelement verweist. Allerdings können Sie bei einer projektbasierten Angebotszeile den Preis für Rollen und Kategorien nicht direkt in der Angebotszeile überschreiben. Um die beiden unterschiedlichen Außerkraftsetzungsmuster zu unterstützen, hat PSA eine neue Preislistenzuordnung eingeführt, die Projektpreisliste.

> [!NOTE]
> Wir empfehlen Ihnen, dass Sie aufgrund der Verhaltensunterschiede zwischen den zwei beim Überschreiben der Preisgestaltung eine separate Preisliste für Ihre Projektressourcen und Ihre Katalogelemente einrichten.

Jeder der folgenden Entitäten kann eine oder mehrere Vertriebspreislisten für die Projektpreisberechnung zugewiesen werden:

- Kunde (Konto) 
- Verkaufschance 
- Angebot 
- Projektvertrag

Die Zuordnung dieser Entitäten mit einer Preisliste wird anhand der Projektpreislisten angegeben. Sie können eine oder mehrere Preislisten den Vertriebsentitäten Kunde, Verkaufschance, Angebot und Projekt zuordnen.

Eine Standardprojektpreisliste wird nicht automatisch in einen Kundendatensatz eingegeben. Sie können jedoch eine Projektpreisliste manuell dem Kundendatensatz anfügen. Dennoch sollten Sie eine Projektpreisliste nur manuell anfügen, wenn Sie eine benutzerdefinierte Preisvereinbarung mit dem Kunden haben. 

Wenn eine Projektpreisliste einer Vertriebsentität angefügt ist, überprüft PSA die folgenden Informationen:

- Die Preisliste hat den Kontext **Vertrieb**. 
- Die Währung der Preisliste stimmt mit der Währung des Kunden überein. 

Bei einem Projektvertrag verwendet PSA die folgende Rangfolge, um verwandte Projektpreislisten automatisch festzulegen:

1. Angebot
2. Verkaufschance
3. Kunde 
4. Globale Einstellungen für PSA

Wenn eine Projektpreisliste standardmäßig angegeben ist, überprüft PSA, dass die Währung mit der Währung des Kunden übereinstimmt, und dass die Standardpreislisten, die eingegeben wurden, den Kontext **Vertrieb** haben.

Sie können mehrere Projektpreislisten den Entitäten Kunde, Verkaufschance, Angebot und Projektvertrag zuordnen. Diese Funktion unterstützt datumsspezifische Standardpreise für einen Projektvertrag mit langer Laufzeit, bei dem mehr als eine Preisliste erforderlich ist, um Preisaktualisierungen zu berücksichtigen, die aufgrund von Inflation auftreten. Wenn die Preislisten, die Sie der Entität Kunden, Verkaufschance, Angebot oder Projektvertrag zuordnen, eine überlappende Datumsgültigkeit haben, sind die Standardpreise unter Umständen falsch. Sie sollten deshalb sicherstellen, dass Projektpreislisten, die eine überlappende Datumsgültigkeit haben, nicht diesen Entitäten zugewiesen sind.

### <a name="deal-specific-price-overrides"></a>Angebotsspezifische Preisaußerkraftsetzungen

Sie können in PSA angebotsspezifische Außerkraftsetzungen für ausgewählte Preise auf Projektpreislisten erstellen, die standardmäßig in einem Angebot oder Projektvertrag eingegeben werden.

Standardmäßig erhält ein Projektvertrag immer eine Kopie der Mastervertriebspreisliste statt eines direkten Links zur Liste. Mithilfe dieses Verhaltens kann garantiert werden, dass Preisvereinbarungen mit einem Kunden über eine Leistungsbeschreibung (statement of work, SOW) nicht geändert werden, wenn die Masterpreisliste geändert wird.

Bei einem Angebot können Sie jedoch eine Masterpreisliste verwenden. Sie können auch eine Masterpreisliste kopieren und sie bearbeiten, um eine benutzerdefinierte Preisliste zu erstellen, die nur für dieses Angebot gilt. Um eine neue Preisliste zu erstellen, die nur für ein bestimmtes Angebot gilt, wählen Sie auf der Seite **Angebot** die Option **Benutzerdefinierte Preisberechnung erstellen** aus. Sie können nur über das Angebot auf die angebotsspezifische Projektpreisliste zugreifen. 

Wenn Sie eine benutzerdefinierte Projektpreisliste erstellen, werden nur die Projektkomponenten der Preisliste kopiert. Das bedeutet, eine neue Preisliste, die als Kopie der vorhandenen Projektpreisliste erstellt wurde, wird dem Angebot angefügt, und diese neue Preisliste hat nur verknüpfte Rollenpreise und Transaktionskategoriepreise.

> ![Anzeigen und Konfigurieren benutzerdefinierter Preisberechnungen für einen Projektvertrag](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Nachverfolgung von Kosten

PSA verfolgt die Kosten für die Nutzung der Personalzeit bei Projekten. Darüber hinaus werden auch die Kosten für andere Ausgaben nachverfolgt, die während des Projekts auflaufen, wie z. B. Reisekosten.

Wie Rechnungssätze werden auch Kostensätze für Personal mithilfe von Preislisten eingerichtet. Hier finden Sie die Hauptunterschiede im Verhalten der Einstandspreisliste und der Vertriebspreisliste:

- Der Kostensatz einer Ressource darf bei einem bestimmten Projekt, Vertrag oder Angebot nicht überschrieben werden. Rechnungssätze können jedoch auf der Grundlage einzelner Angebote überschrieben werden, wenn Änderungen vorgenommen werden, die nur für die Art des Angebots gelten. 

- Die folgende Reihenfolge wird verwendet, um eine Einstandspreisliste abzuschließen:

    1. Die Einstandspreisliste, die der Organisationseinheit angefügt wird.
    2. Die Einstandspreisliste, die den Project Service-Parametern angefügt wird. Da Einstandspreislisten in vielen verschiedenen Währungen den Project Service-Parametern angefügt werden können, führt PSA eine Währungsabstimmtung zwischen der Währung der Vertragsorganisationseinheit des Projekts, Vertrags oder Angebots und der Währung der Einstandspreisliste durch.
    3. Bei Ausgaben gelten die Preisberechnungsmethoden „Zum Einstandswert” und „Aufschlag auf Kosten” nicht für Einstandspreislisten. Selbst wenn diese Preisberechnungsmethoden bei Einstandspreislistenzeilen verwendet werden, um Transaktionskategoriekosten einzurichten, werden diese vom System ignoriert, und es wird kein Standardeinstandspreis angegeben.
