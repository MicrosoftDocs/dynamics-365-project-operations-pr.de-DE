---
title: Project Operations-Integration pro juristische Person konfigurieren
description: Dieses Thema enthält Informationen zum Einrichten einer Integration durch eine juristische Person in Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122882"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Project Operations-Integration pro juristische Person konfigurieren 

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieses Thema führt Sie durch die Schritte, die zum Konfigurieren von Dynamics 365 Project Operations pro juristischer Person erforderlich sind.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Wichtige Funktionen in Dynamics 365 Finance aktivieren

Führen Sie die folgenden Schritte aus, um die erforderlichen Funktionen zu aktivieren.

1. Navigieren Sie in Dynamics 365 Finance zum Arbeitsbereich **Funktionsverwaltung**.
2. Finden Sie in der **Funktionsliste** die folgenden Funktionen und aktivieren Sie diese:
  
    - **Mehrere Vertragszeilen für ein Projekt aktivieren**
    - **Project Operations in Dynamics 365 Customer Engagement** aktivieren

> [!NOTE]
> Wenn **Funktionsschlüssel** nicht aufgeführt ist, prüfen Sie, dass Ihre Finance-Version die Mindestanforderungen der Version erfüllt (Anwendungsversion 10.0.13 mit allen angewendeten Qualitätsupdates oder höher). Wählen Sie **Auf Updates prüfen** aus, um die Funktionsliste zu aktualisieren.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Das Project Operations-Bereitstellungsszenario für eine juristische Person definieren

Sie können Project Operations in Dynamics 365 Customer Engagement auf Ebene einer juristischen Person aktivieren. Sie können eine juristische Person haben, die Project Operations in Dynamics 365 Customer Engagement für ressourcenbasierte/nicht ressourcenbasierte Szenarien verwendet. In derselben Umgebung können Sie eine andere juristische Person haben, die Project Operations für Lager-/Produktionsauftragsszenarien verwendet.

1. Navigieren Sie in Dynamics 365 Finance zu **Projektmanagement und -buchhaltung** > **Einrichtung** > **Globale Projektmanagement und -Buchhaltungsparameter**.
2. Wählen Sie in der Liste der verfügbaren juristischen Personen Entitäten aus, für die mehrere Vertragszeilen und Projektvorgänge in Dynamics 365 Customer Engagement-Funktionen aktiviert sind. Wählen Sie juristische Personen, die Project Operations für Lager-/Fertigungsauftragsszenarien verwenden, weiterhin nicht aus.

> [!NOTE]
> Eine juristische Person kann nur ausgewählt werden, wenn keine Projekte vorhanden sind.

## <a name="configure-project-management-and-accounting-parameters"></a>Projektmanagement und -buchhaltungsparameter konfigurieren

Jede juristische Person, die Project Operations in Dynamics 365 Customer Engagement verwendet, benötigt eine Reihe von Standardparametern. Diese Parameter werden auf der Registerkarte **Project Operations** auf der Seite **Projektmanagement und -buchhaltungsparameter** konfiguriert. Die Parameter lauten wie folgt:

  - **Standards Fakturierungstyp**: Project Operations verwendet einen festen Satz von Standardeinstellungen für Fakturierungstypen, die den Zeileneigenschaften in Finance zugeordnet werden müssen. Erstellen Sie für jeden Fakturierungstyp einen Datensatz: **Unbestimmt**, **Fakturierbar**, **Nicht fakturierbar**, **Kostenlos** und **Nicht verfügbar**.
  - **Standardeinstellungen für Projektkategorien** : Wählen Sie die Standardprojektkategorien aus, die für jeden Transaktionstyp verwendet werden sollen. Diese Standardeinstellungen werden in **Project Operations-Integrationsjournal** und in Vorkalkulationen, in denen keine Transaktionskategorie für die Istwerte des Projekts angegeben ist.
  - **Prognosen**: Wählen Sie das Prognosemodell aus, das für Zeit- und Ausgabenvorkalkulationen verwendet werden soll.
