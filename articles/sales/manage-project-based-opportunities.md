---
title: Projektbasierte Verkaufschancen verwalten
description: Dieses Thema enthält Informationen zum Arbeiten mit Verkaufschancen, die sich auf Projekte beziehen.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: aebff4d3a94735e76bcb9cafd25a058207dae846
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996340"
---
# <a name="manage-project-based-opportunities"></a>Projektbasierte Verkaufschancen verwalten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Projektbasierte Unternehmen haben ihre Geschäftstätigkeit in der Regel auf mehrere Länder und Regionen verteilt. Die Kosten für die Projektdurchführung und -bereitstellung können je nach Region oder Abteilung variieren, die die Bereitstellung verwaltet. Dies kann sich wiederum auf die Margen des Geschäfts auswirken. Die Bereitstellung projektbasierter Dienstleistungen erfordert in der Regel viel Personalzeit, erhebliche Reisekosten, Materialkosten und andere Kosten.

In Dynamics 365 Project Operations werden projektbasierte Verkaufschancen mit Erweiterungen für Dynamics 365 Sales entwickelt. Das Thema enthält Details zu den verschiedenen Feldern und der Geschäftslogik, die in den zusätzlichen Funktionen enthalten sind, die projektbasierte Unternehmen zur Verwaltung projektbasierter Geschäftschancen benötigen.

## <a name="view-all-project-based-opportunities"></a>Alle Projektbasierte Verkaufschancen anzeigen

Eine Liste aller projektbasierten Verkaufschancen finden Sie auf der Listenseite **Verkaufschance**. 

1. Gehen Sie zu **Vertrieb** > **Verkaufschancen**.
2. Verwenden Sie **Ansicht wechseln**, um andere gefilterte Ansichten der Geschäftschancen auszuwählen. Sie können Ihre eigenen Ansichten mit benutzerdefinierten Filterkriterien erstellen, um diese Ansichten und Navigationsoptionen zu konfigurieren.

Projektverkaufschancen können auf dieser Listenseite oder der Detailseite erstellt oder gelöscht werden.

## <a name="business-process-flow-for-project-based-deals"></a>Geschäftsprozessfluss für projektbasierte Deals

Die folgenden Geschäftsprozessflüsse werden für projektbasierte Transaktionen im Project Operations unterstützt:

- Lead-zu-Verkaufschancen-Geschäftsprozess
- Vertriebsprozess Verkaufschance

### <a name="lead-to-opportunity-business-process"></a>Lead-zu-Verkaufschancen-Geschäftsprozess 
Der Lead-zu-Verkaufschance-Geschäftsprozess unterstützt die folgenden Phasen:

| Freigabefenster | Zugeordnete Entität | Funktionalität |
| --- | --- | --- |
| Qualifizieren | Lead | Qualifizieren des Leads, um eine Firma, einen Kontakt und eine Verkaufschance zu erstellen. |
| Entwickeln | Verkaufschance | Entwickeln Sie die Möglichkeit, weitere Informationen über die Arbeit, die wichtigsten Interessengruppen und den Wettbewerb hinzuzufügen. |
| Vorschlagen | Verkaufschance | Entwickeln Sie den Vorschlag und lassen Sie ihn vom internen Überprüfungsteam genehmigen. |
| Schließen | Verkaufschance | Gewinnen Sie die Verkaufschance, um den Handel abzuschließen. |

### <a name="opportunity-sales-process"></a>Vertriebsprozess Verkaufschance
Der Vertriebsprozess Verkaufschance in Project Operations ist eine Erweiterung des Geschäftsablaufs für den Vertriebsprozessflow Verkaufschance in der Sales-Anwendung. Dieser Geschäftsprozess ist sofort einsatzbereit, um die folgenden Phasen einer projektbasierten Verkaufschance zu unterstützen.

| Freigabefenster | Zugeordnete Entität | Funktionalität |
| --- | --- | --- |
| Qualifizieren | Verkaufschance | Qualifizieren des Leads, um eine Firma, einen Kontakt und eine Verkaufschance zu erstellen. |
| Vorschlagen | Angebot | Entwickeln Sie den Vorschlag mit Projektangeboten, und holen Sie sich vom internen Überprüfungsteam eine Genehmigung. |
| Vertrag | Projektvertrag | Gewinnen Sie das Angebot, um den Vertrag zu erstellen, und beginnen Sie mit der Ausführung und Bereitstellung des Projekts. |
| Schließen | Projektvertrag | Beenden Sie die Arbeit erfolgreich und schließen Sie den Projektvertrag. |

> [!NOTE]
> Wenn Ihr projektbasiertes Geschäft mit einem Lead begann, hat der Geschäftsprozess Lead-bis-Verkaufschance Vorrang.
>
> Wenn Ihr projektbasiertes Geschäft mit einer Verkaufschance begann, hat der Verkaufschancen-Verkaufsprozess Vorrang.

Sie können den Geschäftsprozessfluss des Produkts bearbeiten oder eigene Geschäftsprozessabläufe erstellen, um Ihren Verkaufsprozess nach Bedarf zu verfolgen. Weitere Informationen über den Geschäftsprozessfluss finden Sie unter [Geschäftsprozessflüsse, Übersicht](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]