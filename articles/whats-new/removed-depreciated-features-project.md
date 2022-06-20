---
title: Entfernte oder veraltete Funktionen in Dynamics 365 Project Operations
description: Dieser Artikel beschreibt Funktionen, die aus Dynamics 365 Project Operations entfernt wurden bzw. deren Entfernung geplant ist.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: df9d8a40fa853e72416e64846bf59748815048be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921485"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Entfernte oder veraltete Funktionen in Dynamics 365 Project Operations

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung und Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigung_

Dieser Artikel beschreibt Funktionen, die aus Dynamics 365 Project Operations entfernt wurden bzw. deren Entfernung geplant ist.

- Eine *entfernte* Funktion ist im Produkt nicht mehr verfügbar.
- Eine *veraltete* Funktion befindet sich nicht in der aktiven Entwicklung und wird möglicherweise in einem zukünftigen Update entfernt.

Diese Liste soll Ihnen helfen, diese Umzüge und Abschreibungen für Ihre eigene Planung zu berücksichtigen.

> [!NOTE]
> Ausführliche Informationen über Objekte in Finanz- und Betriebs-Apps finden Sie in den [**Technischen Referenzberichten**](/dynamics/s-e/global/axtechrefrep_61). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die in den einzelnen Versionen der Finanz- und Betriebs-Apps geändert oder entfernt wurden.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Entfernte oder veraltete Funktionen im Project Operations Release von März 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parameter „Korrekturbuchung immer erstellen“ für Projektmanagement und Buchhaltung

| &nbsp; | &nbsp; |
|--------|--------|
| **Grund für die Ablehnung/Entfernung** | Regulierungstransaktionen sind für Prüfungszwecke erforderlich. Nach der Einstellung wird dieser Parameter ausgeblendet. Das System erstellt immer Regulierungsbuchungen, so wie es dies derzeit tut, wenn der Parameter auf **Ja** gesetzt ist. |
| **Durch eine andere Funktion ersetzt?** | Nr. |
| **Betroffene Produktbereiche** | Antrag |
| **Bereitstellungsoption** | Project Operations für Szenarien basierend auf Fertigung/vorrätigen Ressourcen |
| **Status** | Veraltet: Bis zum 1. März 2023 werden wir den Parameter ausblenden und das Systemverhalten so ändern, dass Regulierungsbuchungen immer erstellt werden. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parameter „Regulierungsdatum als neues Projektdatum verwenden“ für Projektmanagement und Abrechnung

| &nbsp; | &nbsp; |
|--------|--------|
| **Grund für die Ablehnung/Entfernung** | Dieser Parameter wurde ursprünglich verwendet, um Regulierungen zu ermöglichen, wenn ein Buchhaltungsperiode geschlossen wurde. Er ist jedoch nicht mehr erforderlich, da das Buchungsdatum der Transaktion auf das erste Datum des offenen Zeitraums geändert werden kann, sofern dies konfiguriert ist. Das Projektdatum darf nicht geändert werden, da es das Datum darstellt, an dem die Transaktion stattgefunden hat. |
| **Durch eine andere Funktion ersetzt?** | Nr. |
| **Betroffene Produktbereiche** | Antrag |
| **Bereitstellungsoption** | Project Operations für Szenarien basierend auf Fertigung/vorrätigen Ressourcen |
| **Status** | Veraltet: Bis zum 1. März 2023 werden wir den Parameter ausblenden und das Systemverhalten so ändern, dass das Projektdatum bei Regulierungen nie geändert wird. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Workflow für Ressourcenanforderung in Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigung

| &nbsp; | &nbsp; |
|--------|--------|
| **Grund für die Ablehnung/Entfernung** | Veraltet wegen geringer Nutzung und Beschränkungen des Transaktionsvolumens. |
| **Durch eine andere Funktion ersetzt?** | Nr. |
| **Betroffene Produktbereiche** | Antrag |
| **Bereitstellungsoption** | Project Operations für Szenarien basierend auf Fertigung/vorrätigen Ressourcen |
| **Status** | Veraltet: Bis zum 1. März 2023 werden wir die Option zum Anfordern von Ressourcen für das Projekt mithilfe des Workflows deaktivieren. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Projektrechnungsvorschlagsseite ohne Kopfzeilen- und Zeilenansichten

| &nbsp; | &nbsp; |
|--------|--------|
| **Grund für die Ablehnung/Entfernung** | Veraltet wegen Verbesserungen an der Seite, die zusammen mit dem **Projektrechnungsvorschlags- und Rechnungserfassungsformulare mit der Kopf- und Zeilenansicht verwenden**-Funktionsschlüssel eingeführt wurden. |
| **Durch eine andere Funktion ersetzt?** | Ja |
| **Betroffene Produktbereiche** | Antrag |
| **Bereitstellungsoption** | Project Operations für Szenarien bezüglich Fertigung/vorrätig; Project Operations für Szenarien basierend auf Ressourcen/nicht vorrätig |
| **Status** | Veraltet: Bis zum 1. März 2023 werden wir die frühere (alte) Seite deaktivieren und den **Projektrechnungsvorschlags- und Rechnungserfassungsformulare mit der Kopf- und Zeilenansicht verwenden**-Funktionsschlüssel standardmäßig verwenden. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Entfernte oder veraltete Funktionen im Project Operations Release von Dezember 2021

### <a name="collaboration-workspaces"></a>Arbeitsbereiche für Zusammenarbeit

[Erstellen oder Verknüpfen eines Arbeitsbereichs für die Zusammenarbeit (Projekt)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Grund für die Ablehnung/Entfernung** | Aufgrund geringer Nutzung eingestellt. Kunden, die Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen verwenden, können von [Zusammenarbeit mit Office-Gruppen](../project-management/collaboration-groups.md) profitieren. |
| **Durch eine andere Funktion ersetzt?** | Nr. |
| **Betroffene Produktbereiche** | Antrag  |
| **Bereitstellungsoption** | Project Operations für Szenarien basierend auf Fertigung/vorrätigen Ressourcen |
| **Status** | Veraltet: Ab dem 1. Dezember 2022 wird die Unterstützung von Arbeitsbereichen für Zusammenarbeit nicht mehr vorgesehen sein. |
