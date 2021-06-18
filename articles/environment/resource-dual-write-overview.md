---
title: Dual-Write-Integration für Project Operations
description: Dieses Thema bietet einen Überblick über die Dual-Write-Integration von Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998680"
---
# <a name="project-operations-dual-write-integration-overview"></a>Dual-Write-Integration für Project Operations – Überblick

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Project Operations verwendet [Dual-Write-Funktionen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), um Daten in Microsoft Dataverse und Dynamics 365 Finance zu synchronisieren.

Die folgende Abbildung zeigt, wie Daten im Rahmen dieser Integration zwischen Dataverse und Finance synchronisiert werden.

![Übersicht über die Project Operations-Dataflows](./media/ProjectOperationsFlows.jpg)

Project Operations in Dataverse bietet eine moderne Benutzeroberfläche und eine einfache Erweiterbarkeit ohne Code/Low-Code mit Power Platform Fähigkeiten. Projektmanager, Ressourcenmanager, Mitglieder des Projektteams und andere Front-Office-Mitarbeiter führen ihre Aktivitäten in Project Operations in Dataverse aus.

Project Operations in Finance bietet Unterstützung bei der Projektbuchhaltung und Umsatzrealisierung. Project Operations fügt sich in den Finanzrahmen von Finance ein, um Umsatzsteuerberechnungen, Wechselkurse, Finanzdimensionsberichte und mehr zu erstellen. Die Erfahrungen der Projektbuchhalter befinden sich hauptsächlich in Finance.

Die Project Operations-Integration besteht aus der folgenden Komponentenintegration:


- [Project Operations-Einrichtung und Konfigurationsdatenintegration](resource-dual-write-setup-integration.md) 
- [Projekt-Schätz- und Ist-Werte](resource-dual-write-estimates-actuals.md)
- [Projektrechnungen](resource-dual-write-project-invoice.md)
- [Ausgabenverwaltung](resource-dual-write-expense.md)
- [Kreditorenrechnung](resource-dual-write-vendor-invoice.md)
