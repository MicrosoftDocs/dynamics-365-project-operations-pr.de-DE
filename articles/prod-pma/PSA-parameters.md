---
title: Intgrationsparameter für Project Service Automation
description: In diesem Thema wird erläutert, wie Sie konfigurieren, wie Standarddaten bei der Integration von Microsoft Dynamics 365 for Project Service Automation mit Microsoft Dynamics 365 Finance eingegeben werden.
author: ruhercul
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b8faba1d799e360e58d47a02dc8b46e09fa0d393
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270902"
---
# <a name="project-service-automation-integration-parameters"></a>Intgrationsparameter für Project Service Automation

[!include[banner](../includes/banner.md)]

Auf der Seite **Integrationsparameter für Project Service Automation** können Sie konfigurieren, wie Standarddaten bei der Integration von Dynamics 365 Project Service Automation mit Dynamics 365 Finance eingegeben werden. Damit Projekte erfolgreich von Project Service Automation zu Finance synchronisiert werden können, müssen Sie die folgenden Felder einrichten.

Zum Öffnen der Seite **Integrationsparameter für Project Service Automation** gehen Sie zu **Projektmanagement und Buchhaltung** \> **Einrichtung** \> **Dynamics 365 for Project Service Automation Integrationsparameter**. 

> [!NOTE]
> - Projektaufgabenintegration, Kostentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Funktionssperren sind in Version 8.0 verfügbar.
> - Die tatsächliche Integration ist in Version 8.0.1 oder höher verfügbar.


| Tab                    | Feld                | Beschreibung |
|------------------------|----------------------|-------------|
| Allgemein                | Standard-Projekttyp | Wählen Sie den Standardprojekttyp. Wenn Projekte über Project Service Automation synchronisiert werden, wird dieser Wert verwendet, wenn Sie in der Integrationsvorlage keinen Standardwert angegeben haben. Während der Synchronisation wird das Feld **Projekttyp** für neue Projekte auf diesen Wert gesetzt. Der Wert kann jedoch aktualisiert werden, wenn die Projektvertragszeilen über Project Service Automation synchronisiert werden. |
|                        | Zeitkategorie        | Wählen Sie die Standard-Zeitkategorie aus. Dieser Wert wird verwendet, wenn Stundenschätzungen über Project Service Automation synchronisiert werden. Wenn die Stundenschätzungen und Stundenaktualisierungen von Project Service Automation synchronisiert werden, wird das Feld **Kategorie** für neue Projektstundenprognosen in Finance auf diesen Wert gesetzt. |
|                        | Gebührenkategorie         | Wählen Sie die Standard-Gebührenkategorie aus. Dieser Wert wird verwendet, wenn tatsächliche Gebühren von Project Service Automation synchronisiert werden. Wenn die tatsächlichen Gebühren von Project Service Automation synchronisiert werden, wird das Feld **Kategorie** für neue Gebührentransaktionen in Finance auf diesen Wert gesetzt. |
| Standards für Projektgruppen | Projekttyp         | Klicken Sie auf **Neu**, um eine Zeile hinzuzufügen, in der Sie den Projekttyp auswählen können, für den die Standardprojektgruppe festgelegt werden soll. Ein bestimmter Projekttyp kann in der Konfiguration nur einmal ausgewählt werden. |
|                        | Projektgruppe        | Wählen Sie die Standardprojektgruppe für den ausgewählten Projekttyp aus. Wenn neue Projekte über Project Service Automation synchronisiert werden, wird das Feld **Projektgruppe** auf den Standardwert für den Projekttyp festgelegt, wenn Sie in der Integrationsvorlage keinen Standardwert angegeben haben. |
| Standardeinstellungen für die Abrechnungstyp  | Fakturierungstyp         | Klicken Sie auf **Neu**, um eine Zeile hinzuzufügen, in der Sie den Abrechnungstyp auswählen können, für den die Standardzeileneigenschaft festgelegt werden soll. Ein bestimmter Abrechnungstyp kann in der Konfiguration nur einmal ausgewählt werden. |
|                        | Zeileneigenschaft        | Wählen Sie die Standardzeileneigenschaft für den ausgewählten Rechnungstyp aus. Wenn neue Stundenschätzungen, neue Ausgabenschätzungen oder neue Istwerte von Project Service Automation synchronisiert werden, wird das Feld **Zeilen-Eigenschaft** auf den Standardwert für die Abrechnungsart gesetzt. |
| Sperrung von Funktionen  | Nicht verfügbar       | Wählen Sie die zu deaktivierende Funktion in Finance für Projekte und Verträge aus, die aus Project Service Automation stammen. Sie können beispielsweise die Möglichkeit deaktivieren, Verträge und Projekte zu bearbeiten, Projektstrukturpläne zu erstellen und Arbeitszeittabellen in Finance einzugeben. Buchhaltungsbezogene Felder bleiben weiterhin aktiviert, auch wenn sie durch die Parametereinstellung nicht verfügbar gemacht werden. Standardmäßig sind alle Funktionen aktiviert. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]