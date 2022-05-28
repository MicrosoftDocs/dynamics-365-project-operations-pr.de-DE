---
title: Geschäftsvorfälle in Project Operations
description: Dieses Thema gibt einen Überblick über das Konzept von Geschäftstransaktionen in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582203"
---
# <a name="business-transactions-in-project-operations"></a>Geschäftsvorfälle in Project Operations

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

In Microsoft Dynamics 365 Project Operations ist *Geschäftstransaktion* ein abstraktes Konzept, das von keiner Entität dargestellt wird. Einige häufig verwendete Felder und Prozesse für Entitäten sind jedoch so ausgelegt, dass sie das Konzept von Geschäftstransaktionen verwenden. Die folgenden Entitäten verwenden diese Abstraktion:

- Detailinformationen zur Angebotsposition
- Vertragszeilendetails
- Vorkalkulationszeilen
- Erfassungspositionen
- Ist-Werte

Von diesen Entitäten werden Angebotspositions- und Vertragszeilendetails sowie Vorkalkulationszeilen im Projektlebenszyklus der *Vorkalkulationsphase* zugeordnet. Die Entitäten „Erfassungspositionen“ und „Ist-Werte“ werden im Projektlebenszyklus der *Ausführungsphase* zugeordnet.

Project Operations behandelt Datensätze in allen fünf dieser Entitäten als Geschäftstransaktionen. Die einzige Unterscheidung besteht darin, dass Datensätze in den Entitäten, die zur Vorkalkulationsphase zugeordnet werden (Angebotspositionen, Vertragszeilendetails und Schätzungszeilen), als *Finanzprognosen* gelten, wohingegen die Datensätze in den Entitäten, die zur Ausführungsphase zugeordnet werden (Erfassungspositionen und Ist-Werte), als bereits eingetretene *Finanztatsachen* gelten.

Weitere Informationen finden Sie unter [Vorkalkulationen](../project-management/estimating-projects-overview.md) und [Ist-Werte](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Einzigartige Konzepte für Geschäftstransaktionen

Die folgenden Konzepte sind für das Konzept der Geschäftstransaktionen einzigartig:

- Transaktionstyp
- Transaktionsklasse
- Transaktionsursprung
- Transaktionsverbindung

### <a name="transaction-type"></a>Transaktionstyp

Der Transaktionstyp gibt den Zeitpunkt und den Kontext der finanziellen Auswirkungen auf ein Projekt an. Es wird durch einen Optionssatz definiert, der in Project Operations die folgenden unterstützten Werte aufweist:

- Kosten
- Projektvertrag
- Nicht fakturierte Umsätze
- Fakturierte Umsätze
- Organisationsübergreifender Umsatz
- Kosten der Ressourcenzuordnungseinheit

### <a name="transaction-class"></a>Transaktionsklasse

Die Transaktionsklasse repräsentiert die verschiedenen Arten von Kosten, die für Projekte angefallen sind. Es wird durch einen Optionssatz definiert, der in Project Operations die folgenden unterstützten Werte aufweist:

- Uhrzeit
- Ausgaben
- Material
- Gebühr
- Meilenstein
- Steuer

> [!NOTE]
> Der Wert **Meilenstein** wird in Project Operations in der Regel von der Geschäftslogik für die Festpreisfakturierung verwendet.

### <a name="transaction-origin"></a>Transaktionsursprung

Transaktionsursprung ist eine Entität, die den Ursprung jeder Geschäftstransaktion speichert, um die Berichterstattung und Rückverfolgbarkeit zu unterstützen. Wenn die Projektausführung beginnt, erstellt jeder Geschäftsvorgang einen anderen Geschäftsvorgang, der wiederum einen weiteren Geschäftsvorgang erzeugt, und so weiter.

### <a name="transaction-connection"></a>Transaktionsverbindung

Die Transaktionsverbindung ist eine Entität, die die Beziehung zwischen zwei ähnlichen Geschäftstransaktionen speichert, z. B. Kosten und zugehörige Umsatz-Ist-Werte oder Transaktionsumkehrungen, die durch Fakturierungsaktivitäten wie Rechnungsbestätigung oder Rechnungskorrekturen ausgelöst werden.

Mithilfe der Entitäten Transaktionsursprung und Transaktionsverbindung können Sie Beziehungen zwischen Geschäftstransaktionen und Aktionen nachverfolgen, die zur Erstellung einer bestimmten Geschäftstransaktion führen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
