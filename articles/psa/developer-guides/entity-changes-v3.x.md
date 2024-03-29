---
title: Änderungen an Entitäten, Steuerelementen und der Benutzeroberfläche (Project Service Automation 3.x)
description: Dieser Artikel beschreibt die Lösungsänderungen für Microsoft Dynamics Project Service Automation 3.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8f54d263666c4fb999464f98c0138fc008dbbbd2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926867"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Änderungen an Entitäten, Steuerelementen und der Benutzeroberfläche (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Mit der Veröffentlichung von Microsoft Dynamics Project Service Automation (PSA) 3.x wurden viele Änderungen an den Entitäten, Steuerelementen, Ansichten und der Benutzeroberfläche vorgenommen. Dieser Artikel informiert Sie über diese wichtigen Änderungen.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Parent-Child-Beziehungen für die Entitäten „Vertriebsdokument“, „Vertriebsdokumentzeile“ und „Details der Vertriebsdokumentzeile“
In Versionen von Dynamics 365 Project Service Automation (PSA), die vor Version 3.0 veröffentlicht wurden, wurden einige der Beziehungen zwischen den Entitäten „Vertriebsdokument“, „Vertriebsdokumentzeile“ und „Details der Vertriebsdokumentzeile“ über Zeichenfolgenfelder implementiert, die eine Zeichenfolgendarstellung der GUID der zugehörigen Entität enthielten. Dies war auf Plattformbeschränkungen zurückzuführen, die einen erheblichen benutzerdefinierten Code auf der Server- und Clientseite der Lösung erforderten, damit diese Beziehungen ähnlich wie typische Dynamics CRM-Entitätsbeziehungen funktionierten und Zeichenfolgenfelder wie Nachschlagefelder wirkten.

PSA 3.0 wurde aktualisiert, um die neuen Entitätsbeziehungen zwischen den Entitäten „Vertriebsdokument“ und „Vertriebsdokumentzeile“ zu nutzen.

Da Suchfelder jetzt zum Anzeigen von Verweisen auf Entitäten verwendet werden können, werden die Felder, die in früheren Versionen den Zeichenfolgenwert der GUID der zugehörigen Entität enthielten, nicht mehr benötigt und sind daher veraltet. Der benutzerdefinierte clientseitige und serverseitige Code, der die durch Legacy-Zeichenfolgenfelder definierten Beziehungen verarbeitet, ist ebenfalls veraltet.

### <a name="entity-schema-changes"></a>Änderungen am Entitätsschema
Die folgende Tabelle enthält eine Eins-zu-Eins-Liste der veralteten Zeichenfolgenfelder und der neuen Suchfelder für die Entitäten. 

 Entität |   Veraltetes Feld (Zeichenfolge) | Neues Feld (Suche)
--- | --- | ---
invoicedetail (Rechnungsposition) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (Ist-Wert) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Rechnungszeitplan für Projektvertragszeile) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Meilenstein für Projektvertragszeile) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (Fakt) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Rechnungspositionsdetail) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Erfassungsposition) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Ressourcenkategorie für die Projektvertragszeile) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Projektvertragspositionsdetail) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Transaktionskategorie für die Projektvertragszeile) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Transaktionsklassifizierung für die Projektvertragszeile) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Rechnungszeitplan der Angebotsposition) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Ressourcenkategorie für die Angebotsposition) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Meilenstein der Angebotsposition) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Angebotspositionsdetail) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Transaktionskategorie der Angebotsposition) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Transaktionsklassifizierung der Angebotsposition) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Auftragsposition) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Veraltete benutzerdefinierte Ansichten und Steuerelemente
Die folgenden benutzerdefinierten Ansichten und Steuerelemente und ihre verknüpften Artefakte sind veraltet.

- Fakturierbarkeitsansicht.
- Benutzerdefinierte Rastersteuerelemente zum Anzeigen von Angebotspositionsdetails auf der Seite **Projektinformationen** für die Angebotszeile.
- Benutzerdefinierte Rastersteuerelemente zum Anzeigen von Projektvertragszeilendetails auf der Seite **Projektinformationen** für die Vertriebsauftragsposition.

> [!NOTE]
> Die vollständige Liste veralteter Ressourcen finden Sie unter [Veraltete Webressourcen in Project Service Automation 3.x](../developer-guides/web-resources-deprecated-v3.x.md).

## <a name="unified-client-interface-app-module"></a>Unified Client Interface App-Modul
Mit der Einführung der Unified Client Interface (UCI)-App-Module wurden die PSA-Siteübersichteinträge aus dem System entfernt.  
Die mit dem Formularwechsel verbundenen Funktionen für Verkaufschance, Angebot, Bestellung und Rechnung sind veraltet, da sie nicht mehr erforderlich sind, da das UCI-App-Modul nur PSA-Versionen der Formulare enthält.  

Die folgenden Webressourcen sind veraltet:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Die vollständige Liste veralteter Ressourcen finden Sie unter [Veraltete Webressourcen in Project Service Automation 3.x](../developer-guides/web-resources-deprecated-v3.x.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
