---
title: Project Operations-Integration pro juristische Person konfigurieren
description: Dieser Artikel informiert Sie über die Einrichtung der Integration nach juristischer Entität in Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914677"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Project Operations-Integration pro juristische Person konfigurieren 

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel führt Sie durch die Schritte, die zur Konfiguration von Dynamics 365 Project Operations pro juristischer Entität erforderlich sind.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Funktionsschlüssel in Dynamics 365 Finance aktivieren

Führen Sie die folgenden Schritte aus, um die erforderlichen Funktionen zu aktivieren.

1. Wechseln Sie in Dynamics 365 Finance zum Arbeitsberiech **Funktionsverwaltung**.
2. Finden Sie in der **Funktionsliste** die folgenden Funktionen und aktivieren Sie diese:
  
    - **Mehrere Vertragszeilen für ein Projekt aktivieren**
    - **Project Operations auf Dynamics 365 Customer Engagement aktivieren**

> [!NOTE]
> Wenn **Funktionsschlüssel** nicht aufgeführt ist, prüfen Sie, dass Ihre Finance-Version die Mindestanforderungen der Version erfüllt (Anwendungsversion 10.0.13 mit allen angewendeten Qualitätsupdates oder höher). Wählen Sie **Auf Updates prüfen** aus, um die Funktionsliste zu aktualisieren.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Das Project Operations-Bereitstellungsszenario für eine juristische Person definieren

Sie können Project Operations bei Dynamics 365 Customer Engagement auf Ebene der juristischen Person aktivieren. Sie können eine juristische Person haben, die Project Operations bei Dynamics 365 Customer Engagement für Szenarien auf Basis von Ressourcen/nicht vorrätig verwendet. In derselben Umgebung können Sie eine andere juristische Person haben, die Project Operations für Lager-/Produktionsauftragsszenarien verwendet.

1. Gehen Sie in Dynamics 365 Finance zu **Projektmanagement und -buchhaltung** > **Einrichtung** > **Globales Projektmanagement und Abrechnungsparameter**.
2. Wählen Sie in der Liste der verfügbaren juristischen Personen die Entitäten aus, bei denen mehrere Vertragspositionen und Project Operations on Dynamics 365 Customer Engagement-Funktionen aktiviert werden. Wählen Sie juristische Personen, die Project Operations für Lager-/Fertigungsauftragsszenarien verwenden, weiterhin nicht aus.

> [!NOTE]
> Eine juristische Person kann nur ausgewählt werden, wenn keine Projekte vorhanden sind.

## <a name="configure-project-management-and-accounting-parameters"></a>Projektmanagement und -buchhaltungsparameter konfigurieren

Jede juristische Person, die Project Operations bei Dynamics 365 Customer Engagement verwendet, benötigt eine Reihe von Standardparametern. Diese Parameter werden auf der Registerkarte **Project Operations** auf der Seite **Projektmanagement und -buchhaltungsparameter** konfiguriert. Die Parameter lauten wie folgt:

  - **Standards Fakturierungstyp**: Project Operations verwendet einen festen Satz von Standardeinstellungen für Fakturierungstypen, die den Zeileneigenschaften in Finance zugeordnet werden müssen. Erstellen Sie für jeden Fakturierungstyp einen Datensatz: **Unbestimmt**, **Fakturierbar**, **Nicht fakturierbar**, **Kostenlos** und **Nicht verfügbar**.
  - **Standardeinstellungen für Projektkategorien** : Wählen Sie die Standardprojektkategorien aus, die für jeden Transaktionstyp verwendet werden sollen. Diese Standardeinstellungen werden in **Project Operations-Integrationsjournal** und in Vorkalkulationen, in denen keine Transaktionskategorie für die Istwerte des Projekts angegeben ist.
  - **Prognosen**: Wählen Sie das Prognosemodell aus, das für Zeit- und Ausgabenvorkalkulationen verwendet werden soll.


[!INCLUDE[footer-include](../includes/footer-banner.md)]