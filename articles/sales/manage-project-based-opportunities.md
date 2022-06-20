---
title: Projektbasierte Verkaufschancen verwalten
description: Dieser Artikel beschreibt, wie Sie mit Verkaufschancen arbeiten können, die mit Projekten verbunden sind.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 29e5a2c91186021eee9bb23aba3d42228fcd9381
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933215"
---
# <a name="manage-project-based-opportunities"></a>Projektbasierte Verkaufschancen verwalten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Projektbasierte Unternehmen haben ihre Geschäftstätigkeit in der Regel auf mehrere Länder und Regionen verteilt. Die Kosten für die Projektdurchführung und -bereitstellung können je nach Region oder Abteilung variieren, die die Bereitstellung verwaltet. Dies kann sich wiederum auf die Margen des Geschäfts auswirken. Die Bereitstellung projektbasierter Dienstleistungen erfordert in der Regel viel Personalzeit, erhebliche Reisekosten, Materialkosten und andere Kosten.

In Dynamics 365 Project Operations werden projektbasierte Verkaufschancen mit Erweiterungen für Dynamics 365 Sales entwickelt. Der Artikel enthält Einzelheiten zu den verschiedenen Feldern und der Geschäftslogik, die in der zusätzlichen Funktionalität enthalten sind, die von projektbasierten Firmen für die Verwaltung projektbezogener Verkaufschancen benötigt wird.

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