---
title: Ein Projekt kopieren
description: Dieser Artikel enthält Informationen über das Kopieren von Projekten in Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b358f9e45278d886f3e6e8e8cd747fc0ea30212b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925763"
---
# <a name="copy-a-project"></a>Ein Projekt kopieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Mithilfe von Dynamics 365 Project Operations können Sie schnell neue Projekte erstellen, indem Sie **Projekt kopieren** im Formular **Projekte** auswählen. Um ein Projekt zu kopieren, öffnen Sie das zu kopierende Projekt, und wählen Sie dann **Projekt kopieren** aus. Die Aktion kopiert Folgendes:

- Projekteigenschaften 
- Projektstrukturplan
- Projektteammitglieder
- Projektschätzungen
- Projektausgabenschätzungen
- Materialschätzungen Projekte
- Projektprüflisten
- Projekt-Buckets

## <a name="project-properties"></a>Projekteigenschaften

Beim Kopieren des Projekts werden die Werte in den folgenden Feldern kopiert.

| Feld | Project Operations für „Nicht vorrätige Materialien“ | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Name des Dataflows | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Beschreibung des Dataflows | :heavy_check_mark: | :heavy_check_mark: | |
| Kundin/Kunde | :heavy_check_mark: | :heavy_check_mark: | |
| Kalendervorlage | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Währungen | :heavy_check_mark: | :heavy_check_mark: | |
| Vertragseinheit | :heavy_check_mark: | :heavy_check_mark: | |
| Zuständiges Unternehmen | :heavy_check_mark: | | |
| Projektmanager | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Gesamtprojektstatus | :heavy_check_mark: | :heavy_check_mark: | |
| Anmerkungen | :heavy_check_mark: | :heavy_check_mark: | |
| Schätzungen | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Voraussichtliches Startdatum</p><p><strong>Hinweis:</strong> Dieses Feld gibt das Datum an, an dem das Projekt aus der Kopie erstellt wird. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Voraussichtliches Fertigstellungsdatum</p><p><strong>Hinweis:</strong> Das Datum in diesem Feld wird basierend auf dem Startdatum des neuen Projekts angepasst, das aus der Kopie erstellt wurde.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Aufwand (Stunden) | :heavy_check_mark: | :heavy_check_mark: | |
| Geschätzte Arbeitskosten | :heavy_check_mark: | :heavy_check_mark: | |
| Geschätzte Ausgabenkosten | :heavy_check_mark: | :heavy_check_mark: | |
| Geschätzte Materialkosten | | :heavy_check_mark: | |

> [!NOTE]
> Projekt kopieren ist ein lang andauernder Vorgang. Projektdatensätze, ihre relevanten Attribute und viele zugehörige Entitäten werden ebenfalls kopiert. Aufgrund der langen Laufzeit des Vorgangs wird die Zielprojektseite nach dem Start des Kopiervorgangs für die Bearbeitung gesperrt, bis der Kopiervorgang abgeschlossen ist.

## <a name="work-breakdown-structure"></a>Projektstrukturplan

Beim Kopieren des Projekts wird die gesamte ressourcenintensive Projektstrukturplan kopiert. Benannte Ressourcen werden durch generische Ressourcen ersetzt. Wenn die benannten Ressourcen nicht die gleichen Arbeitszeiten wie die generische Ressource haben, wird der Zeitplan neu berechnet und die Vorgangsdauer kann sich ändern.

## <a name="project-team-members"></a>Projektteammitglieder

Wenn ein Projektteam aus dem Quellprojekt kopiert wird, werden die generischen Ressourcen kopiert. Generische Ressourcenzuweisungen werden wie im Quellprojekt verwaltet. Benannte Ressourcen werden in generische Teammitglieder konvertiert.

> [!NOTE]
> Teammitglieder und Aufgaben werden nicht in Project for the Web kopiert.

## <a name="estimates"></a>Schätzungen

Beim Kopieren des Projekts werden Ressourcen-, Aufwands- und Materialkalkulationszeilen aus dem Quellprojekt kopiert. 

Informationen zum programmgesteuerten Zugriff auf „Projekt kopieren“ finden Sie unter [Projektvorlagen mit „Projekt kopieren“ entwickeln](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Angebote und Verträge

Angebote und Verträge sind nicht mit dem Zielprojekt verknüpft.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
