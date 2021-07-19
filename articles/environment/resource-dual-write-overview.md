---
title: Dual-Write-Integration für Project Operations
description: Dieses Thema bietet einen Überblick über die Dual-Write-Integration von Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 540b6f74d8e79116e5fdb2ceffaa4bbb487ff08f
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368430"
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
